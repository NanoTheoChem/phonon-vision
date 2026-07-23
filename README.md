# phonon-vision

Interactive viewer for phonon band structures.

Live page: https://nanotheochem.github.io/phonon-vision/

A band-structure plot gives the frequency of every vibrational mode of a
crystal, but not the motion behind it. This page shows both: click a point
on the dispersion and the structure below animates that mode, with the
displacement pattern taken from the actual eigenvector (mass weighting and
the Bloch phase between neighbouring cells included).

The left panel shows all phonon branches as surfaces over the first
Brillouin zone. Clicking a sheet selects the nearest exactly-computed mode
and animates it. Surfaces can be coloured by per-species displacement
blend, by the projection onto one species, or drawn plain; the "Extended
zones" toggle repeats the surface over neighbouring Brillouin zones.

Two materials are included, switchable from the Material menu:

* SnSe2 — layered dichalcogenide
* graphene — Materials Project entry mp-990448

## Running it locally

No server or installation is needed. Clone or download the repository and
open `index.html` in a browser. All libraries and data are bundled, so it
also works completely offline.

## Data

Frequencies and eigenvectors were obtained from interatomic force
constants with phonopy (A. Togo and I. Tanaka, Scr. Mater. 108, 1 (2015)),
then baked into the JavaScript payloads read by the page.

The graphene force constants come from the Materials Project (mp-990448,
CC-BY 4.0; A. Jain et al., APL Mater. 1, 011002 (2013)).

Plotly.js and three.js are bundled unmodified under their MIT licenses;
see `THIRD_PARTY.md`.

## License

MIT — see `LICENSE`.
