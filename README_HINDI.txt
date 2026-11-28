SWACHH SULTANPUR ANDROID APP – NATIVE CAMERA + GPS UPDATE

इस संस्करण में Apps Script का URL, PIN login, Google Sheet, Google Drive और backend को नहीं बदला गया है।

मुख्य सुधार:
1. Open Camera बटन अब Android के native Camera app को सीधे खोलता है। फोटो लेने के बाद उसे छोटा/कॉम्प्रेस करके मौजूदा वेब फॉर्म के PHOTO_DATA में दिया जाता है।
2. Gallery बटन अलग से Gallery खोलता है।
3. GPS बटन अब WebView navigator.geolocation पर निर्भर नहीं है। Android LocationManager से GPS/Network location लेकर मौजूदा फॉर्म के GPS object में lat, lng और accuracy भरता है।
4. Camera photo के लिए FileProvider में Pictures folder का path जोड़ा गया है।
5. Camera और Location की Android runtime permissions जरूरत पड़ने पर माँगी जाती हैं।
6. WebView के onGeolocationPermissionsShowPrompt() में HTTPS वेबसाइट origin को अनुमति दी जाती है; Android runtime permission मिलने के बाद ही callback invoke होता है।

महत्वपूर्ण:
- इस ZIP में Apps Script Code.gs / Index.html या Google Sheet में कोई बदलाव नहीं है।
- Android app वही मौजूदा deployed Apps Script URL खोलता है।
- ZIP source project है; APK इसमें शामिल नहीं है। GitHub Actions से नया APK बनाना होगा।
- इस वातावरण में Android SDK/Gradle build और वास्तविक मोबाइल परीक्षण उपलब्ध नहीं था। इस अपडेट में WebView geolocation prompt handler जोड़ा गया है। फिर भी वास्तविक फोन पर अंतिम परीक्षण जरूरी है; build success या device पर 100% कार्य करने का दावा बिना परीक्षण के नहीं किया जा सकता। GitHub Actions build log की जाँच आवश्यक है।

GitHub upload:
ZIP extract करें। अंदर वाले Swachh-PSSultanpurkota-Android-App-main folder के CONTENTS को repository main branch के root में upload/replace करें। पूरा folder एक अतिरिक्त nested folder के रूप में upload न करें।
