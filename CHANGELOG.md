# Changelog

## 1.2.15 - 2020-06-30

### Fixed
- Return list reference on `wishlist/lists/create`. (thanks @BrandonJamesBorders).

## 1.2.14 - 2020-06-15

### Added
- Add `wishlist/lists/update` action to enable list updating from the front-end.

## 1.2.13 - 2020-06-09

> {warning} Please note the deprecation of `item` for Ajax requests. If you're using Ajax to handle the response from add/delete/toggle, please adjust your Javascript code that handles this to use `items`.

### Added
- Full item model is now included in Ajax responses for `toggle` requests.

### Fixed
- Fix incorrect return values for add/delete/toggle for Ajax requests.

### Deprecated
- `item` is now deprecated in Ajax responses for add/delete/toggle actions, and will be removed in the next major release. Please adjust your code to instead rely on `items` which is an array of returned Wishlist items. This is because these actions can support multiple items, rather than just a single one.

## 1.2.12 - 2020-05-31

> {warning} Please note the change in default behaviour for `purgeInactiveLists`.

### Changed
- Change `purgeInactiveLists` to be on by default. This will prevent your wishlists from getting out of control.

## 1.2.11 - 2020-05-29

### Added
- Add `item` model to add/remove ajax actions.
- Implement GraphQL for items and lists. See [docs](https://verbb.io/craft-plugins/wishlist/docs/developers/graphql).

## 1.2.10 - 2020-05-16

> {warning} Please note the change in default behaviour for `mergeLastListOnLogin`.

### Changed
- Change `mergeLastListOnLogin` to be off by default. User lists won't be merged automatically, by default.

## 1.2.9 - 2020-05-14

### Added
- Add `resave/wishlist-items` console command.
- Add `resave/wishlist-lists` console command.

### Fixed
- Fix potential error when fetching an items list, when it doesn’t exist.

## 1.2.8 - 2020-05-12

### Added
- Return “items” when toggling an item. This will be the item ID and the action taken upon an item ('added' or 'removed').

## 1.2.7 - 2020-05-12

### Added
- Add `action` param to all item and list controller actions

## 1.2.6 - 2020-04-16

### Fixed
- Fix logging error `Call to undefined method setFileLogging()`.

## 1.2.5 - 2020-04-16

### Added
- Add `mergeLastListOnLogin`, on by default to merge guests’ lists when logging in with existing saved lists.

### Fixed
- Ensure saved lists for users aren’t overridden on next login.

## 1.2.4 - 2020-04-15

### Changed
- File logging now checks if the overall Craft app uses file logging.
- Log files now only include `GET` and `POST` additional variables.

## 1.2.3 - 2020-04-07

### Fixed
- Fix managing lists on the front-end and requiring permissions.

## 1.2.2 - 2020-04-01

### Fixed
- Only allow editing of list types if editable.
- Fix default data when installing conflicting with project config.
- Ensure plugin project config is removed when uninstalling.

## 1.2.1 - 2020-01-30

### Added
- Allow list actions to be callable via URL.
- Add `manageDisabledLists` config setting to manage disabled lists and their items (default to true).

### Fixed
- Fix error when adding a new item to list in the CP.
- Fix unable to update the element for an item through the CP.

## 1.2.0 - 2020-01-29

### Added
- Craft 3.4 compatibility.

## 1.1.2 - 2020-01-18

### Fixed
- Fix project config error.

## 1.1.1 - 2020-01-18

### Fixed
- Fix list items having incorrect search attributes.

## 1.1.0 - 2020-01-10

### Added
- Add project config support.
- Add support for add/delete/toggle multiple items. See [docs](https://verbb.io/craft-plugins/wishlist/docs/template-guides/managing-items)
- Add `purgeInactiveGuestListsDuration` to set times for guest lists to be purged, separate to user lists. This is default to 1 day.
- Add purge lists to Craft's garbage collection.
- Add guest list to user list when logging in.
- Add email share action for lists. Users can directly and easily send their list via email.
- Allow managing of list items in the CP, including add and delete.

### Changed
- Add `forceSave` to `craft.wishlist.lists()` to force a new list to be generated.

### Fixed
- Fixed SQL error for PostgreSQL. (thanks @Tam).
- Fix `craft.wishlist.item()` when called for a specific list.
- Fix issue when calling multiple lists in the same request not returning the correct list.

## 1.0.6 - 2019-03-02

### Added
- Add update controller action for items.

### Fixed
- Fix title on CP edit item page.
- Fix saving items in the CP.
- Fix missing delete action for items

## 1.0.5 - 2019-03-01

### Fixed
- Fix setting field params via URL not working correctly.

## 1.0.4 - 2019-02-27

### Fixed
- Fix purge function to only remove lists with zero items.

## 1.0.3 - 2019-02-27

### Fixed
- Fix typo in purge lists function.

## 1.0.2 - 2019-02-26

### Fixed
- Fix permissions for lists.
- Fix permissions for list types.
- Fix sidebar menu for using plugin name override.

## 1.0.1 - 2019-02-17

### Added
- Adding option to provide a list type handle or id when adding an Item. (thanks @echantigny).

### Fixed
- Fix owner column not being correct.
- Correct AJAX action for list type deletion. (thanks @AugustMiller).
- Add routing rule for index of list type. (thanks @echantigny).
- Fix error thrown when viewing list when created in the CP. (thanks @echantigny).

## 1.0.0 - 2018-11-26

- Initial release.
