सनातन पंचांग — वेबसाइट पैकेज (GitHub Pages के लिए)
=====================================================

फाइलें:
  index.html        ऐप (268 KB, gzip के बाद ~50 KB)
  img/t/00..11.webp हल्की तस्वीरें (सिर्फ एक महीने की लोड होती है, ~32 KB)
  img/h/00..11.webp बड़ी तस्वीरें (सिर्फ शेयर कार्ड बनाते समय)
  sw.js             ऑफलाइन कैश (दूसरी बार खोलने पर तुरंत)
  manifest.json     "Add to Home screen" के लिए
  icon-192/512.png  ऐप आइकन

GitHub Pages पर लगाने के तरीके:
 1) नया repo बनाइए (public), इन सारी फाइलों को root में अपलोड करें
    (index.html repo के सबसे ऊपर होना चाहिए, किसी फोल्डर के अंदर नहीं)
 2) Settings → Pages → Source: "Deploy from a branch" → Branch: main, Folder: / (root) → Save
 3) 1-2 मिनट बाद लिंक मिलेगा: https://<username>.github.io/<repo>/

मोबाइल पर तेज़ चलाने के लिए:
 • GitHub Pages पहली बार खोलने में धीमा हो सकता है। फ्री Cloudflare (custom domain)
   या jsDelivr CDN लगाने से भारत में स्पीड काफी बढ़ती है:
   https://cdn.jsdelivr.net/gh/<user>/<repo>@main/index.html
 • फाइलें छोटी रखें: एक तस्वीर 40 KB से ज्यादा न हो (यहाँ सब 15-35 KB हैं)।
 • index.html में 12 तस्वीरें embed न करें — अलग फाइल रखें (यहाँ वैसा ही है)।
 • sw.js की वजह से दूसरी बार खोलने पर ऐप ऑफलाइन/तुरंत खुलता है।
 • बदलाव करने पर sw.js में CACHE का नाम बदलें (panchang-v1 → v2), वरना पुराना
   कैश दिखता रहेगा।
