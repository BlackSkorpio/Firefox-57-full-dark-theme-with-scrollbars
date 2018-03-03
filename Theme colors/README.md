<h1>Only the dark theme for firefox</h1>
<p>Following the method described here, you will be able to give dark colors to firefox as shown in the following picture:</p>

<img src="https://i.imgur.com/dmIuudb.png" title="Dark firefox overall UI" />

<h2>Installation</h2>

<p>Most of the job is already done with the userContent.css and userChrome.css files that you have to place in the 
<a href="https://github.com/Izheil/Firefox-57-full-dark-theme-with-scrollbars/tree/master/Theme%20colors#the-chrome-folder">the chrome folder</a> of your firefox profile. For this to work as intended, you should be using a persona (aka lightweight theme) or the default dark theme (The persona used on the screenshot is "<a href="https://addons.mozilla.org/en-US/firefox/addon/deep-dark-blue-forest/">Deek Dark Blue forest</a>" by <b>Sondergaard</b>).</p>
<p>If you would also like a dark version of either <a href="https://addons.mozilla.org/es/firefox/addon/ublock-origin/">Ublock Origin</a>, <a href="https://addons.mozilla.org/es/firefox/addon/flash-video-downloader/">Flash Video Downloader</a>, or <a href="https://addons.mozilla.org/es/firefox/addon/video-downloadhelper/">Video Download Helper</a>, copy the "addons.css" file in your <a href="https://github.com/Izheil/Firefox-57-full-dark-theme-with-scrollbars/tree/master/Theme%20colors#the-chrome-folder">the chrome folder</a> as well.</p>
<p>In case that you just want to change the default scrollbars, you can apply just that without the need
of using the usercontent or userchrome files provided here.</p>

<h4>Step by step:</h4>
<ul>
  <li>Type <code>about:support</code> in your URL bar, then go to that page.</li>
  <li>Click the "open folder" button inside the "profile folder" section.</li>
  <li>Create a folder named "chrome" in your profile folder if it doesn't exist yet.</li>
  <li>Place "usercontent.css" and "userchrome.css" inside the "chrome" folder.</li>
  <li><b>Optional</b>: Follow the method described to change the scrollbars to change the tooltip using the "tooltip.uc.js" file inside the "Scrollbars & tooltips dark theme/profile/" folder in this repository.</li>
  <li><b>Optional</b>: Edit userchrome.css to change any style you aren't fully convinced with (or to give a different style to the unread tabs, etc...).</li>
  <li><b>Optional</b>: If you have <a href="https://addons.mozilla.org/es/firefox/addon/ublock-origin/">Ublock Origin</a> and want the blocked page to be dark as well, edit addons.css (Just follow the instructions commented on top of the file) to have the dynamic url of your ublock extension, and then place it in the "chrome" folder as well.</li>
  <li><b>Optional</b>: If you want a dark version of the <a href="https://addons.mozilla.org/es/firefox/addon/flash-video-downloader/">Flash Video Downloader</a> or <a href="https://addons.mozilla.org/es/firefox/addon/video-downloadhelper/">Video Download Helper</a> extensions, you can also edit the "addons.css" file to update the dynamic URLs of the addons (further explanations inside the "addons.css" file).</li>
</ul>

<h3>The chrome folder</h3>
<p>The fastest way to find it is to just type <code>about:support</code> on the URL bar of your firefox, and then click the <b>open folder</b> button inside the "profile folder" section.</p>
<p>After this, your profile folder will be open. You may or may not see the chrome folder. If you don't see it, just create it and place inside the usercontent.css and userchrome.css files.</p>

<p>If you want to know the exact location for profile folders (information taken from <a href="http://kb.mozillazine.org/Profile_folder_-_Firefox">here</a>):</p>

<h4>On Windows 7 and above, profile folders are in this location, by default:</h4>

<pre>C:\Users\(Windows login/user name)\AppData\Roaming\Mozilla\Firefox\Profiles\(profile folder)</pre>
  
<p>The AppData folder is a hidden folder; to show hidden folders, open a Windows Explorer window and choose "Tools → Folder Options → View (tab) → Show hidden files and folders".</p>

<p>You can also use this path to find the profile folder, even when it is hidden:</p>

<pre>%APPDATA%\Mozilla\Firefox\Profiles\(profile folder)</pre>

<h4>On Linux, profile folders are located in this other location:</h4>

<pre>/home/(Your-username)/.mozilla/firefox/(profile folder)</pre>

<p>The ".mozilla" folder is a hidden folder. To show hidden files in Nautilus (Gnome desktop's default file browser), choose "View -> Show Hidden Files". On others such as Dolphin (Kubuntu's default file browser), you'd have to choose "Control -> Hidden files"</p>

<h4>On Mac, profile folders are in one of these locations:</h4>

<pre>~/Library/Application Support/Firefox/Profiles/(profile folder)
~/Library/Mozilla/Firefox/Profiles/(profile folder)</pre>

<p>The tilde character (~) refers to the current user's Home folder, so ~/Library is the /Macintosh HD/Users/(username)/Library folder. For OS X 10.7 Lion and above, the ~/Library folder is hidden by default.</p>

<p>You can make them visible by typing the following in a terminal window.</p>
<pre>defaults write com.apple.finder AppleShowAllFiles TRUE
killall Finder</pre>
<br /><p>This will also cause any file icons to take on a hazy, 50% alpha look. To restore the old settings (hide the files and make the icons look normal) issue the same commands again, but enter FALSE instead of TRUE.<p>

<h2>The userChrome.css file</h2>

<p>The userchrome file turns dark all context menus, bookmarks, the url bar, the search bar, the main menu, and the toolbar. 
It will, although, not turn dark the extension popups you may have. <p>
<img src="https://i.imgur.com/wWjBcqz.png" title="Dark search menu (spanish)" />
<img src="https://i.imgur.com/7zj3SSq.png" title="Dark context menu (spanish)" />
<p>It will also turn dark the autocomplete popups (mostly a side-effect)</p>
<br />

<h2>The userContent.css file</h2>

<p>The usercontent file will turn dark all the <code>about:about</code> pages.</p>
<img src="https://i.imgur.com/e4zVTC7.png" title="Dark preferences page" /></a>

<p>It will also turn dark the <a href="https://addons.mozilla.org">Mozilla addons page</a>, both the old and the new, the file explorer inside firefox, and the "view source of page" page.</p>