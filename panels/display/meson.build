subdir('icons')

panel_display_sources = [
  'cc-display-panel.c',
  'cc-rr-labeler.c',
  'display-module.c',
  'scrollarea.c',
  gnome.genmarshal('foo-marshal',
    prefix: 'foo_marshal',
    sources: 'foo-marshal.list',
  ),
]

panel_display = shared_library('display',
  panel_display_sources,
  include_directories: rootInclude,
  link_with: [
    libcinnamon_control_center,
  ],
  dependencies: [
    glib,
    gtk,
    cinn_desktop,
    libx11,
    math,
  ],
  install: true,
  install_dir: panels_dir
)


install_data('display-capplet.ui',
  install_dir: ui_dir,
)

install_data(
  'cinnamon-display-panel.desktop',
  install_dir: panel_def_dir
)


install_data('org.cinnamon.control-center.display.gschema.xml',
    install_dir: join_paths(get_option('datadir'), 'glib-2.0', 'schemas')
)
