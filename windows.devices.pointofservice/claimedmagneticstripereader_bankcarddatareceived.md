---
-api-id: E:Windows.Devices.PointOfService.ClaimedMagneticStripeReader.BankCardDataReceived
-api-type: winrt event
---

<!-- Event syntax
public event Windows.Foundation.TypedEventHandler BankCardDataReceived<Windows.Devices.PointOfService.ClaimedMagneticStripeReader,  Windows.Devices.PointOfService.MagneticStripeReaderBankCardDataReceivedEventArgs>
-->

# Windows.Devices.PointOfService.ClaimedMagneticStripeReader.BankCardDataReceived

## -description
Occurs when a bank card is swiped.

## -remarks
An application can register for this event event handler to get the bank card data each time a bank card is swiped through the magnetic stripe reader.

## -examples
The following example shows how to setup the magnetic stripe reader to receive data after a scanning event.



[!code-cpp[SetupMagStripeReader](../windows.devices.pointofservice/code/MagneticStripeReader/cpp/Scenario1.xaml.cpp#SnippetSetupMagStripeReader)]

[!code-cs[SetupMagStripeReader](../windows.devices.pointofservice/code/MagneticStripeReader/cs/Scenario1.xaml.cs#SnippetSetupMagStripeReader)]



[!code-cpp[MagStripeReaderDataReceived](../windows.devices.pointofservice/code/MagneticStripeReader/cpp/Scenario1.xaml.cpp#SnippetMagStripeReaderDataReceived)]

[!code-cs[MagStripeReaderDataReceived](../windows.devices.pointofservice/code/MagneticStripeReader/cs/Scenario1.xaml.cs#SnippetMagStripeReaderDataReceived)]

[!code-js[MagStripeReaderDataReceived](../windows.devices.pointofservice/code/MagneticStripeReader/js/scenario1.js#SnippetMagStripeReaderDataReceived)]



[!code-js[CreateMagStripeReaderJS](../windows.devices.pointofservice/code/MagneticStripeReader/js/scenario1.js#SnippetCreateMagStripeReaderJS)]



[!code-js[MagStripeReaderDataReceivedJS](../windows.devices.pointofservice/code/MagneticStripeReader/js/scenario1.js#SnippetMagStripeReaderDataReceivedJS)]

## -see-also
[Magnetic stripe reader sample (Windows 10)](http://go.microsoft.com/fwlink/p/?LinkId=620017)