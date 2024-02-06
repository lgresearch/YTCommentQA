# YTCommentQA: Video Question Answerability in Instructional Videos

This is the official repository of the following AAAI 2024 paper: [YTCommentQA: Video Question Answerability in Instructional Videos](https://arxiv.org/abs/2401.17343)

- Authors: [Saelyne Yang](https://www.saelyne.com/), Sunghyun Park, [Yunseok Jang](https://yunseokjang.github.io/), [Moontae Lee](https://moontae.people.uic.edu/)

## Dataset

The YTCommentQA dataset can be found at `dataset.json`. It contains naturally-generated questions collected from the YouTube comment section, categorized by their answerability and required modality to answer -- visual, script, or both.


```
{
    ...
	id: {
		"question": "question_text" (string),
		"answerability": [0] | [1] | [2] | [1, 2] | [3] (list of integers) # explanation below
  		"ocr": "ocr_text" (string),
        "evidence": [start_idx (int), end_idx (int)], # index corresponds to "caption"[i]["id"] from the below "caption" field
        "videoID": (string), # YouTube Video ID
		"caption": [
            ...
            {
                "id": sentence_id (int)
                "start": start_timestamp (float)
                "end": end_timestamp (float)
                "text": sentence (string)
            }
            ...
        ],
	}
    ...
}
```

### Answerability

- 0: Unanswerable
- 1: Visual Answerable
- 2: Script Answerable
- 3: Combined Answerable

## License
```
YTCommentQA

MIT License

Copyright (c) 2024 LG AI Research

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## Citation
```
@inproceedings{yang2023ytcommentqa,
  Author    = {Yang, Saelyne and Park, Sunghyun and Jang, Yunseok and Lee, Moontae},
  Title     = {{YTCommentQA: Video Question Answerability in Instructional Videos}},
  Booktitle = {AAAI},
  Year      = {2024}}
```
## Contact
If you have any questions, please send an email to: Saelyne Yang (saelyne@kaist.ac.kr)
