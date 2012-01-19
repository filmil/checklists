# -*- python -*-
import os

env = Environment(ENV=os.environ)

def latex_dependency(base_name, *other_files):
  """Declares a LaTeX dependency.

  Args:
    base_name: string, the base name of the source file
    other_files: strings, the other files that will be used as sources
  """
  other_tex_files = ['%s.tex' % file_name for file_name in other_files]
  dvi = env.DVI(
      target = '%s.dvi' % base_name,
      source = ['%s.tex' % base_name ] + other_tex_files)
  pdf = env.PDF(
      target = '%s.pdf' % base_name,
      source = ['%s.dvi' % base_name])
  Depends(pdf, dvi)

latex_dependency(
    'c172sp-preflight-checklist', 
    'preamble', 'disclaimer')
latex_dependency(
    'checkride-cheatsheet', 
    'preamble', 'disclaimer')
