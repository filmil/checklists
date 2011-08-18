# -*- python -*-
import os

env = Environment(ENV=os.environ)

dviOutput = env.DVI(
    target = 'c172sp-preflight-checklist.dvi', 
    source = [
        'c172sp-preflight-checklist.tex',      # Has to be first.
        'preamble.tex',
        'disclaimer.tex',
    ],
)
pdfOutput = env.PDF(
    target = 'c172sp-preflight-checklist.pdf',
    source = ['c172sp-preflight-checklist.dvi'],
)
Depends(pdfOutput, dviOutput)

