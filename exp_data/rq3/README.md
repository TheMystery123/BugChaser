# RQ3 数据

## 概述

在针对RQ3的实验中，我们基于应用类型和下载数量，从Google Play随机选择了237个流行应用，评估了BugHunter的漏洞检测能力。实验将BugHunter与几种基线方法（Time-Machine、ComboDroid、APE+QT、Humanoid、GPTDroid）进行了比较，所有方法对每个应用进行了60分钟的测试。

实验结果如下：
1. BugHunter在88个应用中检测到了93个崩溃漏洞。
2. 其中，45个应用中的49个漏洞是首次发现，之前没有被任何基线方法检测到。
3. 在这些新发现的漏洞中，表现最好的基线方法GPTDroid仅检测到了7个。
4. 所有基线方法检测到的漏洞都是BugHunter检测到的漏洞的子集。
5. 我们将这49个新发现的漏洞提交给了开发者，到目前为止，已有42个漏洞被修复或确认（33个已修复，9个已确认，无一被拒绝），还有7个仍在等待。

这些数据结果表明，BugHunter在检测未见过的漏洞方面非常有效，能够发现其他方法可能会遗漏的错误。

## Confirmed Bugs

| ID | App name | Category | download | Version | Time-Machine | ComboDroid | APE+QT | Humanoid | GPTDroid |
|----|----------|----------|----------|---------|--------------|------------|---------|----------|----------|
| 1  | BOM Weather | weather | 1M+ | 6.9.1 |  |  |  |  |  |
| 2  | Weawow | weather | 5M+ | 6.2.8 |  |  |  |  |  |
| 3  | To-Do List | productivity | 10M+ | 10.3 |  |  |  |  |  |
| 4  | Roubit | productivity | 1M+ | 6.1.3 |  |  |  | √ |  |
| 5  | Bitget | finance | 5M+ | 2.41.3 |  |  |  |  |  |
| 6  | Tonkeeper | finance | 10M+ | 4.10.0 |  |  |  |  |  |
| 7  | Mi Fitness | health | 10M+ | 3.30.0 |  |  |  |  |  |
| 8  | Fitdays | health | 1M+ | 1.22.2 |  | √ |  |  |  |
| 9  | Tasty | food | 10M+ | 1.97.0 |  |  |  |  |  |


## Pending Bugs

| ID | App name       | Category | download | Version  | Time-Machine | ComboDroid | APE+QT | Humanoid | GPTDroid |
|----|---------------|----------|----------|----------|--------------|------------|---------|----------|----------|
| 1  | DoorDash      | food     | 50M+     | 15.18    |               |            |         |          |          |
| 2  | Daily Meal Planner | food     | 100K+    | 2.5.0    |               |            |         |          |          |
| 3  | Mindbody      | health   | 5M+      | 7.73.0   |               |            |         |          |          |
| 4  | FX File Explorer | business | 10M+     | 12.3     |               |            |         |          |          |
| 5  | App Sharer    | tool     | 10K+     | 1.0.4    |               |            |         |          |          |
| 6  | Send Anywhere  | productivity | 10M+     | 23.2.6   |               |            |         |          |          |
| 7  | Sportplan     | sport    | 50K+     | 3.0.38   |               |            |         |          |          |

## Fixed Bugs

| ID | App name | Category | Download | Version | TimeM | Comb | APE+QT | Humanoid | GPTDroid |
|-------------|-------------------|-------------------|-------------------|------------------|----------------|---------------|-----------------|-------------------|-------------------|
| 1           | Musixmatch        | music             | 50M+              | 7.10.1           |                |               |                 |                   |                   |
| 2           | Time Planner      | productivity      | 5M+               | 3.22             | √     | √    | √      |                   | √        |
| 3           | DailyLife         | lifestyle         | 5M+               | 4.3.0.2          |                |               |                 |                   |                   |
| 4           | Carousell         | shopping          | 10M+              | 2.370.4          |                |               |                 |                   |                   |
| 5           | Hungerstation     | food              | 10M+              | 8.0.19           |                |               |                 |                   |                   |
| 6           | Karrot            | social            | 10M+              | 24.33.0          |                |               |                 |                   |                   |
| 7           | Khan Academy      | education         | 10M+              | 8.1.0            |                |               |                 |                   |                   |
| 8           | Klook             | travel            | 10M+              | 7.3.1            | √     |               | √      | √        | √        |
| 9           | Money Manager     | finance           | 10M+              | 4.9.18           |                |               |                 |                   |                   |
| 10          | Musicolet         | music             | 10M+              | 11.3             |                |               |                 |                   |                   |
| 11          | Notion            | productivity      | 10M+              | 0.6.2419         |                |               |                 |                   |                   |
| 12          | Ringtones         | entertain         | 10M+              | 3.7.1            |                | √    |                 |                   | √        |
| 13          | School Planner    | education         | 10M+              | 8.2.1            | √     |               | √      | √        | √        |
| 14          | ShortMax          | entertain         | 10M+              | 1.9.1            |                |               |                 |                   |                   |
| 15          | Step Tracker      | health            | 10M+              | 1.4.7            |                |               |                 |                   |                   |
| 16          | To-Do List        | productivity      | 10M+              | 3.7.1            |                | √    |                 |                   |                   |
| 17          | Transit           | map               | 10M+              | 5.15.1           |                |               |                 |                   |                   |
| 18          | Zepp              | sport             | 10M+              | 8.12.3           |                |               |                 |                   |                   |
| 19          | BetterMe          | health            | 1M+               | 4.54.0           |                |               |                 |                   |                   |
| 20          | Cathay            | finance           | 1M+               | 5.14.1           |                |               | √      | √        |                   |
| 21          | Coupang           | shopping          | 1M+               | 8.3.1            |                | √    |                 |                   | √        |
| 22          | Drink Water       | health            | 1M+               | 1.102.19         |                |               |                 |                   |                   |
| 23          | eSound            | music             | 1M+               | 4.11.1           |                |               |                 |                   |                   |
| 24          | Fortune City      | finance           | 1M+               | 4.6.1            |                |               |                 |                   |                   |
| 25          | Home Assistant    | house             | 1M+               | 4.3.0            |                |               | √      |                   | √        |
| 26          | MTR Mobile        | travel            | 1M+               | 20.39.1          |                |               |                 |                   |                   |
| 27          | Rabit             | productivity      | 1M+               | 4.1.362          |                |               |                 |                   |                   |
| 28          | Zenmoney          | finance           | 1M+               | 7.9.0            |                |               |                 |                   |                   |
| 29          | MyTranslink       | map               | 500K+             | 3.7.12345        |                |               |                 |                   |                   |
| 30          | New Scientist     | news              | 500K+             | 4.9              |                |               |                 |                   |                   |
| 31          | Turbo Alarm       | tool              | 500K+             | 17.3             |                |               |                 |                   | √        |
| 32          | CodeSnack         | education         | 100K+             | 5.5.1            |                |               |                 |                   |                   |
| 33          | FilterBox         | tool              | 100K+             | 3.3.3            |                |               |                 |                   |                   |
