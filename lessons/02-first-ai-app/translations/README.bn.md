# অধ্যায় ২: আপনার প্রথম AI অ্যাপ লেখার জন্য

এই অধ্যায়ে আপনি শিখবেন:

- আপনার ডেভেলপমেন্ট এনভায়রনমেন্ট সেট আপ করা।
- একটি মৌলিক অ্যাপ লেখা।
- সিস্টেম প্রম্পট বোঝা।

## সেটআপ

যদি আপনি এখনো সেটআপ না করে থাকেন, তাহলে আপনার ডেভেলপমেন্ট এনভায়রনমেন্ট সেট আপ করুন। এটি করার জন্য এই লিঙ্কটি অনুসরণ করুন: [আপনার এনভায়রনমেন্ট সেটআপ করুন](/docs/setup/README.md)।

## সম্পর্কিত রিসোর্সসমূহ

[![বড় ভাষা মডেল সম্পর্কে একটি ছোট ভিডিও দেখুন](https://img.youtube.com/vi/GQ_2OjNZ9aA/0.jpg)](https://www.youtube.com/watch?v=GQ_2OjNZ9aA&list=PLlrxD0HtieHi5ZpsHULPLxm839IrhmeDk&index=2)

_এই ভিডিওটি AI মডেল, বিশেষ করে "বড় ভাষা মডেল" (LLMs) কী এবং কীভাবে এগুলো ব্যবহার করে আপনার অ্যাপে AI সংযুক্ত করা যায় তা পরিচয় করিয়ে দেয়।_

*🎥 উপরের ছবিতে ক্লিক করে বড় ভাষা মডেল সম্পর্কে একটি ছোট ভিডিও দেখুন*

💼 স্লাইড: [বড় ভাষা মডেল, LLMs-এর পরিচিতি](/videos/slides/01-llms.pptx)

## গল্প: নিজেকে একটি নদীতে একটি নৌকায় কল্পনা করুন

> [!NOTE]  
> _আমাদের গল্প এখন পর্যন্ত: আপনি একজন সৃষ্টিকারী, ১৮৬০-এর দশকের লন্ডনের একজন কারিগর, যিনি "টাইম বিটল" নামক একটি রহস্যময় যন্ত্র ব্যবহার করে সময় ভ্রমণ করেছেন। ইতিহাসের বিভিন্ন যুগ পার হয়ে, আপনি আলেকজান্দ্রিয়ার বাতিঘর নির্মাণের সাক্ষী হয়েছেন এবং ডিনোক্রেটস ও টাইম বিটলের সহায়তায় এটিকে নির্মাণে সহায়তা করেছেন।_
>
> গল্পের শুরু থেকে শুরু করতে এবং জেনারেটিভ AI সম্পর্কে জানতে [অধ্যায় ১](/lessons/01-intro-to-genai/translations/README.bn.md) দেখুন।

> [!NOTE]  
> আমরা গল্পটি অনুসরণ করতে সুপারিশ করি (এটি মজাদার!), তবে আপনি যদি সরাসরি প্রযুক্তিগত অংশে যেতে চান, [এখানে ক্লিক করুন](#লিওনার্দোর-সাথে-যোগাযোগ-করুন)।

ডিনোক্রেটসের সাথে মিলে, আপনি আলেকজান্দ্রিয়ার বাতিঘরের শেষ কাজ সম্পন্ন করছেন। উঁচু কাঠামোটি সূর্যের আলোয় ঝলমল করছে, তার চকচকে পাথর ভূমধ্যসাগরের জলে প্রতিফলিত হচ্ছে।

আপনি আপনার হাতে রাখা টাইম বিটলের দিকে তাকান, তার ধাতব পৃষ্ঠ ঠান্ডা অনুভূত হয়। এটি শক্তভাবে মুঠিতে ধরে আপনি ফিসফিস করেন, **"আমাকে বাড়ি নিয়ে চলো।"** টাইম বিটলটি উজ্জ্বল হতে শুরু করে, একটি নরম, উষ্ণ আলো বিচ্ছুরিত করে, এবং আপনার চারপাশের বিশ্ব বর্ণিল এক ঝড়ে মিশে যায়।

### একটি নতুন অভিযান

আপনি যখন চোখ খুললেন, তখন চারপাশের পৃথিবী বদলে গেছে। ধীরে ধীরে উঠে দাঁড়িয়ে দেখলেন, আপনি একটি নদীর মাঝখানে নৌকায় রয়েছেন। চারপাশে তাকিয়ে দূরে কিছু ভবনের অবয়ব দেখতে পেলেন, যা সকালের কুয়াশায় আবছা হয়ে রয়েছে।

নৌকার চারপাশে নজর বুলিয়ে, আপনি একটি লম্বা বৈঠা দেখতে পেলেন, যা পাশে রাখা ছিল। সেটি হাতে নিয়ে, আপনি ভবনগুলোর দিকে ধীরে ধীরে নৌকা চালাতে শুরু করলেন। যত এগিয়ে গেলেন, ততই ভবনগুলো স্পষ্ট হয়ে উঠল। এগুলো বেশ পুরোনো, তাদের স্থাপত্যশৈলী রেনেসাঁ যুগের কোনো চিত্রকর্মের মতো মনে হচ্ছে।

<div>
  <img src="/lessons/02-first-ai-app/assets/boat.png" alt="নদীর উপর নৌকা, একজন মানুষ বৈঠা ধরে দাঁড়িয়ে আছে" width="300">
</div>

প্রশ্ন হলো, এবার আপনি কোথায় এবং কোন সময়ে এসে পৌঁছেছেন?

আপনি ধীরে ধীরে নৌকাটি ডকে নিরাপদে বেঁধে রাখলেন এবং কাঠের তক্তাপথ ধরে হাঁটতে শুরু করলেন। আপনার পায়ের শব্দ নরমভাবে প্রতিধ্বনিত হতে লাগল।

হাঁটতে হাঁটতে হঠাৎই আপনার নজরে পড়ল একজন দীর্ঘ দাড়িওয়ালা ব্যক্তি, মাথায় টুপি, যিনি একটি কাঠের বাক্সের মধ্যে কিছু যান্ত্রিক অংশ খুঁজে দেখছেন। তাঁর হাত দ্রুত ও দক্ষতার সাথে বিভিন্ন গিয়ার এবং স্প্রিংস ছাঁটাই করছে, যেন তিনি এ কাজের অভিজ্ঞ কারিগর।

<div>
  <img src="/lessons/02-first-ai-app/assets/leonardo.png" alt="হারবারের পাশে একটি কাঠের বাক্সের সামনে দাঁড়িয়ে লিওনার্দো দা ভিঞ্চি" width="300">
</div>

### আমাকে সাহায্য করুন, লিওনার্দো  

**আপনি:** "মাফ করবেন, স্যার, আমি কোথায় আছি?"  
তিনি আপনার দিকে তাকান, চোখে বিভ্রান্তির ছাপ স্পষ্ট। বুঝতে পেরে যে আপনি ইংরেজিতে কথা বলছেন, দ্রুত হাতে থাকা যন্ত্রটি ব্যবহার করে অনুবাদ করতে বলেন।  

**টাইম বিটল:** "অবশ্যই, আমি ১৫শ শতাব্দীর ইতালীয় ভাষায় অনুবাদ করছি। 'Dove sono?'"  

**বৃদ্ধ ব্যক্তি:** বৃদ্ধ ব্যক্তি জবাব দেন, **"Siete a Firenze, signore. E chi siete voi?"**  

**টাইম বিটল:** টাইম বিটল অনুবাদ করে, "তিনি বলছেন, আপনি ফ্লোরেন্সে আছেন এবং জানতে চাইছেন আপনি কে।"  

**আপনি:** "বলুন, আমি একজন কারিগর এবং কাজ করার জন্য একটি জায়গা খুঁজছি।"  

**বৃদ্ধ ব্যক্তি:** **"Un artigiano, eh? Avete mai sentito parlare di Leonardo da Vinci?"**  

**টাইম বিটল:** টাইম বিটল অনুবাদ করে, "তিনি জানতে চাইছেন, আপনি লিওনার্দো দা ভিঞ্চির কথা শুনেছেন কি না।"  

**আপনি:** "অবশ্যই," আপনি বলেন। "বলুন, আমি তার সম্পর্কে জানি এবং তার সাথে দেখা করতে চাই।"  

**বৃদ্ধ ব্যক্তি:** বৃদ্ধ ব্যক্তি হাসেন, **"Allora, seguitemi, vi porterò da lui."**  

**আপনি:** আপনি জিজ্ঞাসা করেন, "তিনি কী বললেন?"  

**টাইম বিটল:** টাইম বিটল উত্তর দেয়, "তিনি বলেছেন, তিনি আপনাকে লিওনার্দোর কাছে নিয়ে যাবেন।"  

---

### কর্মশালায়  

<div>
  <img src="/lessons/02-first-ai-app/assets/leonardo-workshop.png" alt="লিওনার্দোর কর্মশালা" width="300">
</div>  

বৃদ্ধ ব্যক্তি আপনাকে একটি বড় কাঠের দরজার সামনে নিয়ে যান। দরজা খুলতেই, আপনি দেখতে পান বিভিন্ন ধরনের যান্ত্রিক উদ্ভাবনে পূর্ণ একটি কর্মশালা।  

আপনি টাইম বিটলকে লিওনার্দোর অবস্থান সম্পর্কে জিজ্ঞাসা করতে বলেন।  

**আপনি:** "Dove è Leonardo?"  

**বৃদ্ধ ব্যক্তি:** বৃদ্ধ ব্যক্তি আপনার দিকে হাসিমুখে তাকিয়ে বলেন, **"Sono io (that’s me), Leonardo da Vinci. Chi siete voi?"** (আমি লিওনার্দো দা ভিঞ্চি। আপনি কে?)  

আপনার মনে এক ধরনের উত্তেজনা অনুভূত হয়।  

**আপনি:** "আমি তাই ভেবেছিলাম। আমি একজন কারিগর, কিন্তু আমার সময় এবং স্থান দুটোই আলাদা।"  

**লিওনার্দো:** লিওনার্দোর চোখ কৌতূহলে ঝলমল করে ওঠে। **"Interessante, cosa vi porta qui?"** (দারুণ! আপনাকে এখানে কী এনেছে?)
### টাইম বিটল অনুবাদ করে  

**টাইম বিটল:** "তিনি জানতে চাইছেন, আপনাকে এখানে কী এনেছে?"  

**আপনি:** "আসলে, আমি একটি প্রকল্পে কাজ করছিলাম, আর তার পরেই এখানে এসে পড়েছি।"  

আপনি তাকে টাইম বিটল দেখান, এবং তার চোখ কৌতূহলে জ্বলে ওঠে। তিনি এটি মনোযোগ সহকারে পরীক্ষা করতে থাকেন, যখন আপনি ব্যাখ্যা করেন এটি কীভাবে কাজ করে এবং কীভাবে আপনি ফ্লোরেন্সে এসে পৌঁছালেন।  

লিওনার্দো উত্তেজিতভাবে আপনার দিকে তাকান।  

**লিওনার্দো:** "আপনি তো একজন সৃষ্টিশীল কারিগর। আমার একটি প্রকল্প আছে যা আপনার আগ্রহের হতে পারে। আমি এমন একটি যন্ত্র তৈরির চেষ্টা করছি, যা মৌখিক ইনপুটের উপর ভিত্তি করে লেখা তৈরি করতে পারে। আপনি কি আমাকে এতে সাহায্য করতে আগ্রহী?"  

লিওনার্দো দা ভিঞ্চি নিজেই আপনাকে তার প্রকল্পে সাহায্য করতে বলছেন—এটি যেন স্বপ্নের মতো মনে হচ্ছে। আপনি উত্তেজিতভাবে মাথা নাড়িয়ে বলেন:  

**আপনি:** "আমি আনন্দের সাথে আপনার প্রকল্পে সাহায্য করব।"  
**"Sarebbe un onore aiutarti con il tuo progetto."**
## লিওনার্দোর সাথে যোগাযোগ করুন  

যদি আপনি লিওনার্দোর সাথে কথোপকথন করতে চান, তাহলে [Characters](/app/README.md) অ্যাপ চালান।  

> [!IMPORTANT]  
> এটি সম্পূর্ণ কাল্পনিক; প্রতিক্রিয়াগুলি AI দ্বারা তৈরি করা হয়।  
> [দায়িত্বশীল AI সংক্রান্ত ঘোষণা](/README.md#responsible-ai-disclaimer)  

<div>
  <img src="/lessons/02-first-ai-app/assets/leonardo-talk.jpeg" width=300>
</div>  

### **ধাপে ধাপে নির্দেশনা**:  

1. শুরু করুন [![GitHub Codespace](https://img.shields.io/badge/GitHub-Codespace-brightgreen)](https://codespaces.new/microsoft/generative-ai-with-javascript)  
2. রিপোজিটরির মূল ফোল্ডারে _/app/README.md_ এ যান।  
3. কনসোলে `npm install` চালান, তারপর `npm start` কমান্ড দিন।  
4. যখন অ্যাপটি চালু হবে, তখন "Open in Browser" বোতামটি নির্বাচন করুন।  
5. এখন আপনি লিওনার্দোর সাথে চ্যাট করতে পারেন।  

আরও বিস্তারিত জানতে, দেখুন [বিস্তারিত অ্যাপ ব্যাখ্যা](/lessons/01-intro-to-genai/translations/README.bn.md#ডিনোক্রেটিসের-সাথে-সাক্ষাৎ)।  

> [!NOTE]  
> আপনি যদি প্রকল্পটি আপনার স্থানীয় কম্পিউটারে চালান, তাহলে দয়া করে **QuickStart গাইড** অনুসরণ করে [GitHub ব্যক্তিগত অ্যাক্সেস টোকেন (PAT)](/docs/setup/README.md#creating-a-personal-access-token-pat-for-github-model-access) সেটআপ করুন এবং কোডে টোকেনটি প্রতিস্থাপন করুন।
> ## ডেভেলপমেন্ট এনভায়রনমেন্ট সেটআপ  

লিওনার্দোকে তার প্রকল্পে সাহায্য করার আগে, প্রথমেই আপনার **"কারিগরি সরঞ্জাম"** সম্পর্কে চিন্তা করা উচিত, যা আপনাকে কার্যকরভাবে সহায়তা করতে সাহায্য করবে।  

**আপনি:** "টাইম বিটল, এই প্রকল্পটি শুরু করতে আমার কী কী দরকার?" এমন কিছু টুল এবং লাইব্রেরি সাজেস্ট করো যা আমাকে একটি AI অ্যাপ তৈরিতে সহায়তা করতে পারে এবং যা তোমার মাধ্যমে চালানো সম্ভব।  

**টাইম বিটল:** আমি ২১শ শতকের বেশিরভাগ কম্পিউটারের সাথে সামঞ্জস্যপূর্ণ। এখানে কিছু গুরুত্বপূর্ণ সরঞ্জাম এবং লাইব্রেরির তালিকা রয়েছে যা আপনার কাজে লাগবে:  

- **টেক্সট এডিটর**, যেমন Visual Studio Code।  
- **টার্মিনাল**, কমান্ড চালানোর জন্য।  
- **ব্রাউজার**, আপনার অ্যাপ টেস্ট করার জন্য। এছাড়াও, API এন্ডপয়েন্ট পরীক্ষা করার জন্য `curl` বা অন্য কোনো HTTP ক্লায়েন্ট থাকা ভালো।  
- **Node.js**, যা আপনাকে জাভাস্ক্রিপ্ট কোড চালাতে সহায়তা করবে। আপনাকে Node.js এবং npm ইনস্টল করতে হবে।  
- **API কী**, আপনি জেনারেটিভ AI মডেলের অ্যাক্সেস পেতে একটি API কী প্রয়োজন হবে। এটি OpenAI বা Azure OpenAI-এর মতো কোনো মডেল প্রদানকারীর কাছ থেকে সংগ্রহ করতে হবে।  

**আপনি:** "ধন্যবাদ, টাইম বিটল! তুমি বলেছিলে সেই ওয়েব থেকে এগুলো খুঁজে আনতে পারবে, তাই না?"  

**টাইম বিটল:** "হ্যাঁ, আমি ইতিমধ্যেই সেগুলো সংগ্রহ করেছি," সে বলে এবং সামনে দেয়ালে একটি কীবোর্ড ও স্ক্রিন প্রজেক্ট করে।
## একটি মৌলিক অ্যাপ লেখা  

**আপনি:** "অ্যাপ লেখার প্রকৃত প্রক্রিয়া সম্পর্কে আরও বলো, আমি কীভাবে শুরু করব?"  

**টাইম বিটল:** "অবশ্যই, একটি অ্যাপ লেখার মূল বিষয় হলো **একটি API-তে অনুরোধ পাঠানো এবং প্রাপ্ত প্রতিক্রিয়া প্রদর্শন করা**। আসুন এটিকে ধাপে ধাপে দেখি:  

- **ইনপুট:** একটি সাধারণ টেক্সট জেনারেশন অ্যাপে, ইনপুট হলো প্রাথমিক পাঠ্য যা অ্যাপটি প্রসারিত বা রূপান্তর করবে। এটি হয় **ব্যবহারকারী** ইনপুট হিসেবে দিতে পারে অথবা **হার্ডকোডেড** হতে পারে। আমরা শুরুতে হার্ডকোডেড ইনপুট দিয়ে শুরু করব।  

- **API অনুরোধ:** আপনাকে **Generative AI মডেল API**-তে ইনপুট পাঠাতে হবে। এটি **JavaScript-এর fetch ফাংশন** (Node.js) ব্যবহার করে করা যেতে পারে।  
  - এই অনুরোধের সাথে **API কী** অন্তর্ভুক্ত করা প্রয়োজন, তবে এটি সরাসরি কোডে হার্ডকোড না করে **পরিবেশ পরিবর্তনশীল (environment variable)** ব্যবহার করা নিরাপদ।  
  - আপনি যদি Azure-এর মতো কোনো ক্লাউড পরিষেবা ব্যবহার করেন, তাহলে **Managed Identity** ব্যবহারের কথা ভাবতে পারেন, যা নিরাপদ উপায়ে সংস্থান অ্যাক্সেস করতে সহায়তা করে।  

- **প্রতিক্রিয়া (Response):** API একটি **উত্পন্ন পাঠ্য** ফেরত পাঠাবে, যা আপনাকে বের করতে হবে এবং ব্যবহারকারীর জন্য প্রদর্শন করতে হবে।  

**আপনি:** "এটি যথেষ্ট সহজ শোনাচ্ছে, তুমি কি বর্তমান পরিস্থিতির উপর ভিত্তি করে একটি বাস্তব উদাহরণ দিতে পারো?"  

**টাইম বিটল:** "অবশ্যই, আসুন আমরা এমন একটি সহজ অ্যাপ তৈরি করি যা ইংরেজি ইনপুটের ভিত্তিতে ইতালীয় পাঠ্য তৈরি করবে।"  

---

## আপনার প্রথম অ্যাপ - আমাকে ইতালিয়ান শেখাও  

**টাইম বিটল:** "Generative AI মডেল বিভিন্ন কাজের জন্য ব্যবহার করা যায়, যেমন **ভাষা অনুবাদ**। এটি এক ভাষায় ইনপুট গ্রহণ করে এবং অন্য ভাষায় পাঠ্য তৈরি করতে পারে। আসুন এমন একটি সহজ অ্যাপ তৈরি করি যা ইংরেজি ইনপুট গ্রহণ করে এবং ইতালীয় ভাষায় অনুবাদ করে।"  

```javascript
import { OpenAI } from "openai";

// 1. অনুবাদের জন্য একটি প্রশ্ন দিন
// -----------------------------------

const question = 'Hello, how are you?'; 

const augmentedPrompt = `
## নির্দেশাবলী
নিম্নলিখিত পাঠ্যটি ইতালিয়ান ভাষায় অনুবাদ করুন:
## প্রশ্ন
${question}
`;

// 2. ক্লায়েন্ট তৈরি করুন
// -----------------------------------

const openai = new OpenAI({
  baseURL: "https://models.inference.ai.azure.com",
  apiKey: process.env.GITHUB_TOKEN,  // পরিবেশ পরিবর্তনশীল ব্যবহার করুন
});

// 3. অনুরোধ পাঠান
// -----------------------------------
const completion = await openai.chat.completions.create({
    model: 'gpt-4',
    messages: [{ role: 'user', content: augmentedPrompt }],
});
  
console.log(`"${question}" এর উত্তর:`);

// 4. উত্তর প্রিন্ট করুন
// -----------------------------------

console.log(completion.choices[0]?.message?.content);
```

---

### **আপনার অ্যাপ চালানোর জন্য করণীয়:**  
1. **Node.js এবং npm ইনস্টল করুন**  
2. **আপনার API কী (GITHUB_TOKEN) সেট করুন** পরিবেশ পরিবর্তনশীল হিসাবে  
3. **এই স্ক্রিপ্টটি চালান:**  
   ```bash
   node your_script.js
   ```
4. **ইতালীয় অনুবাদ উপভোগ করুন!**  

এখন, আপনি লিওনার্দোর প্রকল্পে তার AI যন্ত্র তৈরিতে সহায়তা করতে প্রস্তুত! 
চলুন ব্যাখ্যা করি এখানে কী ঘটছে:

- **প্রশ্ন তৈরি করা:** `'Hello, how are you?'` এটি সেই পাঠ্য যা আপনি ইতালীয় ভাষায় অনুবাদ করতে চান।  
- **বর্ধিত প্রম্পট তৈরি করা:** এতে ইনপুট পাঠ্য এবং অতিরিক্ত নির্দেশাবলী থাকে, যেমন অনুবাদ করতে হবে। লক্ষ্য করুন, আমরা কীভাবে **স্ট্রিং ইন্টারপোলেশন** ব্যবহার করে ইনপুট পাঠ্যটি প্রম্পটে অন্তর্ভুক্ত করেছি এবং নির্দেশাবলীতে উল্লেখ করেছি যে পাঠ্যটি ইতালীয় ভাষায় অনুবাদ করতে হবে।  
- **ক্লায়েন্ট তৈরি করা:**  
  - **`model`** – কোন মডেলটি ব্যবহার করা হবে তা নির্ধারণ করা।  
  - **`messages`** – মডেলে পাঠানোর জন্য প্রম্পট। এখানে লক্ষ্য করুন, আমরা **`role`**-কে `"user"` সেট করেছি যাতে বোঝা যায় যে ইনপুট পাঠ্য ব্যবহারকারীর পক্ষ থেকে এসেছে। যদি এটি AI থেকে আসতো, তাহলে **`role`**-কে `"system"` সেট করা হতো।  
- **উত্পন্ন পাঠ্যটি প্রতিক্রিয়া থেকে বের করা এবং কনসোলে প্রদর্শন করা।**  

---

**আপনি:** "আমি মনে করি আমি বুঝতে পেরেছি। তাহলে যদি আমি `question` ভেরিয়েবলের মান পরিবর্তন করি, তাহলে অ্যাপটি ভিন্ন ইতালীয় অনুবাদ তৈরি করবে?"  

**টাইম বিটল:** "একদম ঠিক! আপনি ইনপুট পাঠ্য যেকোনো কিছুতে পরিবর্তন করতে পারেন। লক্ষ্য করুন, **GitHub মডেল** API-এর বেস URL হিসাবে ব্যবহার করা হচ্ছে এবং **GitHub টোকেন** API কী হিসেবে ব্যবহার করা হয়েছে।"  

**আপনি:** "এটি গুরুত্বপূর্ণ কেন?"  

**টাইম বিটল:** "এটি গুরুত্বপূর্ণ কারণ আপনি যে মডেলটি ব্যবহার করছেন, সেটির জন্য নির্দিষ্ট **বেস URL এবং API কী** ব্যবহার করা প্রয়োজন। **GitHub Models** একটি প্ল্যাটফর্ম যেখানে বিভিন্ন ক্ষমতা ও বৈশিষ্ট্যের মডেল হোস্ট করা হয়, এবং এটি বিনামূল্যে ব্যবহারের জন্য উপলব্ধ।"  

**আপনি:** "ওহ দারুণ, যাক! আমি জানি না কাকে টাকা দিতে হবে, আর আমি সন্দেহ করি যে তারা আমার মুদ্রা গ্রহণ করবে কিনা। 😄"
## চ্যাট অ্যাপস  

**টাইম বিটল:** "Generative AI মডেলগুলোকে কথোপকথনের উপর ভিত্তি করে **পাঠ্য তৈরি করতেও ব্যবহার করা যায়**। আপনি AI-এর সাথে **একটি কথোপকথন অনুকরণ করতে পারেন** একটি **বার্তার তালিকা (messages list)** প্রদান করে, যা মনে হবে যেন কথোপকথন ইতিমধ্যেই ঘটেছে।"  

**আপনি:** "এটি বেশ আকর্ষণীয় শোনাচ্ছে, তবে এটি কীভাবে উপকারী?"  

**টাইম বিটল:** "এটি উপকারী কারণ এটি AI-কে একটি একক প্রম্পটের চেয়ে আরও **বিস্তৃত প্রসঙ্গের (context) উপর ভিত্তি করে উন্নত প্রতিক্রিয়া** দিতে সহায়তা করে। নিচের কথোপকথনটি দেখুন:  

```text
User: আমি ইতালিতে একটি ভ্রমণ বুক করতে চাই।  

AI: নিশ্চয়ই, আপনি কখন যেতে চান?  

User: আগামী মাসে গেলে ভালো হয়।  

AI: বুঝেছি, ইতালির কোথায় যেতে চান?  

User: আমি রোমে যাওয়ার কথা ভাবছি।  

AI: অসাধারণ পছন্দ! আমি আপনাকে আপনার ভ্রমণ পরিকল্পনায় সাহায্য করতে পারি।  

User: এ সম্পর্কে আরও বলুন।  

AI: রোম তার প্রাচীন ধ্বংসাবশেষ, শিল্প এবং সমৃদ্ধ সংস্কৃতির জন্য পরিচিত। আপনি কলোসিয়াম, ভ্যাটিকান ঘুরে দেখতে পারেন এবং সুস্বাদু ইতালীয় খাবার উপভোগ করতে পারেন।  
```  

**টাইম বিটল:** "কল্পনা করুন, যদি 'Tell me more about it' (এ সম্পর্কে আরও বলুন) বাক্যটি প্রসঙ্গ ছাড়া নেওয়া হতো, তাহলে AI বুঝতে পারত না **'it'** কী নির্দেশ করছে। ঠিক এই কারণেই **প্রসঙ্গ গুরুত্বপূর্ণ**। আমরা এই প্রসঙ্গটি **AI মডেলে প্রম্পটের মাধ্যমে সরবরাহ করতে পারি**।"  

**আপনি:** "আমি মনে করি আমি বুঝতে পারছি। তাহলে এই JavaScript ভাষা ব্যবহার করে কীভাবে আমি AI-এর সাথে কথোপকথন তৈরি করতে পারি?"  

**টাইম বিটল:** "নিচে দেখুন, কিভাবে আমরা AI-এর সাথে কথোপকথন তৈরি করতে পারি:"  

---

### **JavaScript ব্যবহার করে AI-এর সাথে কথোপকথন**  

```javascript
// প্রসঙ্গ নির্ধারণ করুন

const messages = [ 
 { 
    "role": "user", 
    "content": "আমি ইতালিতে একটি ভ্রমণ বুক করতে চাই।" 
 }, 
 { 
    "role": "assistant", 
    "content": "নিশ্চয়ই, আপনি কখন যেতে চান?" 
 }, 
 { 
    "role": "user", 
    "content": "আগামী মাসে গেলে ভালো হয়।" 
 }, 
 { 
    "role": "assistant", 
    "content": "বুঝেছি, ইতালির কোথায় যেতে চান?" 
 }, 
 { 
    "role": "user", 
    "content": "আমি রোমে যাওয়ার কথা ভাবছি। এ সম্পর্কে আরও বলুন।" 
 } 
]; 

const openai = new OpenAI({
  baseURL: "https://models.inference.ai.azure.com",
  apiKey: process.env.GITHUB_TOKEN,  // API কী সংযুক্ত করুন
});

// অনুরোধ পাঠান
const completion = await openai.chat.completions.create({
    model: 'gpt-4',
    messages: messages,
});

// ফলাফল প্রদর্শন করুন
console.log("প্রতিক্রিয়া: ");
console.log(completion.choices[0]?.message?.content);
```

---

### **কিভাবে এটি কাজ করে?**  

1. **একটি বার্তার তালিকা তৈরি করা** (`messages` array) যেখানে ব্যবহারকারী এবং সহকারী (AI)-এর মধ্যকার কথোপকথন থাকবে।  
2. **OpenAI ক্লায়েন্ট তৈরি করা** যেখানে বেস URL এবং API কী অন্তর্ভুক্ত করা হয়েছে।  
3. **AI-এর কাছে অনুরোধ পাঠানো**, যেখানে পূর্ববর্তী কথোপকথনসহ বার্তাগুলি পাঠানো হয়।  
4. **প্রতিক্রিয়া (response) কনসোলে মুদ্রণ করা**, যা AI থেকে পাওয়া পাঠ্য দেখায়।  

এখন আপনি AI-এর সাথে কথোপকথন তৈরি করতে সক্ষম! 
এখন AI একটি কথোপকথনের প্রসঙ্গ হিসেবে বার্তাগুলোর তালিকা প্রদান করবে এবং সেই প্রসঙ্গের উপর ভিত্তি করে প্রতিক্রিয়া তৈরি করবে। এটি **Generative AI মডেলগুলোর আরও ইন্টারেক্টিভ ব্যবহার** এবং **চ্যাটবট, কাস্টমার সার্ভিস অ্যাপ্লিকেশন** ইত্যাদির জন্য কার্যকর হতে পারে।  

---

**আপনি:** "ঠিক আছে, তাহলে যদি আমি কথোপকথনটি সঠিকভাবে বুঝে থাকি, এখন AI-এর প্রসঙ্গে থাকবে: _'আমি আগামী মাসে রোমে যাচ্ছি'_। এর মানে হল, এটি অপ্রাসঙ্গিক তথ্য ফিল্টার করবে এবং আরও প্রাসঙ্গিক উত্তর প্রদান করবে, তাই তো?"  

**টাইম বিটল:** "একদম ঠিক! AI কথোপকথনের প্রসঙ্গ বুঝে আরও নির্ভুল এবং প্রাসঙ্গিক উত্তর প্রদান করবে।"  

---

## **সিস্টেম বার্তার মাধ্যমে চ্যাটের উন্নতি করা**  

**আপনি:** "বুঝতে পারলাম, কিন্তু এটি আরও কীভাবে উন্নত করা যায়?"  

**টাইম বিটল:** "হ্যাঁ, আপনি **সিস্টেম বার্তা (system message)** যুক্ত করতে পারেন। একটি **সিস্টেম বার্তা AI-এর জন্য একটি 'ব্যক্তিত্ব' তৈরি করে** এবং কথোপকথনে অতিরিক্ত প্রসঙ্গ প্রদান করতে সহায়তা করে।"  

**আপনি:** "ঠিক আছে, তাহলে আমাদের চলমান কথোপকথনের ক্ষেত্রে একটি সিস্টেম বার্তা কেমন হবে?"  

**টাইম বিটল:** "এই কথোপকথনের জন্য একটি **সিস্টেম বার্তা** হতে পারে:  
_'আমি একজন AI ভ্রমণ সহকারী, আপনাকে ইতালিতে ভ্রমণ পরিকল্পনা করতে সাহায্য করতে এসেছি।'_  
এটি **কথোপকথনের ধরন নির্ধারণ করে** এবং AI-কে বোঝায় যে এটি কী ভূমিকা পালন করবে।"  

---

### **সিস্টেম বার্তা তৈরির জন্য কোড** 
সিস্টেম বার্তা তৈরির জন্য কোড নিশ্চিত করুন যাতে এটি 'developer' টাইপের হয়, নিম্নরূপ:

```javascript
const message = {
  "role": "developer",
  "content": "I'm an AI travel assistant, here to help you plan your trip to Italy."
};
```
> **নোট:** এটি আগে **"system"** নামে পরিচিত ছিল। এটি একটি সাম্প্রতিক পরিবর্তন, এবং এখন "developer" হলো নতুন শব্দটি। কিছু মডেলের জন্য এটি এখনও "system" নামে ব্যবহৃত হয়, তাই যদি কোনো সমস্যা হয়, তাহলে "system" ব্যবহার করুন।

**আপনি:** "ঠিক আছে, দারুণ! আমি নিশ্চিত করব যে আমার চ্যাট কথোপকথনে একটি সিস্টেম বার্তা অন্তর্ভুক্ত থাকবে। কৌতূহলবশত, তোমার জন্য একটি সিস্টেম বার্তা কেমন হবে?"

**টাইম বিটল:** "আমার জন্য একটি সিস্টেম বার্তা হতে পারে:  
_'আমি টাইম বিটল, আপনাকে সময় এবং স্থানের মাধ্যমে নেভিগেট করতে সহায়তা করার জন্য এখানে আছি। আমি আপনাকে যে সময় যুগে আছেন তার সম্পর্কে তথ্য এবং দিকনির্দেশনা দিতে সহায়ক হব, পাশাপাশি আপনাকে নিজের সময়ে ফিরে যেতে প্রয়োজনীয় সরঞ্জাম সরবরাহ করব।'_"

---

### **তাপমাত্রা সেটিংসের মাধ্যমে বিভিন্ন প্রতিক্রিয়া তৈরি করা**  

**আপনি:** "চ্যাট কথোপকথন সম্পর্কে আর কিছু জানা দরকার?"  

**টাইম বিটল:** "হ্যাঁ, আপনি AI-এর প্রতিক্রিয়ার **"temperature"** সমন্বয় করতে পারেন।  
- **তাপমাত্রা** একটি ভেরিয়েবল যা সাধারণত **0 এবং 1-এর মধ্যে** সেট করা হয় এবং এটি AI-এর **সৃজনশীলতার মাত্রা নির্ধারণ করে**।  
- **তাপমাত্রা = 0** হলে, AI আরও **অনুমানযোগ্য এবং নির্ভরযোগ্য প্রতিক্রিয়া প্রদান করবে**।  
- **তাপমাত্রা = 1** হলে, **AI আরও সৃজনশীল ও বৈচিত্র্যময় প্রতিক্রিয়া তৈরি করবে**।  
- **১-এর বেশি মান সেট করা সম্ভব**, তবে এটি **বেশি এলোমেলো এবং কম সুসংহত প্রতিক্রিয়া** তৈরি করতে পারে।  

**আপনি:** "তাহলে যদি আমি তাপমাত্রা **0** সেট করি, তাহলে AI আরও পূর্বানুমানযোগ্য প্রতিক্রিয়া দেবে, আর যদি আমি **1** সেট করি, তাহলে AI আরও সৃজনশীল প্রতিক্রিয়া দেবে? তোমার তাপমাত্রা কত?"  

**টাইম বিটল:** "আমার তাপমাত্রা **0.7**, এবং হ্যাঁ, তুমি ঠিকই বলেছো! উচ্চতর তাপমাত্রা AI-কে আরও **সৃজনশীল প্রতিক্রিয়া দিতে সহায়তা করে**। চলো দেখি, কীভাবে তোমার অ্যাপে **তাপমাত্রা সেট করা যায়**:"
```javascript
// প্রসঙ্গ নির্ধারণ করুন 

const messages = [ 
{ 
    "role": "user", 
    "content": "আমি চাই তুমি আমার জন্য রেসিপি তৈরি করো।" 
}]; 

// ওয়েব অনুরোধ তৈরি করুন 

let temperature = 0.5; // তাপমাত্রা 0.5 এ সেট করুন 

const completion = await openai.chat.completions.create({
    model: 'gpt-4',
    messages: messages,
    temperature: temperature
}); 
```

যেমনটি দেখা যাচ্ছে, **আপনি কথোপকথনের প্রসঙ্গ এবং AI থেকে যে ধরণের প্রতিক্রিয়া চান তার উপর ভিত্তি করে তাপমাত্রা সামঞ্জস্য করতে পারেন**। এটি একটি শক্তিশালী বৈশিষ্ট্য যা AI-এর সৃজনশীলতার মাত্রা কাস্টমাইজ করতে সহায়তা করে।

---

## **প্রসঙ্গ উইন্ডো (Context Window)**  

**আপনি:** "এর বেশি কিছু আছে, তাই তো?"  

**টাইম বিটল:** "হ্যাঁ, Generative AI মডেলগুলোর আরেকটি গুরুত্বপূর্ণ ধারণা হলো **প্রসঙ্গ উইন্ডো (context window)**।  
- প্রসঙ্গ উইন্ডো নির্ধারণ করে **AI কতগুলি পূর্ববর্তী বার্তা ব্যবহার করে প্রতিক্রিয়া তৈরি করবে**।  
- **বড় প্রসঙ্গ উইন্ডো** AI-কে **আরও বেশি তথ্য বিবেচনা করতে এবং আরও সুসংহত প্রতিক্রিয়া তৈরি করতে সহায়তা করে**।  

**টাইম বিটল:** "বিভিন্ন মডেলের আউটপুট টোকেনের সীমা ভিন্ন হয়। নিচের মডেলটি দেখুন:  

**`gpt-4o-2024-08-06` এর নির্দিষ্টকরণ:**  

- **সর্বাধিক আউটপুট টোকেন:** প্রায় **১৬া হাজার টোকেন**।  
- **সর্বাধিক প্রসঙ্গ উইন্ডো:** **১২৮ হাজার টোকেন**।  

এর মানে হলো, **মোট ১২৮k টোকেনের মধ্যে ১৬k টোকেন আউটপুটের জন্য ব্যবহৃত হবে, আর ১১২k টোকেন ইনপুট প্রসঙ্গে ব্যবহার করা যাবে।**  

---

**আপনি:** "বুঝলাম, প্রসঙ্গ উইন্ডো, টোকেন… কিন্তু একটি টোকেন আসলে কী?"  

**টাইম বিটল:** "একটি **টোকেন হলো একটি শব্দ বা শব্দের অংশ**, এবং এটি ভাষার উপর নির্ভর করে কিছুটা পরিবর্তিত হয়।  

এটি পরিমাপ করার জন্য একটি সরঞ্জাম রয়েছে, যা OpenAI সুপারিশ করে, এর নাম **[tokenizer](https://platform.openai.com/tokenizer)**।  

**আসুন একটি বাক্য চেষ্টা করি এবং দেখি এটি কতটি টোকেন ব্যবহার করে:**
```text
I want you to generate recipes for me.
```

![টোকেনাইজার ডেমো](https://raw.githubusercontent.com/microsoft/generative-ai-with-javascript/main/lessons/02-first-ai-app/assets/tokenizer.png)

উপরের বাক্যে **`tokenizer`** চালালে **৯টি টোকেন** পাওয়া যায়।

**আপনি:** "এটা খুব বেশি নয়, তাহলে মনে হচ্ছে আমার প্রসঙ্গ উইন্ডোতে অনেক টোকেন রাখতে পারব?"  

**টাইম বিটল:** "হ্যাঁ, আপনি বিভিন্ন প্রসঙ্গ উইন্ডো আকারের সাথে পরীক্ষা-নিরীক্ষা করতে পারেন এবং এটি কীভাবে AI-এর প্রতিক্রিয়াকে প্রভাবিত করে তা দেখতে পারেন।  

আসলে, যদি আপনি **প্রসঙ্গ উইন্ডোর আকার ১০০ সেট করেন**, তবে এটি **AI-এর ইনপুট এবং আউটপুট বিবেচনার সীমা নির্ধারণ করবে**।  

এখানে দেখুন, কিভাবে আপনি আপনার অ্যাপে প্রসঙ্গ উইন্ডো সেট করতে পারেন:
```javascript
// প্রসঙ্গ নির্ধারণ করুন 
const messages = [ 
{ 
  "role": "user", 
  "content": "আমি চাই তুমি আমার জন্য রেসিপি তৈরি করো।" 
}]; 

// প্রসঙ্গ উইন্ডোর আকার নির্ধারণ করুন 
let max_tokens = 100; // প্রসঙ্গ উইন্ডোর আকার সেট করুন 

// ওয়েব অনুরোধ তৈরি করুন 
const completion = await openai.chat.completions.create({
    model: 'gpt-4',
    messages: messages,
    max_tokens: max_tokens
}); 
```

> **পরামর্শ:** বিভিন্ন প্রসঙ্গ উইন্ডোর আকার নিয়ে পরীক্ষা করুন এবং দেখুন এটি কীভাবে AI-এর প্রতিক্রিয়াকে প্রভাবিত করে।

---

## **অ্যাসাইনমেন্ট - একটি প্রকৌশল সহকারী তৈরি করা**  

লিওনার্দো হঠাৎ **টাইম বিটল** আরও কাছ থেকে পরীক্ষা করতে চাইলেন। তিনি এটিকে চারদিক থেকে দেখলেন, এমনকি এটি নাড়াচাড়া করলেন।  

**লিওনার্দো:** "আমার এমন একটি সহকারী দরকার যে আমাকে **এরিয়াল স্ক্রু (aerial screw)**-এর গণনা ও নকশায় সাহায্য করতে পারবে। তুমি কি আমার জন্য এমন একটি সহকারী তৈরি করতে পারবে?"  

**আপনি:** "অবশ্যই, আমি এটি তোমার জন্য তৈরি করতে পারি। টাইম বিটল, আমরা এতে সাহায্য করতে পারব, তাই তো?"  

**টাইম বিটল:** "হ্যাঁ, কোনো সমস্যা নেই। আসলে **এরিয়াল স্ক্রু** লিওনার্দোর অন্যতম **সবচেয়ে আকর্ষণীয় ও দূরদর্শী আবিষ্কার**। এটি ১৪৮০-এর দশকের শেষের দিকে ডিজাইন করা হয়েছিল..."  

**আপনি:** "আমার শুধু 'হ্যাঁ' দরকার ছিল, লেকচার পরে শুনব!"  

**টাইম বিটল:** "রূঢ়..."  

**আপনি:** "কি?"  

**টাইম বিটল:** "কিছু না..."  

<div>
  <img style="margin-top: 52px; margin-left: 15px; margin-right: 10px" align=right src="/lessons/02-first-ai-app/assets/helicopter.jpg" alt="এরিয়াল স্ক্রু, লিওনার্দো দা ভিঞ্চি" width="300" >
</div>
> [!NOTE]  
> **এরিয়াল স্ক্রু**, যা **হেলিক্যাল এয়ার স্ক্রু** নামেও পরিচিত, এটি মাটির ওপর থেকে উঠতে **বায়ু সংকুচিত** করার নীতির ওপর ভিত্তি করে তৈরি করা হয়েছিল। লিওনার্দোর ডিজাইনটি ছিল একটি বিশাল **সর্পিল-আকৃতির রোটর**, যা **লিনেন দিয়ে তৈরি** এবং **স্টার্চ দিয়ে শক্ত করা** হয়েছিল, এবং এটি একটি কাঠের প্ল্যাটফর্মের ওপর স্থাপন করা হয়েছিল। ধারণাটি ছিল, **একদল মানুষ প্ল্যাটফর্মের চারপাশে ঘুরে ক্র্যাংক ঘোরাবে**, যা স্ক্রুটিকে যথেষ্ট গতিতে ঘোরাতে পারবে, ফলে এটি বাতাসে উঠতে পারবে।  
>  
> যদিও **লিওনার্দো কখনও পূর্ণ-স্কেলের এরিয়াল স্ক্রু তৈরি করতে পারেননি**, তবে তার স্কেচ এবং নোট থেকে স্পষ্ট হয় যে তিনি কীভাবে এটি কাজ করবে বলে কল্পনা করেছিলেন। তিনি বিশ্বাস করতেন, **যদি স্ক্রুটি যথেষ্ট দ্রুত ঘোরানো যায়, তবে এটি বাতাসের বিরুদ্ধে চাপ তৈরি করবে এবং পুরো কাঠামোকে উপরে তুলতে সক্ষম হবে**।  
>  
> তবে, **আধুনিক বিজ্ঞানীরা একমত যে লিওনার্দোর সময়ে বিদ্যমান উপকরণগুলো যথেষ্ট শক্তিশালী বা হালকা ছিল না**, যা এই ধারণাকে বাস্তবে রূপ দিতে পারত।  
>  
> তবুও, এরিয়াল স্ক্রু **লিওনার্দোর প্রতিভার এক অসাধারণ নিদর্শন** এবং তার উদ্ভাবনী চেতনাকে প্রকাশ করে। এটি **বিমান প্রযুক্তির ভবিষ্যৎ উন্নয়নের ভিত্তি** স্থাপন করেছিল এবং এখনো **প্রকৌশলবিদ ও উদ্ভাবকদের অনুপ্রাণিত করে যাচ্ছে**।  
> [আরও পড়ুন](https://en.wikipedia.org/wiki/Leonardo%27s_aerial_screw)  

---

### **অ্যাসাইনমেন্ট: লিওনার্দোর জন্য একটি প্রকৌশল সহকারী তৈরি করুন**  

আপনার কাজ হলো **একটি প্রকৌশল সহকারী তৈরি করা**, যা **এরিয়াল স্ক্রু-এর গণনা এবং নকশার ক্ষেত্রে লিওনার্দোকে সাহায্য করবে**।  

✅ **সহকারীটি ব্যবহারকারীর ইনপুটের উপর ভিত্তি করে পাঠ্য তৈরি করতে পারবে।**  
✅ **আপনাকে একটি "system message" সেট করতে হবে, যা সহকারীকে পরিচয় করিয়ে দেবে।**  

শুরু করতে **[Sample app](/app/)** দেখুন।  

> **পরামর্শ:** **System message** কেমন হওয়া উচিত এবং ব্যবহারকারীর কী ধরনের ইনপুট প্রদান করা উচিত তা বিবেচনা করুন।
## **সমাধান**  

[সমাধান](/lessons/02-first-ai-app/solution/solution.md)  

---

## **জ্ঞান যাচাই (Knowledge Check)**  

**প্রশ্ন:** **Generative AI মডেলগুলোর ক্ষেত্রে প্রসঙ্গ উইন্ডোর উদ্দেশ্য কী?** সঠিক উত্তরগুলো নির্বাচন করুন।  

A. **প্রসঙ্গ উইন্ডো AI-কে আরও প্রসঙ্গ বিবেচনা করতে এবং আরও সুসংহত প্রতিক্রিয়া তৈরি করতে সহায়তা করে।**  

B. **প্রসঙ্গ উইন্ডো হলো পূর্ববর্তী বার্তাগুলোর সংখ্যা, যা AI উত্তর তৈরি করতে ব্যবহার করে।**  

C. **প্রসঙ্গ উইন্ডো নির্ধারণ করে AI-এর প্রতিক্রিয়াগুলো কতটা সৃজনশীল হবে।**  

[কুইজের সমাধান](/lessons/02-first-ai-app/solution/solution-quiz.md)  

---

## **স্ব-অধ্যয়নের জন্য সংস্থানসমূহ**  

- [টেক্সট জেনারেশন](https://platform.openai.com/docs/guides/text-generation)  
- [OpenAI-এর জন্য JavaScript লাইব্রেরি](https://github.com/openai/openai-node/tree/master/examples)  
- [Tokenizer](https://platform.openai.com/tokenizer)  
- [Completion API](https://platform.openai.com/docs/api-reference/completions)  
- [Chat completions](https://platform.openai.com/docs/guides/text-generation#text-generation-models)  
