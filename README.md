# Magic Chess Go Go Mythic Player Match History Dataset

Climbing to Mythic rank in Magic Chess is *tough*! The competition is fierce, and while many players turn to YouTube to follow meta strategies or “templates,” that often takes the fun out of the game. Wouldn’t it be better to dig into actual gameplay data from Mythic-level players and uncover what really works?

This dataset is built on that idea—learning directly from top-tier match history to uncover the most effective patterns. 

## 📂 Dataset Structure

The dataset consists of **three CSV files**: *(currently data is from season 2)*

### 🧙‍♂️ `hero`

| Column Name | Description |
|-------------|-------------|
| `match_id`  | Match ID (visible at the top-left corner of the match history screen) |
| `ranking`   | Player's final ranking in the match (1 to 4) |
| `hero_#`    | The #-th hero in the lineup |
| `star_#`    | Star level of the corresponding # hero |


### 🔗 `synergy`

| Column Name | Description |
|-------------|-------------|
| `match_id`  | Match ID (same as above) |
| `synergy_#` | Name of the synergy formed by the end of the match |
| `num_#`     | Number of the corresponding # synergy |


### 🃏 `card`

| Column Name | Description |
|-------------|-------------|
| `match_id`  | Match ID (same as above) |
| `ranking`   | Player's final ranking in the match (1 to 4) |
| `card_#`    | Card selected and used during the match |


## 🏗️ How It Was Built

- **Manual Data Entry**  
  All data was entered manually into a spreadsheet, match by match.

- **Finding Mythic Players**  
  Players were found by monitoring the **World Chat** and identifying those with **Mythic rank**. I tracked 5 Mythic players and followed them to ensure their match history remained accessible and to collect more data over time for future analysis.

- **Overcoming Limitations**  
  Many Mythic players have hidden match history, and Mythic-tier players appear less frequently in chat compared to lower-tier players.  
  **Workaround:** After identifying a Mythic player’s match, I checked the **other players in the same match**—since they’re likely Mythic too. This way, I could expand the dataset with more high-level matches.

## 🔗 Also Available in Kaggle
[https://www.kaggle.com/datasets/dinanabb/magic-chess-go-go-mythic-ranked-matches](https://www.kaggle.com/datasets/dinanabb/magic-chess-go-go-mythic-ranked-matches)

## 🤝 Pull Request Guide

If you'd like to contribute or add new match entries to this dataset, please follow these guidelines:

1. **Include a Match Screenshot:**  
   Make sure to attach a screenshot of the match result, similar to the ones in the `sources` directory of this repository.  

2. **File Naming:**  
   Name the screenshot using the **match ID**, which can be found marked in red (as shown in the example screenshot below).
   ![match_id](https://github.com/dinanabila/mcgg-matches-dataset/blob/12edd496e046197ba3e9260a1ef9540a3cdbd1dd/sources/ss-example.jpg?raw=true)

4. **Why This Matters:**  
   This helps ensure data accuracy. If there's ever any doubt about an entry, we can refer back to the screenshot for verification.

5. **Season Updates:**  
   When a new season starts, please create a **new folder** named `season-#` (e.g., `season-3`) and store the dataset there.  
   Synergy and hero stats often change between patches, so keeping datasets separate by season helps maintain data integrity.

---

Feel free to contribute, explore, and build on top of this dataset. The ultimate goal is to discover winning patterns and push Magic Chess strategy beyond the obvious ;-)
