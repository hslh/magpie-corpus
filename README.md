# MAGPIE Corpus
This is the **MAGPIE Corpus**, a large sense-annotated corpus of potentially idiomatic expressions (PIEs), based on the British National Corpus (BNC). Potentially idiomatic expressions are like idiomatic expressions, but the term also covers literal uses of idiomatic expressions, such as 'I leave work *at the end of the day*.' for the idiom 'at the end of the day'. The corpus contains 56,622 instances, covering 1,756 different idiom types, all of which have crowdsourced meaning labels. 

## Contents & Usage
This repository contains three jsonl-files containing the annotations. `MAGPIE_unfiltered.jsonl` contains the complete set of PIEs, regardless of annotation confidence or sense label.  The `MAGPIE_filtered_split_*.jsonl` files contain a filtered subset of the full corpus, including only PIEs with an annotation confidence level of 75% and binary sense labels, that is, only with the label *idiomatic* or *literal*. Of these, `MAGPIE_filtered_split_random.jsonl` is randomly split into a training, development, and test set, whereas `MAGPIE_filtered_split_typebased.jsonl` is split so that there is no overlap in idiom types between the training, development, and test sets. 

The corpus is in [JSON Lines](http://jsonlines.org/) format, so it is easy to use across platforms, but also human-readable. 

## Format
One instance in the corpus looks like this:

```
{
    u 'confidence': 0.756291466076927,
        u 'context': [u '\u2018 Bless you , Peggy .',
            u "Of course I wo n't go climbing hills,\u2019 Beth assured her with a light peck on the cheek to show that she was not annoyed at the girl 's being so forward .",
            u "With that , Beth and her son went hand in hand out of the house and down the street , the boy 's constant chatter filtering back to the watching maid and causing her to smile .",
            u '\u2018 Have a good time!\u2019 she called out , over the hustle and bustle of passing carriages .',
            u "Beth 's smile in return gladdened the girl ."
        ],
        u 'document_id': u 'FPK',
        u 'genre': u 'W fict prose',
        u 'id': 12347,
        u 'idiom': u 'go hand in hand',
        u 'judgment_count': 4,
        u 'label': u 'i',
        u 'label_distribution': {
            u '?': 0.0,
            u 'f': 0.0,
            u 'i': 0.756291466076927,
            u 'l': 0.24370853392307304,
            u 'o': 0.0
        },
        u 'non_standard_usage_explanations': [],
        u 'offsets': [
            [29, 33],
            [34, 38],
            [39, 41],
            [42, 46]
        ],
        u 'sentence_no': u '2494',
        u 'split': 'training',
        u 'variant_type': u 'inflection'
}
```
