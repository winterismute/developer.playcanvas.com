---
title: Light
template: usermanual-page.tmpl.html
position: 6
---

The Light component attaches a dynamic light source to the Entity. The 'Type' property determines what kind of light is attached and what other properties are available.

The Light component can be enabled or disabled using the toggle in the top right of the component panel. If enabled, the light will light the scene.

#### Directional
![Light component (Directional)][1]
#### Point
![Light component (Point)][2]
#### Spot
![Light component (Spot)][3]

## Properties

<table class="table table-striped">
    <tr><th>Property</th><th style="width: 75%;">Description</th></tr>
    <tr><td>Lightmap</td><td>Enable lightmap baking from this light</td></tr>
    <tr><td>Affect Dynamic</td><td>If true this light will affect non-lightmapped model components at runtime</td></tr>
    <tr><td>Affect Lightmapped</td><td>If true this light will affect lightmapped model components at runtime</td></tr>
    <tr><td>Color</td><td>The color of the emitted light.</td></tr>
    <tr><td>Intensity</td><td>The intensity of the light, this acts as a scalar value for the light's color. This value can exceed 1.</td></tr>
    <tr><td>Range</td><td>Point and Spot only. The distance from the spotlight source at which its contribution falls to zero.</td></tr>
    <tr><td>Inner Cone Angle</td><td>Spot only. The angle from the spotlight's direction at which light begins to fall from its maximum.</td></tr>
    <tr><td>Outer Cone Angle</td><td>Spot only. The angle from the spotlight's direction at which light falls to zero.</td></tr>
    <tr><td>Cast Shadows</td><td>If checked, the light will cause shadow casting models to cast shadows.</td></tr>
    <tr><td>Shadow Distance</td><td>Directional lights only. The shadow distance is the maximum distance from the camera beyond which shadows that come from Directional Lights are no longer visible. Smaller values produce more detailed shadows. The closer the limit the less shadow data has to be mapped to, and represented by, any shadow map; shadow map pixels are mapped spatially and so the less distance the shadow map has to cover, the smaller the pixels and so the more resolution any shadow has.</td></tr>
    <tr><td>Shadow Resolution</td><td>The resolution of the shadowmap generated by this light source. This property is only used when Cast Shadows is checked. A high value will result in a more accurate shadow but will be at the cost of performance.</td></tr>
    <tr><td>Shadow Bias</td><td>Shadow bias is a constant depth offset applied to a shadow map that enables the tuning of shadows in order to eliminate rendering artifacts, namely 'shadow acne' and 'peter-panning'.</td></tr>
    <tr><td>Falloff Mode</td><td>Point and spot only. Controls the rate at which a light attentuates from its position.</td></tr>
</table>

## Scripting Interface

You can control a Light component's properties using a [script component][4]. The Light component's scripting interface is [here][5].

[1]: /images/user-manual/scenes/components/component-light-directional.jpg
[2]: /images/user-manual/scenes/components/component-light-point.jpg
[3]: /images/user-manual/scenes/components/component-light-spot.jpg
[4]: /user-manual/packs/components/script
[5]: /engine/api/stable/symbols/pc.LightComponent.html

