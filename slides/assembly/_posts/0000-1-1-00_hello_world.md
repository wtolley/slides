<!-- .slide: data-background="#E6F7FF" -->

<section data-transition="none">

## Hello World Disassembly

```assembly[1- 2, 8-9]
0000119d <add>:
    119d:       55                      push   ebp
    119e:       89 e5                   mov    ebp,esp
    11a0:       e8 72 00 00 00          call   1217 <__x86.get_pc_thunk.ax>
    11a5:       05 33 2e 00 00          add    eax,0x2e33
    11aa:       8b 55 08                mov    edx,DWORD PTR [ebp+0x8]
    11ad:       8b 45 0c                mov    eax,DWORD PTR [ebp+0xc]
    11b0:       01 d0                   add    eax,edx
    11b2:       5d                      pop    ebp
    11b3:       c3                      ret

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
