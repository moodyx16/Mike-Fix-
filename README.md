# Mike-Fix-
This contains the fix code to run in the terminal. 
**ALWAYS BACKUP BEFORE USING SOME STRANGER'S AI GENERATED CODE. THIS FIX IS FOR MAC USERS ONLY AND WAS TESTED ONLY ON A M3 MACBOOK AIR ON DELTARUNE CHAPTER 4 WITH A STEAM COPY OF DELTARUNE. I DO NOT KNOW IF THIS BREAKS THE OTHER CHAPTERS IN ANY WAY.**

**These are the commands I used to do a brief testing session.**
tccutil reset Microphone (so far as I understand this just resets the microphone permissions for all apps. Did nothing for me. Mostly harmless, mainly an inconvenience.)
ls "$HOME/Library/Application Support/com.apple.TCC/" (showed no output for me, if it does for you then STOP! Your problem is a different one !)
sqlite3 ~/Library/Application\ Support/com.apple.TCC/TCC.db (same thing as above.)

**For the most part these are the only important ones. The latter two are just diagnostic steps. The first is an inconvenience at worst as every app you use that requires the microphone will now ask you for permissions again. 

**THIS IS THE ACTUAL COMMAND-SET SHOWN IN THE VIDEO.**

cd "$HOME/Library/Application Support/Steam/steamapps/common/DELTARUNE"
echo '{"com.apple.security.device.audio-input":true,"com.apple.security.cs.disable-library-validation":true,"com.apple.security.cs.allow-dyld-environment-variables":true}' | plutil -convert xml1 -o /tmp/ent.plist -
codesign --force --deep --options runtime --entitlements /tmp/ent.plist --sign - DELTARUNE.app
tccutil reset Microphone

**AGAIN IF THIS BREAKS TRY VERIFYING YOUR GAME FILES AGAIN!!!**
Thank You.
