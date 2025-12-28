# my-ha-configs

A repository holding some of my Home Assistant configurations.

> [!NOTE]
> This repository is a constant work in progress (WIP). Configurations and structures may change as I refine my setup.

## Overview

This repository primarily contains Lovelace dashboard configurations and custom card templates.

## Structure

### `button-card/`
Configurations and templates for [custom:button-card](https://github.com/custom-cards/button-card).

- **[climate-ac/](button-card/climate-ac/)**: A layout for controlling A/C climate entities. Features dynamic icon coloring based on HVAC state.
- **[temp-humidity/](button-card/temp-humidity/)**: A reusable pattern for displaying temperature, humidity, and battery levels from sensors (e.g., Tuya TS0201).
