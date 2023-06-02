# RayTracing
School project aiming to create an interactive rendering engine that uses ray tracing on the GPU. The rendering is done with compute shaders, while the interface is made with Qt and C++.

In this project, we implemented ray tracing with the Blinn-Phong model, Fresnel coefficients and textures, then we implemented the Cook-Torrance model. You can switch between the two models in the interface.
In the next step, we focused on adding multiple bounces to each ray to create indirect illumination by using the specular coefficient, while also implementing shadow rays to take into account obstacles.
Then, we aimed to reduce noise in the generated frames by sending several rays per pixel. We implemented two different random rays generators to reduce noise, one using Gold noise, one using Halton sequences to get a quasi random perturbation on the rays, then computes the average value of all the generated rays in relation to time, and focus on sending rays only to pixels where the computations have yet to converge, by storing and updating the variance on each pixel.
Finally, we implemented ray tracing on textures that take into account normal maps, object transparency that either reflect or refract the light rays, and procedural textures to create a marbe-like texture
