---
-api-id: T:Windows.Foundation.Diagnostics.LoggingChannel
-api-type: winrt class
---

<!-- Class syntax.
public class LoggingChannel : Windows.Foundation.Diagnostics.ILoggingChannel, Windows.Foundation.Diagnostics.ILoggingChannel2, Windows.Foundation.Diagnostics.ILoggingTarget, Windows.Foundation.IClosable
-->

# Windows.Foundation.Diagnostics.LoggingChannel

## -description
Represents a source of log messages.

## -remarks
The default [LoggingLevel](logginglevel.md) is **Verbose**.

Add [LoggingChannel](loggingchannel_loggingchannel.md) instances to a [LoggingSession](loggingsession.md) or a [FileLoggingSession](fileloggingsession.md) to enable logging in your app.



> **Windows 10**
> Two modes of operation are now supported: Windows 8.1 compatibility mode and the new behavior supported by Windows 10 and later which allows you to log self-describing Event Tracing for Windows (ETW) events without a manifest. + For Windows 8.1 compatibility mode, create the object using the [LoggingChannel(String)](loggingchannel_loggingchannel.md) constructor.
+ For Windows 10 and later specific behavior, create the object using the [LoggingChannel(String, LoggingChannelOptions)](loggingchannel_loggingchannel_1496214966.md) or [LoggingChannel(String, LoggingChannelOptions, Guid)](loggingchannel_loggingchannel_2599058.md) constructor.
The differences between these two modes are:

<table>
   <tr><th>Windows 8.1 compatibility mode</th><th>Windows 10 and later specific behavior</th></tr>
   <tr><td>Some **LoggingChannel** events may reference the 4bd2826e-54a1-4ba9-bf63-92b73ea1ac4a which is the GUID for the **Microsoft-Windows-Diagnostics-LoggingChannel** manifest that is available on Windows 8.1 or later.</td><td>All events are self-describing. No manifest is required.</td></tr>
   <tr><td>The [Id](loggingchannel_id.md) property is always 4bd2826e-54a1-4ba9-bf63-92b73ea1ac4a, which is the GUID for the **Microsoft-Windows-Diagnostics-LoggingChannel** manifest.</td><td>The [Id](loggingchannel_id.md) property varies based on how the channel is constructed. If the [LoggingChannel(String, LoggingChannelOptions)](loggingchannel_loggingchannel_1496214966.md) constructor is used, the **Id** is determined by hashing the name parameter. If the [LoggingChannel(String, LoggingChannelOptions, Guid)](loggingchannel_loggingchannel_2599058.md) constructor is used, the specified *id* parameter is used.</td></tr>
   <tr><td>Events generated by the **LogMessage**, **LogValuePair**, the [LoggingActivity](loggingactivity_loggingactivity.md) constructors or destructor, or activity.[Activity.Close ](loggingactivity_close.md) method use manifest-based event encoding. All other events use self-describing TraceLogging event encoding.</td><td>All events use self-describing TraceLogging event encoding.</td></tr>
   <tr><td>The channel provider name is Microsoft-Windows-Diagnostics-LoggingChannel. The channel name is recorded in each event in the payload field **LoggingChannelName**.</td><td>The channel name is used as the provider name. Events will not have a **LoggingChannelName** field.</td></tr>
</table>

## -examples

## -see-also
[LoggingSession](loggingsession.md), [FileLoggingSession](fileloggingsession.md), [ILoggingChannel](iloggingchannel.md), [IClosable](../windows.foundation/iclosable.md), [Logging sample (Windows 10)](http://go.microsoft.com/fwlink/p/?LinkId=620565)