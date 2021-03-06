# Changelog

_All notable changes to this project will be documented in this file. This project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html)._

<!-- INSERT HERE -->

## [0.10.3](https://github.com/uber/nebula.gl/compare/v0.10.2...v0.10.3) - 2019-03-01

### Changes

* Fix publishing of readme to npm (#174)
* Add Design Goals (#173)

## [0.10.2](https://github.com/uber/nebula.gl/compare/v0.10.1...v0.10.2) - 2019-02-27

### Changes

* v0.10.2
* Add support for simultaneously editing multiple polygons in translate, rotate, scale, duplicate modes (#160)

## [0.10.1](https://github.com/uber/nebula.gl/compare/v0.10.0...v0.10.1) - 2019-02-14

### Changes

* fix getClusterObjects (#167)
* add scripts/changelog.sh

## [0.10.0](https://github.com/uber/nebula.gl/compare/v0.9.1...v0.10.0)

### Changes

* `featureIndex` renamed to `featureIndexes` (now an array of numbers instead of single number) for the `onEdit` callback.
* `positionIndexes` and `position` now nested under a new `editContext` property for the `onEdit` callback

## [0.9.1](https://github.com/uber/nebula.gl/compare/v0.9.0...v0.9.1)

* move supercluster to react module, upgrade version

## [0.9.0](https://github.com/uber/nebula.gl/compare/v0.8.0...v0.9.0)

### Fixes

* Fix issue with clicking edit handle while drawing polygon (#156)
* Issue 157. Pass Nebula childrens to Deck. (#158)
* Issue 154, avoid crash when nebula getChildContext being called before didMount (#155)

## [0.8.0](https://github.com/uber/nebula.gl/compare/v0.7.6...v0.8.0)

### Changed

* Upgraded deck.gl to 6.3.2
* Renamed `EditableGeoJsonLayer.onClick` to `EditableGeoJsonLayer.onLayerClick`

## [0.7.5](https://github.com/uber/nebula.gl/compare/v0.7.4...v0.7.5) - 2018-12-12

* Ability to split polygon with only right angles

<!-- ## [Unreleased](https://github.com/uber/nebula.gl/compare/v0.7.4...master) -->

## [0.7.4](https://github.com/uber/nebula.gl/compare/v0.7.3...v0.7.4) - 2018-12-10

* Ability to draw polygon with only right angles

## [0.7.3](https://github.com/uber/nebula.gl/compare/v0.7.2...v0.7.3) - 2018-11-26

* Handle null modeConfig
* Implement Split Polygon
* Ability to drag(extrude) an edge

## [0.7.2](https://github.com/uber/nebula.gl/compare/v0.7.1...v0.7.2) - 2018-11-12

* Implement selection-layer
* Detach event listeners on component unmount
* Disable hacky loop sync behind feature flag property

## [0.7.1](https://github.com/uber/nebula.gl/compare/v0.7.0...v0.7.1) - 2018-10-24

* Fix Nebula crashes on attempt to edit polygon layer over segment layer

## [0.7.0](https://github.com/uber/nebula.gl/compare/v0.6.1...v0.7.0) - 2018-10-23

### Added

* Ability to duplicate a feature ([#109](https://github.com/uber/nebula.gl/pull/109))
* Option to configure number of points for circle ([#103](https://github.com/uber/nebula.gl/pull/103))

### Changed

* `EditableGeoJsonLayer`'s `drawAtFront` prop should now be supplied via `modeConfig` prop ([#115](https://github.com/uber/nebula.gl/pull/115))

### Fixed

* Specify 6.0.5 as the minimum version for [deck.gl](https://github.com/uber/deck.gl)
* Fix turf v5 compatibility with boolean operations ([#111](https://github.com/uber/nebula.gl/pull/111))

## [0.6.1](https://github.com/uber/nebula.gl/compare/v0.5.1...v0.6.1) - 2018-10-10

### Added

* Ability to customize existing modes or add new modes using `ModeHandler`s
* `rotate` mode
* `translate` mode
* `scale` mode
* Boolean operations (union, difference, intersection) for polygon draw modes

### Changed

* Renamed `dragStartScreenCoords` to `pointerDownScreenCoords` and `dragStartGroundCoords` to `pointerDownGroundCoords` in `onStartDragging()`, `onStopDragging()`, and `onPointerMove()` events
* `isDragging` is now true whether or not something was picked in `onPointerMove()` event
* Edit handles will now only appear in `modify` and `drawPolygon` modes
* Can add new intermediate points anywhere along a line rather than just from the midpoint

## [0.5.1](https://github.com/uber/nebula.gl/compare/v0.4.3...v0.5.1) - 2018-09-24

### Removed

* `updatedMode` and `updatedSelectedFeatureIndexes` are no longer passed to the `onEdit` callback. It is now up to the consuming application to determine when/if mode or selection should be changed. See `examples/deck` for a demonstration.

### Changed

* Geometry type will no longer be "upgraded" or "downgraded" by nebula. `onEdit` will only be called once the desired geometry type is achieved (e.g. when completing the polygon).
* Renamed `getDrawLineColor` to `getTentativeLineColor`
* Renamed `getDrawFillColor` to `getTentativeFillColor`
* Renamed `getDrawLineWidth` to `getTentativeLineWidth`
* Renamed `getDrawLineDashArray` to `getTentativeLineDashArray`

### Fixes

* Double-click to complete polygon adds a point where the double-click happened

## [0.1.1 through 0.4.3](https://github.com/uber/nebula.gl/compare/v0.1.0...v0.4.3)

* See [commit history](https://github.com/uber/nebula.gl/compare/v0.1.0...v0.4.3) for changelog
