# War on Their Minds: A Comparison of the Concepts Of "Democratization: and "War" in Chinese Newspapers, 1912-1949

## Documentation

### Step 1: Gathering Basic Data

1. Create Excel spread sheet (this will become the main data set):

    | City | Latitude | Longitude | Newspaper | urls | Date

    Fill in data

    End result: The data for the first pages of 2,187 newspapers from Aug 3, 1914, to April 09, 1949, were recorded.

    Cities: Beijing and Nanjing

2. Create a .csv-file from column "urls"

### Step 2: Extract data (texts) from individual newspapers

This step is completed through Parsehub using a specially designed template.

#### Worksteps for Parsehub

Template creation:

1. create project
2. go to "settings"; import csv-file
3. return to "commands"; create **loop** that goes through all the urls recorded in the csv-file; click "+"-sign next to "(page); select "loop"
4. click on "+"-sign next to "For each item in urls"; select "Begin new entry"; rename "list1" in "links"
5. click on "+"-sign next to "Begin new entry in links"; select "Extract"; rename "extract" into "link"; replace "$location.href" with "item"
6. click on "+"-sign next to "Begin new entry in links"; select "Go to template"; select "Go to URL:" and enter item; select "Create New Template" and enter "details"; click on "Create New Template

Fetch Data:

1. Click "Browse" and click on the "Text"-field (the field that contains the transcribed Text) of the opened website to open that field.
2. Click on "+"-sign next to page; select "Select"; click on the text to copy to the command
3. Rename "selection1" as "text1"
4. Repeat as necessary
5. When finished click "Get Data", "Run"
Parsehub will now run the template and fetch the data of all urls that were initially selected. The new data set can be downloaded either in csv or json format. In this case, the data set was to big for a csv-file and could only be downloaded as json (which is not a problem).

Result: The texts of all 2,187 newspapers (only the first page) were fetched.

### Step 3: Search for keywords in the extracted texts

Using Parsehub it was possible to create a file containing the following data (example) of the selected newspapers:

link: "<https://gpa.eastview.com/crl/lqrcn/newspapers/bfhq19300919-01.1.1>"

text1: 一一級織赤色 ；1： 會等 ， 這 ^ ？ 全世界機曾主義者大都相一同的奴性。爲什歷 ？ 因趕他們不願意佔 :^ 工一的客觀形勢 ， 不願湓蔚見 ： 丄人要求政治鬥 # 的迫切 II , 所以機曾主義落祗看到工人的經濟要求 ， 認饬工人的經 ^ 要求比政治耍求斑迫切得多。

These texts were searched for the following keywords regarding democratic concepts:

- 民主 - democracy
- 民主主義 - democracy
- 民主化 - democratization
- 公民 - citizen
- 共和國 - republic
- 國家 - country
- 憲法 - constitution
- 民權 civil rights
- 主權 - sovereignty

Since China was constantly at war during this time (the Second Sino-Japanese War from 1937-1945 and the Chinese Civil War from 1927-1949), the following keywords related to “war” were also searched for:

- 戰爭 - war
- 大戰 - great war
- 世界大戰 - World War
- 戰 - to fight / fight / war / battle
- 失敗 - to be defeated / to lose
- 投降 - to surrender
- 佔領 - to capture; to seize; to occupy by force
- 侵占 - to invade and occupy (territory)
- 海軍 - navy
- 陸軍 - army
- 空軍 - air force
- 日空軍 - Japanese Air Force
- 日軍 - Japanese Army

The actual search was carried out in a Kaggle Notebook. Kaggle is a host for jupyter notebooks (online). It is also very good for collaboration, as the notebooks can be quickly shared with others. However, one should keep in mind that Kaggle is a cloud-based application and therefore sensitive data may perhaps not be processed with Kaggle.

The biggest advantage of Kaggle is that one works with a package consisting of the raw data, the code, and an output (in this case an Excel spreadsheet) and that one can achieve the desired results with a certain degree of efficiency.

For this project, the following steps were performed in a Kaggle Notebook:

Input:

- upload of the main data set (the excel sheet from step 1)
- upload of the run results from parsehub (as a json file)

Code:

Link to kaggle notebook: <https://www.kaggle.com/code/wolfgangschwalenberg/lqrcn-data-results/notebook?scriptVersionId=171055548>

Output:

An Excel spread sheet is created that shows the frequency of mentions of the above search terms in the various newspapers (connected to the url).

The data from this spread sheet is then pasted into the main data set.

### Step 4: Analysis

The actual analysis of the data is done using Excel. The corresponding graphics are also created with Excel and saved on GitHub for later use in the actual essay.
