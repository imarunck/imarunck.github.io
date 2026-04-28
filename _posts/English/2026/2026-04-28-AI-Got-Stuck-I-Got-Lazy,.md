---
layout: post
title: AI Got Stuck, I Got Lazy, Font Got Done
date: 2026-04-28
categories: blog english
author: arun
tag: [type design, kannada projects]
image: /assets/images/encoding.jpg
---

# AI Got Stuck, I Got Lazy, Font Got Done

*AI is fast, but still needs a human to finish the job.*

---

So I wanted to import particular glyph slots from another font.

I asked AI.

It gave some general method.  
Didn’t work.

Asked again.  
It suggested Python script.

Error.

Tried again.  
Another script.

Still error.

Then I went back to general method again.  
Didn’t work.

At this point I was too lazy to actually think properly 😅  
So I kept doing one thing —  
copy error → paste in chat → “fix this”

AI kept trying.  
But it started going in circles.

Because this is very niche area —  
FontLab scripting + encoding + slots —  
it didn’t have enough clear data to solve it properly.

Finally it said:

> “Do it manually one by one.”

There were around **230 slots**.

No way I’m doing that 😄

---

So I tried myself.

Just simple thinking.

I removed all unwanted glyphs from the source font,  
kept only those 230.

Exported the encoding.

Then imported that encoding into my target font.

Done.

---

Maybe there is a better way.  
But that’s not the point.

---

## The point is:

AI alone can’t always solve everything.  
Sometimes it gets stuck in a loop.

But also —  
without AI, I wouldn’t even try scripting.

Before:

- writing 800 lines of code → 1 full day

Now:

- AI gives working base in 1 minute

---

## Final thought

> Human needs AI  
> AI needs human

Both together → work gets done.