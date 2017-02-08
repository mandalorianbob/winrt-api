---
-api-id: P:Windows.ApplicationModel.VoiceCommands.VoiceCommandResponse.Message
-api-type: winrt property
---

<!-- Property syntax
public Windows.ApplicationModel.VoiceCommands.VoiceCommandUserMessage Message { get;  set; }
-->

# Windows.ApplicationModel.VoiceCommands.VoiceCommandResponse.Message

## -description
The initial message that is spoken by **Cortana** and shown on the **Cortana** canvas.


This message should be:

+ An informative statement on progress, completion, and error screens (see [ReportProgressAsync](voicecommandserviceconnection_reportprogressasync.md), [ReportSuccessAsync](voicecommandserviceconnection_reportsuccessasync.md), [ReportFailureAsync](voicecommandserviceconnection_reportfailureasync.md)).
+ An unambiguous question that can be answered with either yes or no on confirmation screens (see [RequestConfirmationAsync](voicecommandserviceconnection_requestconfirmationasync.md)).
+ A request for the user to select from the list of choices presented on disambiguation screens (see [RequestDisambiguationAsync](voicecommandserviceconnection_requestdisambiguationasync.md)).


## -property-value
The message that is spoken or shown by **Cortana**.

## -remarks

## -examples

## -see-also
[VoiceCommandContentTiles](voicecommandresponse_voicecommandcontenttiles.md), [RepeatMessage](voicecommandresponse_repeatmessage.md), [ elements and attributes v1.2](voice_command_elements_and_attributes_1_2.md), [Cortana interactions](http://msdn.microsoft.com/library/4c11a7cf-da26-4ca1-a9b9-fe52670101f5), [Cortana design guidelines](http://msdn.microsoft.com/library/a92c084b-9913-4718-9a04-569d51ace55d), [Cortana voice command sample](http://go.microsoft.com/fwlink/p/?LinkID=619899)