<!-- .slide: data-background="#E6F7FF" -->

<section data-transition="none">

## Coding

```assembly[1-2]
    1149:       f3 0f 1e fa             endbr64
    114d:       48 83 ec 08             sub    rsp,0x8
    1151:       ba 01 00 00 00          mov    edx,0x1
    1156:       48 8d 35 a7 0e 00 00    lea    rsi,[rip+0xea7]        # 2004 <_IO_stdin_used+0x4>
    115d:       bf 01 00 00 00          mov    edi,0x1
    1162:       b8 00 00 00 00          mov    eax,0x0
    1167:       e8 e4 fe ff ff          call   1050 <__printf_chk@plt>
    116c:       b8 00 00 00 00          mov    eax,0x0
    1171:       48 83 c4 08             add    rsp,0x8
    1175:       c3                      retimport dataclasses

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
