# rulespec-pe

Peru RuleSpec source registry.

This repository targets the Peruvian tax-benefit surface simulated by PERUMOD (the SOUTHMOD tax-benefit microsimulation model for Peru, UNU-WIDER; v2.4, policy years 2019–24): personal income tax under the TUO de la Ley del Impuesto a la Renta (DS 179-2004-EF; UIT-banded schedule, Articles 33–34 categories), IGV and ISC under the TUO DS 055-99-EF (Artículo 17: dieciséis por ciento — eighteen percent total with the two percent municipal promotion tax), EsSalud health contributions under Ley 26790 (employer nine percent; micro-enterprises split fifty/fifty), pension contributions (ten percent AFP / thirteen percent ONP — the operative instruments are a tranche-2 capture), the Pensión 65 subsidised pension (DS 081-2011-PCM; ~S/250 bimonthly at 65+ under SISFOH), and the Juntos conditional cash transfer (creation decree DS 032-2005-PCM, tranche-2 capture).

All encoded law lives under a single `pe/` namespace. The validation frame is PERUMOD v2.4 (report CR-PERUMOD-v2-4).

## Source Priority

Policy must come from the furthest upstream available source: El Peruano prints and official consolidations first (SUNAT/MEF TUO compilations, the Congreso law library, gob.pe official document CDN — record the host in manifest metadata), decretos supremos and institutional resolutions next, agency guidance only after the governing instrument is identified.
