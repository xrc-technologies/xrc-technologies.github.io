---
title: FHSS Shaping
parent: NOVALINK mLRS Radio System
nav_order: 16
---

# FHSS Shaping
{: .d-inline-block }

Frequency Hopping Spread Spectrum allows the Transmitter and Receiver to hop very quickly between frequencies.

The enables a variety of improvements such as:

- Better resistance to interference

- Higher reliability

- Better performance with multiple pilots

FHSS **is not** encryption, but it primarily used to enhance the practical performance of a radio system.

NOVALINK supports FHSS on the `70 cm HAM` band through the `Ortho` parameter.

The `bind phrase` mechanism minimizes interference between different mLRS systems operating in the same RF band. However, the possibility of mutual interference is not eliminated since the set of frequencies generated from different bind phrases can overlap. The `ortho` mechanism modifies the set of frequencies generated from a bind phrase into three further sets which are guaranteed to be strictly different (hence the term orthogonal). This allows for up to three mLRS systems to stay out of each others way.

To activate, set band to `70 cm HAM` and change the `Ortho` setting.

<img src="{{ '/assets/images/novalink-74.png' | relative_url }}"
         alt="NOVALINK radio system"
         width="600">

- `off`: normal behavior
- `1/3`: the 1st out of the three available frequency sets is used
- `2/3`: the 2nd out of the three available frequency sets is used
- `3/3`: the 3rd out of the three available frequency sets is used

In order to use the `ortho` mechanism, mLRS systems need to be configured with the same bind phrase, but use different settings for the `Ortho` parameter. `Ortho` should not be set to `off` for any of them.

For more details, please visit the <a href="https://github.com/olliw42/mLRS-docu/blob/main/docs/FHSS_SHAPING.md" target="_blank" rel="noopener noreferrer">mLRS Official Documentation for FHSS Shaping</a>.
