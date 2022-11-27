---
title: "Phonological History of Manevian"
---

There are a lot of known (and unknown) issues with this.
Said issues are being resolved as fast as possible.

<pre>
Feature type(*cons, vowel)

Feature place(labial, alveolar, postalveolar, palatal, velar, uvular, glottal)
Feature manner(plosive, fricative, nasal, approximant, lateral, trill, tap, affricate)
Feature voicedness(*voiced, voiceless, ejective)
Feature sibilance(nonsib, sibilant)

Feature height(open, nearopen, openmid, mid, closemid, nearclose, close)
Feature fronting(front, central, back)
Feature rounding(*unrounded, rounded)

Feature length(*short, long, nasalized)
Feature secart(*none, palatalized, velarized)
Feature stress(*unstressed, stressed)

Diacritic ˈ [stressed]
Diacritic ̃ [nasalized]
Diacritic ʼ [ejective]
Diacritic ː [long]

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
Symbol q [voiceless uvular plosive]
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
Symbol xʼ [ejective nonsib velar fricative]
Symbol x [voiceless nonsib velar fricative]
Symbol ɣ [nonsib velar fricative]
Symbol χ [voiceless nonsib uvular fricative]
Symbol ʁ [nonsib uvular fricative]
Symbol h [voiceless glottal fricative]
Symbol m [labial nasal]
Symbol n [alveolar nasal]
Symbol ɲ [palatal nasal]
Symbol ŋ [velar nasal]
Symbol ɴ [uvular nasal]
Symbol r [alveolar trill]
Symbol ɾ [alveolar tap]
Symbol l [alveolar lateral]
Symbol ʎ [palatal lateral]
Symbol ɫ [velar lateral]
Symbol j [palatal approximant]
Symbol ɥ [rounded palatal approximant]
Symbol w [rounded velar approximant]
Symbol i [close front vowel]
Symbol ɪ [nearclose front vowel]
Symbol y [close front rounded vowel]
Symbol ʏ [nearclose front rounded vowel]
Symbol ɯ [close back vowel]
Symbol ɯ̽ [nearclose back vowel]
Symbol u [close back rounded vowel]
Symbol ʊ [nearclose back rounded vowel]
Symbol e [closemid front vowel]
Symbol ø [closemid front rounded vowel]
Symbol ɤ [closemid back vowel]
Symbol o [closemid back rounded vowel]
Symbol ə [mid central vowel]
Symbol ɛ [nearopen front vowel]
Symbol œ [nearopen front rounded vowel]
Symbol ʌ [nearopen back vowel]
Symbol ɔ [nearopen back rounded vowel]
Symbol æ [open front vowel]
Symbol a [open central vowel]
Symbol ɑ [open back vowel]
Symbol ɒ [open back rounded vowel]

consonant-shifts1:
  {pʼ, tʼ, kʼ} => {p, t, q}
  {p, t, k} => {f, θ, χ}
  {b, d, g} => {w, l, ʁ}
  {fʼ, sʼ, xʼ} => {f, s, χ}
  {f, s, x} => {θ, ʃ, h}
  {v, z, ɣ} => {w, l, ʁ}
  ŋ => ɴ

cons-shifts:
  ɴ => n
  {uw, ij} => {w, j} / _ [vowel]
  {wu, ji} => {u, i} / [vowel] _

monophthongization:
  {ju, je, jo, ja} => {yː, eː, øː, eː} // [vowel] _
  {wi, we, wo, wa} => {yː, øː, oː, oː} // [vowel] _
  {uj, ej, oj, aj} => {yː, eː, øː, eː} // _ [vowel]
  {iw, ew, ow, aw} => {yː, øː, oː, oː} // _ [vowel]

vc-shifts:
  {il, iːl} => {y, yː} / _ {[cons], $}
  yːl => uː / _ {[cons], $}
  {ul, uːl} => {u, uː} / _ {[cons], $}
  {el, eːl} => {ø, øː} / _ {[cons], $}
  {øl, øːl} => {o, oː} / _ {[cons], $}
  {ol, oːl} => {o, oː} / _ {[cons], $}
  al => o / _ {[cons], $}
  {iʁ, iːʁ} => {ɯ, ɯː} / _ {[cons], $}
  yːʁ => uː / _ {[cons], $}
  {uʁ, uːʁ} => {u, uː} / _ {[cons], $}
  {eʁ, eːʁ} => {ɤ, ɤː} / _ {[cons], $}
  {øʁ, øːʁ} => {o, oː} / _ {[cons], $}
  {oʁ, oːʁ} => {o, oː} / _ {[cons], $}
  aʁ => ɑ  / _ {[cons], $}
  {iχ, iːχ} => {ɯ, ɯː} / _ {[cons], $}
  yːχ => uː / _ {[cons], $}
  {uχ, uːχ} => {u, uː} / _ {[cons], $}
  {eχ, eːχ} => {ɤ, ɤː} / _ {[cons], $}
  {øχ, øːχ} => {o, oː} / _ {[cons], $}
  {oχ, oːχ} => {o, oː} / _ {[cons], $}
  aχ => ɑ  / _ {[cons], $}

debuccalization:
  [vowel short] {f, θ, s, ʃ, χ, h} => [vowel long] * / _ {[cons], $}

diphthongization:
  {iː, yː, ɯː, uː} => {ei, øy, ɤɯ, ou}
  {eː, øː, ɤː, oː} => {ai, ay, aɯ, au}
  aː => e / {[alveolar], [labial], [palatal], $} _ 
  aː => o / [uvular] _

uvular-shifts:
  [uvular] {i, y, ɯ, u, e, ø, ɤ, o, a} => [velar] {ɪ, ʏ, ɯ̽, ʊ, ɛ, œ, ʌ, ɔ, ɑ}
  [uvular] {ei, øy, ɤɯ, ou} => [velar] {ɛi, œy, ʌɯ, ɔu}
  [uvular] {ai, ay, aɯ, au} => [velar] {əi, əy, əɯ, əu}

monophthongization2:
  {ei, øy, ɤɯ, ou} => {i, y, ɯ, u}
  {ai, ay, aɯ, au} => {e, ø, ɤ, o}
  {ɪ, ʏ, ɯ̽, ʊ, ɛ, ɑ, a} => {e, ø, ɤ, o, a, ɑ, a}
  {ɛi, əi} => ɛ
  {œy, əy} => œ
  {ʌɯ, əɯ} => ʌ
  {ɔu, əu} => ɔ

gh-shift:
  ɣ => x

semivowel-drop:
  {ij, yɥ, uw} => {i, y, u} / _ {$, [cons]}
  {j, ɥ, w} => {i, y, u} / [vowel] _ // _ [vowel]

nasalization:
  [vowel] [nasal] => [nasalized vowel] * / _ {[cons], $}

denasalization:
  {ĩ, ỹ, ɯ̃, ũ} => {e, ø, ɤ, o}
  {ẽ, ø̃, ɤ̃, õ} => {ɛ, œ, ʌ, ɔ}
  {ɛ̃, œ̃, ʌ̃, ɔ̃} => {a, ɶ, ɑ, ɒ}
  ã => ɛ / {[alveolar], [labial], [palatal], $} _ 
  ɑ̃ => ɔ / [velar] _
  Then: [vowel nasalized] => [vowel short]

vowel-assimilation:
  [front rounded vowel] => [unrounded]
  [back unrounded vowel] => [rounded]

monophthongization3:
  {ei, ou} => {i, u}
  {ɛi, ɔu} => {e, o}
  {ai, au} => {ɛ, ɔ}
  {ɒi, ɒu} => {œ, ɔ}

intv-lenition:
  {p, t, k} => {f, θ, x} / [vowel] _ [vowel]
  x => h / [vowel] _ [vowel]

umlaut:
  a => æ
  {u, o, ɔ, ɒ} => {y, ø, œ, a} / _ [cons] {i, e, ɛ}
  Then:
  {i, e, ɛ} => {e, ɛ, a} / {y, ø, œ, a} [cons] _
  Then:
  æ => a

h-drop-shifts:
  {h, ʔ} => *
  Then:
  [vowel] [vowel] => [short vowel] [short vowel]
  Then:
  {i, y, u} => {j, ɥ, w} / _ {e, ɛ, a, ø, œ, o, ɔ, ɒ}
  {e, ø, o} => {i, y, u} / {a, ɒ, ɛ, œ, ɔ} _
  {ɛ, œ, ɔ} => {a, a, ɒ} / _ {e, ø, o, i, y, u}
  {ii, ee, ɛɛ, aa, yy, øø, œœ, uu, oo, ɔɔ, ɒɒ} => {iː, eː, ɛː, aː, yː, øː, œː, uː, oː, ɔː, ɒː}
  {eø, øe, oø, øo, eo, oe} => øː
  {eɛ, ɛe} => eː
  {øɛ, ɛø, oɛ, ɛo, eœ, œo, oœ, œo, eɔ, ɔe, øɔ, ɔø} => øː 
  ɔœ => œː
  {oɔ, ɔo} => oː
  {ea, oa} => {eː, oː}
  {aɛ, ɛa} => ɛː
  {aœ, œa} => œː
  {aɔ, ɔa} => ɔː
  {ɒɛ, ɛɒ} => œː
  {ɒœ, œɒ} => œː
  {ɒɔ, ɔɒ} => ɔː
  {ey, oy} => øː
  {i, y, u} => {j, ɥ, w} / [vowel] _ [vowel]
  {e, ø, o} => {j, ɥ, w} / [vowel] _ [vowel]

monophthongization4:
  je => eː // [vowel] _
  {jø, jo, ɥe, ɥø, ɥo, we, wø} => øː // [vowel] _
  wo => oː // [vowel] _
  {jɛ, ja}  => ɛː // [vowel] _
  {jœ, jɔ, jɒ, ɥɛ, ɥœ, ɥɔ, ɥa, ɥɒ, wɛ, wœ} => œː // [vowel] _
  {wɔ, wa, wɒ} => ɔː // [vowel] _

insert-stress3:
  [vowel unstressed] => [vowel stressed] / $ [cons]? _
  Then: (
  [vowel unstressed] => [vowel stressed] / $ [cons]? [vowel stressed] [cons]? [cons] [vowel unstressed] [cons]? [cons] _ [cons]? $
  Else:
  [vowel unstressed] => [vowel stressed] / [cons] _ [cons]? [cons] [vowel] [cons]? $
)

diphthongization2:
  {ɛ, œ, ɔ, a, ɒ}&[unstressed] => ə
  Then:
  [vowel stressed] => [vowel unstressed]
  Then:
  {iː, yː, uː} => {ei, øy, ou}
  {eː, øː, oː} => {ai, ay, au}
  {ɛː, œː, ɔː} => {e, ø, o}
  {aː, ɶː, ɒː} => {ɛ, œ, ɔ}

palatalization:
  {k, g, x, ɣ} {j, i, e, ɛ} => {c, ɟ, ç, ʝ} {*, e, ɛ, a}
  {t, d, s, z} j => {tʃ, dʒ, ʃ, ʒ} *

schwa-drop:
  ə => *

post-shifts:
  {lr, rl} => r
  Then:
  [vowel] {f, θ, s, ʃ, h, m, n, r} => [vowel long] * / _ {[cons], $}
  {ei, ey, øi, øy, oi, oy, ou, ai, ay, au} => {eː, øː, øː, øː, øː, øː, oː, ɛː, œː, ɔː}
  Then:
  {j, ɥ, w, l} => {i, y, u, i} / [vowel] _ {[cons], $}
  Then:
  {ii, yy, uu} => {iː, yː, uː}
  {iy, iu, ui, uy, yi, yu} => {yː}
  [voiced plosive] [voiceless] => [voiceless] 
  [voiced fricative] [voiceless] => [voiceless]

rounding-and-place-assimilation:
  {eu, ey, øi, oi} => øy
  {ɛ, œ, ɔ} i => a i

vowel-shifts2:
  [vowel] {iː, yː, uː} => [vowel] {i, y, u}
  Then:
  {ei, øy, ou} => {i, y, u}
  {ai, ay, au} => {e, ø, o}
  {iː, yː, uː} => {ei, øy, ou}
  {eː, øː, oː} => {ai, ay, au}
  {ɛː, œː, ɔː} => {i, y, u}
  {aː, ɒː} => {e, o}
  {i, y, u} => {e, ø, o}
  {e, ø, o} => {ɛ, œ, ɔ}
  {ɛ, œ, ɔ, a, ɒ} => a

palatal-shifts:
  {c, ɟ, {ç, x}, ʝ} => {s, z, h, j}
  
h-shifts:
  {i, {y, u}, e, {ø, o}, ɛ, {œ, ɔ}, a} h => {iː, uː, eː, oː, ɛː, ɔː, ɑː} * / _ {[cons], $} // [vowel] _
  [vowel] h => [vowel] * / [vowel] _

vowel-breaking:
  {e, ø, o} => {ie, yø, uo} / _ [cons] // {[lateral], [tap], [trill], [approximant]} _
  {ɛ, œ, ɔ} => {e, ø, o}

unrounding2:
  {ɥ, y, ø} => {j, i, e}

misc-shifts:
  {t, d, f, v, s, z, θ, l, r, n} ie => {tʃ, dʒ, ç, ʝ, ʃ, ʒ, ç, ʎ, ʝ, ɲ} e
  {t, d, θ, n} uo => {p, b, f, m} o
  {p, b, f, m} uo => w o
  {k, g} uo => w o

vowel-shifts4:
  {iː, uː, eː, oː, ɛː, ɔː, ɑː} => {ei, ou, ai, au, i, u, o}

semi-shift:
  {i, u} => {j, w} / _ [vowel]

gh-removal:
  ɣ j => j *
  ʝ j => j *

modern-romanizer:
  {θ, ʃ, ç, ɣ} => {th, sh, ch, gh}
  {je, wo} => {ie, uo} // [vowel] _
  {ʎ, ɲ, j} => {ly, ny, y}
</pre>