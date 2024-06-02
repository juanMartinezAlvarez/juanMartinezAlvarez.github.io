---
layout: post
title: MATLAB codes for modelling light propagation in stratified media
date: 2024-06-02 21:01:00
description: The transfer matrix method is used to calculate the transmission and reflection coefficients of stratified media. I have implemented it on MATLAB, the codes are freely availabl
tags: optics code
categories: 
thumbnail: assets/img/post_MATLABCode_TMM/TMM_thumbnail.jpg
---

It is well known that the behavior of a light wave at an interface can be described in terms of the Fresnel coefficients, which give the transmitted and reflected fields in terms of the conditions at the interface. Real materials have at least two boundaries due to their finite thickness, and thus the simplest real case is the freestanding film, discussed in a previous post.

Stratified media, a stack of multilayers, are an important architecture due to their interesting properties. They are a scheme commonly used in antireflection coatings, and in multijunction photovoltaic solar cells, which are the most efficient photovoltaic cells available. In the case of stratified media, the method of tracking the multiple reflections and transmissions individually, as done in the freestanding film, becomes extremely cumbersome, which necessitates the development of other techniques. One of them is the Transfer Matrix Method (TMM), originally proposed by Abeles in the 1950s, and then reformulated by other authors in terms of the Fresnel coefficients. This method defines matrices composed of the Fresnel coefficients for each interface, and other propagation (also called layer) matrices that model the phase change and absorption when the wave propagates within a layer. These matrices are then multiplied consecutively to give the general matrix of the stratified media. From the elements of this matrix, the global transmission and reflection coefficients are found.

Recent works have developed ways to include light propagating incoherently (without interference phenomena) inside some layers while preserving the coherence in others. The Effective Medium Approximation (EMA) also permits to model layers composed of more than one material if the scale of the mixture is much smaller than the wavelength of light.

As part of my <a href='https://www.researchgate.net/publication/381041132_Light_propagation_in_multilayered_nanostructures?channel=doi&linkId=665a40650b0d28457479a1d3&showFulltext=true'>master’s thesis</a>, I implemented these techniques in MATLAB, and used them to explore the optical properties of materials of very different natures. All the MATLAB codes are freely available in a <a href='https://github.com/juanMartinezAlvarez/Transfer_Matrix_Method_TMM'>GitHub repository</a>.



