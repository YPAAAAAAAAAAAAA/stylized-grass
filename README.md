# Stylized Grass

Instanced stylized grass and flowers with wind. This GitBrew post plays that one effect, full-bleed, as soon as the page loads.

The meadow is the `/grass` idea from [cortiz2894/stylized-components](https://github.com/cortiz2894/stylized-components) (MIT). Copyright (c) 2026 Christian Ortiz (Cortiz). Blades and flowers are scattered on a rolling ground, then bent by a shared wind field in the vertex shader. The sky is a gradient dome with a low sun. Menus and the Leva panel are not part of this play page.

The original scene shipped a multi-megabyte glTF, a field buffer, and large flower and bark textures. This play page rebuilds the same kind of meadow in WebGL from a few thousand procedural blades and billboard flowers so the first frame can draw immediately. No image files are loaded. If the GL context cannot be created, the canvas stays black.

Drag to look around. Pinch to move closer or farther. The field keeps swaying on its own.

## iPhone WebGL

WebGL only (`webgl2`, or `webgl` when that is what the phone offers). There is no other graphics backend. Device pixel ratio is capped so the meadow stays inside a phone's fill budget. Nothing is fetched at runtime.
