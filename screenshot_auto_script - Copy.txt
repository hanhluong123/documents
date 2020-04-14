:: set path, url variables
SET folder_path=G:\Hanh\LGG - work from home\LGS sites\auto_screenshot
SET chrome_exe_path=c:\Program Files (x86)\Google\Chrome\Application\chrome.exe
SET firefox_exe_path=c:\Program Files\Mozilla Firefox\firefox.exe

:: set urls
SET homepage_url=https://www.logigear.com/
SET why_logigear_url=https://www.logigear.com/why-logigear
SET leave_msg_url=https://www.logigear.com/company/contact-us/leave-a-message

:: set size for Home page on device
SET laptop_home_size=1366,4590
SET ipad_home_size=768,7530
SET iphoneX_home_size=375,8900

:: set size for Why LogiGear page on device
SET laptop_whyLgg_size=1366,2000
SET ipad_whyLgg_size=768,4000
SET iphoneX_whyLgg_size=375,3900

:: set size for Leave A Message on device
SET laptop_leaveMsg_size=1366,3050
SET ipad_leaveMsg_size=768,5100
SET iphoneX_leaveMsg_size=375,5400

:: capture screenshot for homepage
"%chrome_exe_path%" --headless --screenshot="%folder_path%chrome_laptop_homepage.png" --window-size=%laptop_home_size% "%homepage_url%"
"%chrome_exe_path%" --headless --screenshot="%folder_path%chrome_ipad_homepage.png" --window-size=%ipad_home_size% "%homepage_url%"
"%chrome_exe_path%" --headless --screenshot="%folder_path%chrome_iphoneX_homepage.png" --window-size=%iphoneX_home_size% "%homepage_url%"

:: capture screenshot for Why LogiGear
"%chrome_exe_path%" --headless --screenshot="%folder_path%chrome_laptop_whyLgg.png" --window-size=%laptop_whyLgg_size% "%why_logigear_url%"
"%chrome_exe_path%" --headless --screenshot="%folder_path%chrome_ipad_whyLgg.png" --window-size=%ipad_whyLgg_size% "%why_logigear_url%"
"%chrome_exe_path%" --headless --screenshot="%folder_path%chrome_iphoneX_whyLgg.png" --window-size=%iphoneX_whyLgg_size% "%why_logigear_url%"

:: capture screenshot for Leave A Message
"%chrome_exe_path%" --headless --screenshot="%folder_path%chrome_laptop_leaveMsg.png" --window-size=%laptop_leaveMsg_size% "%leave_msg_url%"
"%chrome_exe_path%" --headless --screenshot="%folder_path%chrome_ipad_leaveMsg.png" --window-size=%ipad_leaveMsg_size% "%leave_msg_url%"
"%chrome_exe_path%" --headless --screenshot="%folder_path%chrome_iphoneX_leaveMsg.png" --window-size=%iphoneX_leaveMsg_size% "%leave_msg_url%"

:: capture screenshot on Firefox\firefox
"%firefox_exe_path%" --headless --screenshot="%folder_path%firefox_laptop_homepage.png" "%homepage_url%"
"%firefox_exe_path%" --headless --screenshot="%folder_path%firefox_laptop_whyLgg.png" "%why_logigear_url%"
"%firefox_exe_path%" --headless --screenshot="%folder_path%firefox_laptop_leaveMsg.png" "%leave_msg_url%"

ECHO Completed.
PAUSE