# Errors detected
- [`Error parsing recipe; Failed to parse either. First: No key amount; No key id; Second: Failed to parse either. First: No key id; Second: Failed to parse either. First: Not a JSON object; Second: Compat cannot be deserialized; Failed to parse either. First: No key amount; No key id; Second: Failed to parse either. First: No key id; Second: Failed to parse either. First: Not a JSON object; Second: Compat cannot be deserialized; Failed to parse either. First: No key amount; No key id; Second: Failed to parse either. First: No key id; Second: Failed to parse either. First: Not a JSON object; Second: Compat cannot be deserialized`](#error-parsing-recipe-failed-to-parse-either-first-no-key-amount-no-key-id-second-failed-to-parse-either-first-no-key-id-second-failed-to-parse-either-first-not-a-json-object-second-compat-cannot-be-deserialized-failed-to-parse-either-first-no-key-amount-no-key-id-second-failed-to-parse-either-first-no-key-id-second-failed-to-parse-either-first-not-a-json-object-second-compat-cannot-be-deserialized-failed-to-parse-either-first-no-key-amount-no-key-id-second-failed-to-parse-either-first-no-key-id-second-failed-to-parse-either-first-not-a-json-object-second-compat-cannot-be-deserialized)
- [`Error parsing recipe; No key itemIdRegex; Unknown registry key; Unknown registry key; Unknown registry key; No key validItems;`](#error-parsing-recipe-no-key-itemidregex-unknown-registry-key-unknown-registry-key-unknown-registry-key-no-key-validitems)
- [`Error parsing recipe; No key validItems;`](#error-parsing-recipe-no-key-validitems)
- [`Error parsing recipe; Unknown registry key;`](#error-parsing-recipe-unknown-registry-key)
- [`Error parsing recipe; Unknown registry key; No key validItems;`](#error-parsing-recipe-unknown-registry-key-no-key-validitems)
- [`Error parsing recipe; Unknown registry key; Unknown registry key; No key validItems;`](#error-parsing-recipe-unknown-registry-key-unknown-registry-key-no-key-validitems)
- [`Failed to read required component 'spirits: spirit_ingredient[]'`](#failed-to-read-required-component-spirits-spirit_ingredient)
- [`Invalid component ingredients: ingredient[]`](#invalid-component-ingredients-ingredient)
- [`Invalid component key: pattern<ingredient>`](#invalid-component-key-patterningredient)

##### `Error parsing recipe; Failed to parse either. First: No key amount; No key id; Second: Failed to parse either. First: No key id; Second: Failed to parse either. First: Not a JSON object; Second: Compat cannot be deserialized; Failed to parse either. First: No key amount; No key id; Second: Failed to parse either. First: No key id; Second: Failed to parse either. First: Not a JSON object; Second: Compat cannot be deserialized; Failed to parse either. First: No key amount; No key id; Second: Failed to parse either. First: No key id; Second: Failed to parse either. First: Not a JSON object; Second: Compat cannot be deserialized`

<details>
<summary>malum:create/milling/grim_talc</summary>

`java.lang.IllegalArgumentException: Error parsing recipe malum:create/milling/grim_talc: Failed to parse either. First: No key amount in MapLike[{"chance":0.25,"count":4,"item":"minecraft:bone_meal"}]; No key id in MapLike[{"chance":0.25,"count":4,"item":"minecraft:bone_meal"}]; Second: Failed to parse either. First: No key id in MapLike[{"chance":0.25,"count":4,"item":"minecraft:bone_meal"}]; Second: Failed to parse either. First: Not a JSON object: "minecraft:bone_meal"; Second: Compat cannot be deserialized; Failed to parse either. First: No key amount in MapLike[{"chance":0.25,"item":"minecraft:yellow_dye"}]; No key id in MapLike[{"chance":0.25,"item":"minecraft:yellow_dye"}]; Second: Failed to parse either. First: No key id in MapLike[{"chance":0.25,"item":"minecraft:yellow_dye"}]; Second: Failed to parse either. First: Not a JSON object: "minecraft:yellow_dye"; Second: Compat cannot be deserialized; Failed to parse either. First: No key amount in MapLike[{"count":6,"item":"minecraft:bone_meal"}]; No key id in MapLike[{"count":6,"item":"minecraft:bone_meal"}]; Second: Failed to parse either. First: No key id in MapLike[{"count":6,"item":"minecraft:bone_meal"}]; Second: Failed to parse either. First: Not a JSON object: "minecraft:bone_meal"; Second: Compat cannot be deserialized`

`mod/malum`

```json
{
  "neoforge:conditions": [
    {
      "type": "almostunified:conditional",
      "conditions_met": true,
      "original_conditions": [
        {
          "type": "neoforge:mod_loaded",
          "modid": "create"
        }
      ]
    }
  ],
  "type": "create:milling",
  "ingredients": [
    {
      "item": "malum:grim_talc"
    }
  ],
  "processing_time": 100,
  "results": [
    {
      "count": 6,
      "item": "minecraft:bone_meal"
    },
    {
      "chance": 0.25,
      "item": "minecraft:yellow_dye"
    },
    {
      "chance": 0.25,
      "count": 4,
      "item": "minecraft:bone_meal"
    }
  ]
}
```

</details>

##### `Error parsing recipe; No key itemIdRegex; Unknown registry key; Unknown registry key; Unknown registry key; No key validItems;`

<details>
<summary>malum:malum/spirit_repair/undergarden/forgotten</summary>

`java.lang.IllegalArgumentException: Error parsing recipe malum:malum/spirit_repair/undergarden/forgotten: No key itemIdRegex in MapLike[{}]; Unknown registry key in ResourceKey[minecraft:root / malum:spirit_types]: minecraft:eldritch; Unknown registry key in ResourceKey[minecraft:root / malum:spirit_types]: minecraft:arcane; Unknown registry key in ResourceKey[minecraft:root / malum:spirit_types]: minecraft:earthen; No key validItems in MapLike[{"neoforge:conditions":[{"type":"almostunified:conditional","conditions_met":true,"original_conditions":[{"type":"neoforge:mod_loaded","modid":"undergarden"}]}],"type":"malum:spirit_repair","itemIdRegex":"forgotten_.+","modIdRegex":"undergarden","durabilityPercentage":0.75,"inputs":[],"repairMaterial":{"item":"undergarden:forgotten_ingot","count":1},"spirits":[{"type":"earthen","count":20},{"type":"arcane","count":12},{"type":"eldritch","count":2}],"regex":{}}]`

`mod/malum`

```json
{
  "neoforge:conditions": [
    {
      "type": "almostunified:conditional",
      "conditions_met": true,
      "original_conditions": [
        {
          "type": "neoforge:mod_loaded",
          "modid": "undergarden"
        }
      ]
    }
  ],
  "type": "malum:spirit_repair",
  "itemIdRegex": "forgotten_.+",
  "modIdRegex": "undergarden",
  "durabilityPercentage": 0.75,
  "inputs": [],
  "repairMaterial": {
    "item": "undergarden:forgotten_ingot",
    "count": 1
  },
  "spirits": [
    {
      "type": "earthen",
      "count": 20
    },
    {
      "type": "arcane",
      "count": 12
    },
    {
      "type": "eldritch",
      "count": 2
    }
  ],
  "regex": {}
}
```

</details>

##### `Error parsing recipe; No key validItems;`

<details>
<summary>malum:malum/spirit_repair/occultism/gold_chalk</summary>

`java.lang.IllegalArgumentException: Error parsing recipe malum:malum/spirit_repair/occultism/gold_chalk: No key validItems in MapLike[{"neoforge:conditions":[{"type":"almostunified:conditional","conditions_met":true,"original_conditions":[{"type":"neoforge:mod_loaded","modid":"occultism"}]}],"type":"malum:spirit_repair","durabilityPercentage":1,"repairMaterial":{"count":1,"tag":"c:dusts/gold"},"spirits":[{"type":"malum:arcane","count":8}],"inputs":["occultism:chalk_gold"]}]`

`mod/malum`

```json
{
  "neoforge:conditions": [
    {
      "type": "almostunified:conditional",
      "conditions_met": true,
      "original_conditions": [
        {
          "type": "neoforge:mod_loaded",
          "modid": "occultism"
        }
      ]
    }
  ],
  "type": "malum:spirit_repair",
  "durabilityPercentage": 1,
  "repairMaterial": {
    "count": 1,
    "tag": "c:dusts/gold"
  },
  "spirits": [
    {
      "type": "malum:arcane",
      "count": 8
    }
  ],
  "inputs": [
    "occultism:chalk_gold"
  ]
}
```

</details>

<details>
<summary>malum:malum/spirit_repair/occultism/purple_chalk</summary>

`java.lang.IllegalArgumentException: Error parsing recipe malum:malum/spirit_repair/occultism/purple_chalk: No key validItems in MapLike[{"neoforge:conditions":[{"type":"almostunified:conditional","conditions_met":true,"original_conditions":[{"type":"neoforge:mod_loaded","modid":"occultism"}]}],"type":"malum:spirit_repair","durabilityPercentage":1,"repairMaterial":{"count":2,"tag":"c:dusts/obsidian"},"spirits":[{"type":"malum:arcane","count":8}],"inputs":["occultism:chalk_purple"]}]`

`mod/malum`

```json
{
  "neoforge:conditions": [
    {
      "type": "almostunified:conditional",
      "conditions_met": true,
      "original_conditions": [
        {
          "type": "neoforge:mod_loaded",
          "modid": "occultism"
        }
      ]
    }
  ],
  "type": "malum:spirit_repair",
  "durabilityPercentage": 1,
  "repairMaterial": {
    "count": 2,
    "tag": "c:dusts/obsidian"
  },
  "spirits": [
    {
      "type": "malum:arcane",
      "count": 8
    }
  ],
  "inputs": [
    "occultism:chalk_purple"
  ]
}
```

</details>

<details>
<summary>malum:malum/spirit_repair/occultism/red_chalk</summary>

`java.lang.IllegalArgumentException: Error parsing recipe malum:malum/spirit_repair/occultism/red_chalk: No key validItems in MapLike[{"neoforge:conditions":[{"type":"almostunified:conditional","conditions_met":true,"original_conditions":[{"type":"neoforge:mod_loaded","modid":"occultism"}]}],"type":"malum:spirit_repair","durabilityPercentage":1,"repairMaterial":{"count":1,"item":"occultism:afrit_essence"},"spirits":[{"type":"malum:arcane","count":8}],"inputs":["occultism:chalk_red"]}]`

`mod/malum`

```json
{
  "neoforge:conditions": [
    {
      "type": "almostunified:conditional",
      "conditions_met": true,
      "original_conditions": [
        {
          "type": "neoforge:mod_loaded",
          "modid": "occultism"
        }
      ]
    }
  ],
  "type": "malum:spirit_repair",
  "durabilityPercentage": 1,
  "repairMaterial": {
    "count": 1,
    "item": "occultism:afrit_essence"
  },
  "spirits": [
    {
      "type": "malum:arcane",
      "count": 8
    }
  ],
  "inputs": [
    "occultism:chalk_red"
  ]
}
```

</details>

<details>
<summary>malum:malum/spirit_repair/occultism/white_chalk</summary>

`java.lang.IllegalArgumentException: Error parsing recipe malum:malum/spirit_repair/occultism/white_chalk: No key validItems in MapLike[{"neoforge:conditions":[{"type":"almostunified:conditional","conditions_met":true,"original_conditions":[{"type":"neoforge:mod_loaded","modid":"occultism"}]}],"type":"malum:spirit_repair","durabilityPercentage":1,"repairMaterial":{"count":1,"item":"occultism:burnt_otherstone"},"spirits":[{"type":"malum:arcane","count":8}],"inputs":["occultism:chalk_white"]}]`

`mod/malum`

```json
{
  "neoforge:conditions": [
    {
      "type": "almostunified:conditional",
      "conditions_met": true,
      "original_conditions": [
        {
          "type": "neoforge:mod_loaded",
          "modid": "occultism"
        }
      ]
    }
  ],
  "type": "malum:spirit_repair",
  "durabilityPercentage": 1,
  "repairMaterial": {
    "count": 1,
    "item": "occultism:burnt_otherstone"
  },
  "spirits": [
    {
      "type": "malum:arcane",
      "count": 8
    }
  ],
  "inputs": [
    "occultism:chalk_white"
  ]
}
```

</details>

##### `Error parsing recipe; Unknown registry key;`

<details>
<summary>malum:malum/spirit_repair/undergarden/slingshot</summary>

`java.lang.IllegalArgumentException: Error parsing recipe malum:malum/spirit_repair/undergarden/slingshot: Unknown registry key in ResourceKey[minecraft:root / malum:spirit_types]: minecraft:earthen`

`mod/malum`

```json
{
  "neoforge:conditions": [
    {
      "type": "almostunified:conditional",
      "conditions_met": true,
      "original_conditions": [
        {
          "type": "neoforge:mod_loaded",
          "modid": "undergarden"
        }
      ]
    }
  ],
  "type": "malum:spirit_repair",
  "durabilityPercentage": 0.5,
  "repairMaterial": {
    "item": "undergarden:twistytwig",
    "count": 1
  },
  "spirits": [
    {
      "type": "earthen",
      "count": 2
    }
  ],
  "validItems": [
    "undergarden:slingshot"
  ]
}
```

</details>

##### `Error parsing recipe; Unknown registry key; No key validItems;`

<details>
<summary>malum:malum/spirit_repair/undergarden/cloggrum</summary>

`java.lang.IllegalArgumentException: Error parsing recipe malum:malum/spirit_repair/undergarden/cloggrum: Unknown registry key in ResourceKey[minecraft:root / malum:spirit_types]: minecraft:earthen; No key validItems in MapLike[{"neoforge:conditions":[{"type":"almostunified:conditional","conditions_met":true,"original_conditions":[{"type":"neoforge:mod_loaded","modid":"undergarden"}]}],"type":"malum:spirit_repair","durabilityPercentage":0.5,"repairMaterial":{"item":"undergarden:cloggrum_ingot","count":2},"spirits":[{"type":"earthen","count":12}],"regex":{"itemIdRegex":"cloggrum_.+","modIdRegex":"undergarden"}}]`

`mod/malum`

```json
{
  "neoforge:conditions": [
    {
      "type": "almostunified:conditional",
      "conditions_met": true,
      "original_conditions": [
        {
          "type": "neoforge:mod_loaded",
          "modid": "undergarden"
        }
      ]
    }
  ],
  "type": "malum:spirit_repair",
  "durabilityPercentage": 0.5,
  "repairMaterial": {
    "item": "undergarden:cloggrum_ingot",
    "count": 2
  },
  "spirits": [
    {
      "type": "earthen",
      "count": 12
    }
  ],
  "regex": {
    "itemIdRegex": "cloggrum_.+",
    "modIdRegex": "undergarden"
  }
}
```

</details>

##### `Error parsing recipe; Unknown registry key; Unknown registry key; No key validItems;`

<details>
<summary>malum:malum/spirit_repair/undergarden/froststeel</summary>

`java.lang.IllegalArgumentException: Error parsing recipe malum:malum/spirit_repair/undergarden/froststeel: Unknown registry key in ResourceKey[minecraft:root / malum:spirit_types]: minecraft:arcane; Unknown registry key in ResourceKey[minecraft:root / malum:spirit_types]: minecraft:aqueous; No key validItems in MapLike[{"neoforge:conditions":[{"type":"almostunified:conditional","conditions_met":true,"original_conditions":[{"type":"neoforge:mod_loaded","modid":"undergarden"}]}],"type":"malum:spirit_repair","durabilityPercentage":0.5,"repairMaterial":{"item":"undergarden:froststeel_ingot","count":2},"spirits":[{"type":"aqueous","count":8},{"type":"arcane","count":4}],"regex":{"itemIdRegex":"froststeel_.+","modIdRegex":"undergarden"}}]`

`mod/malum`

```json
{
  "neoforge:conditions": [
    {
      "type": "almostunified:conditional",
      "conditions_met": true,
      "original_conditions": [
        {
          "type": "neoforge:mod_loaded",
          "modid": "undergarden"
        }
      ]
    }
  ],
  "type": "malum:spirit_repair",
  "durabilityPercentage": 0.5,
  "repairMaterial": {
    "item": "undergarden:froststeel_ingot",
    "count": 2
  },
  "spirits": [
    {
      "type": "aqueous",
      "count": 8
    },
    {
      "type": "arcane",
      "count": 4
    }
  ],
  "regex": {
    "itemIdRegex": "froststeel_.+",
    "modIdRegex": "undergarden"
  }
}
```

</details>

<details>
<summary>malum:malum/spirit_repair/undergarden/utherium</summary>

`java.lang.IllegalArgumentException: Error parsing recipe malum:malum/spirit_repair/undergarden/utherium: Unknown registry key in ResourceKey[minecraft:root / malum:spirit_types]: minecraft:infernal; Unknown registry key in ResourceKey[minecraft:root / malum:spirit_types]: minecraft:arcane; No key validItems in MapLike[{"neoforge:conditions":[{"type":"almostunified:conditional","conditions_met":true,"original_conditions":[{"type":"neoforge:mod_loaded","modid":"undergarden"}]}],"type":"malum:spirit_repair","durabilityPercentage":0.5,"inputs":[],"repairMaterial":{"item":"undergarden:utherium_crystal","count":2},"spirits":[{"type":"arcane","count":12},{"type":"infernal","count":12}],"regex":{"itemIdRegex":"utherium_.+","modIdRegex":"undergarden"}}]`

`mod/malum`

```json
{
  "neoforge:conditions": [
    {
      "type": "almostunified:conditional",
      "conditions_met": true,
      "original_conditions": [
        {
          "type": "neoforge:mod_loaded",
          "modid": "undergarden"
        }
      ]
    }
  ],
  "type": "malum:spirit_repair",
  "durabilityPercentage": 0.5,
  "inputs": [],
  "repairMaterial": {
    "item": "undergarden:utherium_crystal",
    "count": 2
  },
  "spirits": [
    {
      "type": "arcane",
      "count": 12
    },
    {
      "type": "infernal",
      "count": 12
    }
  ],
  "regex": {
    "itemIdRegex": "utherium_.+",
    "modIdRegex": "undergarden"
  }
}
```

</details>

##### `Failed to read required component 'spirits: spirit_ingredient[]'`

<details>
<summary>malum:malum/spirit_repair/undergarden/slingshot</summary>

`java.lang.IllegalStateException: Unknown registry key in ResourceKey[minecraft:root / malum:spirit_types]: minecraft:earthen`

`mod/malum`

```json
{
  "neoforge:conditions": [
    {
      "type": "almostunified:conditional",
      "conditions_met": true,
      "original_conditions": [
        {
          "type": "neoforge:mod_loaded",
          "modid": "undergarden"
        }
      ]
    }
  ],
  "type": "malum:spirit_repair",
  "durabilityPercentage": 0.5,
  "repairMaterial": {
    "item": "undergarden:twistytwig",
    "count": 1
  },
  "spirits": [
    {
      "type": "earthen",
      "count": 2
    }
  ],
  "validItems": [
    "undergarden:slingshot"
  ]
}
```

</details>

##### `Invalid component ingredients: ingredient[]`

<details>
<summary>herbsandharvest:pepperoni</summary>

`Component 'ingredient' is not allowed to be empty!`

`mod/herbsandharvest`

```json
{
  "type": "minecraft:crafting_shapeless",
  "category": "misc",
  "ingredients": [
    {
      "tag": "c:foods/beef"
    },
    {
      "tag": "c:foods/pork"
    },
    {
      "tag": "c:foods/minced_garlic"
    },
    {
      "tag": "c:items/pepper"
    },
    {
      "item": "herbsandharvest:mustard_seeds"
    }
  ],
  "result": {
    "count": 1,
    "id": "herbsandharvest:pepperoni"
  }
}
```

</details>

<details>
<summary>herbsandharvest:sausage</summary>

`Component 'ingredient' is not allowed to be empty!`

`mod/herbsandharvest`

```json
{
  "type": "minecraft:crafting_shapeless",
  "category": "misc",
  "ingredients": [
    {
      "tag": "c:foods/pork"
    },
    {
      "tag": "c:foods/minced_garlic"
    },
    {
      "item": "herbsandharvest:chopped_sage"
    },
    {
      "item": "herbsandharvest:chopped_thyme"
    },
    {
      "item": "herbsandharvest:chopped_rosemary"
    },
    {
      "tag": "c:items/salt"
    },
    {
      "tag": "c:items/pepper"
    }
  ],
  "result": {
    "count": 1,
    "id": "herbsandharvest:sausage"
  }
}
```

</details>

##### `Invalid component key: pattern<ingredient>`

<details>
<summary>createthrusters:diagnostic_tablet</summary>

`Component 'ingredient' is not allowed to be empty!`

`mod/createthrusters`

```json
{
  "type": "minecraft:crafting_shaped",
  "category": "misc",
  "pattern": [
    "BBB",
    "GCG",
    " I "
  ],
  "key": {
    "B": {
      "item": "createthrusters:acc_display_panel"
    },
    "G": {
      "tag": "c:glass"
    },
    "C": {
      "item": "createthrusters:computation_mechanism"
    },
    "I": {
      "item": "createthrusters:blackstone_sheet"
    }
  },
  "result": {
    "id": "createthrusters:diagnostic_tablet",
    "count": 1
  }
}
```

</details>

