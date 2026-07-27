links = []
if colord.found()
  links += ['cinnamon-color-panel.desktop']
endif
if libnm.found()
  links += ['cinnamon-network-panel.desktop']
endif
if libwacom.found()
  links += ['cinnamon-wacom-panel.desktop']
endif

foreach link: links
  install_symlink(link,
    install_dir: panel_def_dir,
    pointing_to: '../../applications' / link
  )
endforeach
