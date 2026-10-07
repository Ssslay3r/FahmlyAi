# Typography

The agreed Latin direction is **Inter**. **IBM Plex Sans Arabic** is the proposed Arabic companion, pending visual review. Neither font is bundled or downloaded in this redesign; the offline prototype uses installed fonts with Segoe UI/Tahoma/system fallbacks.

Use display, H1, H2, H3, title, body, small body, caption, button, and label roles defined in [tokens.json](../../design-system/tokens/tokens.json). Educational text uses a relaxed line height; Arabic body text uses 1.8. Arabic uses no negative letter spacing.

Mirror layouts with `dir="rtl"` and logical spacing. Keep English technical abbreviations and filenames in LTR spans when embedded in Arabic. Do not mirror the mascot or nondirectional symbols; mirror back/forward arrows with the reading direction.
