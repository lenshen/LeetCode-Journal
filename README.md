# LeetCode-Journal
# LeetCode 演算法修煉筆記

這是我記錄 LeetCode 解題思路與程式碼的地方。詳細解析與 Solution 皆記錄於 [HackMD](https://hackmd.io/folders/p7db3lYn3ebU3MskK9Vsv)。
讚嘆靈神

## 學習進度
- **累積進度**：
    - 🟢 Easy: 0
    - 🟡 Medium: 1
    - 🔴 Hard: 0

---

## 定長滑動窗口 (Fixed-size Sliding Window)
> **核心思維：進、算、出**
> 1. **進**：新元素進入窗口，更新狀態。
> 2. **算**：當窗口達到固定長度 $K$，更新答案。
> 3. **出**：左側元素離開窗口，恢復狀態。


| 題號 | 題目名稱 | 難度 | 完整筆記 (含程式碼) | 狀態 |
| :--- | :--- | :--- | :--- | :--- |
| 1456 | [定長子串中元音的最大數目](https://leetcode.cn/problems/maximum-number-of-vowels-in-a-substring-of-given-length/) | 🟢 Easy | [Link]() | ⬜ |
| 643 | [子數組最大平均數 I](https://leetcode.cn/problems/maximum-average-subarray-i/) | 🟢 Easy | [Link]() | ⬜ |
| 1343 | [大小為 K 且平均值大於等於閾值的子數組數目](https://leetcode.cn/problems/number-of-sub-arrays-of-size-k-and-average-greater-than-or-equal-to-threshold/) | 🟡 Medium | [Link]() | ⬜ |
| 2090 | [半徑為 k 的子數組平均值](https://leetcode.cn/problems/k-radius-subarray-averages/) | 🟡 Medium | [Link]() | ⬜ |
| 2379 | [得到 K 個黑塊的最少塗色次數](https://leetcode.cn/problems/minimum-recolors-to-get-k-consecutive-black-blocks/) | 🟢 Easy | [Link]() | ⬜ |
| 1052 | [愛生氣的書店老闆](https://leetcode.cn/problems/grumpy-bookstore-owner/) | 🟡 Medium | [Link]() | ⬜ |
| 1461 | [檢查一個字串是否包含所有長度為 K 的二進位代碼](https://leetcode.cn/problems/check-if-a-string-contains-all-binary-codes-of-size-k/) | 🟡 Medium | [點我閱讀](https://hackmd.io/@lenshen/r16F2U_PWe) | ✅ |
| 2841 | [幾乎唯一子數組的最大和](https://leetcode.cn/problems/maximum-sum-of-almost-unique-subarrays/) | 🟡 Medium | [Link]() | ⬜ |
| 2461 | [長度為 K 且子數組元素各不相同的最大子數組和](https://leetcode.cn/problems/maximum-sum-of-distinct-subarrays-with-length-k/) | 🟡 Medium | [Link]() | ⬜ |
| 2653 | [滑動窗口中的第 K 個最小整數](https://leetcode.cn/problems/sliding-subarray-beauty/) | 🟡 Medium | [Link]() | ⬜ |
| 2156 | [查找給定哈希值的子字串](https://leetcode.cn/problems/find-substring-with-given-hash-value/) | 🔴 Hard | [Link]() | ⬜ |
| 567 | [字串的排列](https://leetcode.cn/problems/permutation-in-string/) | 🟡 Medium | [Link]() | ⬜ |
| 438 | [找到字串中所有字母異位詞](https://leetcode.cn/problems/find-all-anagrams-in-a-string/) | 🟡 Medium | [Link]() | ⬜ |

## 不定長滑動窗口 (Variable-size Sliding Window)
> **核心思維：維護一個「合法」的窗口。右指針（入隊）擴張，左指針（出隊）收縮。**



### §2.1 越短越合法 / 求最長 / 最大
這類題目的特點是：窗口越短越容易滿足條件。當窗口滿足條件時，我們試著拉長它（移動右指針）；當不滿足時，才收縮它（移動左指針）。

| 題號 | 題目名稱 | 難度 | 筆記 | 狀態 |
| :--- | :--- | :--- | :--- | :--- |
| 3 | [無重複字符的最長子串](https://leetcode.cn/problems/longest-substring-without-repeating-characters/) | 🟡 Medium | [Link]() | ⬜ |
| 3090 | [每個字符最多出現兩次的最長子字符串](https://leetcode.cn/problems/maximum-length-substring-with-two-occurrences/) | 🟢 Easy | [Link]() | ⬜ |
| 1493 | [刪掉一個元素以後全為 1 的最長子數組](https://leetcode.cn/problems/longest-subarray-of-1s-after-deleting-one-element/) | 🟡 Medium | [Link]() | ⬜ |
| 1208 | [盡可能使字串相等](https://leetcode.cn/problems/get-equal-substrings-within-budget/) | 🟡 Medium | [Link]() | ⬜ |
| 904 | [水果成籃](https://leetcode.cn/problems/fruit-into-baskets/) | 🟡 Medium | [Link]() | ⬜ |
| 1695 | [刪除子數組的最大得分](https://leetcode.cn/problems/maximum-erasure-value/) | 🟡 Medium | [Link]() | ⬜ |
| 2958 | [最多 K 個重複元素的最長子數組](https://leetcode.cn/problems/length-of-longest-subarray-with-at-most-k-frequency/) | 🟡 Medium | [Link]() | ⬜ |
| 2024 | [考試的最大困擾度](https://leetcode.cn/problems/maximize-the-confusion-of-an-exam/) | 🟡 Medium | [Link]() | ⬜ |
| 1004 | [最大連續 1 的個數 III](https://leetcode.cn/problems/max-consecutive-ones-iii/) | 🟡 Medium | [Link]() | ⬜ |
| 2730 | [找到最長的半重複子字串](https://leetcode.cn/problems/find-the-longest-semi-repetitive-substring/) | 🟡 Medium | [Link]() | ⬜ |
| 2779 | [數組的最大美麗值](https://leetcode.cn/problems/maximum-beauty-of-an-array-after-applying-operation/) | 🟡 Medium | [Link]() | ⬜ |
| 1658 | [將 x 減到 0 的最小操作數](https://leetcode.cn/problems/minimum-operations-to-reduce-x-to-zero/) | 🟡 Medium | [Link]() | ⬜ |
| 1838 | [最高頻元素的頻數](https://leetcode.cn/problems/frequency-of-the-most-frequent-element/) | 🟡 Medium | [Link]() | ⬜ |
| 2516 | [每種字符至少取 K 個](https://leetcode.cn/problems/take-k-of-each-character-from-left-and-right/) | 🟡 Medium | [Link]() | ⬜ |
| 2831 | [找出最長等值子數組](https://leetcode.cn/problems/find-the-longest-equal-subarray/) | 🟡 Medium | [Link]() | ⬜ |
| 2106 | [摘水果](https://leetcode.cn/problems/fruit-picking/) | 🔴 Hard | [Link]() | ⬜ |
| 76 | [最小覆蓋子串](https://leetcode.cn/problems/minimum-window-substring/) | 🔴 Hard | [Link]() | ⬜ |

### §2.2 越長越合法 / 求最短 / 最小
這類題目的特點是：窗口要長到一定程度才會滿足條件。一旦滿足條件，我們就嘗試收縮左指針，直到找到「剛好滿足條件」的最短長度。

| 題號 | 題目名稱 | 難度 | 筆記 | 狀態 |
| :--- | :--- | :--- | :--- | :--- |
| 209 | [長度最小的子數組](https://leetcode.cn/problems/minimum-size-subarray-sum/) | 🟡 Medium | [Link]() | ⬜ |
| 1234 | [替換子串得到平衡字串](https://leetcode.cn/problems/replace-the-substring-for-balanced-string/) | 🟡 Medium | [Link]() | ⬜ |
| 2875 | [無限數組的最短子數組](https://leetcode.cn/problems/minimum-size-subarray-in-infinite-array/) | 🟡 Medium | [Link]() | ⬜ |
| 632 | [最小區間](https://leetcode.cn/problems/smallest-range-covering-elements-from-k-lists/) | 🔴 Hard | [Link]() | ⬜ |

---

## 參考資源
- **題單來源**: [靈茶山艾府 (EndlessCheng)](https://github.com/EndlessCheng/codeforces-go/blob/master/leetcode/README.md)

---
*最後更新於: 2026-02-10*
