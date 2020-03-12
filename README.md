# Facebook magma helm charts

## Adding this helm repo in OSM

```bash
osm repo-add --type helm-chart --description "Repository for Facebook Magma helm Chart" magma https://felipevicens.github.io/fb-magma-helm-chart
```

## Download the NF and NS artifacts

```bash
wget https://github.com/felipevicens/fb-magma-helm-chart/raw/gh-pages/osm_packages/fb_magma_ns.tar.gz
wget https://github.com/felipevicens/fb-magma-helm-chart/raw/gh-pages/osm_packages/fb_magma_knf.tar.gz
```

## Upload the artifacts to OSM

```bash
osm nfpkg-create fb_magma_knf.tar.gz
osm nspkg-create fb_magma_ns.tar.gz
```

## Instantiate the KNF

```bash
osm ns-create --ns_name magma --nsd_name <name> --vim_account <your_vim>
```
