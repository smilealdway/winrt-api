---
-api-id: T:Windows.UI.Xaml.Automation.DropTargetPatternIdentifiers
-api-type: winrt class
---

<!-- Class syntax.
public class DropTargetPatternIdentifiers : Windows.UI.Xaml.Automation.IDropTargetPatternIdentifiers
-->

# Windows.UI.Xaml.Automation.DropTargetPatternIdentifiers

## -description
Contains values used as identifiers by [IDropTargetProvider](../windows.ui.xaml.automation.provider/idroptargetprovider.md).

## -remarks
Classes such as [DropTargetPatternIdentifiers](droptargetpatternidentifiers.md) are the identifiers for the Windows Runtime implementation of a common provider pattern for Microsoft UI Automation. You might use these identifiers if you are implementing a Windows Runtime custom automation peer that reports support for [IDropTargetProvider](http://msdn.microsoft.com/library/eccdc429-4829-46e0-ae77-270024e2da48) in its [GetPattern](../windows.ui.xaml.automation.peers/automationpeer_getpattern.md) implementation. These identifiers are needed for the [RaisePropertyChangedEvent](../windows.ui.xaml.automation.peers/automationpeer_raisepropertychangedevent.md) calls that you make from control code that references your own peer, or for [FindItemByProperty](../windows.ui.xaml.automation.provider/iitemcontainerprovider_finditembyproperty.md) in an items container peer.

This same pattern is usually exposed to clients in a different way, depending on which technology they use to implement the client and examine the Microsoft UI Automation tree. [IDropTargetProvider](http://msdn.microsoft.com/library/eccdc429-4829-46e0-ae77-270024e2da48) is also presented as a Component Object Model (COM) interface.

## -examples

## -see-also
[IDropTargetProvider](http://msdn.microsoft.com/library/eccdc429-4829-46e0-ae77-270024e2da48), [Control patterns and interfaces](http://msdn.microsoft.com/library/2091883c-5d0c-44ed-936a-709022926a42), [Custom automation peers](http://msdn.microsoft.com/library/aa8da53b-fe6e-40ac-9f0a-cb09637c87b4)