*Coffeereview.com*

*Data documentation template adapted by Hannes Datta.* 

*Originally based on Gebru, Morgenstern, Vecchione, Vaughan,* 

*Wallach, Daumeé, and Crawford. (2018). Datasheets for Datasets.*

*1\.		Motivation* 

*1.1	What primary research question, business problem, or knowledge gap motivated the creation of this dataset (“data context”)? How does the dataset offer insights into new phenomena, contribute to developing new models, or streamline gathering essential information? Why is this dataset valuable to the broader research community or industry stake-holders?* 

**Research question:** 

What tasting notes are most associated with highly rated coffees?

Does the price of coffee influence its rating?

Since the 12th century, coffee has been a much-loved drink that has become an integral part of everyday life. With developments in speciality and sustainable production and increasing prosperity, coffee has become a drink with many different flavours. Partly as a result of these developments, coffee consumption continues to grow. Partly due to these developments, coffee consumption continues to grow with around two billion cups per day De Freitas (n.d.). This growing demand for high quality coffee has led to a wider and more diverse market, with speciality coffee shops continuing to search for the best beans to meet the demanding tastes of consumers.

By analyzing the tasting notes linked to highly rated coffees, researchers can identify flavor profiles that are most popular under experts. Experts can use this information for for instance coffee shops and inform marketing strategies and product development to align with consumer tastes.

The structured nature of the dataset allows for the application of machine learning algorithms to predict coffee ratings based on tasting notes. For instance, a study titled by Lohse et al. (2023) utilized textual data from certified coffee reviews to accurately predict corresponding scores, demonstrating the potential for developing predictive models in this domain.

The dataset consolidates comprehensive information on various coffee attributes, including origin, roast level, and tasting notes, in a standardized format. This consolidation facilitates efficient data collection and analysis, reducing the time and resources required for people interested in high-end coffee to gather essential information. 

The dataset enables the examination of trends in coffee preferences over time, assisting businesses in staying ahead of market shifts and adapting their offerings accordingly. By understanding the tasting notes associated with higher ratings, producers can focus on cultivating and promoting coffee profiles that are more likely to achieve favorable reviews, thereby enhancing product quality and consumer satisfaction.

*1.2	Please compare the various websites and APIs you assessed relevant to your data context. A table may help to compare data sources. Why did you choose your specific data source? Discuss the research fit, extraction method (e.g., web scraping vs. APIs), efficiency of resource use, and any other factors that made it emerge as the best choice. For tips, see challenges 1.1 and 1.2 in Boegershausen et al. 2022\.*

### Assessment of Websites and APIs for Data Collection

Before selecting a primary data source, several potential alternatives were evaluated, considering their content quality, accessibility, and relevance to this research.

| Website/API | Type | Pros | Cons |
| ----- | ----- | ----- | ----- |
| Coffee Review ([www.coffeereview.com](http://www.coffeereview.com)) | Ratings & Reviews | Established authority, detailed cupping scores, organised structure, large dataset (8200+) | Rated by one party, potential scraping restrictions |
| Pull & Pour Coffee ([www.pullandpourcoffee.com](http://www.pullandpourcoffee.com)) | Blog & Reviews | In-depth reviews, expert insights, niche specialty coffee focus, detailed cupping scores, organised structure | Rated by one party, requires web scraping, no structured API, limited dataset (433) |
| Coffee Judge ([www.coffeejudge.co.uk/archive/202112](https://www.coffeejudge.co.uk/archive/202112)) | Consumer Reviews | UK-based coffee reviews, diverse product evaluations, rated by multiple consumers, structured dataset | Limited dataset (169), community-driven, reviews may not be as detailed, no cupping scores |
| The Love of Coffee ([https://www.theloveofcoffee.co.uk/customer-reviews-61-c.asp](https://www.theloveofcoffee.co.uk/customer-reviews-61-c.asp)) | Customer Reviews | User-generated coffee reviews, UK-focused insights, structured dataset | Lacks expert evaluations, only positive reviews, no cupping scores |
| Coffee Roast ([https://coffeeroast.com/](https://coffeeroast.com/)) | Community Ratings | User-driven ratings and reviews of coffee roasts, structured dataset | Community-driven, may lack expert analysis, no cupping scores |
| Reddit r/coffee ([https://www.reddit.com/r/Coffee/comments/1ilccyy/mod\_the\_daily\_question\_thread/](https://www.reddit.com/r/Coffee/comments/1ilccyy/mod_the_daily_question_thread/))  | User Discussions | Diverse opinions, community-driven trends | Unstructured data, hard to filter relevant content |
| Amazon Product Reviews API | E-commerce | Structured product data, user sentiment analysis  | Focused on mass-market coffee, lacks specialty insights, scraping limitations |
| Twitter API (X API) | Social Media | Real-time trends and opinions | Requires NLP for meaningful insights, API rate limits, scraping limitations |

After evaluating the potential data sources above, CoffeeReview.com emerged as the best choice for answering our research question: “What tasting notes are most associated with highly rated coffees?”. Below are the key reasons for its selection.

**Research Fit:** 

CoffeeReview.com is Highly Relevant to Our Study as it provides reviews written by industry professionals rather than casual consumers, ensuring a high degree of reliability and credibility. This makes it a strong data source for research on specialty coffee tasting notes and their correlation with high ratings. Each review on the platform includes a cupping score (scale on which coffee is rated) and a structured list of flavor descriptors, allowing us to systematically analyze which tasting notes are most commonly associated with highly rated coffees. The combination of quantitative (numerical ratings) and qualitative (tasting notes) data ensures that our study can incorporate both statistical analysis and in-depth insights into flavor trends.

**Extraction Method:** Web Scraping is Feasible and Efficient

Since CoffeeReview.com does not offer an API, we will extract data using web scraping techniques. The consistent structure of the website, where each review follows a fixed format with labeled tasting notes and numerical scores, makes it particularly suitable for scraping. This is far more efficient than extracting data from unstructured sources like Reddit or Twitter, which would require extensive Natural Language Processing (NLP) techniques to filter and standardize tasting notes. Furthermore, unlike platforms that impose strict scraping limitations (Amazon, Twitter), CoffeeReview.com’s data remains accessible for careful extraction, provided that ethical and legal guidelines are followed.

**Efficiency of Resource Use:** Maximizing Research Value

Using CoffeeReview.com allows for time-efficient data collection compared to sources like Reddit, where significant NLP preprocessing would be required, or Amazon, which lacks tasting notes relevant to specialty coffee. The dataset is high quality, consisting of expert reviews with standardized tasting descriptors, reducing data noise and inconsistency. Additionally, CoffeeReview.com covers a wide range of specialty coffee brands and varieties, making it a more comprehensive source compared to mass-market platforms like Amazon, which primarily features commodity-grade coffee.

Why Not Other Platforms?

While Pull & Pour Coffee provides in-depth reviews of specialty coffee, it has a smaller dataset and lacks a structured rating system like CoffeeReview.com. Reddit and Twitter contain valuable discussions on coffee preferences, but their unstructured nature makes extracting meaningful insights resource-intensive, requiring advanced NLP techniques to interpret user-generated tasting notes. Amazon and Coffee Roast primarily feature consumer-driven ratings, which focus more on basic product satisfaction rather than detailed cupping scores and tasting profiles. Lastly, UK-based sources like Coffee Judge and The Love of Coffee provide a regional perspective, but their coverage is limited compared to the global specialty coffee insights available on CoffeeReview.com.

Thus, CoffeeReview.com was selected as the primary data source because it offers expert-driven coffee ratings rather than general consumer opinions, ensuring a high level of credibility and consistency. The platform provides structured cupping scores and tasting notes, allowing for efficient trend analysis without the need for extensive data cleaning or interpretation. Additionally, web scraping is feasible on this site, requiring minimal Natural Language Processing (NLP) or preprocessing, unlike unstructured sources such as social media or user reviews. With a large dataset of over 8200 high-quality specialty coffee reviews ranging from 1997 till now, CoffeeReview.com is highly relevant to our research question, enabling a data-driven analysis of which flavors are most commonly associated with highly rated coffees. These factors make it the most relevant, structured, and resource-efficient choice for our study.

*1.3	Please identify potentially relevant contextual information (Boegershausen et al. 2022, challenge 1.3). Provide an overview here and save any relevant information in the digital submission of your project.*

Below is an overview of potentially relevant contextual information, as recommended by Boegershausen et al. (2022, challenge 1.3). Any significant  details have been documented and saved in the digital submission of our project.

*Table 2: contextual information*

| Dimension | Condition/Version | Condition Description | Observed Differences on Landing Page | Observed Differences on Review Page |
| ----- | ----- | ----- | ----- | ----- |
| **OS** | Windows vs. Mac | Tested on Windows 11 and macOS Sequoia 15.3.1 | None  | None |
| **Browser** | Chrome vs. Safari | Chrome and Safari on Mac | None | None |
| **Website Version** | Today vs. Archived | Current site on 14/02/2025 vs. archived versions on  [https://web.archive.org/](https://web.archive.org/) (Wayback Machine)  | Minor layout changes (historical) | Minor layout changes (historical) |
| **VPN Status** | Off vs. On – Germany  | Surfshark VPN connected to Germany | None | None |
| **VPN Status** | Off vs. On – Belgium | Surfshark VPN connected to Belgium | None | None |
| **VPN Status** | Off vs. On – Netherlands | Surfshark VPN connected to Netherlands | None | None |

**How we identified  relevant contextual information:**

We conducted a comprehensive comparison of CoffeeReview.com across several dimensions to assess potential differences in user interface and functionality. The dimensions tested included operating system (OS), browser type, website version, and VPN status.

For the OS dimension, we compared the website’s appearance on Windows 11 and macOS Sequoia 15.3.1 and found no observable differences on either the landing page or the review pages. This indicates that CoffeeReview.com maintains a consistent design and functionality regardless of the operating system used.

Under the browser dimension, we tested the site on Chrome and Safari (both on Mac) and observed no differences in layout, navigation, or content display. This consistency suggests that CoffeeReview.com is optimized for cross-browser compatibility.

We also compared the current version of the website (as of 14/02/2025) with archived versions from the Wayback Machine. Minor layout changes were noted on both the landing and review pages, reflecting historical design updates. However, the core structure and functionality remained unchanged, ensuring the stability of data extraction over time.

For the VPN status dimension, we tested the website with Surfshark VPN connected to the Netherlands, Germany and Belgium. In all three cases, no differences were observed in the interface, language, or content presentation on the landing and review pages. This suggests that CoffeeReview.com does not employ geolocation-based customization or region-specific modifications.

Overall, the consistency across all tested dimensions enhances the reliability and efficiency of our web scraping process, as no regional, device-specific, or historical variations need to be accounted for. This uniformity supports the validity of our research on tasting notes and coffee ratings.

**Why this is important:**

While CoffeeReview.com currently maintains a consistent interface and source code across different locations and devices, it is important to consider a scenario in which the website’s layout or source code changes, which may cause our web scraper to no longer function correctly. Web scraping relies on the structure and organization of HTML elements to accurately extract data. Any modifications to the site’s design, such as changes in class names, tag hierarchies, or the introduction of dynamic content, could disrupt our data extraction process.

This risk is particularly relevant because website owners frequently update their platforms for various reasons, including design enhancements, user experience improvements, or security measures. Even minor adjustments to the site’s HTML or CSS could render our scraper ineffective or lead to inaccurate data collection. In the worst-case scenario, our scraper might fail to retrieve any data or, worse, collect incorrect information that could compromise the validity of our research.

To mitigate this risk, we are documenting the version of CoffeeReview.com that our scraper is built for by providing detailed screenshots of the website as it appeared during development. These screenshots capture the specific layout, class names, and structural elements we relied on. By doing so, we create a visual reference that allows future developers to quickly identify if and when the website's design has changed. This also facilitates the debugging process and helps in updating the scraper to accommodate any modifications.

Additionally, these screenshots serve as evidence of the original data context, ensuring transparency and reproducibility of our research findings. If the website undergoes significant changes, we will have a clear record of the environment under which our data was collected, preserving the integrity of our analysis.

In conclusion, while CoffeeReview.com currently provides a stable and consistent interface, we acknowledge the potential risk of future changes. By proactively documenting the website’s appearance and structure, we aim to safeguard the reliability and continuity of our data extraction and analysis process, ensuring that our research remains accurate and valid even if the website is updated.

*1.4	Who created this dataset (e.g., which team). Mention you are students of the Marketing Analytics program at Tilburg University.*

This dataset was developed by Team 2 as part of the Online Data Collection and Management course, offered by Hannes Datta. This course is an integral part of the Master's program in Marketing Analytics at Tilburg University, where students gain hands-on experience in data collection, management, and analysis. The project reflects our team's commitment to applying the theoretical knowledge gained during the program to real-world challenges in data-driven marketing research.

*2\.		Data Extraction Plan*

*→ This should belong in this section*

*1.3	Please identify potentially relevant contextual information (Boegershausen et al. 2022, challenge 1.3). Provide an overview here and save any relevant information in the digital submission of your project.*

*See different user interfaces (different EN instead of NL) and for mac or windows, phone or laptop. Site looks like this today, but the interface can change which influences the webscraping.*   
*We can provide screenshots of how it looks now.* 

*How reliable / generalizable is the data, if another group is going to scrape e.g.* 

1. ***Overview of the Data Collection Methodology**: Describe the overall approach your team used to gather data. This can include web scraping techniques, the use of APIs, or any other data collection methods. Be clear about why you chose these methods for your specific research context or business idea.*

We use web scraping to collect coffee reviews from [CoffeeReview.com](https://www.coffeereview.com/) as it provides **detailed tasting notes and ratings**, which are crucial for our research question: “What tasting notes are most associated with highly rated coffees?” Since the website lacks a public API, scraping allows us to extract and structure this data efficiently. Using Python with BeautifulSoup and Requests, we automate data collection, ensuring scalability and accuracy. This method is cost-effective, allowing us to analyze large volumes of reviews, identify trends, and uncover correlations between tasting notes and high ratings in a structured, data-driven manner.

2. ***Tools and Technologies Used**: Provide a list of the programming languages, libraries, and tools that were utilized in the data collection process. For example, if you used Python with Beautiful Soup for web scraping, or if you connected to third-party APIs using requests, include this information.*

*We used Python with Beautiful Soup from the bs4 library for the collection and processing of our data. Python is a well versed programming language with many applications. It allows for importing packages which saves a great amount of time and smooths the collection process. Beautiful* 

*The request package is used for accessing the url and the json package is used to store the data once collected.* 

3. ***Step-by-Step Process**: Outline the specific steps taken to collect the data. This can involve detailing how you accessed the web pages or APIs, what kind of data was extracted, and any pre-processing steps that were performed on the data (like cleaning or formatting).*

4. ***Challenges and Solutions**: Discuss any challenges your team faced during the data collection process, and how you resolved them. This could relate to technical issues, data accessibility, or issues with the accuracy of data.*

5. ***Ethical Considerations**: Highlight any ethical considerations that were taken into account during the data collection process. Discuss how you ensured the protection of personal information, any anonymization measures you implemented, and adherence to relevant data protection regulations.*

*In our web scraping process, we ensured ethical data collection by extracting only publicly available information from CoffeeReview.com while avoiding personal data. We respected the website’s guidelines by reviewing its robots.txt file and limiting request frequency to prevent server strain. All data was anonymized, focusing only on aggregated tasting notes and ratings without linking them to individuals.* 

6. ***Final Checks**: Confirm that final checks were conducted on the collected data to ensure accuracy and reliability. Explain how you verified that the data was indeed valid and useful for your project objectives.*

*2.1	Please describe your data extraction plan in such a way that another researcher or team could replicate your data collection process. Which information to extract from which pages, how to sample, at which frequency to extract the data, and how to process the data during the collection. In your description, explain how you tackled the various validi-ty, legal/ethical, and technical challenges. See Boegershausen et al. (2022, challenges 2.1-2.4) for tips.*

*2.2	Does the dataset contain data that might be considered confidential or sensitive (e.g., personal data such as usernames or IP addresses, data that reveals racial or ethnic origins, sexual orientations, religious beliefs, political opinions or union memberships, financial or health data, biometric or genetic data, social security numbers, passwords, etc.)? If so, please provide a description.*

*2.3 If the dataset relates to people, is it possible to identify individuals (i.e., one or more natural persons), either directly or indirectly (i.e., in combination with other data) from the dataset? If so, please describe how.*

*3\.		Data Extraction Process*

*3.1	When was the data collected?* 

*3.2 	Please describe any technical challenges you encountered while scaling your data collection. How did you resolve them? Please provide a clear explanation of the debugging process (see Boegershausen et al. 2022, challenge 3.1).*

*3.3 	What measures or monitoring systems were in place to ensure and validate the quality of the extracted data? Can you describe how these monitoring systems functioned? (see Boegershausen et al. 2022, challenge 3.2).*

*3.4 	Can you specify the infrastructure you used for the deployment and execution of your data collection?*

*4\.		Preprocessing, cleaning, labeling*

*4.1 After collecting the data, did you perform any data processing? If yes, please provide specific examples and explain the reasoning behind each step.*

*4.2 Were any measures implemented to ensure privacy, such as anonymizing user data? Please describe the methods used.*

*4.3 How did you address and clean out any implausible or erroneous observations in the dataset?*

*4.4 Did you modify the data structure for long-term storage, like rearranging the dataset or renaming columns for clari-ty? If so, provide details on these changes and their rationale.*

*4.5 What potential threats or biases could arise from your pre-processing steps? Please elaborate on any risks associat-ed with the modifications made to the data and how they might impact the dataset's integrity or utility.*

*5\.		Data inspection*

*5.1	Please provide a variety of meaningful summary statistics and plots. For example, consider means/SDs for contin-uous variables, frequency distributions for categorical variables or – in the case of plots – bar charts, line plots, or his-tograms. This part of the documentation is intended to illustrate the richness of the collected data.*

*5.2	Is any information missing from individual instances? If so, please describe why this information is missing (e.g., because it was unavailable). This does not include intentionally removed information but might include, e.g., redacted text.*

*6\.		Uses*

*6.1	Has the dataset been used for any tasks already? If so, please provide a description.*

*6.2	What (other) tasks / research projects could the dataset be used for? Provide a set of potential research questions or ideas for research projects.*

*6.3	Is there anything about the composition of the dataset or the way it was collected and preprocessed/cleaned/labeled that might impact future uses? For example, is there anything that a future user might need to know to avoid uses that could result in unfair treatment of individuals or groups (e.g., stereotyping, quality of service issues) or other undesira-ble harms (e.g., financial harms, legal risks) If so, please provide a description. Is there anything a future user could do to mitigate these undesirable harms?*

*6.4	Are there tasks for which the dataset should not be used? If so, please provide a description.*

References

De Freitas, T. (n.d.). *Coffee Facts | British Coffee Association*. British Coffee Association. [https://www.britishcoffeeassociation.org/coffee-in-the-uk/coffee-facts](https://www.britishcoffeeassociation.org/coffee-in-the-uk/coffee-facts)  
Lohse, C., Lemsom, J., & Kalogiratos, A. (2023). Syrupy Mouthfeel and Hints of Chocolate \-- Predicting Coffee Review Scores using Text Based Sentiment. *arXiv (Cornell University)*. [https://doi.org/10.48550/arxiv.2301.12417](https://doi.org/10.48550/arxiv.2301.12417)  
Different coffee review sites:  
[www.coffeereview.com](http://www.coffeereview.com)   
[www.pullandpourcoffee.com](http://www.pullandpourcoffee.com)  
[www.coffeejudge.co.uk/archive/202112](https://www.coffeejudge.co.uk/archive/202112)  
[https://www.theloveofcoffee.co.uk/customer-reviews-61-c.asp](https://www.theloveofcoffee.co.uk/customer-reviews-61-c.asp)          
[https://coffeeroast.com/](https://coffeeroast.com/)   
[https://www.reddit.com/r/Coffee/comments/1ilccyy/mod\_the\_daily\_question\_thread/](https://www.reddit.com/r/Coffee/comments/1ilccyy/mod_the_daily_question_thread/)  
[https://www.koffiekwaliteit.nl/reviews/?srsltid=AfmBOop6yoMiDRLh-68Jw0JkdMn9YqMPP5B-HwMe-dbC\_VmSPyS2P99S](https://www.koffiekwaliteit.nl/reviews/?srsltid=AfmBOop6yoMiDRLh-68Jw0JkdMn9YqMPP5B-HwMe-dbC_VmSPyS2P99S) 

Regional / not (primarily) dedicated to reviews  
[https://europeancoffeetrip.com/](https://europeancoffeetrip.com/)   
[https://www.beanscenemag.com.au/](https://www.beanscenemag.com.au/)   
[https://perfectdailygrind.com/](https://perfectdailygrind.com/) 