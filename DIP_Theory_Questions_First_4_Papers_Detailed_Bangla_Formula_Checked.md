> **File format:** UTF-8 Markdown. Bengali text is saved as Unicode, and formulas use standard `$...$` inline math and `$$...$$` display math notation.

# DIP — Previous 4 Question Papers: Theory Questions & Short Answers

**Source:** `DIP Question fresh.pdf` (65-page Question Bank)

**Papers covered:** Spring 2025, Fall 2024, Spring 2024, Fall 2023. These are the first four exam papers listed in the Question Bank index.

## কীভাবে এই নোট ব্যবহার করবে

প্রতিটি প্রশ্নের সঙ্গে আছে:
- **Reference:** Question Bank PDF-এর page এবং question/subpart।
- **প্রশ্নে কী করতে বলেছে:** বাংলায় কাজের নির্দেশ।
- **Short answer (English):** সহজ শব্দে, সর্বোচ্চ ৩টি বাক্য।
- **বাংলায় বুঝিয়ে বলা:** English answer-এ কী বলা হয়েছে, সেটা একটু বিস্তারিত ও সহজ করে।

শুধু theory বা theory-প্রধান subpart রাখা হয়েছে। যেসব প্রশ্ন সম্পূর্ণ numerical, সেগুলো বাদ; mixed প্রশ্নের theory অংশ রাখা হয়েছে।

---

# 1. Spring 2025

**Question Bank PDF pages 2–4**

## Q1(a) — Objectives of Sharpening Spatial Filters
**Reference:** PDF p.2, Spring 2025 Q1(a)

**Question:** What are the objectives of sharpening spatial filters? Derive the Laplacian operator using image derivatives and draw four Laplacian masks.

**প্রশ্নে কী করতে হবে:** Sharpening filter কেন ব্যবহার করা হয় তা বলতে হবে; Laplacian-এর derivative formula এবং চারটি mask-ও লিখতে বলা হয়েছে।

**Short answer (English):** Sharpening filters enhance fine details and edges. The Laplacian uses second-order derivatives: $\nabla^2 f=f_{xx}+f_{yy}$.

**বাংলায় বুঝিয়ে বলা:** ছবির edge বা সূক্ষ্ম detail ঝাপসা হলে sharpening সেটাকে বেশি স্পষ্ট করে। Laplacian ছবির intensity কত দ্রুত পরিবর্তিত হচ্ছে তার দ্বিতীয়-order পরিবর্তন দেখে; প্রশ্নে mask আঁকতে বললে চারটি standard mask-ও আঁকতে হবে।

## Q1(b) — 4-, 8- and m-Connectivity
**Reference:** PDF p.2, Spring 2025 Q1(b)

**Question:** State the difference between 4-neighbor, 8-neighbor and m-connectivity, and discuss the effect of diagonal adjacency.

**প্রশ্নে কী করতে হবে:** তিন ধরনের connectivity-এর পার্থক্য এবং diagonal pixel যুক্ত হলে component-এর কী পরিবর্তন হয় তা ব্যাখ্যা করতে হবে। মূল প্রশ্নের connected-component গণনা numerical অংশ; এখানে theory-টুকু দেওয়া হয়েছে।

**Short answer (English):** 4-connectivity uses the four direct neighbors, while 8-connectivity also includes diagonal neighbors. m-connectivity allows diagonal connection only when the common 4-neighbors do not contain a foreground pixel.

**বাংলায় বুঝিয়ে বলা:** 4-connectivity-তে ওপর, নিচ, বাম ও ডানের pixel দিয়ে সংযোগ হয়। 8-connectivity-তে diagonal-ও সংযোগ তৈরি করতে পারে, তাই component একত্র হওয়ার সম্ভাবনা বাড়ে। m-connectivity diagonal সংযোগে অতিরিক্ত শর্ত দেয়, যাতে অপ্রয়োজনীয় বা ambiguous connection কমে।

## Q1(c) — Color Image, Additive/Subtractive Mixing and Color Models
**Reference:** PDF p.2, Spring 2025 Q1(c)

**Question:** Define a color image. Explain additive and subtractive color mixing, the purpose of color models, and suitable models for printing and segmentation.

**প্রশ্নে কী করতে হবে:** Color image কী, আলো মিশিয়ে ও ink মিশিয়ে রং তৈরির পার্থক্য এবং RGB/CMYK/HSI-এর ব্যবহার লিখতে হবে।

**Short answer (English):** A color image represents colors using multiple components. RGB is additive and is used for displays, while CMY/CMYK is subtractive and is used for printing; HSI is useful for color-based analysis and segmentation.

**বাংলায় বুঝিয়ে বলা:** Color image সাধারণত Red, Green, Blue-এর মতো একাধিক component দিয়ে তৈরি হয়। Screen আলো যোগ করে রং তৈরি করে, তাই RGB; printer-এর ink আলো শোষণ করে, তাই CMY/CMYK উপযোগী। HSI-তে রঙের ধরন ও উজ্জ্বলতা আলাদা করে দেখা যায়, তাই color-based segmentation সহজ হতে পারে।

## Q1(d) — Data Redundancy
**Reference:** PDF p.2, Spring 2025 Q1(d)

**Question:** What is data redundancy in images? Name its three main types, explain variable-length coding, and state how relative data redundancy is calculated.

**প্রশ্নে কী করতে হবে:** Redundancy-এর অর্থ, তিনটি ধরন, variable-length code-এর কাজ এবং relative redundancy-এর formula লিখতে হবে।

**Short answer (English):** The three types are coding, interpixel and psychovisual redundancy. Variable-length coding reduces coding redundancy by assigning shorter codes to more frequent symbols.

$$
R_D=1-\frac{1}{C_R}
$$

**বাংলায় বুঝিয়ে বলা:** Redundancy মানে image-এর data-তে এমন পুনরাবৃত্তি বা কম-প্রয়োজনীয় অংশ থাকা, যা কম data দিয়ে প্রকাশ করা যায়। Coding redundancy-তে code-এর bit কমানো হয়; interpixel redundancy-তে কাছাকাছি pixel-এর মিল কাজে লাগে; psychovisual redundancy-তে মানুষের চোখে কম গুরুত্বপূর্ণ তথ্য বাদ দেওয়া যায়। $C_R$ হলো original size ÷ compressed size, আর $R_D$ হলো relative redundancy।

## Q1(e) — Edge Detection, NMS and Region Growing
**Reference:** PDF p.2, Spring 2025 Q1(e)

**Question:** State the goal of edge detection, name two gradient-based operators, explain non-maximum suppression in Canny, and define Region Growing.

**প্রশ্নে কী করতে হবে:** Edge detection-এর উদ্দেশ্য, দুটি edge operator, Canny-এর NMS ধাপ এবং Region Growing-এর অর্থ লিখতে হবে।

**Short answer (English):** Edge detection finds sharp intensity changes, and Sobel and Prewitt are gradient-based operators. Non-maximum suppression thins edges, while Region Growing groups connected pixels with similar properties.

**বাংলায় বুঝিয়ে বলা:** Edge সাধারণত object-এর boundary বা intensity হঠাৎ বদলে যাওয়ার জায়গা। Sobel ও Prewitt horizontal/vertical intensity change মাপে। NMS মোটা edge response থেকে সবচেয়ে শক্তিশালী point রেখে edge-কে পাতলা করে; Region Growing seed pixel থেকে কাছাকাছি মিল থাকা pixel যোগ করে region তৈরি করে।

## Q1(f) — Dilation, Opening and Closing
**Reference:** PDF p.2, Spring 2025 Q1(f)

**Question:** Define dilation for a binary image, explain opening and closing, and state what closing does to small holes.

**প্রশ্নে কী করতে হবে:** Dilation-এর mathematical definition, Opening/Closing-এর ক্রম এবং Closing-এর ব্যবহার লিখতে হবে।

**Short answer (English):** Dilation expands foreground objects and erosion shrinks them. Opening is erosion followed by dilation; closing is dilation followed by erosion, and closing can fill small holes or gaps.

**বাংলায় বুঝিয়ে বলা:** Binary image-এ foreground সাধারণত 1-valued object। Dilation object-কে বড় করে, আর erosion ছোট করে। Opening ছোট foreground noise সরাতে কাজে লাগে; Closing object-এর ছোট hole বা সরু gap বন্ধ করতে সাহায্য করে।

## Q2(c)(iii) — RLE on Alternating Pixels
**Reference:** PDF p.3, Spring 2025 Q2(c)(iii)

**Question:** Explain RLE performance on an alternating row such as `ABABAB...`.

**প্রশ্নে কী করতে হবে:** পরপর একই symbol না থাকলে Run-Length Encoding কার্যকর হয় কি না ব্যাখ্যা করতে হবে; byte গণনার অংশ numerical।

**Short answer (English):** RLE is inefficient for alternating pixels because each pixel forms a separate run. The encoded data can be larger than the original.

**বাংলায় বুঝিয়ে বলা:** RLE একই symbol পরপর কতবার এসেছে তা `(symbol, count)` দিয়ে রাখে। `ABABAB...`-এ প্রতিটি run-এর length 1, তাই compression হয় না; count লেখার অতিরিক্ত খরচে file আরও বড় হতে পারে।

## Q2(d)(iii) — Hough Transform
**Reference:** PDF p.3, Spring 2025 Q2(d)(iii)

**Question:** Derive the polar representation of a line used in Hough Transform and explain why it is preferred.

**প্রশ্নে কী করতে হবে:** Hough Transform-এ line-এর polar equation এবং slope-intercept form-এর তুলনায় এর সুবিধা লিখতে হবে।

**Short answer (English):**

$$
\rho=x\cos\theta+y\sin\theta
$$

This form represents vertical and horizontal lines without the slope problem of $y=mx+c$, making line detection easier.

**বাংলায় বুঝিয়ে বলা:** এখানে $\rho$ হলো origin থেকে line-এর লম্ব দূরত্ব এবং $\theta$ হলো সেই লম্বের angle। $y=mx+c$-তে vertical line-এর slope অসীম হয়, কিন্তু polar form-এ সেটিও প্রকাশ করা যায়; তাই Hough Transform-এ এটি সুবিধাজনক।

## Q3(a) — Scanned Document Enhancement for OCR
**Reference:** PDF pp.3–4, Spring 2025 Q3(a)(i–iii)

**Question:** For a scanned document with uneven illumination, faded ink and background noise, choose enhancement methods, a sharpening method, and text/text-line segmentation for OCR.

**প্রশ্নে কী করতে হবে:** দুইটি enhancement technique, Laplacian বনাম Sobel-এর মধ্যে নির্বাচন এবং text ও line আলাদা করার technique বলতে হবে।

### (i) Two enhancement techniques

**Short answer (English):** Use illumination correction and contrast enhancement such as histogram equalization.

**বাংলায় বুঝিয়ে বলা:** Uneven lighting ঠিক করতে background/illumination correction কাজে লাগে। Faded ink-এর contrast বাড়াতে histogram equalization বা contrast stretching ব্যবহার করা যায়।

### (ii) Laplacian or Sobel?

**Short answer (English):** Laplacian sharpening can enhance fine text details and edges. Reduce noise first because sharpening may also amplify noise.

**বাংলায় বুঝিয়ে বলা:** এই প্রশ্নে ছোট text detail স্পষ্ট করা মূল লক্ষ্য, তাই Laplacian যুক্তিযুক্ত পছন্দ। তবে noise আগে কমানো দরকার, কারণ sharpening noise-ও বাড়িয়ে দিতে পারে; Sobel মূলত gradient/edge detection-এ বেশি ব্যবহৃত।

### (iii) Text and text-line segmentation

**Short answer (English):** Use adaptive thresholding to separate text from background and horizontal projection to segment text lines.

**বাংলায় বুঝিয়ে বলা:** Uneven illumination থাকলে adaptive thresholding local area অনুযায়ী threshold বদলায়। এরপর প্রতিটি row-তে foreground pixel গুনে horizontal projection করা যায়; যেখানে লেখা নেই এমন ফাঁকা row দিয়ে line আলাদা করা যায়।

## Q3(c) — Morphology for Satellite Road Images
**Reference:** PDF p.4, Spring 2025 Q3(c)(i–iv)

**Question:** Remove small bright spots, connect small gaps in roads, highlight road boundaries, and say whether boundary highlighting helps separate roads from background.

**প্রশ্নে কী করতে হবে:** প্রতিটি সমস্যা অনুযায়ী morphological operation বেছে নিয়ে কেন তা কাজ করবে, সংক্ষেপে বলতে হবে।

### (i) Remove small bright spots

**Short answer (English):** Use opening, which is erosion followed by dilation. It can remove small bright foreground spots while preserving larger structures.

**বাংলায় বুঝিয়ে বলা:** Erosion ছোট foreground spot মুছে দিতে পারে; এরপর dilation বড় road-এর আকার কিছুটা ফিরিয়ে আনে। Structuring element খুব বড় হলে সরু road-ও ক্ষতিগ্রস্ত হতে পারে, তাই আকার উপযুক্ত নিতে হবে।

### (ii) Connect road gaps

**Short answer (English):** Use closing, which is dilation followed by erosion. It can bridge small gaps and connect nearby road parts.

**বাংলায় বুঝিয়ে বলা:** Dilation road-কে সামান্য প্রসারিত করে কাছের অংশকে ছুঁইয়ে দিতে পারে। Erosion পরে বাইরের অতিরিক্ত প্রসার কমায়; খুব বড় gap সবসময় বন্ধ হবে এমন নয়।

### (iii) Highlight road boundaries

**Short answer (English):** Use the morphological gradient, calculated as dilation minus erosion. It highlights the boundary of foreground objects.

**বাংলায় বুঝিয়ে বলা:** Dilation object-এর বাইরের দিকে বাড়ে, আর erosion ভেতরের দিকে সরে। এই দুই ফলের পার্থক্য boundary-কে highlight করে।

### (iv) Can boundaries distinguish roads from background?

**Short answer (English):** Yes, boundaries help show where roads meet the background. They may need thresholding or region information for reliable separation.

**বাংলা:** Boundary রাস্তা কোথা থেকে শুরু ও শেষ হয়েছে তা বোঝাতে সাহায্য করে। শুধু boundary সবসময় road/background আলাদা করার জন্য যথেষ্ট নয়; intensity বা region information-ও লাগতে পারে।

## Q3(d) — Medical Image Processing
**Reference:** PDF p.4, Spring 2025 Q3(d)

**Question:** Explain how chain code, histogram analysis, Hough Transform and power-law transformation contribute to fracture detection/enhancement in X-ray images.

**প্রশ্নে কী করতে হবে:** চারটি technique-এর কাজ, ব্যবহার বা সীমাবদ্ধতা সংক্ষেপে আলাদা করে বলতে হবে।

**Short answer (English):** Chain code represents bone boundaries, histogram analysis studies intensity distribution, Hough Transform detects lines, and power-law transformation adjusts brightness and contrast.

**বাংলায় বুঝিয়ে বলা:** Chain code bone-এর boundary-র shape বা direction represent করে। Histogram bone ও background-এর intensity distribution বুঝতে সাহায্য করে; Hough Transform রেখার মতো structure খুঁজতে পারে। Power-law transformation brightness/contrast বদলে fracture-এর detail দৃশ্যমান করতে পারে, তবে একা fracture নিশ্চিত করে না।

---

# 2. Fall 2024

**Question Bank PDF pages 5–7**

## Q1(a) — Human Eye and Visual System
**Reference:** PDF p.5, Fall 2024 Q1(a)

**Question:** Describe the functions of the main components of the human eye related to vision.

**প্রশ্নে কী করতে হবে:** চোখের প্রধান অংশগুলোর নাম ও vision-এ তাদের কাজ লিখতে হবে; পরীক্ষায় cross-section sketch-ও চাওয়া হয়েছে।

**Short answer (English):** The iris controls light entry, the lens focuses light, the retina converts light into signals, and the optic nerve carries signals to the brain.

**বাংলায় বুঝিয়ে বলা:** Iris হলো আলো প্রবেশ নিয়ন্ত্রণের অংশ; lens আলোকে retina-তে focus করে। Retina আলো থেকে neural signal তৈরি করে এবং optic nerve সেই signal মস্তিষ্কে পাঠায়।

## Q1(b) — Image Sensor and Image Acquisition
**Reference:** PDF p.5, Fall 2024 Q1(b)

**Question:** Define an image sensor and describe different sensor arrangements used for image acquisition.

**প্রশ্নে কী করতে হবে:** Image sensor-এর সংজ্ঞা এবং single, line ও array arrangement কীভাবে image নেয় তা লিখতে হবে।

**Short answer (English):** An image sensor converts incoming light into electrical signals. Common arrangements use a single sensor, a line sensor, or a two-dimensional sensor array.

**বাংলায় বুঝিয়ে বলা:** Sensor আলোকে electrical signal-এ বদলায়। Single sensor দিয়ে point-by-point scanning, line sensor দিয়ে এক সারি করে এবং 2D array দিয়ে একই সময়ে পুরো image-এর অনেক pixel সংগ্রহ করা যায়।

## Q1(c) — Neighborhood, Connectivity and Regions
**Reference:** PDF p.5, Fall 2024 Q1(c)

**Question:** Briefly describe neighborhood, connectivity and regions of an image pixel.

**প্রশ্নে কী করতে হবে:** Pixel-এর আশপাশের pixel, তাদের সংযোগ এবং region-এর ধারণা বোঝাতে হবে।

**Short answer (English):** A neighborhood is the set of pixels around a pixel. Connectivity defines which pixels are linked, and a region is a connected group of pixels sharing a property.

**বাংলায় বুঝিয়ে বলা:** Neighborhood-এ কোনো pixel-এর আশেপাশের pixel থাকে। Connectivity বলে কোন pixel-কে একে অন্যের সঙ্গে connected ধরা হবে; একই বৈশিষ্ট্যের connected pixel-গুলোর দলকে region বলা হয়।

## Q1(d) — CT Image Reconstruction
**Reference:** PDF p.5, Fall 2024 Q1(d)

**Question:** Describe image reconstruction using Computed Tomography (CT).

**প্রশ্নে কী করতে হবে:** CT কীভাবে বিভিন্ন angle-এর projection ব্যবহার করে cross-sectional image তৈরি করে তা বোঝাতে হবে।

**Short answer (English):** CT collects X-ray projections from multiple angles. A reconstruction algorithm combines these projections to create a cross-sectional image.

**বাংলায় বুঝিয়ে বলা:** শরীরের চারপাশের বিভিন্ন angle থেকে X-ray projection নেওয়া হয়। Computer সেই projection-গুলো মিলিয়ে শরীরের ভেতরের slice বা cross-section তৈরি করে।

## Q2(c) — Gamma Transformation
**Reference:** PDF p.5, Fall 2024 Q2(c), theory subpart

**Question:** Transform pixel intensities using gamma values and discuss the effect of changing $\gamma$.

**প্রশ্নে কী করতে হবে:** Numerical-এ pixel transform করতে হবে; theory অংশে gamma বদলালে brightness কীভাবে বদলায় তা লিখতে হবে।

**Short answer (English):** Gamma transformation is $s=cr^\gamma$. For normalized intensities with $c=1$, $\gamma<1$ brightens the image, while $\gamma>1$ darkens it.

**বাংলায় বুঝিয়ে বলা:** $r$ হলো input intensity আর $s$ হলো output intensity। $\gamma$ কম হলে mid-tone pixel সাধারণত উজ্জ্বল হয়; $\gamma$ বেশি হলে mid-tone অন্ধকার হয়। বাস্তব ফল input range ও $c$-এর ওপরও নির্ভর করে।

## Q3(b)(i) — Histogram Equalization
**Reference:** PDF p.6, Fall 2024 Q3(b)(i)

**Question:** Define histogram equalization, explain its effects, and show that the intensity transformation can produce an approximately uniform PDF.

**প্রশ্নে কী করতে হবে:** Histogram equalization-এর সংজ্ঞা ও contrast-এর প্রভাব লিখতে হবে; প্রশ্নে transformation-এর mathematical derivation-ও চাওয়া হয়েছে।

**Short answer (English):** Histogram equalization uses the cumulative distribution of intensities to improve contrast. It spreads gray levels across a wider range, though a discrete image does not always produce a perfectly uniform histogram.

**বাংলায় বুঝিয়ে বলা:** CDF ব্যবহার করে প্রতিটি পুরোনো gray level-কে নতুন gray level-এ map করা হয়। এতে আগে যে ছোট intensity range-এ pixel বেশি জমা ছিল, তা আরও বড় range-এ ছড়াতে পারে; তবে discrete level ও rounding-এর কারণে histogram পুরোপুরি সমান হওয়া জরুরি নয়।

## Q3(b)(ii) — 2-D Fourier Transform of a Box Function
**Reference:** PDF p.6, Fall 2024 Q3(b)(ii)

**Question:** Derive the 2-D Fourier transform of a box function and draw its magnitude spectrum.

**প্রশ্নে কী করতে হবে:** Box-shaped image function-এর Fourier transform derivation ও magnitude spectrum-এর sketch দিতে হবে।

**Short answer (English):** The Fourier transform of a 2-D rectangular box is the product of two sinc functions. Its magnitude has a central peak with side lobes that decrease away from the center.

**বাংলায় বুঝিয়ে বলা:** Box function-এর horizontal ও vertical dimension আলাদাভাবে transform করলে দুইটি sinc factor পাওয়া যায়। এগুলোর গুণফল 2D spectrum তৈরি করে; centre-এর কাছে low-frequency energy বেশি থাকে, আর পাশে ছোট side lobe থাকে।

## Part B Q1(a) — RGB Color Cube
**Reference:** PDF p.7, Fall 2024 Part B Q1(a)

**Question:** Draw the RGB color cube and explain how colors and gray levels are formed.

**প্রশ্নে কী করতে হবে:** RGB coordinate cube আঁকতে হবে এবং primary color মিশিয়ে color ও gray-level তৈরি হওয়ার নিয়ম লিখতে হবে।

**Short answer (English):** RGB is an additive color model based on red, green and blue light. Equal values of all three components produce gray, while different combinations produce other colors.

**বাংলায় বুঝিয়ে বলা:** RGB-তে তিনটি light component-এর intensity যোগ করে রং তৈরি হয়। তিনটির value সমান হলে black থেকে white পর্যন্ত gray shade হয়; ভিন্ন মানের combination-এ অন্য রং পাওয়া যায়।

## Part B Q1(b) — HSI Color Model
**Reference:** PDF p.7, Fall 2024 Part B Q1(b)

**Question:** Draw the HSI models and explain how HSI represents color.

**প্রশ্নে কী করতে হবে:** Hue, Saturation, Intensity-এর অর্থ ও HSI model কীভাবে color আলাদা করে তা ব্যাখ্যা করতে হবে।

**Short answer (English):** HSI represents color using Hue, Saturation and Intensity. It separates color type and purity from brightness, which can make color analysis easier.

**বাংলায় বুঝিয়ে বলা:** Hue বলে কোন রং, Saturation বলে রং কতটা বিশুদ্ধ বা ফ্যাকাশে, এবং Intensity বলে কতটা উজ্জ্বল। তাই brightness পরিবর্তিত হলেও color information আলাদাভাবে বিশ্লেষণ করা সহজ হয়।

---

# 3. Spring 2024

**Question Bank PDF pages 8–11**

## Q1(a) — Distance Metrics
**Reference:** PDF p.8, Spring 2024 Q1(a)

**Question:** State the properties of a distance metric and describe City Block, Chessboard and Euclidean distances.

**প্রশ্নে কী করতে হবে:** Distance metric-এর নিয়ম এবং তিন ধরনের distance-এর formula লিখতে হবে; point-এর coordinate দেওয়া থাকলে numerical calculation-ও করতে হবে।

**Short answer (English):** A distance metric is non-negative, symmetric, zero only for identical points, and follows the triangle inequality. City Block adds coordinate differences, Chessboard takes their maximum, and Euclidean uses the square root of the sum of squares.

**বাংলায় বুঝিয়ে বলা:** Distance কখনো negative নয়; point A থেকে B ও B থেকে A-এর distance সমান; একই point-এর distance শূন্য; এবং triangle inequality মানে। City Block-এ horizontal ও vertical difference যোগ হয়, Chessboard-এ বড় difference নেওয়া হয়, আর Euclidean-এ সরলরেখার distance পাওয়া যায়।

Formulas:

$$
D_4=|\Delta x|+|\Delta y|
$$

$$
D_8=\max(|\Delta x|,|\Delta y|)
$$

$$
D_E=\sqrt{(\Delta x)^2+(\Delta y)^2}
$$

## Q1(b) — First- and Second-Order Derivatives
**Reference:** PDF p.8, Spring 2024 Q1(b)

**Question:** Define first- and second-order discrete derivatives and explain their relation for a constant-slope ramp.

**প্রশ্নে কী করতে হবে:** দুই derivative কী মাপে এবং constant-slope ramp-এ তাদের value/behavior কেমন হয় তা লিখতে হবে।

**Short answer (English):** The first derivative measures intensity change, while the second derivative measures changes in that rate. For a constant-slope ramp, the first derivative is constant and the second derivative is zero inside the ramp.

**বাংলায় বুঝিয়ে বলা:** First derivative পাশাপাশি pixel-এর intensity কতটা বদলেছে তা দেখায়। Second derivative সেই পরিবর্তনের হার আবার বদলাচ্ছে কি না তা দেখায়; constant slope-এ rate একই থাকে, তাই ramp-এর ভেতরে second derivative শূন্য হয়।

## Q1(c) — Erosion, Dilation, Opening and Closing
**Reference:** PDF p.8, Spring 2024 Q1(c)

**Question:** Write the mathematical equations of erosion and dilation and describe opening and closing.

**প্রশ্নে কী করতে হবে:** Erosion ও dilation-এর mathematical notation এবং Opening/Closing-এর sequence লিখতে হবে।

**Short answer (English):** Dilation expands foreground objects, while erosion shrinks them. Opening is erosion followed by dilation; closing is dilation followed by erosion.

**বাংলায় বুঝিয়ে বলা:** Binary image-এ foreground সাধারণত 1-valued object। Dilation তার এলাকা বাড়ায়, erosion কমায়। Opening ছোট object/noise সরাতে পারে; Closing ছোট hole বা gap বন্ধ করতে সাহায্য করে।

$$
A\circ B=(A\ominus B)\oplus B
$$

$$
A\bullet B=(A\oplus B)\ominus B
$$

## Q1(d) — Color Model Selection
**Reference:** PDF p.8, Spring 2024 Q1(d)

**Question:** Which color model is appropriate for color printing and computer displaying? Explain why.

**প্রশ্নে কী করতে হবে:** Printing ও display-এর জন্য উপযুক্ত color model নির্বাচন করে কারণ লিখতে হবে।

**Short answer (English):** CMY/CMYK is suitable for printing because inks subtract light. RGB is suitable for displays because screens add red, green and blue light.

**বাংলায় বুঝিয়ে বলা:** Printer-এর ink আলো শোষণ করে, তাই subtractive CMY/CMYK model ব্যবহৃত হয়। Monitor/pixel লাল, সবুজ, নীল আলো যোগ করে রং বানায়, তাই সেখানে additive RGB উপযুক্ত।

## Q1(e) — Canny Hysteresis Thresholding
**Reference:** PDF p.8, Spring 2024 Q1(e)

**Question:** What is hysteresis thresholding? What are false positive and false negative edge pixels, and how does Canny handle them?

**প্রশ্নে কী করতে হবে:** Hysteresis-এর কাজ এবং ভুল edge শনাক্ত হওয়ার দুই ধরন ব্যাখ্যা করতে হবে।

**Short answer (English):** Hysteresis uses high and low thresholds to keep strong edges and weak edges connected to them. False positives are incorrect edges; false negatives are real edges that were missed.

**বাংলায় বুঝিয়ে বলা:** High threshold-এর ওপরে থাকা pixel strong edge হিসেবে ধরা হয়, আর low ও high-এর মাঝখানের weak edge তখনই রাখা হয় যখন তা strong edge-এর সঙ্গে connected। এতে একা থাকা noise edge কমে এবং সত্যিকারের edge-এর connected অংশ বাঁচতে পারে।

## Q3(a)(i) — Removing Salt-and-Pepper Noise
**Reference:** PDF p.10, Spring 2024 Q3(a)(i)

**Question:** An image is corrupted by salt-and-pepper noise in the object region; state the best way to denoise it and explain.

**প্রশ্নে কী করতে হবে:** কালো ও সাদা impulse noise দূর করার উপযুক্ত filtering technique ও কারণ লিখতে হবে।

**Short answer (English):** A Median Filter is suitable because it replaces each pixel with the median of its neighborhood. It removes extreme noise values while often preserving edges better than averaging.

**বাংলায় বুঝিয়ে বলা:** Salt-and-pepper noise-এ কিছু pixel হঠাৎ 0 বা সর্বোচ্চ intensity হয়ে যায়। Median Filter neighborhood সাজিয়ে middle value নেয়, তাই ওই অস্বাভাবিক extreme value অনেক সময় বাদ পড়ে যায়।

## Q3(a)(ii) — Morphological Noise Removal
**Reference:** PDF p.10, Spring 2024 Q3(a)(ii)

**Question:** Which morphological operation would you use to eliminate small unwanted foreground noise?

**প্রশ্নে কী করতে হবে:** ছোট foreground noise সরানোর morphological operation ও তার process বলতে হবে।

**Short answer (English):** Opening can remove small foreground objects. It performs erosion followed by dilation.

**বাংলায় বুঝিয়ে বলা:** Erosion ছোট foreground spot মুছে দিতে পারে। এরপর dilation বড় object-কে কিছুটা ফিরিয়ে আনে; structuring element সঠিক না হলে ছোট দরকারি detail-ও হারাতে পারে।

## Q3(d) — Chain-Code Invariance
**Reference:** PDF p.10, Spring 2024 Q3(d)

**Question:** Explain how to make a boundary chain code invariant to both starting point and rotation.

**প্রশ্নে কী করতে হবে:** Starting point ও rotation পরিবর্তন হলেও shape-এর representation কীভাবে তুলনাযোগ্য রাখা যায় তা বলতে হবে; প্রশ্নে final chain-code calculation-ও আছে।

**Short answer (English):** Starting-point invariance can be obtained by choosing the smallest circular shift of the chain code. Rotation invariance can be obtained by using the first difference of the chain-code directions and then normalizing the circular sequence.

**বাংলায় বুঝিয়ে বলা:** Boundary-কে কোন pixel থেকে শুরু করে লেখা হচ্ছে, সেটা বদলালে chain code ঘুরে যেতে পারে; circular shift-এর মধ্যে canonical/ছোট representation বেছে নিলে starting-point effect কমে। Shape ঘুরলে direction numbers বদলায়; consecutive direction-এর difference নিলে পুরো code-এ একই rotation offset যোগ হওয়ার প্রভাব দূর করা যায়।

---

# 4. Fall 2023

**Question Bank PDF pages 12–15**

## Q1(a) — Image Histogram
**Reference:** PDF p.12, Fall 2023 Q1(a)

**Question:** What is an image histogram? Can an image be reconstructed from its histogram, and how does it look for dark, bright, low-contrast and high-contrast images?

**প্রশ্নে কী করতে হবে:** Histogram-এর সংজ্ঞা, histogram থেকে original image ফেরত পাওয়া যায় কি না, এবং brightness/contrast অনুযায়ী histogram-এর অবস্থান বলতে হবে।

**Short answer (English):** A histogram shows the frequency of each gray level. It usually cannot reconstruct the original image because it does not preserve pixel positions; dark and bright images concentrate at low and high intensities, respectively.

**বাংলায় বুঝিয়ে বলা:** Histogram বলে কোন intensity কতবার আছে, কিন্তু কোন pixel কোথায় ছিল তা বলে না; তাই একই histogram-এর অনেক ভিন্ন image হতে পারে। Dark image-এ bar সাধারণত low gray level-এ, bright image-এ high gray level-এ থাকে। Low contrast-এ intensity ছোট range-এ জমা হয়; high contrast-এ wider range ব্যবহার হয়।

## Q1(b) — Negative Transformation and Intensity-Level Slicing
**Reference:** PDF p.12, Fall 2023 Q1(b)

**Question:** Write short notes on negative transformation and intensity-level slicing.

**প্রশ্নে কী করতে হবে:** দুইটি intensity transformation-এর কাজ এবং negative-এর formula লিখতে হবে।

**Short answer (English):** Negative transformation reverses intensity using $s=(L-1)-r$. Intensity-level slicing highlights a selected range of gray levels.

**বাংলায় বুঝিয়ে বলা:** Negative image-এ উজ্জ্বল অংশ অন্ধকার এবং অন্ধকার অংশ উজ্জ্বল হয়। Intensity-level slicing-এ নির্দিষ্ট range-এর pixel-কে highlight করা হয়, যাতে প্রয়োজনীয় feature সহজে দেখা যায়।

## Q1(c) — RGB Color Cube
**Reference:** PDF p.12, Fall 2023 Q1(c)

**Question:** Draw the RGB color cube and explain how colors and gray scales are formed.

**প্রশ্নে কী করতে হবে:** RGB cube-এর তিনটি axis এবং color/gray তৈরির নিয়ম বলতে হবে।

**Short answer (English):** RGB combines red, green and blue light. Equal values of all three components produce gray, while different values produce different colors.

**বাংলায় বুঝিয়ে বলা:** R, G ও B তিনটি component-এর intensity যোগ করে রং তৈরি হয়। তিনটির মান সমান হলে gray shade হয়; মান ভিন্ন হলে অন্য রং পাওয়া যায়।

## Q1(d) — Image Compression and Data Redundancy
**Reference:** PDF p.12, Fall 2023 Q1(d)

**Question:** Why do we need image compression? Name and briefly describe the types of data redundancy.

**প্রশ্নে কী করতে হবে:** Compression-এর প্রয়োজন এবং redundancy-এর তিনটি ধরন সংক্ষেপে লিখতে হবে।

**Short answer (English):** Image compression reduces storage and transmission requirements. The three main types of redundancy are coding, interpixel and psychovisual redundancy.

**বাংলায় বুঝিয়ে বলা:** Image/video file বড় হওয়ায় storage ও network bandwidth বেশি লাগে; compression data size কমায়। Coding redundancy code-এর bit কমানোর সুযোগ, interpixel redundancy কাছাকাছি pixel-এর মিল, আর psychovisual redundancy মানুষের চোখে কম গুরুত্বপূর্ণ তথ্য বোঝায়।

## Q1(e) — Segmentation and Canny Steps
**Reference:** PDF p.12, Fall 2023 Q1(e)

**Question:** Name segmentation types based on intensity properties and list the steps of Canny Edge Detection.

**প্রশ্নে কী করতে হবে:** Intensity-এর ভিত্তিতে segmentation-এর দুইটি মূল ধারণা ও Canny-এর ধাপগুলো লিখতে হবে।

**Short answer (English):** Segmentation can use intensity discontinuities or similarities. Canny performs smoothing, gradient calculation, non-maximum suppression, double thresholding and edge tracking by hysteresis.

**বাংলায় বুঝিয়ে বলা:** Discontinuity-ভিত্তিক method edge-এর মতো হঠাৎ পরিবর্তন খোঁজে; similarity-ভিত্তিক method মিল থাকা pixel একত্র করে। Canny আগে noise smooth করে, তারপর gradient বের করে, edge পাতলা করে এবং threshold/hysteresis দিয়ে final edge বেছে নেয়।

## Q2(b)(iii) — Can Max or Min Filter Remove Salt-and-Pepper Noise?
**Reference:** PDF p.13, Fall 2023 Q2(b)(iii)

**Question:** Can salt-and-pepper noise be removed by applying only a Max or Min Filter? Justify.

**প্রশ্নে কী করতে হবে:** শুধু Max বা Min filter ব্যবহার করলে দুই ধরনের noise ঠিকমতো দূর হয় কি না কারণসহ বলতে হবে।

**Short answer (English):** No; a Max Filter may suppress dark pepper noise but spread bright salt noise, while a Min Filter may do the opposite. A Median Filter is generally better for both.

**বাংলায় বুঝিয়ে বলা:** Max Filter আশপাশের maximum নেয়, তাই কালো outlier-এর জায়গায় উজ্জ্বল value আসতে পারে; কিন্তু সাদা noise ছড়িয়ে যেতে পারে। Min Filter এর উল্টো কাজ করে; তাই salt-and-pepper noise-এর জন্য Median Filter সাধারণত বেশি উপযুক্ত।

## Q3(a)(ii–iii) — Canny Edge Detection and Thresholds
**Reference:** PDF p.14, Fall 2023 Q3(a)(ii–iii)

**Question:** Identify false positive/false negative edges and explain the effect of choosing very high and very low thresholds in Canny.

**প্রশ্নে কী করতে হবে:** ভুলভাবে পাওয়া edge ও বাদ পড়া edge-এর পার্থক্য এবং threshold খুব বেশি বা কম হলে কী ঘটে তা লিখতে হবে।

**Short answer (English):** A false positive is a non-edge marked as an edge, while a false negative is a real edge that is missed. Very high thresholds can miss weak real edges; very low thresholds can accept noise as edges.

**বাংলায় বুঝিয়ে বলা:** False positive হলে যেখানে আসল boundary নেই সেখানেও edge ধরা হয়; false negative হলে আসল boundary বাদ পড়ে। High threshold বেশি কঠোর, তাই weak edge হারাতে পারে; low threshold খুব শিথিল হলে noise-ও edge হিসেবে ঢুকে যায়।

## Q3(b)(i) — Separating Touching Coins
**Reference:** PDF p.14, Fall 2023 Q3(b)(i)

**Question:** Which morphological operations can separate touching coins for accurate counting?

**প্রশ্নে কী করতে হবে:** পাশাপাশি লেগে থাকা coin আলাদা করতে কোন operation ব্যবহার করা যায় এবং কেন, তা বলতে হবে।

**Short answer (English):** Erosion can break narrow connections between touching coins. Dilation may restore their size, while watershed can help separate touching objects more reliably.

**বাংলায় বুঝিয়ে বলা:** Coin দুটির মাঝখানে সরু foreground bridge থাকলে erosion সেটি ভাঙতে পারে। পরে dilation দিয়ে object-এর আকার ফিরিয়ে আনা যায়; coin বেশি লেগে থাকলে distance transform ও watershed segmentation আরও উপযুক্ত হতে পারে।

## Q3(b)(ii) — Removing Small Particles
**Reference:** PDF p.14, Fall 2023 Q3(b)(ii)

**Question:** Which morphological operations remove small particles while preserving larger particles?

**প্রশ্নে কী করতে হবে:** ছোট particle মুছে বড় particle রাখার operation ও কারণ বলতে হবে।

**Short answer (English):** Opening can remove small foreground particles when the structuring element is chosen properly. Larger particles remain if they are large enough to survive erosion.

**বাংলায় বুঝিয়ে বলা:** Opening-এর প্রথম ধাপ erosion ছোট object-কে মুছে দিতে পারে, এরপর dilation বড় object-কে কিছুটা restore করে। Structuring element খুব বড় হলে প্রয়োজনীয় ছোট detail-ও হারাতে পারে।

---

# Quick Revision — One-Line Answers

| Topic | মনে রাখার কথা |
|---|---|
| Sharpening | Enhances fine details and edges |
| 4-connectivity | Up, down, left, right |
| 8-connectivity | Direct + diagonal neighbors |
| m-connectivity | Diagonal link with an extra condition |
| RGB | Additive; displays |
| CMY/CMYK | Subtractive; printing |
| HSI | Separates hue, saturation and intensity |
| Redundancy | Coding, interpixel, psychovisual |
| RLE | Works best with repeated consecutive symbols |
| Hough Transform | $\rho=x\cos\theta+y\sin\theta$ |
| Opening | Erosion → Dilation |
| Closing | Dilation → Erosion |
| Median Filter | Good for salt-and-pepper noise |
| Canny | Smoothing → Gradient → NMS → Double threshold → Hysteresis |
| Histogram | Frequency of gray levels |
| Negative transform | $s=(L-1)-r$ |
| Gamma | Controls brightness response |
| CT | Multiple X-ray projections produce cross-sectional images |

## Exam tip

যদি প্রশ্নে **Define, Explain, Differentiate, Why** থাকে, short answer ও বাংলা ব্যাখ্যার মূল point লিখবে। **Derive, Draw, Calculate, Apply** থাকলে শুধু theory লিখে থেমো না—প্রয়োজনীয় formula, diagram বা calculation-ও দেখাবে।
