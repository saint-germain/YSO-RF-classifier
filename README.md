# YSO-RF-classifier
Results from the first RADA: Big Data Colombia workshop

Classifying YSOs and other beasties with IR fluxes from MSX/RMS and HiGAL data.

Notes:

- If ? and ?? classes are left in, the classifier does a decent job of grouping them together
- If the ? and ?? classes are folded together with their main class, the classifier does a not-so-great job anymore -> ? and ?? classes might be something else
- If Rejected class is left in, the classifier can also do a good job
- Weighting does not seem to make a difference
- GridSearchCV never worked, however see https://stackoverflow.com/questions/26210471/scikit-learn-gridsearch-giving-valueerror-multiclass-format-is-not-supported/26210645
- Randomizing Herschel flux did not work very well, better to only use data for which 70 micron flux is known
- Can't recall precisely how Flux_70.csv file was obtained, (Herschel query notebook does not seem to do the trick in quite the same manner, e.g. matching and sorting are seemingly done elsewhere). It might just be a direct RMS name query. Juan Rendón might know.
- There is a Simbad OTYPE catalog, could be useful for benchmarking this classification.
- Slack: http://rada-dirty-work.slack.com/
