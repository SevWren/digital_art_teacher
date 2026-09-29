# Light and Value

**Status:** Work in progress.

Value (relative lightness or darkness) is the primary carrier of form, depth, and hierarchy. Colour is applied on top of a value structure; a weak value design cannot be rescued by colour alone.

## Value Families

Most professional work organises the image into a small number of value families (commonly two or three):

- Light family (areas receiving direct or strong light)
- Shadow family (areas in form shadow or cast shadow)
- Optional mid-tone or accent family

Keeping the light family and shadow family clearly separated is the single most reliable way to maintain readable form.

## Components of Light on Form

For a simple lit form (sphere, cylinder, box):

- **Highlight** — specular reflection of the light source (small, high value).
- **Light** — surface facing the light source.
- **Halftone / Mid-tone** — transitional planes.
- **Core shadow** — the darkest part of the form shadow, where the surface turns away from the light and receives little or no reflected light.
- **Reflected light** — light bouncing from surrounding surfaces into the shadow side (usually lower in value than the light family).
- **Cast shadow** — shadow projected onto another surface; its edge hardness depends on the size and distance of the light source.
- **Occlusion / Contact shadow** — the darkest value where two surfaces meet and ambient light is blocked.

## Light Types and Roles

- **Key light** — primary, directional light that defines the main form modelling.
- **Fill light** — softer, lower-intensity light that lifts shadow values without erasing the key.
- **Rim / Back light** — light from behind that separates the subject from the background.
- **Ambient / Environment light** — diffuse illumination from the surroundings.

Describe light direction with clock position (viewer’s perspective) and elevation in degrees when precision is required.

## Decision Criteria

1. Decide the light direction and quality (hard vs soft) before detailed rendering.
2. Establish the value hierarchy of the whole image (which areas are lightest and darkest) before local form modelling.
3. Keep the light-family values and shadow-family values from mixing indiscriminately.
4. Use cast-shadow shape and edge quality as additional information about light direction and surface distance.

## Common Failure Modes

- “Muddy” values: light and shadow families intermixed so that form reading collapses.
- Over-reliance on local colour without a clear value structure.
- Ignoring reflected light or occlusion, producing floating or cut-out forms.
- Changing the light direction midway without updating all dependent shadows and highlights.

## Relationship to Pipeline

Value and lighting are the primary concern of stage 06 and remain the structural backbone for stages 07–10. The value study is a primary source that later colour and rendering stages should respect.
