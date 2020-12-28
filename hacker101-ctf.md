# Hacker101 CTF

> The [Hacker101 CTF](https://ctf.hacker101.com/) is a game designed to let you learn to hack in a safe, rewarding environment. Hacker101 is a free educational site for hackers, run by [HackerOne](https://hackerone.com/). This CTF is another integral component in our plans to make the world a better place, one bug at a time.

> All flags take the form "^FLAG^...hex...$FLAG$" but you can omit everything but the hex.

## A little something to get you started - Web

#### Flag 1

By inspecting the page, we can see that the header has a `<style>` element with the following CSS selector:

```css
body { background-image: url("background.png"); }
```

The flag is at `/background.png`:

```
^FLAG^009e59d511c6f84de174ff02c49493269ae2dcfa52281901875872facf53715f$FLAG$
```

## Micro-CMS v1 - Web

#### Flag 2

By noticing that when I created a new page, the new URL had an integer at the end, I had to look and see what I could find if I followed the number from 0 to the new page number.

The flag is at `/page/edit/4`:

```
^FLAG^b07436d8757b3b3fad10ffc96072f136dfdf06c477549720143789ab6b0b034b$FLAG$
```

#### Flag 3

`/page/4` is `Forbidden`, and it says:

> You don't have the permission to access the requested resource. It is either read-protected or not readable by the server.

The other pages, except the first ones and the newly created page, return `Not Found`.
