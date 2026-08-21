# EEReserve

The Home Assistant theme for the Double E Reserve farm dashboards.

EEReserve owns the color palettes used by the custom property, energy, equipment,
family-management, overview, and Agribuddy cards. Layout and component styling stay
inside each card; this theme supplies surfaces, text, accents, status colors, and
card-specific identity colors.

## Install with HACS

1. Open **HACS** in Home Assistant.
2. Open the three-dot menu and select **Custom repositories**.
3. Add `https://github.com/gravytrain/ha-eereserve-theme` with category
   **Theme**.
4. Find and download **EEReserve** in HACS.

Themes must be enabled in Home Assistant:

```yaml
# configuration.yaml
frontend:
  themes: !include_dir_merge_named themes
```

Restart Home Assistant after enabling themes for the first time. For later theme
updates, run the `frontend.reload_themes` action and choose **EEReserve** from the
theme selector in your Home Assistant profile.

## Manual installation

Copy `themes/eereserve.yaml` into your Home Assistant `themes/` directory,
reload themes, and select **EEReserve**.

## Theme contract

The cards first read the documented `home-ui-*` variables supplied here, then
fall back to standard Home Assistant theme variables, and finally to their
original built-in colors. This means the cards retain their intended appearance
under EEReserve while remaining usable with someone else's Home Assistant theme.

The generic `home-ui-*` palette retains the graphite/brass Meter Register look.
The mode-specific `home-ui-management-*` palette retains the Farmhouse Ledger
olive/parchment light and dark treatments formerly selected with the private
`theme: farm` card option.

## License

EEReserve is available under the [MIT License](LICENSE).
