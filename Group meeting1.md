# Discussion on data collected by sentinel-3#
## 2022/4/27 ##

----------

###1、Pre knowledge###

----------
**Radiance:** In radiometry, radiance is the radiant flux emitted, reflected, transmitted or received by a given surface, per unit solid angle per unit projected area. Spectral radiance is the radiance of a surface per unit frequency or wavelength, depending on whether the spectrum is taken as a function of frequency or of wavelength. 

**Reflectance:** The reflectance of the surface of a material is its effectiveness in reflecting radiant energy. It is the fraction of incident electromagnetic power that is reflected at the boundary.

**Atmospheric correction:** Atmospheric correction is the process of removing the effects of the atmosphere on the reflectance values of images taken by satellite or airborne sensors.Atmospheric effects in optical remote sensing are significant and complex, dramatically altering the spectral nature of the radiation reaching the remote sensor. The atmosphere both absorbs and scatters various wavelengths of the visible spectrum which must pass through the atmosphere twice, once from the sun to the object and then again as it travels back up the image sensor.

----------

###2、data collected by sentinel-3###
According to the news, a serious oil spill occurred in the Pacific Ocean near the Peruvian capital Lima on January 15, 2022 due to the eruption of submarine volcanoes.   
I collected sentinel-3 data about the coast near Lima from January 10 to 31, and used 'snap' software(offerd by European Space Agency) to analyse those data.

Sentinel-3 offer 3 different processing levels products.
Level-0 products are internal products only. They are not distributed to SENTINEL-3 users. Level-1 products did some processing on the basis of Level-0 products, such as radiometrical calibration. Compare with Level-1 products, Level-2 converts radiances into reflectances.

![](http://markdown-2022.oss-cn-beijing.aliyuncs.com/1.png)

The above is the RGB image of level-1 product on the coast of Lima on January 11. It can be seen that clouds have a great impact.

![](https://markdown-2022.oss-cn-beijing.aliyuncs.com/2.png)
We can check the longitude and latitude information of each place, and select a band (sentinel-3 has 21 bands, all in the range of visible light to near-infrared light) to check the radiance. What we expect is to distinguish between oil and sea water by the parameter of radiance or reflectance. However, we need to eliminate the impact of the clouds.

I downloaded level-2 data at the same time and place.
![](https://markdown-2022.oss-cn-beijing.aliyuncs.com/3.png)
The radiance has been converted into reflection. And pixels containing clouds had been discarded. This does not seem to be the result we want.

----------

###3、future work###
1. try to find good algorithms for eliminating the impact of the clouds.
2. data from sentinel-3 do not seem to be suitable for the study of marine oil spills. Check some literature to see if there are other suitable satellites.
3. Study marine satellite science.