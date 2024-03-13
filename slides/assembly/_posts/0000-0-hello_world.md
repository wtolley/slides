<section data-transition="none">

## Coding

```python[1-2]
import dataclasses
import yaml2pyclass

class Config(yaml2pyclass.CodeGenerator):
    @dataclasses.dataclass
    class ClusterConfigClass:
        eps: float
        min_num_samples: int

    image_size: list
    cluster_config: ClusterConfigClass
    path_output: str
```

First do `import`s

</section>

<section data-transition="none">

## Coding

```python[4-12]
import dataclasses
import yaml2pyclass

class Config(yaml2pyclass.CodeGenerator):
    @dataclasses.dataclass
    class ClusterConfigClass:
        eps: float
        min_num_samples: int

    image_size: list
    cluster_config: ClusterConfigClass
    path_output: str
```

Then follows the rest

</section>

---

## Coding large

```html[3-5|18-20]
<table>
  <tr>
    <td>Apples</td>
    <td>$1</td>
    <td>7</td>
  </tr>
  <tr>
    <td>Oranges</td>
    <td>$2</td>
    <td>18</td>
  </tr>
  <tr>
    <td>Kiwi</td>
    <td>$3</td>
    <td>1</td>
  </tr>
  <tr>
    <td>Banana</td>
    <td>$2</td>
    <td>2</td>
  </tr>
</table>

```

---
