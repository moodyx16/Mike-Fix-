# Mike-Fix-
This contains the fix code to run in the terminal. 
**ALWAYS BACKUP BEFORE USING SOME STRANGER'S AI GENERATED CODE. THIS FIX IS FOR MAC USERS ONLY AND WAS TESTED ONLY ON A M3 MACBOOK AIR ON DELTARUNE CHAPTER 4 WITH A STEAM COPY OF DELTARUNE. I DO NOT KNOW IF THIS BREAKS THE OTHER CHAPTERS IN ANY WAY.**

cd "$HOME/Library/Application Support/Steam/steamapps/common/DELTARUNE"
echo '{"com.apple.security.device.audio-input":true,"com.apple.security.cs.disable-library-validation":true,"com.apple.security.cs.allow-dyld-environment-variables":true}' | plutil -convert xml1 -o /tmp/ent.plist -
codesign --force --deep --options runtime --entitlements /tmp/ent.plist --sign - DELTARUNE.app
tccutil reset Microphone

**AGAIN IF THIS BREAKS TRY VERIFYING YOUR GAME FILES AGAIN!!!**
Thank You.
