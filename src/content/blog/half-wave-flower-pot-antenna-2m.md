---
title: "Project 1: Building a half-wave flower pot antenna for 2 m"
description: "A cheap, effective home-built vertical for 2 m VHF — the classic VK2ZOI flower pot, with the exact dimensions and my build notes."
pubDate: "Jul 26 2026"
heroImage: "/blog-placeholder-4.jpg"
tags: ["Antennas", "2m", "Build", "VHF"]
---

My first real project is the **half-wave "flower pot" antenna** for 2 m — the design by
**John Bishop, VK2ZOI**. It's popular for good reason: it costs a few dollars, uses coax and a length
of electrical conduit, needs no radials, and comfortably out-performs the rubber-duck whip on a
handheld. Best of all, it hides inside a piece of PVC, so it looks like nothing at all on the balcony.

I'm building mine straight from the VK2ZOI article:
[**Half-Wave Flower Pot Antenna**](https://vk2zoi.com/articles/half-wave-flower-pot/). This post is my
working copy of the key numbers plus notes to myself — always defer to the original article.

> ⚠️ **Foundation licence note:** under my licence I can build and use antennas like this. As always,
> keep antennas well clear of powerlines, and never install where a falling mast could reach one.

## How it works (in one paragraph)

The flower pot is an **end-fed half-wave vertical**. The top section is the coax's exposed centre
conductor; the section below the feedpoint is the intact coax, whose braid forms the lower half of the
radiator. Just below that, the feed coax is wound into a **choke coil** ("ugly balun"). That choke
stops RF flowing back down the *outside* of the feedline — which is what stops the whole thing
detuning when you touch the cable or move it around. The choke is a decoupler, **not** a loading coil:
it doesn't change the antenna's electrical length. VK2ZOI notes the choke should be self-resonant
about **5–6 % below** the operating frequency.

## Materials

- **RG58 coax — braided shield only.** One continuous length, ~5–6 m, so a single run reaches from the
  antenna all the way to the radio. **Do not use foil-shielded coax** — the foil cracks at the sharp
  bends where the coil enters/exits the conduit and the antenna won't work.
- **25 mm grey electrical conduit**, at least 1 m long (longer gives more room below the coil to
  attach to a support).
- One conduit **end cap**.
- **Fishing line** (thin nylon), ~0.5 m, to tension the radiator.
- Connector to suit your radio (SMA / BNC / PL-259).
- Heatshrink and PVC tape for weatherproofing.

## Dimensions for 146 MHz (2 m)

Cut to these. The element lengths already include VK2ZOI's ~2 % shortening for the grey conduit.

| Section | Length | Notes |
| --- | --- | --- |
| **Top element (radiator)** | **457 mm** | Strip off the outer sheath **and** braid — expose the centre conductor only |
| **Lower element** | **447 mm** | Measured **down from the feedpoint** to the top of the choke; leave the coax intact |
| **Choke coil** | **9 turns** | Wound on the outside of the 25 mm conduit |
| **Top coil hole** | **≈ 925 mm from the conduit end** | = radiator length + clearance to the end cap |
| **Coil holes** | **≈ 6 mm, spaced ≈ 45 mm** | Exact spacing depends on the coax — wind 9 turns temporarily and measure first |

The **feedpoint** is where the braid/sheath starts again — i.e. the join between the 457 mm exposed
top element and the 447 mm intact lower element.

## Build steps

1. **Prep the conduit.** Cut the choke holes: the top hole ≈ 925 mm from the end. Wind 9 turns of the
   coax on the conduit temporarily to get the real spacing (~45 mm), then drill the two ~6 mm holes and
   **file the edges smooth** so they don't nick the cable at the bends.
2. **Form the top element.** From one end of the coax, strip **457 mm** of outer sheath and braid,
   leaving just the centre conductor. If it ends up a touch short, you can solder a scrap of wire or
   the discarded braid on to reach length.
3. **Tie on the fishing line.** With a few half-hitches, tie ~0.5 m of nylon line to the top of the
   element. This pulls the radiator taut and later gets clamped under the end cap.
4. **Mark the lower element.** Measure **447 mm down from the feedpoint** and mark it (tape/paint).
   That mark is your stop point — the top of the choke coil.
5. **Feed it in.** Push the radiator + nylon line up through the top coil hole until your 447 mm mark
   just disappears into the hole. Fish the line out the top and pull it taut to straighten the radiator
   and set the bend at the coil.
6. **Wind the choke.** Wind **9 turns** on the outside of the conduit, then feed the remaining cable in
   through the bottom hole and work it down until the coil is tight and secure — **without** moving the
   447 mm mark (you should still just see it through the top hole).
7. **Secure the top.** Cut a small notch in the conduit edge, pull the nylon line taut and nip it into
   the notch (the end cap will clamp it permanently later).
8. **Fit the connector and measure VSWR.** Trim the top element only if needed — VK2ZOI says very
   little trimming is usually required.
9. **Finish.** Once you're happy with the VSWR, cap the top. **Leave the bottom open** so condensation
   can drain.

## Tuning

Check VSWR across 2 m with an analyser or your radio's meter. Aim for the dip around **146 MHz**;
under ~1.5:1 across the band is a good result. Trim the **top element** to raise the resonant
frequency. To scale the whole design to another frequency:

`new length = current length × (desired frequency ÷ measured frequency)`

## Weatherproofing & "cocky proofing"

Straight from the article's tips — worth doing here in Canberra:

- Heatshrink the **feedpoint** and the coil's **entry/exit holes** against water. Heatshrink the bottom
  to neaten the base and buffer the exiting coax.
- **Cocky proofing:** white cockatoos love to attack the coil. Cover it with a shield — an empty
  silicone-sealant cartridge fits neatly over a 2 m coil (wrap the coil in PVC tape first).

## My build log

*(I'll update this as I go.)*

- [ ] Cut conduit and drilled/filed the coil holes
- [ ] Stripped 457 mm top element, marked 447 mm lower element
- [ ] Wound the 9-turn choke, fed cable through
- [ ] First VSWR sweep — resonant frequency: **___ MHz**, VSWR at 146 MHz: **___:1**
- [ ] Trimmed / retuned
- [ ] Capped, cocky-proofed, mounted
- [ ] First contact through a Canberra repeater with it

## References

- John Bishop, VK2ZOI — [Half-Wave Flower Pot Antenna](https://vk2zoi.com/articles/half-wave-flower-pot/) (the build I'm following)
- VK2ZOI — [Dual Band Half-Wave Flower Pot (PDF)](https://www.zl2ko.org.nz/wp-content/uploads/2019/08/VK2ZOI-Dual-Band-Half-Wave-Flower-Pot-Antenna.pdf)

Next time: results from the VSWR sweep, and whether it gets me into the repeaters I currently can't
reach from home. **73!**
