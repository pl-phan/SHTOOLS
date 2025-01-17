---
title: DownContFilterMC()
keywords: spherical harmonics software package, spherical harmonic transform, legendre functions, multitaper spectral analysis, Python, gravity, magnetic field
sidebar: mydoc_sidebar
permalink: pydowncontfiltermc.html
summary:
tags: [python]
toc: false
editdoc: pydoc
---

Compute the minimum-curvature downward continuation filter of Wieczorek and Phillips (1998).

## Usage

wl = DownContFilterMC (l, half, r, d)

## Returns

wl : float, ndarray
:   The amplitude of the downward continuation filter.

## Parameters

l : integer, array_like
:   The spherical harmonic degree.

half : integer, array_like
:   The spherical harmonic degree where the filter is equal to 0.5.

r : float, array_like
:   The reference radius of the gravitational field.

d : float, array_like
:   The radius of the surface to downward continue to.

## Description

DownContFilterMC will calculate the minimum-curvature downward continuation filter of Wieczorek and Phillips (1998) as a function of spherical harmonic degree l. The input parameters include half, which is the degree where the filter is equal to 0.5, and r and d, which are the reference radius of the gravitational field and the radius of the surface to downward continue to, respectively.

Following the methodology of Wieczorek and Phillips (1998), a simple analytic expression exists for the downward continuation filter only when taking the first, third, fifth, and so on, derivatives of their equation 17. For this minimum-curvature filter, which corresponds to the second derivative, the form has simply been generalized using the solutions of the odd derivatives. The form of this filter is numerically very similar to the Cartesian minimum-curvature filter of Phipps Morgan and Blackman (1993).

## References

Phipps Morgan, J., and D. K. Blackman, Inversion of combined gravity and bathymetry data for crustal structure: A prescription for downward continuation, Earth Planet. Sci. Lett., 119, 167-179, 1993.

Wieczorek, M. A. and R. J. Phillips, Potential anomalies on a sphere: applications to the thickness of the lunar crust, J. Geophys. Res., 103, 1715-1724, 1998.
