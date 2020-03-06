# Intro to Recommendation Engines
## Juan Arévalo, Cepsa

* Juan's motto is "Put the median into production", meaning: first evaluate the business model and put the most simple solution into production.

* The output of a recommendation engine is an ordered list.

* Recommendation engines can be based on past usage or content based.

* Recommendation algorithms: they firstly recommend the most popular. (reading: "Should I follow the crowd?" by Pablo Castells, UAM).

### Metrics

* Recommendation engines based on previous ratings (0-10) were used to predict ratings for new items (like movies). Prediction models are scored using RMSE, and as seen on the Netflix challenge they are not good for that. They ended being good on predicting ratings for low-rated movies. That's why Netflix moved from ratings to thumbs up feedbacks. The problem is that positive feedback has a lot of bias.

* Recommendation engines cannot measure false negatives. So they are not valid for offline systems.

* In the end, nowadays, prediction and classification for recommendation engines are discarded as valid. Now RL (Reinforced Learning) is used.

### Great recommendation engines

* MOVIX.AI



