---
-api-id: M:Windows.UI.Notifications.TileFlyoutUpdater.StartPeriodicUpdate(Windows.Foundation.Uri,Windows.Foundation.DateTime,Windows.UI.Notifications.PeriodicUpdateRecurrence)
-api-type: winrt method
---

<!-- Method syntax
public void StartPeriodicUpdate(Windows.Foundation.Uri tileFlyoutContent, Windows.Foundation.DateTime startTime, Windows.UI.Notifications.PeriodicUpdateRecurrence requestedInterval)
-->

# Windows.UI.Notifications.TileFlyoutUpdater.StartPeriodicUpdate

## -description
Launches a series of [periodic](http://msdn.microsoft.com/library/4615a86a-849f-4d40-9a96-2670a856c468) updates for a tile flyout (mix view) notification, beginning at a specified time. Update content is retrieved from a specified Uniform Resource Identifier (URI).

## -parameters
### -param tileFlyoutContent
The Uniform Resource Identifier (URI) from which the XML content of the tile flyout update is retrieved.

### -param startTime
The date and time at which the Uniform Resource Identifier (URI) should first be polled for new content.

### -param requestedInterval
The frequency with which the Uniform Resource Identifier (URI) is polled for new content, following the initial update at *startTime*.

## -remarks

## -examples

## -see-also
[StartPeriodicUpdate(Uri, PeriodicUpdateRecurrence)](tileflyoutupdater_startperiodicupdate_1967457783.md)