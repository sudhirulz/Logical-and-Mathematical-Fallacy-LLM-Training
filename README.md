# Detecting Logical Fallacies with Language Models

I started this project as a debater. I wanted to understand fallacies more formally and test whether a language model could learn to recognise them.

## Fallacy detection

I first fine-tuned RoBERTa to tell apart five fallacies: Hasty Generalization, Appeal to Nature, Texas Sharpshooter, No True Scotsman and Affirming the Consequent. I built the dataset myself, writing each example around the logical form of its fallacy. Untrained, the model scored 20%, which is chance for five classes. After fine-tuning it scored 100% on a small 50-example test set. That set is small and written in a similar style to the training data, so I treat it as a proof of concept.

## Circular reasoning in maths

I applied the same approach to proofs, fine-tuning CodeBERT to separate valid proofs from circular ones, which assume what they set out to prove. The dataset is small, so this part is exploratory.

## Busted! (the app)

I then built a web app on top of a larger 12-class model (11 fallacies plus "No Fallacy"). It splits a passage into sentences, flags likely fallacies and explains each one. It reaches 98.6% on templated test data, but it over-flags real news text, so it does not yet generalise.

## Next steps

- Build a labelled test set of real text
- Add confidence thresholds and passage context
- Learn the linguistics and NLP needed for structure-aware detection

I would value guidance from mentors on these.

*Sudarshan Manikantan, Dhirubhai Ambani International School, Mumbai*
