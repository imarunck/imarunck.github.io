---
layout: post
title: I Accidentally Built My Own Cloud Music Platform
date: 2026-05-19
categories: blog english
author: arun
tag: [vibe coding, programming]
image: /assets/images/music.jpg
---

# I Accidentally Built My Own Cloud Music Platform

> Music was never simple for me.

I listen to too much variety of music. Kannada, Hindi, Urdu, old retro songs, bhakti songs, ghazals, independent artists, random YouTube uploads, film albums, feelgood songs, sad songs everything. At one point of time I literally had premium subscriptions of almost every music platform available. Spotify Premium, Apple Music, JioSaavn Pro and others. Still somehow some songs were missing.

Some artist upload only on YouTube.
Some songs are removed because of rights.
Some albums are incomplete.
Some versions are not available.

And I hated that feeling of “this song is not available in your region” when I am already paying money.

So slowly I started downloading my own songs.

At first it was just folders inside my computer. Then slowly it became a proper library. Albums, cover arts, lyrics, organized folders. I realised I was no more streaming music. I was collecting it.

But then another problem started.

### How do I sync this across my devices?

I tried almost everything I could find. Cloud syncing apps, music sync apps, random services, local network apps, file sharing methods. Some worked for few days then became annoying. Some had limits. Some had bad apps. Some were expensive. Some felt very temporary.

Nothing felt sustainable.

Then I went into the self-hosting rabbit hole.

I tried setting up Jellyfin and similar systems using my laptop. Technically it worked. But practically it was pain. Keeping system online, same wifi syncing, local network issues, remote access, ports, keeping laptop alive all the time. It felt like too much infrastructure just to listen songs.

Then I thought okay let’s build my own thing.

That was honestly a bad idea at first.

I started trying to create a complete music app with backend, frontend, user accounts, syncing playlists, storing user data, authentication and all those things. Using AI coding tools I kept generating code and fixing things. Some parts worked. Some completely broke.

Very quickly I understood why building streaming apps is hard.

The moment user data starts going back to server everything becomes complicated. Authentication, APIs, syncing, state management, offline support, databases. I accidentally started rebuilding Spotify.

### Then came the main breakthrough.

I realised I actually don’t need two-way interaction.

> I am the only user.

So I changed the entire architecture.

Instead of making users interact with server, I made the server only mirror my library. One direction only.

Now everything happens while uploading.

Music files go into cloud storage.
A script scans the library.
It generates one single library.json file.
The frontend reads only that file and streams directly from cloud storage.

No backend.
No database.
No VPS.
No Docker.
No virtual machine.
No server maintenance.

Suddenly the entire system became extremely simple.

That one idea changed everything.

Then the project became less about music and more about systems.

I started learning how metadata actually works inside audio files. Lyrics, synced lyrics, tags, genres, embedded cover arts, compression, streaming behavior, service workers, offline caching everything.

### One of my favorite things was playlist generation.

I embedded tags directly inside music metadata.

So instead of manually creating playlists, playlists are generated dynamically from tags like:

kannada + love
hindi + retro
urdu + ghazal

which creates playlists automatically like:
Kannada Love
Hindi Retro
Urdu Ghazal

That part felt very satisfying honestly.

The final architecture became surprisingly lightweight.

Cloudflare R2 stores the music.
Cloudflare Pages hosts the app.
Node.js generates the metadata.
The web app streams directly from static files.

That’s it.

No heavy infrastructure.

*For offline playback* I added service worker caching. So whichever songs I already listened gets cached locally and works offline later. Similar to how streaming apps do downloads, but simplified.

Ethically speaking this whole thing probably exists in a gray area. But this is my personal music collection for my own listening. I am not redistributing anything. For me this was more about ownership and accessibility than piracy.

## But honestly the best part was not even the app.

It was the process.

As a designer, as someone from science background, and as someone who likes hacking random things together, this project taught me a lot. About systems, about architecture, about metadata, about cloud storage, about how modern web apps actually work internally.

And most importantly it reminded me that sometimes building weird personal projects teaches more than structured learning.

Every weekend I try making something random like this. Some fail completely. Some become useful. Some become stories.

This one became all three.

## And now yes, I can flex a little that I built my own cloud music platform.

-Arun CK

![My Cloud Music Platform](/assets/images/musicc.jpg)