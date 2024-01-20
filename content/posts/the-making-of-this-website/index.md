+++
title = 'The Making of This Website'
date = 2023-12-19T08:25:37+08:00
draft = false
+++

This is my new website. It's a [Hugo](https://gohugo.io/) website and I used a theme called *[Blowfish](https://blowfish.page/)* by [Nuno Coração](https://github.com/nunocoracao/). It's an awesome theme with a lot of stuff you can customize. I created a new color scheme for this website using Nuno's NodeJS application called *[Fugu](https://github.com/nunocoracao/fugu)* to generate the color scheme I called **Rose**.

{{< github repo="nunocoracao/fugu" >}}

<br>

#### Rose
{{< swatches "#a73937" "#d4625e" "#40101a" >}}
**Hex colors:** #A73937 *(Neutral)*, #D4625E *(Primary)*, #40101A *(Secondary)*

{{< alert icon="circle-info" >}} Check out Rose color scheme on Gist: [rose.css](https://gist.github.com/mksalada/2fb904ad45d2196eac5885c4d192a586) {{< /alert >}}

<br>

I also added and changed some of its styling (CSS).

```
# assests/css/custom.css

:root {
    --neutral-color:    #a73937;
    --primary-color:    #d4625e;
    --secondary-color:  #40101a;
}

::selection {
    color:      var(--primary-color);
    background: var(--secondary-color);
}

input,
textarea {
    box-sizing: border-box !important;
    outline:    none !important;
    border:     1px solid var(--primary-color) !important;
    color:      var(--primary-color) !important;
}

input:focus,
textarea:focus {
    border:          1px solid var(--primary-color) !important;
    --tw-ring-color: var(--primary-color) !important;
}
```

<br>

If you also like to have a website like this one, see the following documentations:
- [Hugo Documentation](https://gohugo.io/documentation/)
- [Blowfish Documentation](https://blowfish.page/docs/)
- [Fugu Repository](https://github.com/nunocoracao/fugu/#fugu)
