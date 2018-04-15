<HTML>
<HEAD>
<TITLE>AGI Commands</TITLE>
</HEAD>
<BODY>
<CENTER><B><H1>AGI Commands</H1></B></CENTER>

<TABLE BORDER="0" CELLSPACING="10">
<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>answer - Answer channel </B></TH></TR>
<TR><TD ALIGN="CENTER">Answers channel if not already in answer state. Returns '-1' on channel</TD></TR>
<TR><TD ALIGN="CENTER">
failure, or '0' if successful.<BR>
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>asyncagi break - Interrupts Async AGI </B></TH></TR>
<TR><TD ALIGN="CENTER">Interrupts expected flow of Async AGI commands and returns control to previous</TD></TR>
<TR><TD ALIGN="CENTER">
source (typically, the PBX dialplan).<BR>
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>channel status - Returns status of the connected channel. </B></TH></TR>
<TR><TD ALIGN="CENTER">Returns the status of the specified &lt;channelname&gt;. If no channel name is given</TD></TR>
<TR><TD ALIGN="CENTER">
then returns the status of the current channel.<BR>
Return values:<BR>
    0 - Channel is down and available.<BR>
    1 - Channel is down, but reserved.<BR>
    2 - Channel is off hook.<BR>
    3 - Digits (or equivalent) have been dialed.<BR>
    4 - Line is ringing.<BR>
    5 - Remote end is ringing.<BR>
    6 - Line is up.<BR>
    7 - Line is busy.<BR>
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>database del - Removes database key/value </B></TH></TR>
<TR><TD ALIGN="CENTER">Deletes an entry in the Asterisk database for a given &lt;family&gt; and &lt;key&gt;.</TD></TR>
<TR><TD ALIGN="CENTER">
Returns '1' if successful, '0' otherwise.<BR>
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>database deltree - Removes database keytree/value </B></TH></TR>
<TR><TD ALIGN="CENTER">Deletes a &lt;family&gt; or specific &lt;keytree&gt; within a &lt;family&gt; in the Asterisk</TD></TR>
<TR><TD ALIGN="CENTER">
database.<BR>
Returns '1' if successful, '0' otherwise.<BR>
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>database get - Gets database value </B></TH></TR>
<TR><TD ALIGN="CENTER">Retrieves an entry in the Asterisk database for a given &lt;family&gt; and &lt;key&gt;.</TD></TR>
<TR><TD ALIGN="CENTER">
Returns '0' if &lt;key&gt; is not set. Returns '1' if &lt;key&gt; is set and returns the<BR>
variable in parenthesis.<BR>
Example return code: 200 result=1 (testvariable)<BR>
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>database put - Adds/updates database value </B></TH></TR>
<TR><TD ALIGN="CENTER">Adds or updates an entry in the Asterisk database for a given &lt;family&gt;, &lt;key&gt;,</TD></TR>
<TR><TD ALIGN="CENTER">
and &lt;value&gt;.<BR>
Returns '1' if successful, '0' otherwise.<BR>
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>exec - Executes a given Application </B></TH></TR>
<TR><TD ALIGN="CENTER">Executes &lt;application&gt; with given &lt;options&gt;.</TD></TR>
<TR><TD ALIGN="CENTER">
Returns whatever the &lt;application&gt; returns, or '-2' on failure to find<BR>
&lt;application&gt;.<BR>
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>get data - Prompts for DTMF on a channel </B></TH></TR>
<TR><TD ALIGN="CENTER">Stream the given &lt;file&gt;, and receive DTMF data.</TD></TR>
<TR><TD ALIGN="CENTER">
Returns the digits received from the channel at the other end.<BR>
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>get full variable - Evaluates a channel expression </B></TH></TR>
<TR><TD ALIGN="CENTER">Returns '0' if &lt;variablename&gt; is not set or channel does not exist. Returns '1'</TD></TR>
<TR><TD ALIGN="CENTER">
if &lt;variablename&gt; is set and returns the variable in parenthesis. Understands<BR>
complex variable names and builtin variables, unlike GET VARIABLE.<BR>
Example return code: 200 result=1 (testvariable)<BR>
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>get option - Stream file, prompt for DTMF, with timeout. </B></TH></TR>
<TR><TD ALIGN="CENTER">Behaves similar to STREAM FILE but used with a timeout option.</TD></TR>
<TR><TD ALIGN="CENTER">
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>get variable - Gets a channel variable. </B></TH></TR>
<TR><TD ALIGN="CENTER">Returns '0' if &lt;variablename&gt; is not set. Returns '1' if &lt;variablename&gt; is set</TD></TR>
<TR><TD ALIGN="CENTER">
and returns the variable in parentheses.<BR>
Example return code: 200 result=1 (testvariable)<BR>
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>hangup - Hangup a channel. </B></TH></TR>
<TR><TD ALIGN="CENTER">Hangs up the specified channel. If no channel name is given, hangs up the</TD></TR>
<TR><TD ALIGN="CENTER">
current channel<BR>
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>noop - Does nothing. </B></TH></TR>
<TR><TD ALIGN="CENTER">Does nothing.</TD></TR>
<TR><TD ALIGN="CENTER">
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>receive char - Receives one character from channels supporting it. </B></TH></TR>
<TR><TD ALIGN="CENTER">Receives a character of text on a channel. Most channels do not support the</TD></TR>
<TR><TD ALIGN="CENTER">
reception of text. Returns the decimal value of the character if one is<BR>
received, or '0' if the channel does not support text reception. Returns '-1'<BR>
only on error/hangup.<BR>
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>receive text - Receives text from channels supporting it. </B></TH></TR>
<TR><TD ALIGN="CENTER">Receives a string of text on a channel. Most channels do not support the</TD></TR>
<TR><TD ALIGN="CENTER">
reception of text. Returns '-1' for failure or '1' for success, and the string<BR>
in parenthesis.<BR>
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>record file - Records to a given file. </B></TH></TR>
<TR><TD ALIGN="CENTER">Record to a file until a given dtmf digit in the sequence is received. Returns</TD></TR>
<TR><TD ALIGN="CENTER">
'-1' on hangup or error.  The format will specify what kind of file will be<BR>
recorded. The &lt;timeout&gt; is the maximum record time in milliseconds, or '-1' for<BR>
no &lt;timeout&gt;. &lt;offset samples&gt; is optional, and, if provided, will seek to the<BR>
offset without exceeding the end of the file. &lt;beep&gt; can take any value, and<BR>
causes Asterisk to play a beep to the channel that is about to be recorded.<BR>
&lt;silence&gt; is the number of seconds of silence allowed before the function<BR>
returns despite the lack of dtmf digits or reaching &lt;timeout&gt;. &lt;silence&gt; value<BR>
must be preceded by 's=' and is also optional.<BR>
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>say alpha - Says a given character string. </B></TH></TR>
<TR><TD ALIGN="CENTER">Say a given character string, returning early if any of the given DTMF digits</TD></TR>
<TR><TD ALIGN="CENTER">
are received on the channel. Returns '0' if playback completes without a digit<BR>
being pressed, or the ASCII numerical value of the digit if one was pressed or<BR>
'-1' on error/hangup.<BR>
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>say digits - Says a given digit string. </B></TH></TR>
<TR><TD ALIGN="CENTER">Say a given digit string, returning early if any of the given DTMF digits are</TD></TR>
<TR><TD ALIGN="CENTER">
received on the channel. Returns '0' if playback completes without a digit<BR>
being pressed, or the ASCII numerical value of the digit if one was pressed or<BR>
'-1' on error/hangup.<BR>
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>say number - Says a given number. </B></TH></TR>
<TR><TD ALIGN="CENTER">Say a given number, returning early if any of the given DTMF digits are</TD></TR>
<TR><TD ALIGN="CENTER">
received on the channel.  Returns '0' if playback completes without a digit<BR>
being pressed, or the ASCII numerical value of the digit if one was pressed or<BR>
'-1' on error/hangup.<BR>
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>say phonetic - Says a given character string with phonetics. </B></TH></TR>
<TR><TD ALIGN="CENTER">Say a given character string with phonetics, returning early if any of the</TD></TR>
<TR><TD ALIGN="CENTER">
given DTMF digits are received on the channel. Returns '0' if playback<BR>
completes without a digit pressed, the ASCII numerical value of the digit if<BR>
one was pressed, or '-1' on error/hangup.<BR>
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>say date - Says a given date. </B></TH></TR>
<TR><TD ALIGN="CENTER">Say a given date, returning early if any of the given DTMF digits are received</TD></TR>
<TR><TD ALIGN="CENTER">
on the channel. Returns '0' if playback completes without a digit being<BR>
pressed, or the ASCII numerical value of the digit if one was pressed or '-1'<BR>
on error/hangup.<BR>
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>say time - Says a given time. </B></TH></TR>
<TR><TD ALIGN="CENTER">Say a given time, returning early if any of the given DTMF digits are received</TD></TR>
<TR><TD ALIGN="CENTER">
on the channel. Returns '0' if playback completes without a digit being<BR>
pressed, or the ASCII numerical value of the digit if one was pressed or '-1'<BR>
on error/hangup.<BR>
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>say datetime - Says a given time as specified by the format given. </B></TH></TR>
<TR><TD ALIGN="CENTER">Say a given time, returning early if any of the given DTMF digits are received</TD></TR>
<TR><TD ALIGN="CENTER">
on the channel. Returns '0' if playback completes without a digit being<BR>
pressed, or the ASCII numerical value of the digit if one was pressed or '-1'<BR>
on error/hangup.<BR>
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>send image - Sends images to channels supporting it. </B></TH></TR>
<TR><TD ALIGN="CENTER">Sends the given image on a channel. Most channels do not support the</TD></TR>
<TR><TD ALIGN="CENTER">
transmission of images. Returns '0' if image is sent, or if the channel does<BR>
not support image transmission.  Returns '-1' only on error/hangup. Image names<BR>
should not include extensions.<BR>
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>send text - Sends text to channels supporting it. </B></TH></TR>
<TR><TD ALIGN="CENTER">Sends the given text on a channel. Most channels do not support the</TD></TR>
<TR><TD ALIGN="CENTER">
transmission of text. Returns '0' if text is sent, or if the channel does not<BR>
support text transmission. Returns '-1' only on error/hangup.<BR>
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>set autohangup - Autohangup channel in some time. </B></TH></TR>
<TR><TD ALIGN="CENTER">Cause the channel to automatically hangup at &lt;time&gt; seconds in the future. Of</TD></TR>
<TR><TD ALIGN="CENTER">
course it can be hungup before then as well. Setting to '0' will cause the<BR>
autohangup feature to be disabled on this channel.<BR>
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>set callerid - Sets callerid for the current channel. </B></TH></TR>
<TR><TD ALIGN="CENTER">Changes the callerid of the current channel.</TD></TR>
<TR><TD ALIGN="CENTER">
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>set context - Sets channel context. </B></TH></TR>
<TR><TD ALIGN="CENTER">Sets the context for continuation upon exiting the application.</TD></TR>
<TR><TD ALIGN="CENTER">
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>set extension - Changes channel extension. </B></TH></TR>
<TR><TD ALIGN="CENTER">Changes the extension for continuation upon exiting the application.</TD></TR>
<TR><TD ALIGN="CENTER">
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>set music - Enable/Disable Music on hold generator </B></TH></TR>
<TR><TD ALIGN="CENTER">Enables/Disables the music on hold generator. If &lt;class&gt; is not specified, then</TD></TR>
<TR><TD ALIGN="CENTER">
the 'default' music on hold class will be used. This generator will be stopped<BR>
automatically when playing a file.<BR>
Always returns '0'.<BR>
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>set priority - Set channel dialplan priority. </B></TH></TR>
<TR><TD ALIGN="CENTER">Changes the priority for continuation upon exiting the application. The</TD></TR>
<TR><TD ALIGN="CENTER">
priority must be a valid priority or label.<BR>
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>set variable - Sets a channel variable. </B></TH></TR>
<TR><TD ALIGN="CENTER">Sets a variable to the current channel.</TD></TR>
<TR><TD ALIGN="CENTER">
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>stream file - Sends audio file on channel. </B></TH></TR>
<TR><TD ALIGN="CENTER">Send the given file, allowing playback to be interrupted by the given digits,</TD></TR>
<TR><TD ALIGN="CENTER">
if any. Returns '0' if playback completes without a digit being pressed, or the<BR>
ASCII numerical value of the digit if one was pressed, or '-1' on error or if<BR>
the channel was disconnected. If musiconhold is playing before calling stream<BR>
file it will be automatically stopped and will not be restarted after<BR>
completion.<BR>
It sets the following channel variables upon completion:<BR>
${PLAYBACKSTATUS}: The status of the playback attempt as a text string.<BR>
    SUCCESS<BR>
    FAILED<BR>
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>control stream file - Sends audio file on channel and allows the listener to control the stream. </B></TH></TR>
<TR><TD ALIGN="CENTER">Send the given file, allowing playback to be controlled by the given digits, if</TD></TR>
<TR><TD ALIGN="CENTER">
any. Use double quotes for the digits if you wish none to be permitted. If<BR>
offsetms is provided then the audio will seek to offsetms before play starts.<BR>
Returns '0' if playback completes without a digit being pressed, or the ASCII<BR>
numerical value of the digit if one was pressed, or '-1' on error or if the<BR>
channel was disconnected. Returns the position where playback was terminated as<BR>
endpos.<BR>
It sets the following channel variables upon completion:<BR>
${CPLAYBACKSTATUS}: Contains the status of the attempt as a text string<BR>
    SUCCESS<BR>
    USERSTOPPED<BR>
    REMOTESTOPPED<BR>
    ERROR<BR>
${CPLAYBACKOFFSET}: Contains the offset in ms into the file where playback was<BR>
at when it stopped. '-1' is end of file.<BR>
${CPLAYBACKSTOPKEY}: If the playback is stopped by the user this variable<BR>
contains the key that was pressed.<BR>
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>tdd mode - Toggles TDD mode (for the deaf). </B></TH></TR>
<TR><TD ALIGN="CENTER">Enable/Disable TDD transmission/reception on a channel. Returns '1' if</TD></TR>
<TR><TD ALIGN="CENTER">
successful, or '0' if channel is not TDD-capable.<BR>
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>verbose - Logs a message to the asterisk verbose log. </B></TH></TR>
<TR><TD ALIGN="CENTER">Sends &lt;message&gt; to the console via verbose message system. &lt;level&gt; is the</TD></TR>
<TR><TD ALIGN="CENTER">
verbose level (1-4). Always returns '1'<BR>
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>wait for digit - Waits for a digit to be pressed. </B></TH></TR>
<TR><TD ALIGN="CENTER">Waits up to &lt;timeout&gt; milliseconds for channel to receive a DTMF digit. Returns</TD></TR>
<TR><TD ALIGN="CENTER">
'-1' on channel failure, '0' if no digit is received in the timeout, or the<BR>
numerical value of the ascii of the digit if one is received. Use '-1' for the<BR>
&lt;timeout&gt; value if you desire the call to block indefinitely.<BR>
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>speech create - Creates a speech object. </B></TH></TR>
<TR><TD ALIGN="CENTER">Create a speech object to be used by the other Speech AGI commands.</TD></TR>
<TR><TD ALIGN="CENTER">
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>speech set - Sets a speech engine setting. </B></TH></TR>
<TR><TD ALIGN="CENTER">Set an engine-specific setting.</TD></TR>
<TR><TD ALIGN="CENTER">
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>speech destroy - Destroys a speech object. </B></TH></TR>
<TR><TD ALIGN="CENTER">Destroy the speech object created by 'SPEECH CREATE'.</TD></TR>
<TR><TD ALIGN="CENTER">
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>speech load grammar - Loads a grammar. </B></TH></TR>
<TR><TD ALIGN="CENTER">Loads the specified grammar as the specified name.</TD></TR>
<TR><TD ALIGN="CENTER">
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>speech unload grammar - Unloads a grammar. </B></TH></TR>
<TR><TD ALIGN="CENTER">Unloads the specified grammar.</TD></TR>
<TR><TD ALIGN="CENTER">
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>speech activate grammar - Activates a grammar. </B></TH></TR>
<TR><TD ALIGN="CENTER">Activates the specified grammar on the speech object.</TD></TR>
<TR><TD ALIGN="CENTER">
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>speech deactivate grammar - Deactivates a grammar. </B></TH></TR>
<TR><TD ALIGN="CENTER">Deactivates the specified grammar on the speech object.</TD></TR>
<TR><TD ALIGN="CENTER">
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>speech recognize - Recognizes speech. </B></TH></TR>
<TR><TD ALIGN="CENTER">Plays back given &lt;prompt&gt; while listening for speech and dtmf.</TD></TR>
<TR><TD ALIGN="CENTER">
</TD></TR>
</TABLE></TD></TR>

<TR><TD><TABLE BORDER="1" CELLPADDING="5" WIDTH="100%">
<TR><TH ALIGN="CENTER"><B>gosub - Cause the channel to execute the specified dialplan subroutine. </B></TH></TR>
<TR><TD ALIGN="CENTER">Cause the channel to execute the specified dialplan subroutine, returning to</TD></TR>
<TR><TD ALIGN="CENTER">
the dialplan with execution of a Return().<BR>
</TD></TR>
</TABLE></TD></TR>

</TABLE>
</BODY>
</HTML>
