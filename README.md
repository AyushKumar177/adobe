# Curvetopia: A Journey into the World of Curves

Welcome to Curvetopia, where we bring order and beauty to the world of 2D curves! This project focuses on identifying, regularizing, and beautifying various types of curves in 2D Euclidean space. Our goal is to transform complex, imperfect polylines into clean, aesthetically pleasing sets of cubic Bézier curves, contributing to fields such as computer graphics, computer vision, and digital art.

## Objective

The primary objective of this project is to develop a comprehensive framework for the identification, regularization, and beautification of curves in 2D Euclidean space. We aim to achieve the following:

1. **Curve Identification:** Accurately identify the underlying geometric shapes (lines, circles, ellipses, etc.) in a set of input polylines.
2. **Curve Regularization:** Refine the identified shapes to remove noise and irregularities, ensuring smooth and precise curves.
3. **Curve Beautification:** Enhance the aesthetic quality of curves by optimizing their symmetry and completeness.

## Theoretical Background

### 2D Euclidean Spaces

2D Euclidean space, denoted as \( \mathbb{R}^2 \), is a two-dimensional plane characterized by an orthogonal coordinate system. In this space, each point is represented by a pair of coordinates \((x, y)\). Curves in this space can be described by a continuous set of points, which we aim to represent using cubic Bézier curves.

### Cubic Bézier Curves

Cubic Bézier curves are parametric curves commonly used in computer graphics and vector graphics. A cubic Bézier curve is defined by four control points \(\mathbf{P}_0\), \(\mathbf{P}_1\), \(\mathbf{P}_2\), and \(\mathbf{P}_3\). The curve is given by:

\[
\mathbf{B}(t) = (1-t)^3\mathbf{P}_0 + 3(1-t)^2t\mathbf{P}_1 + 3(1-t)t^2\mathbf{P}_2 + t^3\mathbf{P}_3
\]

where \( t \) is a parameter ranging from 0 to 1. These curves are favored for their flexibility and smoothness, making them ideal for representing complex shapes.

### Curve Regularization

Curve regularization involves refining a set of identified shapes (such as polylines) to remove irregularities and noise. This process ensures that the curves are smooth, continuous, and adhere to the expected geometric properties (e.g., a circle remains circular, a line remains straight).

### Symmetry and Aesthetics

Symmetry is a fundamental aspect of visual aesthetics. In this project, symmetry detection and enhancement play a key role in the beautification of curves. By identifying symmetrical properties and enforcing them during curve regularization, we create curves that are not only accurate but also visually pleasing.

### Curve Completion

Curve completion addresses the challenge of reconstructing incomplete or occluded curves. By leveraging interpolation techniques and geometric modeling, we ensure that even partially visible curves can be restored to their full, intended form.

## Problem Description

The ultimate goal of Curvetopia is to develop an end-to-end process that converts a raster image (such as a PNG) of line art into a set of cubic Bézier curves. However, for simplification in the initial phase, we focus on input provided as polylines.

### Input

- A finite subset of paths from the set of all paths in \( \mathbb{R}^2 \). Each path is a finite sequence of points representing a polyline.

### Output

- A set of paths represented by cubic Bézier curves, with regularization, symmetry, and completeness applied.

### Visualization

- The output curves are visualized using the SVG format, allowing them to be rendered in any modern web browser.

## Key Sections

### 1. Regularizing Curves

Regularization is the process of refining curves to remove irregularities and ensure that they conform to standard geometric shapes. In Curvetopia, we focus on:

- **Straight Lines:** Detecting and fitting linear segments within a polyline.
- **Circles and Ellipses:** Identifying curves where points are equidistant from a center (circle) or have two focal points (ellipse), and fitting these shapes precisely.

### 2. Curve Completion

Curve completion deals with reconstructing incomplete curves. This is particularly important in cases where portions of the curve are missing or occluded. The completion algorithms used include interpolation techniques and linear regression models.

### 3. Symmetry Detection

Symmetry detection is crucial for ensuring that the curves are aesthetically balanced. The project includes methods to detect and enforce symmetry in curves, making them more visually appealing.

