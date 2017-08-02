# Shufflepuck

Play shufflepuck in [here4](http://www.here4.io/).

## Code

To put a plain Shufflepuck table into your world:

```elm
import Shufflepuck

...
    , apps =
        [ ...
        , Shufflepuck.create Shufflepuck.default
        ...
```

To style your table:

```elm

import Shufflepuck

...
    , apps =
        [ ...
        , let
            s =
                Shufflepuck.default
          in
            Shufflepuck.create
                { s
                    | id = "shufflepuck"
                    , position = vec3 20 0 12
                    , tableTexture = "textures/table.jpg"
                    , puckTexture = "textures/puck.jpg"
                    , paddleTexture = "textures/paddle.jpg"
                }
        ...
```

You can also modify gameplay values like goalWidth, puckMass, paddleMass, and puckMaxSpeed.
See the definition of Shufflepuck.default for more ideas.

