### Server Rendering-এর সুবিধাসমূহ (Benefits of Server Rendering)

**Server rendering** বা **Server-Side Rendering (SSR)** হল একটি টেকনিক যেখানে ওয়েবপেজের HTML কনটেন্ট সার্ভার সাইডে রেন্ডার করা হয় এবং তা ব্রাউজারে পাঠানো হয়। এই পদ্ধতিতে বেশ কিছু গুরুত্বপূর্ণ সুবিধা রয়েছে। নিচে সেগুলো বিশদভাবে ব্যাখ্যা করা হলো।

#### 1. **ডেটা ফেচিং (Data Fetching)**

- **কেন ব্যবহার করবেন?**: Server Components আপনাকে ডেটা ফেচিং সার্ভার সাইডে করতে সাহায্য করে, যা আপনার ডেটা সোর্সের কাছাকাছি। এর ফলে, ডেটা রেন্ডার করার জন্য যে সময় লাগে তা কমে যায় এবং ক্লায়েন্টের জন্য আরও কম রিকোয়েস্ট করতে হয়।
  
- **কিভাবে উপকারিতা পাওয়া যায়?**: ক্লায়েন্ট সাইডে কম রিকোয়েস্ট এবং কম সময় ধরে ডেটা ফেচিং হয়, যার ফলে পেজ লোডিং দ্রুত হয়। 

#### 2. **সিকিউরিটি (Security)**

- **কেন ব্যবহার করবেন?**: Server Components আপনাকে সেনসিটিভ ডেটা (যেমন টোকেন, API কী ইত্যাদি) সার্ভারের উপর রাখার সুযোগ দেয়, যা ক্লায়েন্ট সাইডে লিক হওয়ার ঝুঁকি কমিয়ে দেয়।
  
- **কিভাবে উপকারিতা পাওয়া যায়?**: সার্ভারে সিকিউরিটি রক্ষা করা হয়, এবং ক্লায়েন্ট সাইডে কোনো গোপন তথ্য ফাঁস হয় না।

#### 3. **ক্যাশিং (Caching)**

- **কেন ব্যবহার করবেন?**: সার্ভারে রেন্ডার করা HTML ক্যাশ করা যায় এবং পরবর্তীতে পুনরায় ব্যবহার করা যায়। এর ফলে, পরবর্তী রিকোয়েস্টে একই HTML আবার রেন্ডার করার প্রয়োজন হয় না, যা সার্ভার এবং ক্লায়েন্টের উপর চাপ কমিয়ে দেয়।
  
- **কিভাবে উপকারিতা পাওয়া যায়?**: ক্যাশিংয়ের মাধ্যমে পেজ রেন্ডারিংয়ের সময় কমে যায় এবং সার্ভারের ওপরে কম চাপ পড়ে, যার ফলে কোস্টও কমে আসে।

#### 4. **পারফরম্যান্স (Performance)**

- **কেন ব্যবহার করবেন?**: Server Components আপনাকে এমন টুলস প্রদান করে যেগুলো পারফরম্যান্স অপটিমাইজ করতে সাহায্য করে। উদাহরণস্বরূপ, যদি আপনার অ্যাপ্লিকেশনটা সম্পূর্ণ ক্লায়েন্ট কম্পোনেন্ট দিয়ে তৈরি হয়, তাহলে ক্লায়েন্ট সাইড জাভাস্ক্রিপ্ট কমানোর জন্য কিছু UI অংশ সার্ভার কম্পোনেন্টে নিয়ে যেতে পারেন।
  
- **কিভাবে উপকারিতা পাওয়া যায়?**: এতে ক্লায়েন্ট সাইডে কম জাভাস্ক্রিপ্ট লোড হয়, যা ব্রাউজারকে দ্রুত পেজ রেন্ডার করতে সাহায্য করে। বিশেষত, যারা ধীর ইন্টারনেট কানেকশন বা কম ক্ষমতাসম্পন্ন ডিভাইস ব্যবহার করেন, তাদের জন্য এটি উপকারী।

#### 5. **প্রথম পেজ লোড এবং ফার্স্ট কনটেন্টফুল পেইন্ট (Initial Page Load and First Contentful Paint - FCP)**

- **কেন ব্যবহার করবেন?**: সার্ভারে HTML রেন্ডার করলে ব্যবহারকারীরা পেজটি দ্রুত দেখতে পারে, কারণ তাদের আর ক্লায়েন্ট সাইডের জাভাস্ক্রিপ্ট ডাউনলোড, পার্স এবং এক্সিকিউট করার জন্য অপেক্ষা করতে হয় না।
  
- **কিভাবে উপকারিতা পাওয়া যায়?**: ব্যবহারকারী দ্রুত প্রথম কনটেন্ট দেখতে পাবেন, এবং প্রথম পেজ লোড হয়ে যাবে।

#### 6. **সার্চ ইঞ্জিন অপটিমাইজেশন এবং সোশ্যাল নেটওয়ার্ক শেয়ার (Search Engine Optimization and Social Network Shareability)**

- **কেন ব্যবহার করবেন?**: রেন্ডারড HTML সার্চ ইঞ্জিন বটদের জন্য ইন্ডেক্স করা যায়, এবং সোশ্যাল মিডিয়া বটগুলোর জন্য সোশ্যাল কার্ড প্রিভিউ তৈরি করা যায়। এর ফলে SEO বৃদ্ধি পায় এবং সোশ্যাল মিডিয়াতে শেয়ার করার সময় আরও আকর্ষণীয় প্রিভিউ দেখা যায়।

- **কিভাবে উপকারিতা পাওয়া যায়?**: সার্চ ইঞ্জিন আপনার পেজগুলো ভালভাবে ইনডেক্স করতে পারে, এবং সোশ্যাল মিডিয়াতে শেয়ার করা হলে সঠিক প্রিভিউ এবং মেটাডেটা দেখা যায়।

#### 7. **স্ট্রিমিং (Streaming)**

- **কেন ব্যবহার করবেন?**: Server Components আপনাকে রেন্ডারিং কাজকে ছোট ছোট অংশে ভাগ করে ক্লায়েন্টের কাছে পাঠাতে দেয়। এর ফলে, পুরো পেজটি রেন্ডার হওয়ার আগেই ব্যবহারকারী পেজের কিছু অংশ দেখতে পারে।
  
- **কিভাবে উপকারিতা পাওয়া যায়?**: ব্যবহারকারী পুরো পেজ লোড হওয়ার আগেই কিছু অংশ দেখতে পায়, যার ফলে ইউজার এক্সপেরিয়েন্স উন্নত হয় এবং তারা অপেক্ষা করার সময় কম অনুভব করে।

---

### বাস্তব উদাহরণ:

ধরা যাক আপনি একটি **নিউজ সাইট** তৈরি করছেন, যেখানে প্রতিদিন নতুন নতুন সংবাদ আপডেট হয়। এখানে যদি আপনি **Server-Side Rendering (SSR)** ব্যবহার করেন:

- **ডেটা ফেচিং**: সার্ভারে খবরগুলোর ডেটা রেন্ডার হবে, এবং এর ফলে নিউজ আর্টিকেলগুলো দ্রুত লোড হবে।
- **সিকিউরিটি**: API কীগুলো সার্ভার সাইডে রক্ষা করা হবে, যাতে সেগুলো ক্লায়েন্ট সাইডে ফাঁস না হয়।
- **ক্যাশিং**: আগের নিউজ পেজগুলো ক্যাশ হয়ে যাবে এবং পরবর্তী ভিজিটের জন্য দ্রুত লোড হবে।
- **পারফরম্যান্স**: সার্ভারে রেন্ডার হওয়া HTML ব্রাউজারে খুব দ্রুত প্রদর্শিত হবে, ক্লায়েন্ট সাইডের জাভাস্ক্রিপ্ট কম ব্যবহার হবে।
- **SEO**: সার্চ ইঞ্জিনগুলো সহজে আপনার নিউজ সাইট ইন্ডেক্স করতে পারবে এবং সোশ্যাল মিডিয়ায় শেয়ার করার সময় প্রিভিউ দেখাবে।

এভাবে **Server-Side Rendering (SSR)** ব্যবহার করার মাধ্যমে আপনি সাইটের পারফরম্যান্স, সিকিউরিটি এবং SEO-র উন্নতি ঘটাতে পারবেন।

### Server Components কীভাবে রেন্ডার করা হয়? (How are Server Components rendered?)

**Next.js**-এ **Server Components** রেন্ডার করার জন্য **React** এর APIs ব্যবহার করা হয়। এই রেন্ডারিং কাজটি ছোট ছোট অংশে বিভক্ত করা হয়, যেমন প্রতিটি **রুট সেগমেন্ট** এবং **Suspense Boundaries** অনুযায়ী।

#### ১. **প্রথম ধাপ - সার্ভারে রেন্ডারিং**

রেন্ডারিং দুটি ধাপে সম্পন্ন হয়:

- **React** সার্ভার কম্পোনেন্টগুলোকে একটি বিশেষ ডেটা ফরম্যাটে রেন্ডার করে, যার নাম **React Server Component Payload (RSC Payload)**।
- তারপর, **Next.js** এই **RSC Payload** এবং **Client Component JavaScript** নির্দেশাবলী ব্যবহার করে HTML রেন্ডার করে সার্ভারে।

#### ২. **দ্বিতীয় ধাপ - ক্লায়েন্টে রেন্ডারিং**

ক্লায়েন্টে:

- **HTML** ব্যবহার করে পেজটি দ্রুত এবং নন-ইন্টারঅ্যাকটিভ প্রিভিউ দেখানো হয়, যা **প্রাথমিক পেজ লোড** এর জন্য উপযোগী।
- এরপর, **React Server Components Payload** ব্যবহার করে ক্লায়েন্ট এবং সার্ভার কম্পোনেন্ট গাছকে পুনরায় একত্রিত করা হয় এবং DOM আপডেট করা হয়।
- **JavaScript নির্দেশাবলী** ব্যবহার করে ক্লায়েন্ট কম্পোনেন্টগুলো হাইড্রেট করা হয় এবং অ্যাপ্লিকেশনটি ইন্টারঅ্যাকটিভ হয়ে ওঠে।

---

### React Server Component Payload (RSC) কী?

**React Server Component Payload (RSC Payload)** হল একটি কমপ্যাক্ট বাইনারি রূপ যা রেন্ডার করা **React Server Components** গাছের প্রতিনিধিত্ব করে। এটি ক্লায়েন্টে **React** দ্বারা ব্রাউজারের DOM আপডেট করতে ব্যবহৃত হয়। **RSC Payload** এর মধ্যে নিম্নলিখিত জিনিসগুলো থাকে:

- **Server Components** এর রেন্ডার করা ফলাফল।
- যেখানে **Client Components** রেন্ডার হবে তার জন্য **Placeholders** এবং তাদের JavaScript ফাইলের রেফারেন্স।
- যে কোনও **props** যা **Server Component** থেকে **Client Component**-এ পাঠানো হয়।

### উদাহরণ:

ধরা যাক আপনি একটি ব্লগ সাইট তৈরি করছেন যেখানে প্রাথমিক পেজটি সার্ভারে রেন্ডার করা হয়। প্রথমে সার্ভার HTML তৈরি করে, যাতে ব্যবহারকারী পেজটি দ্রুত দেখতে পারে। এরপর, React সার্ভার কম্পোনেন্টগুলো ক্লায়েন্ট সাইডে **RSC Payload** হিসেবে পাঠানো হয় এবং **JavaScript** ব্যবহার করে ক্লায়েন্ট কম্পোনেন্টগুলোকে ইন্টারঅ্যাকটিভ করা হয়।

এই পদ্ধতি ব্যবহার করলে সার্ভারে রেন্ডার করা ব্লগ পোস্টগুলো দ্রুত এবং কার্যকরভাবে লোড হয় এবং ব্যবহারকারীরা দ্রুত একটি ইন্টারঅ্যাকটিভ অ্যাপ্লিকেশন পেয়ে যান।

### Dynamic Rendering (ডাইনামিক রেন্ডারিং)

**ডাইনামিক রেন্ডারিং** হল এমন একটি প্রক্রিয়া যেখানে প্রতিটি রিকোয়েস্টে ইউজারের জন্য রাউটগুলি রেন্ডার করা হয়। এর মাধ্যমে, রিকোয়েস্ট সময়ে প্রতিটি পৃষ্ঠার জন্য সঠিক ডেটা প্রস্তুত করা হয়, যা ইউজারের ব্যক্তিগতকৃত তথ্য বা অন্য কোন ডেটার উপর ভিত্তি করে হতে পারে।

#### **কখন ব্যবহার করবেন?**
ডাইনামিক রেন্ডারিং তখন ব্যবহার করা হয় যখন কোনও রাউটের ডেটা ইউজারের উপর ভিত্তি করে পরিবর্তিত হয়, অথবা রিকোয়েস্ট টাইমে প্রাপ্ত তথ্যের ওপর নির্ভর করে, যেমন কুকি অথবা ইউআরএল এর সার্চ প্যারামিটার।

#### **কিভাবে কাজ করে?**
ডাইনামিক রেন্ডারিং মূলত এমন রাউটগুলির জন্য ব্যবহৃত হয় যেগুলোর ডেটা কোনও নির্দিষ্ট ব্যবহারকারীর জন্য বা রিকোয়েস্ট টাইমে নির্ধারিত হয়। যেমন, একটি ইকমার্স সাইটে পণ্য তালিকা ক্যাশে করা হতে পারে কিন্তু প্রতিটি ব্যবহারকারীর জন্য তাদের কাস্টম ডেটা (যেমন ক্রয় ইতিহাস বা পছন্দ) বিভিন্ন হতে পারে। এই ধরনের পৃষ্ঠাগুলি রেন্ডার করার সময়, প্রয়োজনীয় ডেটা শুধুমাত্র ইউজার বা রিকোয়েস্ট টাইমে পাওয়া যাবে।

#### **ক্যাশ করা ডেটা সহ ডাইনামিক রাউটস**
বেশিরভাগ সাইটে, রাউটগুলি পুরোপুরি স্ট্যাটিক বা পুরোপুরি ডাইনামিক হয় না, বরং এটি একটি স্পেকট্রাম (বিভিন্ন মাত্রার)। উদাহরণস্বরূপ, আপনি একটি ইকমার্স পেজ পেতে পারেন যেখানে পণ্যের তথ্য ক্যাশে করা আছে এবং তা পুনরায় যাচাই (revalidate) করা হয় নির্দিষ্ট সময় পরপর, কিন্তু কাস্টমার ডেটা (যেমন প্রোফাইল তথ্য) একে অপরের থেকে ভিন্ন। 

**Next.js** এ, আপনি ডাইনামিক রেন্ডারিংয়ের রাউটগুলিতে ক্যাশে করা এবং uncached (অক্যাশ) ডেটা ব্যবহার করতে পারেন। এর কারণ হল, RSC Payload এবং ডেটা আলাদাভাবে ক্যাশে করা হয়। এর ফলে, আপনি ডাইনামিক রেন্ডারিং এ প্রবেশ করতে পারেন এবং রিকোয়েস্ট সময়ে সমস্ত ডেটা অনুসন্ধান করার পারফরমেন্স সমস্যাগুলি নিয়ে চিন্তা করতে হয় না।

#### **উদাহরণ (JavaScript)**:

```javascript
// pages/product/[id].js

export async function getServerSideProps({ params }) {
  // Dynamic content based on user data or cookies
  const productData = await fetch(`https://api.example.com/products/${params.id}`);
  const product = await productData.json();

  // Personalized content (uncached data)
  const userData = await fetch(`https://api.example.com/user/profile`);
  const user = await userData.json();

  return {
    props: {
      product,
      user
    }
  }
}

export default function ProductPage({ product, user }) {
  return (
    <div>
      <h1>{product.name}</h1>
      <p>{product.description}</p>
      <p>Welcome back, {user.name}!</p>
    </div>
  );
}
```

### **কীভাবে লাভবান হবেন?**
1. **পারফরমেন্স উন্নতি**: আপনি ক্যাশে ডেটা ব্যবহার করে রেন্ডারিং সময় কমাতে পারেন এবং শুধুমাত্র পরিবর্তনশীল ডেটা রেন্ডার করতে পারেন।
2. **ব্যক্তিগতকৃত অভিজ্ঞতা**: ব্যবহারকারীদের জন্য একটি নির্দিষ্ট অভিজ্ঞতা প্রদান করতে পারবেন (যেমন, তাদের প্রোফাইল বা পছন্দসই পণ্যগুলি)।
3. **স্কেলেবিলিটি**: ক্যাশিং এবং ডাইনামিক রেন্ডারিং এর মিশ্রণ সাইটের পারফরমেন্স উন্নত করে, বিশেষত যদি আপনার সাইটে বিভিন্ন ধরনের ডেটা থাকে।

এভাবে, ডাইনামিক রেন্ডারিং সাইটগুলির জন্য পারফরমেন্স এবং ব্যবহারকারীদের জন্য উপযুক্ত অভিজ্ঞতা প্রদান করতে সহায়ক।

### Dynamic Rendering এ স্যুইচ করা (Switching to Dynamic Rendering)

**Dynamic Rendering** হল একটি প্রক্রিয়া যেখানে রাউটগুলি ডাইনামিকভাবে ইউজারের জন্য রেন্ডার করা হয়, অর্থাৎ প্রতিটি রিকোয়েস্টের জন্য নতুনভাবে ডেটা রেন্ডার হয়। যখন কোনো **Dynamic API** বা `{ cache: 'no-store' }` ফেচ অপশন ব্যবহার করা হয়, তখন Next.js পুরো রাউটটি ডাইনামিকভাবে রেন্ডার করবে। 

এটি গুরুত্বপূর্ণ কারণ ডাইনামিক রেন্ডারিং নিশ্চিত করে যে আপনি রিকোয়েস্ট টাইমে সর্বশেষ ডেটা পাবেন, যা প্রায়ই পরিবর্তিত হতে পারে, যেমন ব্যবহারকারীর পছন্দ বা প্রোফাইল তথ্য।

#### **কিভাবে কাজ করে?**
Next.js এমন একটি সিস্টেম ব্যবহার করে, যেখানে ডেটা কaching এর উপর ভিত্তি করে রেন্ডারিং স্ট্যাটিক বা ডাইনামিক হতে পারে। এই কৌশলটির মাধ্যমে, সিস্টেম নিজে থেকেই সিদ্ধান্ত নেয় কোন রাউটটি স্ট্যাটিক রেন্ডার হবে এবং কোনটি ডাইনামিক রেন্ডার হবে।

নিচের টেবিলটি এটি ব্যাখ্যা করে কিভাবে **Dynamic APIs** এবং ডেটা ক্যাশিং রাউটের রেন্ডারিং পদ্ধতিতে প্রভাব ফেলে:

| **Dynamic APIs** | **Data**   | **Route**            |
|------------------|------------|----------------------|
| No               | Cached     | Statically Rendered  |
| Yes              | Cached     | Dynamically Rendered |
| No               | Not Cached | Dynamically Rendered |
| Yes              | Not Cached | Dynamically Rendered |

#### **ব্যাখ্যা**:

- **No Cached**: যদি রাউটের ডেটা ক্যাশ করা না থাকে, তবে এটি ডাইনামিকভাবে রেন্ডার হবে।
- **Yes Cached**: যদি রাউটের ডেটা ক্যাশ করা থাকে, তবে এটি ডাইনামিকভাবে রেন্ডার হবে, যদি ডাইনামিক API ব্যবহার করা হয়।
- **No Not Cached**: ডেটা ক্যাশ না হলে এবং ডাইনামিক API ব্যবহৃত হলে, রাউটটি ডাইনামিকভাবে রেন্ডার হবে।

#### **কীভাবে এটি কাজ করে?**

এখন, আপনি যখন **Dynamic API** বা `{ cache: 'no-store' }` অপশন ব্যবহার করবেন, তখন Next.js রাউটটিকে ডাইনামিকভাবে রেন্ডার করবে, এবং ক্যাশিংয়ের মাধ্যমে কোনও পূর্ববর্তী রেন্ডারিং ডেটা ব্যবহার করবে না। 

Next.js ডেভেলপারদের জন্য স্বয়ংক্রিয়ভাবে সিদ্ধান্ত নেয় যে, কোন রাউটটি স্ট্যাটিকভাবে রেন্ডার হবে এবং কোনটি ডাইনামিক রেন্ডার হবে। এর মানে হল যে, আপনি ডেভেলপার হিসেবে শুধুমাত্র ডেটা ক্যাশিং এবং রিভ্যালিডেশন কন্ট্রোল করতে পারেন এবং UI এর অংশগুলিকে স্ট্রিম করতে পছন্দ করতে পারেন।

#### **রিয়েল-টাইম উদাহরণ (JavaScript)**:

```javascript
// pages/profile.js

export async function getServerSideProps() {
  // Dynamic data (not cached)
  const userData = await fetch('https://api.example.com/user/profile', {
    cache: 'no-store',
  });
  const user = await userData.json();

  return {
    props: {
      user,
    },
  };
}

export default function ProfilePage({ user }) {
  return (
    <div>
      <h1>{user.name}'s Profile</h1>
      <p>Email: {user.email}</p>
    </div>
  );
}
```

এখানে, `getServerSideProps()` ফাংশনে `cache: 'no-store'` ব্যবহার করা হয়েছে, যার ফলে **Dynamic Rendering** সঞ্চালিত হবে এবং ইউজারের প্রোফাইল ডেটা রিকোয়েস্ট টাইমে লোড হবে।

### **লাভ এবং উপকারিতা**:

1. **স্বয়ংক্রিয় রেন্ডারিং কৌশল নির্বাচন**: Next.js স্বয়ংক্রিয়ভাবে ডাইনামিক এবং স্ট্যাটিক রেন্ডারিংয়ের মধ্যে সঠিক কৌশল বেছে নেয়। ডেভেলপারদের কোনও একটিকে পছন্দ করতে হয় না।
   
2. **ডেটা কন্ট্রোল**: আপনি কখন এবং কীভাবে ডেটা ক্যাশ করবেন, রিভ্যালিডেট করবেন তা নিয়ন্ত্রণ করতে পারবেন।
   
3. **স্ট্রিমিং**: আপনি UI এর কিছু অংশ স্ট্রিম করতে পারেন, যাতে ইউজার দ্রুত কনটেন্ট দেখতে পারে, বিশেষ করে যদি আপনি বড় এবং ইন্টারেক্টিভ পেজ তৈরি করছেন।

এইভাবে, **Dynamic Rendering** ব্যবহারে আপনাকে রিয়েল-টাইমে ডেটা রেন্ডার করতে দেয়, এবং একই সাথে পারফরমেন্স এবং ইউজার এক্সপেরিয়েন্সের উন্নতি ঘটায়।



### Dynamic APIs (ডাইনামিক API)

**Dynamic APIs** হল এমন API গুলি যেগুলি এমন তথ্যের উপর নির্ভর করে যা শুধুমাত্র রিকোয়েস্ট টাইমে জানা যায় (প্রেরণের সময় নয়)। এই API গুলি ব্যবহার করলে ডেভেলপাররা স্পষ্টভাবে নির্দেশ দেন যে তারা রিকোয়েস্ট টাইমে ডাইনামিক রেন্ডারিং চাচ্ছেন। এর মানে হল যে, যখন এই API গুলি ব্যবহার করা হবে, তখন পুরো রাউটটি ডাইনামিকভাবে রেন্ডার হবে।

এই ধরনের API গুলির মধ্যে কিছু সাধারণ API হলো:

1. **Cookies (কুকি)**: ব্যবহারকারীর ব্রাউজারে সংরক্ষিত তথ্য। উদাহরণস্বরূপ, ইউজার লগ ইন করেছে কিনা তা জানার জন্য কুকি ব্যবহার করা হতে পারে।
   
2. **Headers (হেডার)**: রিকোয়েস্ট বা রেসপন্সের অংশ হিসেবে প্রেরিত অতিরিক্ত তথ্য। এটি সাধারণত অ্যাক্সেস কন্ট্রোল, অথেনটিকেশন, এবং অন্যান্য প্রয়োজনীয় সেটিংস পাঠাতে ব্যবহৃত হয়।

3. **Connection (কানেকশন)**: ব্যবহারকারীর ব্রাউজারের সাথে সার্ভারের কানেকশনের স্ট্যাটাস বা ধরন।

4. **draftMode (ড্রাফট মোড)**: কিছু কন্টেন্ট বা ডেটা যা কেবলমাত্র ডেভেলপার বা প্রশাসকের জন্য প্রদর্শিত হয়, বিশেষত কন্টেন্ট ম্যানেজমেন্ট সিস্টেমে।

5. **searchParams prop (সার্চ প্যারামিটার প্রোপ)**: ইউআরএল থেকে প্যারামিটার, যেমন `?id=123` যা ডাইনামিক রাউট লোড করতে সাহায্য করে।

6. **unstable_noStore (অনস্টেবল_নো স্টোর)**: যে তথ্য ক্যাশ করা যাবে না, অর্থাৎ এটি রিকোয়েস্ট টাইমে রেন্ডার হবে এবং ক্যাশ করা হবে না।

7. **Streaming (স্ট্রিমিং)**: স্ট্রিমিং হল একটি প্রযুক্তি যার মাধ্যমে আপনি সেগমেন্ট অনুযায়ী রাউটের UI পার্ট পার্ট করে রেন্ডার করতে পারেন। এর মাধ্যমে, ব্যবহারকারী পুরো পেজটি রেন্ডার হওয়ার আগে কিছু অংশ দেখতে শুরু করতে পারে।

---

### **Streaming (স্ট্রিমিং)**

**Streaming** হল একটি প্রযুক্তি যা ইউজারকে দ্রুত UI প্রদর্শন করতে সাহায্য করে। এই প্রযুক্তিতে, কাজটি ছোট ছোট সেগমেন্টে ভাগ হয়ে সার্ভার থেকে ক্লায়েন্টে স্ট্রিম করা হয়। এর ফলে, পুরো পেজ রেন্ডার হওয়ার আগে ইউজার কিছু অংশ দেখতে পারে। 

এটি এমন বিশেষ ক্ষেত্রে উপকারী যেখানে ডেটা ধীরে লোড হয়, এবং পুরো পেজ রেন্ডার না হয়ে ইউজাররা দেখতে শুরু করে। উদাহরণস্বরূপ, যদি আপনার পেজে প্রোডাক্টের রিভিউ লোড হতে অনেক সময় নেয়, তবে স্ট্রিমিং ব্যবহার করে আপনি রিভিউ বিভাগটি ধীরে ধীরে ইউজারের কাছে পৌঁছাতে পারবেন।

---

### **Streaming-এর সুবিধা**

1. **প্রাথমিক পেজ লোডিং দ্রুত**: প্রথম পেজ লোডিং এর সময় কিছু অংশ রেন্ডার হয়ে যায়, তাই ব্যবহারকারী দ্রুত দেখতে শুরু করতে পারে। পুরো পেজ রেন্ডার হওয়ার পরেও পেজের বাকি অংশ স্ট্রিম করা হতে থাকে।

2. **ধীর ডেটা ফেচিং**: যদি কিছু অংশের জন্য ডেটা ফেচিং ধীর হয়, তবে পুরো পেজ ব্লক না হয়ে শুধুমাত্র ধীর লোড হওয়া অংশগুলো স্ট্রিমিংয়ের মাধ্যমে লোড হতে পারে। উদাহরণস্বরূপ, প্রোডাক্ট পেজে রিভিউ বা কমেন্ট সেকশন।

3. **React Suspense**: স্ট্রিমিং, React Suspense ব্যবহার করে, UI এর অংশগুলো অগ্রাধিকার ভিত্তিতে লোড হতে সাহায্য করে, যখন বাকি অংশগুলো ধীরে ধীরে লোড হচ্ছে।

---

### **ব্যবহার উদাহরণ (JavaScript)**:

**উদাহরণ ১:**

```javascript
// pages/product.js

import { Suspense } from 'react';

// This is a dynamically loaded component
function Reviews() {
  const reviews = fetch('https://api.example.com/reviews').then((res) => res.json());
  return (
    <div>
      {reviews.map((review) => (
        <p key={review.id}>{review.comment}</p>
      ))}
    </div>
  );
}

export default function ProductPage() {
  return (
    <div>
      <h1>Product Page</h1>
      <Suspense fallback={<div>Loading reviews...</div>}>
        <Reviews />
      </Suspense>
    </div>
  );
}
```

এই উদাহরণে, `Reviews` কম্পোনেন্টটি ধীরে ধীরে লোড হবে এবং যখন ডেটা আসবে তখন এটি দেখানো হবে। `Suspense` দ্বারা `fallback` দেখানো হবে, যখন ডেটা লোড হতে থাকবে।

---

### **উপকারিতা (Benefits)**

1. **ডাইনামিক রেন্ডারিং**: যেহেতু সমস্ত তথ্য রিকোয়েস্ট টাইমে রেন্ডার করা হয়, এটি ব্যবহারকারীর জন্য আরো প্রাসঙ্গিক এবং কাস্টমাইজড তথ্য প্রদান করে।
   
2. **স্ট্রিমিং ক্ষমতা**: স্ট্রিমিং দ্বারা UI দ্রুত লোড হয় এবং ধীরে ধীরে পেজটি পুরোপুরি লোড হয়, যা ব্যবহারকারীর অভিজ্ঞতা উন্নত করে।

3. **ক্যাশিং**: আপনি যদি কিছু অংশ ক্যাশ করেন এবং অন্য কিছু অংশ ডাইনামিকভাবে রেন্ডার করেন, তবে এটি পারফরমেন্স এবং ইউজার এক্সপেরিয়েন্স উভয়ই উন্নত করতে সহায়ক।


Dynamic APIs এবং স্ট্রিমিং ব্যবহার করলে, আপনি আপনার অ্যাপ্লিকেশনের পারফরমেন্স এবং ইউজার এক্সপেরিয়েন্স উন্নত করতে পারেন, বিশেষ করে যদি অ্যাপ্লিকেশনটি ধীর লোডিং ডেটা বা কাস্টমাইজড তথ্যের সাথে কাজ করে।
