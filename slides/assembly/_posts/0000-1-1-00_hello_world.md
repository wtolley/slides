<!-- .slide: data-background="#E6F7FF" -->

<section data-transition="none">

## Hello World Disassembly

```assembly[2]
endbr64
sub    rsp,0x8
mov    edx,0x1
lea    rsi,[rip+0xea7]        # 2004 <_IO_stdin_used+0x4>
mov    edi,0x1
mov    eax,0x0
call   1050 <__printf_chk@plt>
mov    eax,0x0
add    rsp,0x8
ret

```

What is this instruction doing?

</section>

<section data-transition="none">

## Hello World Disassembly

```assembly[2]
endbr64
sub    rsp,0x8
mov    edx,0x1
lea    rsi,[rip+0xea7]        # 2004 <_IO_stdin_used+0x4>
mov    edi,0x1
mov    eax,0x0
call   1050 <__printf_chk@plt>
mov    eax,0x0
add    rsp,0x8
ret

```

Subtracting 8 from the stack pointer. Why?

</section>

<section data-transition="none">

## Hello World Disassembly

```assembly[2]
endbr64
sub    rsp,0x8
mov    edx,0x1
lea    rsi,[rip+0xea7]        # 2004 <_IO_stdin_used+0x4>
mov    edi,0x1
mov    eax,0x0
call   1050 <__printf_chk@plt>
mov    eax,0x0
add    rsp,0x8
ret

```

Create room for local variables (can also be used for alignment/padding).

</section>


<section data-transition="none">

## Hello World Disassembly

```assembly[3]
endbr64
sub    rsp,0x8
mov    edx,0x1
lea    rsi,[rip+0xea7]        # 2004 <_IO_stdin_used+0x4>
mov    edi,0x1
mov    eax,0x0
call   1050 <__printf_chk@plt>
mov    eax,0x0
add    rsp,0x8
ret

```

What's going on here?

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
