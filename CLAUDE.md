# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This is a Drupal sub-theme based on Olivero (Drupal core's default frontend theme). It provides visual customizations through CSS custom property overrides without modifying Olivero's templates or JavaScript.

## Architecture

The theme uses a minimal approach:
- **tedbow_demo.info.yml**: Theme metadata declaring Olivero as the base theme and attaching the enhancements library globally
- **tedbow_demo.libraries.yml**: Defines the `enhancements` asset library
- **css/enhancements.css**: All customizations via CSS custom property overrides targeting Olivero's design tokens

## Customization Approach

Olivero exposes CSS custom properties (e.g., `--color--primary-60`, `--font-sans`, `--border-radius`) that control its visual design. This theme overrides these in `:root` for site-wide changes. Direct CSS selectors (`.site-header`, `.footer-block`) are used sparingly for effects Olivero doesn't expose as variables.

## Drupal Compatibility

Supports Drupal 10 and 11 (`core_version_requirement: ^10 || ^11`).
