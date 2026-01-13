
---

## Background

| Parameter                             | Type      | Description                                                                              |
|---------------------------------------| --------- |------------------------------------------------------------------------------------------|
| **Body Background Texture**           | Texture2D | Background texture to be lerped into the body texture.                                   |
| **Body Background Texture Intensity** | Scalar    | Luminosity multiplier which determines how strongly the body background texture shows.   |
| **Border Background Intensity**       | Scalar    | Luminosity multiplier which determines how strongly the border background texture shows. |
| **Border Background Texture**         | Texture2D | Background texture to be lerped into the border texture.                                 |
| **Body Background Lower Strength**    | Scalar    | Lower bound multiplier for the color of the Body Background.                             |
| **Body Background Upper Strength**    | Scalar    | Upper bound multiplier for the color of the Body Background.                             |
| **Border Background Lower Strength**  | Scalar    | Lower bound multiplier for the color of the Border Background.                           |
| **Border Background Upper Strength**  | Scalar    | Upper bound multiplier for the color of the Border Background.                           |

---

## Button

| Parameter            | Type      | Description                                                                                    |
|----------------------|-----------|------------------------------------------------------------------------------------------------|
| **Button Size**      | Scalar    | Used to control the size of the button, particularly during animation.                         |
| **Mipmap bias**      | Scalar    | Used to provide a weak blue effect for minor AA. Seg Mip Gen Settins = Blur 1 in your texture. |
| **Position Y**       | Scalar    | Control of the Y value of the UV, useful for pressed animations.                               |
| **Button Texture**   | Texture2D | Red: Border, Blue: Body, Green: Opacity Mask                                                   |
| **Opacity Strength** | Scalar    | Scalar multiplier to Opacity                                                                   |
---

## Color

| Parameter        | Type           | Description                                     |
| ---------------- | -------------- |-------------------------------------------------|
| **Body Color**   | Vector (Color) | Multiplies into the body texture to color it.   |
| **Border Color** | Vector (Color) | Multiplies into the border texture to color it. |

---

## Glow

| Parameter                     | Type   | Description                                                                                                                                  |
| ----------------------------- | ------ |----------------------------------------------------------------------------------------------------------------------------------------------|
| **Body Inner Glow Intensity** | Scalar | Strungth of the of radial gradient which applied to the center of the body. Positive is a Dodge, legative is a burn. Used for Hover effects. |
| **Body Inner Glow Radius**    | Scalar | Radius of radial gradient which applied to the center of the body. Positive is a Dodge, legative is a burn. Used for Hover effects.          |

---

## Gradient

| Parameter                          | Type   | Description                                                                                                                                                                                                                      |
|------------------------------------|--------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Use Border Horizontal Gradient** | Scalar | Whether or not to apply a border horizontal gradient. 0 use none, 1 use all, inbetween use some. Play with this and the other use gradient params. You can create tons of different gradients types by moving the values around. | 
| **Use Border Vertical Gradient**   | Scalar | Whether or not to apply a border vertical gradient. 0 use none, 1 use all, inbetween use some. Play with this and the other use gradient params. You can create tons of different gradients types by moving the values around.   | 
| **Use Body Horizontal Gradient**   | Scalar | Whether or not to apply a body horizontal gradient. 0 use none, 1 use all, inbetween use some. Play with this and the other use gradient params. You can create tons of different gradients types by moving the values around.   | 
| **Use Body Vertical Gradient**     | Scalar | Whether or not to apply a body vertical gradient. 0 use none, 1 use all, inbetween use some. Play with this and the other use gradient params. You can create tons of different gradients types by moving the values around.     | 
| **Body Gradient Height**           | Scalar | Height of the Body Gradient(0, No gradient), (1, Gradient applies to to the full width as a scalar)                                                                                                                              |
| **Body Gradient Lower Strength**   | Scalar | Lower bound multiplier for the color of the Body Gradient.                                                                                                                                                                       |
| **Body Gradient Upper Strength**   | Scalar | Upper bound multiplier for the color of the Body Gradient.                                                                                                                                                                       |
| **Border Gradient Lower Strength** | Scalar | Lower bound multiplier for the color of the Border Gradient.                                                                                                                                                                     |
| **Border Gradient Upper Strength** | Scalar | Upper bound multiplier for the color of the Border Gradient.                                                                                                                                                                     |
| **BorderHorizontalGradientHeight** | Scalar | Height of the Border Gradient(0, No gradient), (1, Gradient applies to to the full width as a scalar)                                                                                                                            |
| **BorderVerticalGradientHeight**   | Scalar | Height of the Border Gradient(0, No gradient), (1, Gradient applies to to the full width as a scalar)                                                                                                                            |

---

## Grunge

| Parameter                        | Type      | Description                                                                          |
|----------------------------------|-----------|--------------------------------------------------------------------------------------|
| **Body Grunge Intensity**        | Scalar    | Luminosity multiplier which determines how strongly the Body Grunge Texture shows.   |
| **Body Grunge Texture**          | Texture2D | Grunge  texture to be lerped into the Body Texture.                                  |
| **Border Grunge Intensity**      | Scalar    | Luminosity multiplier which determines how strongly the Border Grunge Texture shows. |
| **Border Grunge Texture**        | Texture2D | Grunge Texture to be lerped into the Border Texture.                                 |
| **Body Grunge Lower Strength**   | Scalar    | Lower bound multiplier for the color of the Body Grunge.                             |
| **Body Grunge Upper Strength**   | Scalar    | Upper bound multiplier for the color of the Body Grunge.                             |
| **Border Grunge Lower Strength** | Scalar    | Lower bound multiplier for the color of the Border Grunge.                           |
| **Border Grunge Upper Strength** | Scalar    | Upper bound multiplier for the color of the Border Grunge.                           |

---

## Noise

| Parameter                         | Type      | Description                                                                         |
|-----------------------------------| --------- |-------------------------------------------------------------------------------------|
| **Body Noise Intensity**          | Scalar    | Luminosity multiplier which determines how strongly the Body Noise Texture shows.   |
| **Border Noise Intensity**        | Scalar    | Luminosity multiplier which determines how strongly the Border Noise Texture shows. |
| **Noise Texture**                 | Texture2D | Noise  texture to be lerped into the Body Texture.                                  |
| **Body Noise Lower Strength**     | Scalar    | Lower bound multiplier for the color of the Body Noise.                             |
| **Body Noise Upper Strength**     | Scalar    | Upper bound multiplier for the color of the Body Noise.                             |
| **Border Noise Lower Strength**   | Scalar    | Lower bound multiplier for the color of the Border Noise.                           |
| **Border Noise Upper Strength**   | Scalar    | Upper bound multiplier for the color of the Border Noise.                           |

---

## Stencil

| Parameter                           | Type      | Description                                                                                        |
| ----------------------------------- | --------- |----------------------------------------------------------------------------------------------------|
| **Body Stencil Gradient Height**    | Scalar    | Max value of the Gradient(0, No gradient), (1, Gradient applies to to the full width as a scalar). |
| **Body Stencil Gradient Sharpness** | Scalar    | How steep is the curve of the gradient. Flattens out the curve at the beginning.                   |
| **Body Stencil Intensity**          | Scalar    | Intensity of the stencil overlay on the body of the button.                                        |
| **Body Stencil Texture**            | Texture2D | Stenciled design for the image.                                                                    |
