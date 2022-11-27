---
title: "Phonological History of Liran"
---

A complete list of every sound change from Proto-Daimarian to Modern Liran.

Currently, the list is in Lexurgy's *.lsc format, and I am not planning to update it to proper phonological rule syntax any time soon.
It is too time costly, and is not worth the effort for such little tradeoff in the end. 

There may or may not be issues in this page, but will be resolved if found. 

<pre>
Feature type(*cons, vowel)

Feature place(labial, alveolar, postalveolar, palatal, velar, glottal)
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
Diacritic ʲ [palatalized]
Diacritic ˠ [velarized]
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
Symbol ɪ [nearclose front vowel]
Symbol y [close front rounded vowel]
Symbol ʏ [nearclose front rounded vowel]
Symbol u [close back rounded vowel]
Symbol ʊ [nearclose back rounded vowel]
Symbol e [closemid front vowel]
Symbol ø [closemid front rounded vowel]
Symbol o [closemid back rounded vowel]
Symbol ə [mid central vowel]
Symbol ɛ [nearopen front vowel]
Symbol œ [nearopen front rounded vowel]
Symbol ɔ [nearopen back rounded vowel]
Symbol æ [open front vowel]
Symbol a [open central vowel]
Symbol ɑ [open back vowel]

proto-to-east-5600:
  [ejective plosive] => [voiceless plosive]
  [voiceless plosive] => [voiced plosive]
  [voiced plosive] => [nonsib voiced fricative]
  [ejective fricative] => [voiceless fricative]
  {v, z, ɣ} => {w, r, j}
  s => θ
  {f, x} => h
  Then: 
  [vowel] h => [vowel long] * / _ {[cons], $} 

devoicing-5500:
  [voiced plosive] [voiceless] => [voiceless] 
  [voiced fricative] [voiceless] => [voiceless]
  [vowel] => [vowel nasalized] / _ [nasal] {[cons], $}
  Then:
  [nasal] => * / [vowel nasalized] _

eastern-shifts-5400:
  {j, w} => {i, u} / [vowel] _ {[cons], $}
  {uw, ij} => {w, j} / _ [vowel]
  {ji, ij} => iː / {[cons], $} _ {[cons], $}
  {wu, uw} => uː / {[cons], $} _ {[cons], $}
  Then:
  [vowel short] => [vowel long] / {[cons], $} _ [nonsib voiceless fricative] {[cons], $}
  Then:
  {ii, uu} => {iː, uː}
  [nonsib voiceless fricative] => * / [vowel long] _

palatalization-5200:
  {k, g, x, ɣ, ŋ} {i, e, j, iː, eː, ĩ, ẽ} => {c, ɟ, ç, ʝ, ɲ} {ɪ, ɛ, *, i, e, ĩ, ẽ}
  {t, d, θ, ð, s, z, l, n} j => {tʃ, dʒ, ç, ʝ, ɕ, ʑ, ʎ, ɲ} *
  {p, b, t, d, f, v, θ, ð, s, z, m, n, r, l} ɣ => {b, β, d, ð, v, w, ð, l, z, r, ŋ, ŋ, l, w} *

misc-shifts-4800:
  [palatal plosive] => [sibilant affricate]
  {x, ç} => h
  {ɣ, ʝ} => j
  [vowel nasalized] => [vowel long]

semi-vowel-shifts-4500:
  {ji, ij, iji} => iː / {[cons], $} _ {[cons], $}
  {wu, uw, uwu} => uː / {[cons], $} _ {[cons], $}
  {j, w} => {i, u} / [vowel] _ {[cons], $}
  {ji, wu} => {i, u} / [vowel] _ {[cons], $}

palatal-shifts-4300:
  {tɕ, dʑ} => {tʃ, dʒ}
  {ɕ, ʑ} => {ʃ, ʒ}
  {ʎ, ɲ} => {j, n}

monophthongization-4200:
  {ei, ai} => eː
  {eu, oi} => øː
  {ou, au} => oː

umlaut-4100:
  {[back rounded vowel], a, aː} [cons] {iː, eː, i, e} => {[front rounded vowel], e, eː} [cons] {i, e, ɪ, ɛ}

h-drop-3700:
  {h, ʔ} => *
  {wu, ji} => {u, i} / [vowel] _

comp-short:
  [vowel] [vowel] => [short vowel] [short vowel]

hdropvshifts-3500:
  {wiː, wuː, wyː, jiː, juː, jyː} => {yː, uː, yː, iː, yː, yː} / [cons] _ {[cons], $}
  {iy, yi, iu, ui, yu, uy} => yː
  {ii, yy, uu} => {iː, yː, uː}
  {eø, øe, eo, oe, øo, oø} => øː
  {ee, øø, oo} => {eː, øː, oː}
  {a, aː} {e, ø, o} => {a, aː} {i, y, u}
  {e, ø, o} {a, aː}=> {eː, øː, oː} *
  {i, y, u} => {j, ɥ, w} / _ {[closemid vowel], [openmid vowel], [open vowel]}
  {iːiː, yːyː, uːuː, eːeː, øːøː, oːoː, aːaː} => {{iː, yː, uː, iː, yː, uː, eː}}
  {ɪi, ɪy, ɪu, ɪe, ɪø, ɪo, ɪɛ, ɪɪ, ɪa, ɪiː, ɪyː, ɪuː, ɪeː, ɪøː, ɪoː, ɪɛː, ɪɪː, ɪaː} => {iː, yː, yː, eː, øː, øː, e, i, e, iː, yː, yː, eː, øː, øː, eː, iː, eː}
  {iɪ, yɪ, uɪ, eɪ, øɪ, oɪ, ɛɪ, ɪɪ, aɪ, iːɪ, yːɪ, uːɪ, eːɪ, øːɪ, oːɪ, ɛːɪ, ɪːɪ, aːɪ} => {je, ɥe, we, eː, øː, øː, e, i, e, iː, yː, yː, eː, øː, øː, eː, iː, eː}
  {ɛi, ɛy, ɛu, ɛe, ɛø, ɛo, ɛɛ, ɛɪ, ɛa, ɛiː, ɛyː, ɛuː, ɛeː, ɛøː, ɛoː, ɛɛː, ɛɪː, ɛaː} => {ai, ay, au, eː, øː, øː, e, i, aː, iː, yː, yː, eː, øː, øː, eː, iː, eː}
  {iɛ, yɛ, uɛ, eɛ, øɛ, oɛ, ɛɛ, ɪɛ, aɛ, iːɛ, yːɛ, uːɛ, eːɛ, øːɛ, oːɛ, ɛːɛ, ɪːɛ, aːɛ} => {ja, ɥa, wa, eː, øː, øː, e, i, aː, iː, yː, yː, eː, øː, øː, eː, iː, eː}
  {iːi, yːy, uːu} => {iː, yː, uː}
  {eːe, øːø, oːo} => {iː, yː, uː}
  {eeː, øøː, ooː} => {iː, yː, uː}

comp-short2:
  [vowel] [vowel] => [short vowel] [short vowel]

vowel-shifts1-3300:
  {uy, yu} => yː
  {eː, øː, oː} => {i, y, u}
  aː => ɑ
  {i, y, u} => {ɪ, ʏ, ʊ}
  {e, ø, o} => {ɛ, œ, ɔ}
  {ɪ, ɛ} => ə

deaffrication-3000:
  {tʃ, dʒ} => {ʃ, ʒ}

intv-lenition-3000:
  [plosive] => [nonsib fricative] / [vowel] _ [vowel]
  [plosive] => [nonsib fricative] / [vowel] _ {[cons], $}

misc-shifts2-2700:
  {ff, θθ, xx} => {f, θ, x}
  {x, ɣ, ŋ} => {h, j, n}
  [vowel] {f, θ, x} => [vowel long] * / _ {[cons], $} 

insert-stress1:
  [vowel unstressed] => [vowel stressed] / $ [cons]? [cons]? _
  Then: (
  [vowel unstressed] => [vowel stressed] / $ [cons]? [cons]? [vowel stressed] [cons]? [cons] [cons]? [vowel unstressed] [cons]? [cons] [cons]?  _ [cons]? $
  Else:
  [vowel unstressed] => [vowel stressed] / [cons] [cons]? _ [cons]? [cons] [cons]? [vowel] [cons]? $
)

stressdeletion:
  {a}&[unstressed] => ə
  [mid central vowel stressed] => a
  {ɪ, ʏ, ʊ} => {e, ø, o}

hdrop2-2500:
  h => *

remove-stress:
  [vowel stressed] => [vowel unstressed]

fix-ai-ay-au:
  {iː, yː, uː} => {ai, ay, au}

hdrop2vshifts-2400:
  {əj, əw} => {e, o} // _ [vowel]
  {ai, ay, au} => {e, ø, o} / _ {ai, ay, au, i, y, u} {[cons], $}
  {ɛ, œ, ɔ} => {e, ø, o} / _ {i, y, u} {[cons], $}
  {ɛai, ɛay, ɛau} => {ei, ey, eu} / _ {[cons], $}
  {i, y, u} => {j, ɥ, w} / _ {ai, ay, au, e, ø, o, ɛ, œ, ɔ, a, ɑ}
  {aai, aay, aau} => {ai, ay, au}
  {ɑai, ɑay, ɑau} => {ɑi, ɑy, ɑu}
  {e, ø, o} => {i, y, u} / {a, ɑ} _ {[cons], $}
  ii => iː / _ {[cons], $}
  {iy, iu, yi, yy, yu, ui, uy} => yː / _ {[cons], $}
  uu => uː / _ {[cons], $}
  ee => eː / _ {[cons], $}
  {eø, eo, øe, øø, øo, oe, oø} => øː / _ {[cons], $}
  oo => oː / _ {[cons], $}
  ɛe => eː / _ {[cons], $}
  {ɛø, ɛo, œe, œø, œo, ɔe, ɔø} => øː / _ {[cons], $}
  ɔo => oː / _ {[cons], $}
  eɛ => eː / _ {[cons], $}
  {eœ, eɔ, øɛ, øœ, øɔ, oɛ, oœ} => øː / _ {[cons], $}
  oɔ => oː / _ {[cons], $}
  ɛɛ => eː / _ {[cons], $}
  {ɛœ, ɛɔ, œɛ, œœ, œɔ, ɔɛ, ɔœ} => øː / _ {[cons], $}
  ɔɔ => oː / _ {[cons], $}
  {aɛ, aœ, ɑɛ, ɑœ, aa, aɑ, aə, əɛ} => aː / _ {[cons], $}
  {aɔ, ɑɔ, ɑa, ɑɑ, ɑə, əɔ} => ɑː / _ {[cons], $}
  {aie, aiɛ, aia, aiɑ} => eː / _ {[cons], $}
  {aiø, aio, aiœ, aiɔ, aye, ayø, ayo, ayɛ, ayœ, ayɔ, aya, ayɑ, aue, auø, auɛ, auœ} => øː
  {auo, auɔ, aua, auɑ} => oː
  {e, ø, o} {a, ɑ} => {eː, øː, oː} * / _ {[cons], $}
  
  {ji, ij} => iː / _ {[cons], $} // [vowel] _ {[cons], $}
  {jy, yj, ju, uj, ɥi, iɥ, ɥy, yɥ, ɥu, uɥ, wi, iw, wy, yw} => yː / _ {[cons], $} // [vowel] _ {[cons], $}
  {wu, uw} => uː / _ {[cons], $} // [vowel] _ {[cons], $}

schwadrop-2200:
  ə => *
  {a, ɑ} => a / _ [vowel]
  Then:
  {fv, vf, θð, ðθ, sz, zs, ʃʒ, ʒʃ} => {f, f, θ, θ, s, s, ʃ,ʃ}
  {ʃθ, θʃ, ʒð, ðʒ} => {ʃ, ʃ, ʒ, ʒ}
  Then:
  [fricative voiced] => [fricative voiceless] / _ [cons voiceless]
  [fricative voiceless] => [fricative voiced] / _ [cons voiced]
  Then:
  {lð, ðl} => l
  {lr, rl, ðr, rð, rʒ, ʒr} => r
  {r, l} => {a, u} / [cons] _ [cons]
  {ml, nl} => {mu, nu} / _ $
  {l, v, r} => {u, o, a} / [cons] _ $
  {vw, wv} => w
  {mm, nn, ww, rr, ll, jj, ff, vv, θθ, ðð, ss, zz, ʃʃ, ʒʒ} => {m, n, w, r, l, j, f, v, θ, ð, s, z, ʃ, ʒ}

semi-correction-2100:
  ij => i / [vowel] _ {$, [cons]}
  {yj, iw, uj, uɥ, iɥ} => y / [vowel] _ {$, [cons]}
  uw => u / [vowel] _ {$, [cons]}

vowelshifts3-2000:
  {ɪ, ʏ, ʊ} => {e, ø, o}
  {ɪː, ʏː, ʊː} => {eː, øː, oː}
  Then:
  {ja, ea, ei, je, ai, aj} => eː / _ {[cons], $} // [vowel] _
  {ɥa, øa, ey, eu, øi, øy, øu, oi, oy, jø, jo, ɥe, ɥø, ɥo, we, wø, ay, aɥ} => øː / _ {[cons], $} // [vowel] _
  {wa, oa, ou, wo, au, aw} => oː / _ {[cons], $} // [vowel] _
  jeː => iː / _ {[cons], $} // [vowel] _
  {jøː, joː, ɥeː, ɥoː, weː, wøː} => yː / _ {[cons], $} // [vowel] _
  woː => uː / _ {[cons], $} // [vowel] _
  jɛ => e / _ {[cons], $} // [vowel] _
  {jœ, jɔ, ɥɛ, ɥœ, ɥɔ, wɛ, wœ} => ø / _ {[cons], $} // [vowel] _ 
  wɔ => o / _ {[cons], $} // [vowel] _ 
  ɛj => e / _ {[cons], $} // _ [vowel]
  {œj, ɔj, ɛɥ, œɥ, ɔɥ, ɛw, œw} => ø / _ {[cons], $} // _ [vowel]
  ɔw => o / _ {[cons], $} // _ [vowel]

elision-1400:
  {i, y, u, e, ø, o, ɛ, œ, ɔ, a, ɑ} {f, θ, s, ʃ} => {iː, yː, uː, eː, øː, oː, ɛː, œː, ɔː, aː, ɑː} * / _ {[cons], $}
  {iː, yː, uː, eː, øː, oː, ɛː, œː, ɔː, aː, ɑː} {f, θ, s, ʃ} => {iː, yː, uː, iː, yː, uː, eː, øː, oː, eː, oː} * / _ {[cons], $}
  {v, ð, z, ʒ} => {w, l, r, j} / [vowel] _ {[cons], $}
  l => ɫ / [vowel] _ {[cons], $}
  {i, y, u, e, ø, o, ɛ, œ, ɔ, a, ɑ, iː, yː, uː, eː, øː, oː, ɛː, œː, ɔː, aː, ɑː} [nasal] => {iː, yː, uː, eː, øː, oː, ɛː, œː, ɔː, aː, ɑː, iː, yː, uː, iː, yː, uː, eː, øː, oː, eː, oː} * / _ {[cons], $}
  Then:
  {lr, rr} => r

r-elision-1100:
  {i, y, u, e, ø, o, ɛ, œ, ɔ, a, ɑ, iː, yː, uː, eː, øː, oː, ɛː, œː, ɔː, aː, ɑː} [trill] => {iː, yː, uː, eː, øː, oː, ɛː, œː, ɔː, aː, ɑː, iː, yː, uː, iː, yː, uː, eː, øː, oː, eː, oː} * / _ {[cons], $}

unrounding-800: 
  [front rounded vowel] => [unrounded]
  {i, iː} {j} => iː * // _ [vowel]
  {u, uː} {w} => uː * // _ [vowel]

insert-stress2:
  [vowel unstressed] => [vowel stressed] / $ [cons]? _
  Then: (
  [vowel unstressed] => [vowel stressed] / $ [cons]? [vowel stressed] [cons]? [cons] [vowel unstressed] [cons]? [cons] _ [cons]? $
  Else:
  [vowel unstressed] => [vowel stressed] / [cons] _ [cons]? [cons] [vowel] [cons]? $
)

vowelshift4-700:
  {a, ɑ, ɛ, ɔ}&[unstressed] => ə
  Then: [vowel stressed] => [vowel unstressed]
  Then:
  {iː, uː} => {ai, au} // _ ɫ
  {iː, uː} => {i, u} / _ ɫ
  {eː, oː} => {i, u}
  {ɛː, ɔː} => {e, o}
  {aː, ɑː} => {e, o}
  {i, u} => {e, o}
  {e, o} => {ɛ, ɔ}
  {ɑ, ɛ, ɔ} => a

misc-shifts3-400:
  {θ, ð} => {s, z}
  {w, ɫ} => u / [vowel] _ {[cons], $}
  l => i / [vowel] _ {[cons], $}
  j => i / [vowel] _ {[cons], $}
  Then:
  {ii, uu} => {ei, ou}

insert-stress3:
  [vowel unstressed] => [vowel stressed] / $ [cons]? _
  Then: (
  [vowel unstressed] => [vowel stressed] / $ [cons]? [vowel stressed] [cons]? [cons] [vowel unstressed] [cons]? [cons] _ [cons]? $
  Else:
  [vowel unstressed] => [vowel stressed] / [cons] _ [cons]? [cons] [vowel] [cons]? $
)

diphshifts-250:
  {əi, əu} => {e, o}
  {ɛ, ɔ, ə}&[unstressed] => {ə, ə, *} / _ $
  Then: [vowel stressed] => [vowel unstressed]
  Then: 
  {ai, au} => {ei, ou}  
  {ui, iu} => {oi, eu}
  {ɛi, ɔi} => {ai}
  {ɛu, ɔu} => {au}
  {əi, əu} => {ai, au}
  {j, w} => {i, u} / [vowel] _ {$, [cons]}

romanizer-modern-liro:
  {e, o} => {é, ó}
  {ɛ, ɔ} => {e, o}
  ə => a
  {ɾ, j} => {r, y}
  {ʃ, ʒ} => {x, j}
</pre>
