---
title: "Phonological History of Wiplang"
---

<pre>
Feature type(*cons, vowel)

Feature place(labial, alveolar, postalveolar, palatal, velar, glottal)
Feature manner(plosive, fricative, nasal, approximant, lateral, trill, tap, affricate)
Feature voicedness(*voiced, voiceless, ejective)
Feature sibilance(nonsib, sibilant)

Feature height(open, nearopen, openmid, mid, closemid, nearclose, close)
Feature fronting(front, central, back)
Feature rounding(*unrounded, rounded)
Feature nasalization(*oral, nasalized)

Feature length(*short, long, overlong)
Feature secart(*none, palatalized, velarized)
Feature stress(*unstressed, stressed)

Diacritic ˈ [stressed]
Diacritic ̃ [nasalized]
Diacritic ʲ [palatalized]
Diacritic ˠ [velarized]
Diacritic ʼ [ejective]
Diacritic ː [long]
Diacritic ːː [overlong]

Symbol pʼ [ejective labial plosive]
Symbol p [voiceless labial plosive]
Symbol b [labial plosive]
Symbol tʼ [ejective alveolar plosive]
Symbol t [voiceless alveolar plosive]
Symbol d [alveolar plosive]
Symbol c [voiceless palatal plosive]
Symbol ɟ [palatal plosive]
Symbol kʼ [ejective velar plosive]
Symbol k [voiceless velar plosive]
Symbol g [velar plosive]
Symbol tɕ [voiceless sibilant palatal affricate]
Symbol dʑ [sibilant palatal affricate]
Symbol cç [voiceless nonsib palatal affricate]
Symbol ɟʝ [nonsib palatal affricate]
Symbol fʼ [ejective nonsib labial fricative]
Symbol f [voiceless nonsib labial fricative]
Symbol v [nonsib labial fricative]
Symbol θ [voiceless nonsib alveolar fricative]
Symbol ð [nonsib alveolar fricative]
Symbol sʼ [ejective sibilant alveolar fricative]
Symbol s [voiceless sibilant alveolar fricative]
Symbol z [sibilant alveolar fricative]
Symbol ʃ [voiceless sibilant postalveolar fricative]
Symbol ʒ [sibilant postalveolar fricative]
Symbol ç [voiceless nonsib palatal fricative]
Symbol ʝ [nonsib palatal fricative]
Symbol ɕ [voiceless sibilant palatal fricative]
Symbol ʑ [sibilant palatal fricative]
Symbol xʼ [ejective nonsib velar fricative]
Symbol x [voiceless nonsib velar fricative]
Symbol ɣ [nonsib velar fricative]
Symbol h [voiceless glottal fricative]
Symbol m [labial nasal]
Symbol n [alveolar nasal]
Symbol ɲ [palatal nasal]
Symbol ŋ [velar nasal]
Symbol r [alveolar trill]
Symbol ɾ [alveolar tap]
Symbol l [alveolar lateral]
Symbol ʎ [palatal lateral]
Symbol ɫ [velar lateral]
Symbol j [palatal approximant]
Symbol ɥ [rounded palatal approximant]
Symbol w [rounded velar approximant]
Symbol i [close front vowel]
Symbol ɨ [close central vowel]
Symbol ɪ [nearclose front vowel]
Symbol y [close front rounded vowel]
Symbol ʏ [nearclose front rounded vowel]
Symbol u [close back rounded vowel]
Symbol ʉ [close central rounded vowel]
Symbol ʊ [nearclose back rounded vowel]
Symbol e [closemid front vowel]
Symbol ø [closemid front rounded vowel]
Symbol o [closemid back rounded vowel]
Symbol ə [mid central vowel]
Symbol ɛ [nearopen front vowel]
Symbol œ [nearopen front rounded vowel]
Symbol ɔ [nearopen back rounded vowel]
Symbol ɐ [nearopen central vowel]
Symbol a [open front vowel]
Symbol ɶ [open front rounded vowel]
Symbol ɑ [open back vowel]
Symbol ɒ [open back rounded vowel]

first-shift:
  {b, d, g} => {p, t, k}
  {p, t, k} => {f, s, x}
  {v, z, ɣ} => {f, s, x}
  {f, s, x} => h
  ŋ => n
  Then:
  [vowel] h => [vowel long] * // _ [vowel]

onsetless-metathesis:
  [vowel]$1 [cons]$2 => $2 $1 / _ {$, ![vowel]} // [cons] _

approx-to-vowel:
  {j, w} => {i, u} / [vowel] _ {$, [cons]}
  Then:
  {ji, wu, ij, uw} => {i, u, i, u}

h-drop:
  h => *

h-drop-v-shift:
  {i, u} => {j, w} / [vowel] _ [vowel]
  Then:
  {ui, iu, io, ue} => yː
  {oi, eu, oe, eo} => øː
  {ei, ai, ia, ae, ea} => eː
  {ou, ao, oa} => oː
  {ie, uo} => {iː, uː}

intv-len:
  {p, t, k} => {f, s, x} / [vowel] _ [vowel]
  {p, t, k} => {f, s, x} / _ {$, [cons]}

onsetless-metathesis2:
  [vowel]$1 [cons]$2 => $2 $1 / _ {$, ![vowel]} // [cons] _
  Then:
  [cons]$1 [vowel]$2 => $2 $1 / [cons] _ $

nasal-dropping:
  [vowel] [nasal] => [vowel nasalized] * / _ {$, [cons]}

misc-cons-shifts:
  {j, w} => {i, u} / [vowel] _ {$, [cons]}
  s => r / [vowel] _ [vowel]
  {p, t, k} => {f, s, x} / [vowel] _ [vowel]
  {p, t, k} => {f, s, x} / _ {$, [cons]}
  [vowel] {f, s, x} => [long] * / _ {$, [cons]}
  x => h
  xʼ => x

vowel-shifts:
  {ĩː, ỹː, ẽː, ø̃ː, ũː, õː, ãː} => {ɨː, ʉː, ɪː, ʏː, ʉː, ʊː, ɐː}
  {ĩ, ẽ, ũ, õ, ã} => {ɨ, ɪ, ʉ, ʊ, ɐ}

l-mutation:
  [front vowel] l => [back rounded vowel] * / _ {$, [cons]}
  [front vowel] l => [front rounded vowel] r / _ [vowel]
  [back rounded vowel] l => [long] * / _ {$, [cons]}
  Then:
  [open back rounded vowel] => [unrounded]
  [open front rounded vowel] => [back unrounded]

insert-stress:
  [vowel unstressed] => [vowel stressed] / $ [cons]? _ [cons]? $
  [vowel unstressed] => [vowel stressed] / $ [cons]? [vowel] [cons] [cons]? _
  Then:
  [vowel unstressed] => [stressed] / [vowel unstressed] [cons] [cons]? _ [cons]? $

unstressed-reduction:
  {i, y, e, ø, u, o, a, ɑ}&[unstressed] => {ɨ, ʉ, ɪ, ʏ, ʉ, ʊ, ɐ, ɐ}
  {iː, yː, eː, øː, uː, oː, aː, ɑː}&[unstressed] => {ɨː, ʉː, ɪː, ʏː, ʉː, ʊː, ɐː, ɐː}

strdel:
  [vowel stressed] => [unstressed]

front-unrounding:
  [front rounded vowel] => [unrounded]

r-to-l:
  r => l / _ [vowel] r

long-vowel-changes:
  {iː, eː, uː, oː, aː, ɑː} => {ei, ai, ou, au, ɑ, o}
  {ɨː, ʉː, ɪː, ʊː, ɐː} => {i, u, e, o, ɑ}
  {ɪ, ʊ} => {ɨ, ʉ}
  ɐ => ə

velar-shifts:
  x => h
  h => *
  [ejective] => [voiceless]

vshifts:
  {əɨ, əʉ} => {ɨː, ʉː}
  [vowel] {ə, ɨ, ʉ} => [long] *
  {ə, ɨ, ʉ} [vowel] => * [long]

vshifts2:
  {iː, eː, uː, oː, aː, ɑː, ɨː, ʉː, əː} [vowel] => {i, i, u, u, ɑ, o, i, u, ɨ} [vowel]
  {eo, oe, ae, ao, ɑe, ɑo} => {eu, oi, ai, au, ɑi, ɑu}
  Then:
  {ei, oi, ai, eu, ou, au, ɑi, ɑu} => {eː, eː, ɛː, oː, oː, ɔː, ɛː, ɔː} / _ [cons] {$, [cons]}

lvshifts:
  {iː, eː, ɛː, uː, oː, ɔː, aː, ɑː, ɨː, ʉː, əː} => {ei, ai, e, ou, au, o, e, o, i, u, ɨ} // _ [cons] {$, [cons]}
  {iː, eː, ɛː, uː, oː, ɔː, aː, ɑː, ɨː, ʉː, əː} => {i, e, ɛ, u, o, ɔ, ɛ, o, i, u, ɨ} / _ [cons] {$, [cons]}

corrections:
  {uw, ij} => {w, j} / _ [vowel]

insert-stress2:
  [vowel unstressed] => [vowel stressed] / $ [cons]? _ [cons]? $
  [vowel unstressed] => [vowel stressed] / $ [cons]? [vowel] [cons] [cons]? _
  Then:
  [vowel unstressed] => [stressed] / [vowel unstressed] [cons] [cons]? _ [cons]? $

vdel:
  {ɨ, ʉ} => * / $ [cons]? _ [cons] [cons]? [vowel]
  [unstressed mid central vowel] => *
  [stressed mid central vowel] => ɨ

stdel2:
  [vowel stressed] => [unstressed]

cons-clusters:
  {l, n, m, r}$1 {f, s}$2 => $2 $1 // [vowel] _
  j$1 {p, t, k, f, s, h, m, n, l, r}$2 => $2 $1 // [vowel] _
  Then:
  {ww, ll, rr, jj} => {w, l, r, j}
  {pp, tp, kp} => {p, tw, kw}
  {pt, tt, kt} => {pr, t, kr}
  {pk, tk, kk} => {pj, tj, k}
  {pf, tf, kf} => {pw, tw, kw}
  {ps, ts, ks} => {pr, tr, kr}
  {t, k, f, s, h, l, n, m} j => {c, c, ç, ʃ, ç, ʎ, ɲ, ɲ} *
  {m, n} {l, r, j} => {b, d} {l, r, j}
  {f, s} => {p, t} / _ r
  {lr, rl} => r
  {lm, ln} => {bl, dl}
  {sf, fs} => {sw, pr}
  {jw, wj} => {w, j} // [vowel] _
  Then:
  dl => dr
  Then:
  {b, d} => {p, t}

approx-v-shifts:
  {ji, wu} => {i, u}
  {ij, uw} => {i, u} / _ {$, [cons]}
  {ij, uw} => {j, w} / _ [vowel]
  {j, w} => {i, u} / [vowel] _ {$, [cons]}
  Then:
  {iu, ui} => {ɨ, }

modern-romanizer:
  ɨ => y
  ʉ => w
  e => ê
  o => ô
  ɑ => â
  ɛ => e
  ɔ => o
  j => i
  w => u
  ʃ => sj
  c => kj
  ç => hj
  ʎ => lj
  ɲ => nj
  
</pre>
