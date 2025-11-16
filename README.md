# Anime Sources API

A simple API wrapper for fetching anime sources from anicrush.to.

## Setup

1. Install dependencies:
```bash
npm install
```

2. Start the server:
```bash
npm start
```

For development with auto-reload:
```bash
npm run dev
```

## API Endpoints

### Map AniList ID to Anicrush

```
GET /api/mapper/{anilistId}
```

Maps an AniList ID to anicrush.to anime ID and episode information.

Example Request:
```
GET http://localhost:3000/api/mapper/21
```

Example Response:
```json
{
    "anilist_id": "21",
    "anicrush_id": "vRPjMA",
    "titles": {
        "romaji": "One Piece",
        "english": "One Piece",
        "native": "ワンピース",
        "anicrush": "One Piece"
    },
    "total_episodes": 1000,
    "episodes": [
        {
            "number": 1,
            "id": "vRPjMA&episode=1"
        },
        // ... more episodes
    ],
    "format": "TV",
    "status": "RELEASING"
}
```

### Search Anime

```
GET /api/anime/search
```

Query Parameters:
- `keyword` (required): Search term
- `page` (optional): Page number (default: 1)
- `limit` (optional): Results per page (default: 24)
Eg 
```
https://anicrush-api-six.vercel.app/api/anime/search?keyword=dragon
Result : 
{
"status": true,
"result": {
"movies": [
{
"id_number": 5453,
"name": "Blue Dragon: Tenkai no Shichi Ryuu",
"name_english": "Blue Dragon: The Seven Dragons of the Heavens",
"slug": "blue-dragon-the-seven-dragons-of-the-heavens",
"overview": "After the events of the Blue Dragon series, Shu and Bouquet join a resistance group to fight General Rogi's army of invasion.They encounter a mysterious child , Noi, who has the power to revive Shu's shadow counter-part Blue Dragon, and save her from the pursuit of a red dragon. Now Shu and his company have to set foot once again on a journey to discover the purpose of the dragons, undergo their tests and stop the chains of events which threatens the fate of humanity. \r\n\r\n(Source: ANN)",
"type": "TV",
"country_code": "jp",
"poster_path": "b7/82/b78242ac4c108bd2c7b89233bfcfb618/b78242ac4c108bd2c7b89233bfcfb618.jpg",
"total_episodes": 51,
"latest_episode_sub": 51,
"latest_episode_dub": 0,
"airing_status": 1,
"aired_from": "Apr 5, 2008",
"runtime": 20,
"rating_type": "PG",
"has_sub": 1,
"has_dub": 0,
"mal_score": 6.57,
"genres": [
{
"id": 2,
"name": "Adventure",
"slug": "adventure"
},
{
"id": 4,
"name": "Comedy",
"slug": "comedy"
},
{
"id": 10,
"name": "Fantasy",
"slug": "fantasy"
},
{
"id": 37,
"name": "Supernatural",
"slug": "supernatural"
}
],
"id": "FP2H77"
},
{
"id_number": 5026,
"name": "Ikkitousen: Dragon Destiny Specials",
"name_english": "Ikkitousen: Dragon Destiny Specials",
"slug": "ikkitousen-dragon-destiny-specials",
"overview": "Ikkitousen Dragon Destiny Specials.",
"type": "Special",
"country_code": "jp",
"poster_path": "3d/75/3d75505d1b9ca53859949f9f1c18029f/3d75505d1b9ca53859949f9f1c18029f.jpg",
"total_episodes": 6,
"latest_episode_sub": 6,
"latest_episode_dub": 0,
"airing_status": 1,
"aired_from": "Jun 24, 2007",
"runtime": 3,
"rating_type": "R+",
"has_sub": 1,
"has_dub": 0,
"mal_score": 6.66,
"genres": [
{
"id": 9,
"name": "Ecchi",
"slug": "ecchi"
},
{
"id": 17,
"name": "Martial Arts",
"slug": "marial-arts"
},
{
"id": 23,
"name": "School",
"slug": "school"
},
{
"id": 31,
"name": "Super Power",
"slug": "super-power"
}
],
"id": "AVlyI1"
},
{
"id_number": 18118,
"name": "Yowai 5000-nen no Soushoku Dragon, Iwarenaki Jaryuu Nintei",
"name_english": "A Gentle Dragon of 5000 Years Old, It Was Recognized as an Evil Dragon Without Any Cause",
"slug": "a-gentle-dragon-of-5000-years-old-it-was-recognized-as-an-evil-dragon-without-any-cause",
"overview": "A 5000-year-old vegan dragon was living peacefully when one day a young girl showed up in his cave. She offered herself as a sacrifice in order to gain favor for her village. He played along as the great \"Evil Dragon, the Demon Lord's Army Leader\" in order to get rid of her. However, his little white lie awoke her hidden powers and his peaceful life suddenly ended.",
"type": "ONA",
"country_code": "cn",
"poster_path": "8f/ee/8feee86c100b4d1c9931bdc1e426b7bc/8feee86c100b4d1c9931bdc1e426b7bc.png",
"total_episodes": 12,
"latest_episode_sub": 12,
"latest_episode_dub": 0,
"airing_status": 1,
"aired_from": "Jul 30, 2022",
"runtime": 14,
"rating_type": "PG-13",
"has_sub": 1,
"has_dub": 0,
"mal_score": null,
"genres": [
{
"id": 2,
"name": "Adventure",
"slug": "adventure"
},
{
"id": 4,
"name": "Comedy",
"slug": "comedy"
},
{
"id": 10,
"name": "Fantasy",
"slug": "fantasy"
}
],
"id": "cp8ogK"
},
{
"id_number": 1455,
"name": "Fairy Tail Movie 2: Dragon Cry",
"name_english": "Fairy Tail Movie 2: Dragon Cry",
"slug": "fairy-tail-movie-2-dragon-cry",
"overview": "<p>Dragon Cry is a magical artifact of deadly power, formed into a staff by the fury and despair of dragons long gone. Now, this power has been stolen from the hands of the Fiore kingdom by the nefarious traitor Zash Caine, who flees with it to the small island nation of Stella. Frightened that the power has fallen into the wrong hands, the King of Fiore hastily sends Fairy Tail to retrieve the staff. But this task proves frightening as a shadowy secret lies in the heart of the kingdom of Stella. Dragon Cry follows their story as they muster up all their strength to recover the stolen staff and save both kingdoms.<br><br>[Written by MAL Rewrite]</p>",
"type": "Movie",
"country_code": "jp",
"poster_path": "ff/86/ff86d76c2ce368fd96d2dabc47f9619a/ff86d76c2ce368fd96d2dabc47f9619a.jpg",
"total_episodes": 1,
"latest_episode_sub": 1,
"latest_episode_dub": 1,
"airing_status": 1,
"aired_from": "May 6, 2017",
"runtime": 84,
"rating_type": "PG-13",
"has_sub": 1,
"has_dub": 1,
"mal_score": 7.54,
"genres": [
{
"id": 1,
"name": "Action",
"slug": "action"
},
{
"id": 2,
"name": "Adventure",
"slug": "adventure"
},
{
"id": 4,
"name": "Comedy",
"slug": "comedy"
},
{
"id": 10,
"name": "Fantasy",
"slug": "fantasy"
},
{
"id": 16,
"name": "Magic",
"slug": "magic"
},
{
"id": 27,
"name": "Shounen",
"slug": "shounen"
}
],
"id": "rZr9bp"
},
{
"id_number": 15767,
"name": "Kobayashi-san Chi no Maid Dragon SHORTS",
"name_english": "Miss Kobayashi's Dragon Maid Mini Shorts",
"slug": "miss-kobayashis-dragon-maid-mini-shorts",
"overview": "Kobayashi-san Chi no Maid Dragon S (小林さんちのメイドラゴンS, Kobayashi-san Chi no Meidoragon S) is the second season of the animated adaptation of the manga of the same name. It was announced alongside the release of Dragon Maid Volume 8. It is scheduled to broadcast in July 2021.",
"type": "TV",
"country_code": "jp",
"poster_path": "46/19/46199d4c778e0d27b1a4238ea2c29b68/46199d4c778e0d27b1a4238ea2c29b68.jpg",
"total_episodes": 13,
"latest_episode_sub": 13,
"latest_episode_dub": 4,
"airing_status": 1,
"aired_from": "Jul 1, 2021",
"runtime": 2,
"rating_type": "PG-13",
"has_sub": 1,
"has_dub": 0,
"mal_score": 0,
"genres": [
{
"id": 4,
"name": "Comedy",
"slug": "comedy"
},
{
"id": 10,
"name": "Fantasy",
"slug": "fantasy"
},
{
"id": 36,
"name": "Slice of Life",
"slug": "slice-of-life"
}
],
"id": "8e4Cf5"
},
{
"id_number": 17878,
"name": "Kobayashi-san Chi no Maid Dragon 2nd Season",
"name_english": "Miss Kobayashi's Dragon Maid 2nd Season",
"slug": "miss-kobayashis-dragon-maid-2nd-season",
"overview": "Tohru learns about a new Maid Café had opened nearby and decides to work there during her free time. Kobayashi and Kanna drop later at the café to check on her just to find that she has become their cook. Tohru uses dark magic to enchant the dishes served there, which makes the café a success, until she decides to quit, but before leaving, she teaches the other maids to use dark magic as well. A few days later, Tohru and Kobayashi are attacked by Ilulu, an extremist from the Chaos Faction who berates Tohru for coexisting with humans. Tohru gets herself in a disadvantage against Ilulu as she protects the city from her attacks until Kobayashi enlists Elma's help by bribing her with sweets, allowing Tohru to fight with all her power and defeat Ilulu. Ilulu later returns and attempts to seduce Kobayashi but fails. Certain that Kobayashi has not fallen for her because she's a woman, Ilulu retreats for a while, but not before transforming Kobayashi into a male.",
"type": "TV",
"country_code": "jp",
"poster_path": "94/88/9488f6f6af65c6a0af6e2d32ba74a6a7/9488f6f6af65c6a0af6e2d32ba74a6a7.jpg",
"total_episodes": 12,
"latest_episode_sub": 12,
"latest_episode_dub": 12,
"airing_status": 1,
"aired_from": "Jul 6, 2021",
"runtime": 24,
"rating_type": "PG-13",
"has_sub": 1,
"has_dub": 1,
"mal_score": null,
"genres": [
{
"id": 2,
"name": "Adventure",
"slug": "adventure"
},
{
"id": 4,
"name": "Comedy",
"slug": "comedy"
},
{
"id": 10,
"name": "Fantasy",
"slug": "fantasy"
}
],
"id": "xRdylC"
},
{
"id_number": 3242,
"name": "Kuutei Dragons",
"name_english": "Drifting Dragons",
"slug": "drifting-dragons",
"overview": "Dragons, the rulers of the sky. To many people on the surface, they are a dire threat, but at the same time, a valuable source of medicine, oil, and food. There are those who hunt the dragons. They travel the skies in dragon-hunting airships. This is the story of one of those ships, the “Quin Zaza,” and its crew. \r\n\r\n(Source: Official site)",
"type": "ONA",
"country_code": "jp",
"poster_path": "fd/ec/fdec431fe617bd9e111193bf63e260b1/fdec431fe617bd9e111193bf63e260b1.jpg",
"total_episodes": 12,
"latest_episode_sub": 12,
"latest_episode_dub": 12,
"airing_status": 1,
"aired_from": "Jan 9, 2020",
"runtime": 23,
"rating_type": "PG-13",
"has_sub": 1,
"has_dub": 0,
"mal_score": 7.09,
"genres": [
{
"id": 2,
"name": "Adventure",
"slug": "adventure"
},
{
"id": 10,
"name": "Fantasy",
"slug": "fantasy"
},
{
"id": 42,
"name": "Seinen",
"slug": "seinen"
}
],
"id": "zU2zDb"
},
{
"id_number": 4701,
"name": "Dragon Crisis!",
"name_english": "Dragon Crisis!",
"slug": "dragon-crisis",
"overview": "A normal high school boy Kisaragi Ryuji's peaceful life is turned into an adventure by the return of his second cousin Eriko. Ryuji and Eriko seize a relic box from a black broker. In the box, they find a red dragon girl Rose. In order to protect Rose from the black organization, Ryuji decides to fight using his power as a relic handler.",
"type": "TV",
"country_code": "jp",
"poster_path": "34/e6/34e6f775cc0a5ca46d53dee2aa800405/34e6f775cc0a5ca46d53dee2aa800405.jpg",
"total_episodes": 12,
"latest_episode_sub": 12,
"latest_episode_dub": 0,
"airing_status": 1,
"aired_from": "Jan 11, 2011",
"runtime": 23,
"rating_type": "PG-13",
"has_sub": 1,
"has_dub": 0,
"mal_score": 6.73,
"genres": [
{
"id": 1,
"name": "Action",
"slug": "action"
},
{
"id": 16,
"name": "Magic",
"slug": "magic"
},
{
"id": 22,
"name": "Romance",
"slug": "romance"
},
{
"id": 23,
"name": "School",
"slug": "school"
},
{
"id": 37,
"name": "Supernatural",
"slug": "supernatural"
},
{
"id": 42,
"name": "Seinen",
"slug": "seinen"
}
],
"id": "l9A63m"
},
{
"id_number": 15692,
"name": "Dragon, Ie wo Kau.",
"name_english": "Dragon's House-Hunting",
"slug": "dragons-house-hunting",
"overview": "When a dragon fails to live up to the fearsome standards set for him, his family kicks him out. He embarks on a quest to find a new home, but soon finds that life on the road is no place for a cowardly beast of legend. In a fantasy world full of elves, dwarves, and other mythical creatures, where everyone wants a piece of him—literally!—the frustrations of house-hunting reach a whole new level.\r\n\r\n(Source: Seven Seas Entertainment)",
"type": "TV",
"country_code": "jp",
"poster_path": "8f/52/8f52982518614850d94b344fc57ce2d1/8f52982518614850d94b344fc57ce2d1.jpg",
"total_episodes": 12,
"latest_episode_sub": 12,
"latest_episode_dub": 12,
"airing_status": 1,
"aired_from": "Apr 4, 2021",
"runtime": 23,
"rating_type": "PG-13",
"has_sub": 1,
"has_dub": 1,
"mal_score": 0,
"genres": [
{
"id": 4,
"name": "Comedy",
"slug": "comedy"
},
{
"id": 10,
"name": "Fantasy",
"slug": "fantasy"
},
{
"id": 27,
"name": "Shounen",
"slug": "shounen"
}
],
"id": "E157z4"
},
{
"id_number": 1334,
"name": "Dragon Ball Z Special 1: Tatta Hitori no Saishuu Kessen",
"name_english": "Dragon Ball Z Special 1: Bardock, The Father of Goku",
"slug": "dragon-ball-z-special-1-bardock-the-father-of-goku",
"overview": "Bardock, Son Goku's father, is a low-ranking Saiyan soldier who was given the power to see into the future by the last remaining alien on a planet he just destroyed. He witnesses the destruction of his race and must now do his best to stop Frieza's impending massacre.\n\n(Source: ANN)",
"type": "Special",
"country_code": "jp",
"poster_path": "3f/45/3f455fe83e1bf8ffce978cbd0995f22d/3f455fe83e1bf8ffce978cbd0995f22d.jpg",
"total_episodes": 1,
"latest_episode_sub": 1,
"latest_episode_dub": 1,
"airing_status": 1,
"aired_from": "Oct 17, 1990",
"runtime": 47,
"rating_type": "PG-13",
"has_sub": 1,
"has_dub": 1,
"mal_score": 7.58,
"genres": [
{
"id": 2,
"name": "Adventure",
"slug": "adventure"
},
{
"id": 4,
"name": "Comedy",
"slug": "comedy"
},
{
"id": 10,
"name": "Fantasy",
"slug": "fantasy"
},
{
"id": 24,
"name": "Sci-Fi",
"slug": "sci-fi"
},
{
"id": 27,
"name": "Shounen",
"slug": "shounen"
}
],
"id": "gVQ2o4"
},
{
"id_number": 7630,
"name": "Dragon",
"name_english": "Dragon",
"slug": "dragon",
"overview": "Based on a world-famous action RPG set in an open world, Dragon's Dogma from Capcom will be brought to life as a Netflix original anime series. The story follows a man's journey seeking revenge on a dragon who stole his heart. On his way, the man is brought back to life as an \"Arisen.\" An action adventure about a man challenged by demons who represent the seven deadly sins of humans. \r\n\r\n(Source: Netflix)",
"type": "ONA",
"country_code": "jp",
"poster_path": "74/0c/740cec04b30a383618b5955346320535/740cec04b30a383618b5955346320535.jpg",
"total_episodes": 7,
"latest_episode_sub": 7,
"latest_episode_dub": 7,
"airing_status": 1,
"aired_from": "Sep 17, 2020",
"runtime": 26,
"rating_type": "G",
"has_sub": 0,
"has_dub": 1,
"mal_score": 6.08,
"genres": [
{
"id": 1,
"name": "Action",
"slug": "action"
},
{
"id": 2,
"name": "Adventure",
"slug": "adventure"
},
{
"id": 10,
"name": "Fantasy",
"slug": "fantasy"
}
],
"id": "BNc6gS"
},
{
"id_number": 1151,
"name": "Dragon Quest: Adventure of Dai (TV)",
"name_english": "Dragon Quest: Dai no Daibouken (TV)",
"slug": "dragon-quest-dai-no-daibouken-tv",
"overview": "After the defeat of the demon lord Hadlar all of the monsters were unleashed from his evil will and moved to the island of Delmurin to live in peace. Dai is the only human living on the island. Having been raised by the kindly monster Brass, Dai's dream is to grow up to be a hero. He gets to become one when Hadlar is resurrected and the previous hero, Avan, comes to train Dai to help in the battle. But Hadlar, announcing that he now works for an even more powerful demon lord, comes to kill Avan. To save his students Avan uses a Self-Sacrifice spell to attack, but is unable to defeat Hadlar. When it seems that Dai and Avan's other student Pop are doomed a mark appears on Dai's forehead and he suddenly gains super powers and is able to fend off Hadlar. The two students then go off on a journey to avenge Avan and bring peace back to the world.\r\n\r\n(Source: ANN)",
"type": "TV",
"country_code": "jp",
"poster_path": "27/90/2790b7e0956d90bbfa33d177444d5fae/2790b7e0956d90bbfa33d177444d5fae.jpg",
"total_episodes": 46,
"latest_episode_sub": 46,
"latest_episode_dub": 0,
"airing_status": 1,
"aired_from": "Oct 17, 1991",
"runtime": 24,
"rating_type": "G",
"has_sub": 1,
"has_dub": 0,
"mal_score": 7.65,
"genres": [
{
"id": 2,
"name": "Adventure",
"slug": "adventure"
},
{
"id": 4,
"name": "Comedy",
"slug": "comedy"
},
{
"id": 6,
"name": "Demons",
"slug": "demons"
},
{
"id": 10,
"name": "Fantasy",
"slug": "fantasy"
},
{
"id": 16,
"name": "Magic",
"slug": "magic"
},
{
"id": 17,
"name": "Martial Arts",
"slug": "marial-arts"
},
{
"id": 27,
"name": "Shounen",
"slug": "shounen"
}
],
"id": "KY0Boj"
},
{
"id_number": 2410,
"name": "Dragon Quest: Dai no Daibouken (2020)",
"name_english": "Dragon Quest: Adventure of Dai (2020)",
"slug": "dragon-quest-adventure-of-dai-2020",
"overview": "A long time ago, there was a valiant swordsman who came to be known simply as \"the hero.\" There was a demon who has caused people suffering. The hero and his companions arrived to challenge the demon to a battle and by combining their powers, the battle was brought swift conclusion. With no one around to cause trouble, the island became a quiet place where everyone could live together in peace.\r\n\r\nSeveral years later, the demon is revived. Our present-day protagonist, Dai, lives on a remote island in the southern seas and dreams of becoming a great hero. When he hears about the demon's revival, Dai and his friends take it upon themselves to stop him and the evil force that revived him. Along the way, Dai discovers the identity of \"the hero,\" the truth behind the evil force who revived the demon, and Dai's own hidden powers that surface in times of peril.",
"type": "TV",
"country_code": "jp",
"poster_path": "56/7e/567e9a3ead04fec9a8ad1a0c5f363d43/567e9a3ead04fec9a8ad1a0c5f363d43.jpg",
"total_episodes": 100,
"latest_episode_sub": 100,
"latest_episode_dub": 100,
"airing_status": 1,
"aired_from": "Oct 3, 2020",
"runtime": 24,
"rating_type": "PG-13",
"has_sub": 1,
"has_dub": 1,
"mal_score": 7.24,
"genres": [
{
"id": 1,
"name": "Action",
"slug": "action"
},
{
"id": 2,
"name": "Adventure",
"slug": "adventure"
},
{
"id": 10,
"name": "Fantasy",
"slug": "fantasy"
},
{
"id": 27,
"name": "Shounen",
"slug": "shounen"
}
],
"id": "OHQs6Y"
},
{
"id_number": 2564,
"name": "Kobayashi-san Chi no OO Dragon",
"name_english": "Miss Kobayashi's Dragon Maid Specials",
"slug": "miss-kobayashis-dragon-maid-specials",
"overview": "Specials included with the BD/DVD release of Kobayashi-san Chi no Maid Dragon.",
"type": "Special",
"country_code": "jp",
"poster_path": "8c/22/8c2252b63d4cdc6fe1025a82a94c6b51/8c2252b63d4cdc6fe1025a82a94c6b51.jpg",
"total_episodes": 7,
"latest_episode_sub": 7,
"latest_episode_dub": 0,
"airing_status": 1,
"aired_from": "Mar 15, 2017",
"runtime": 3,
"rating_type": "PG-13",
"has_sub": 1,
"has_dub": 0,
"mal_score": 7.25,
"genres": [
{
"id": 4,
"name": "Comedy",
"slug": "comedy"
},
{
"id": 10,
"name": "Fantasy",
"slug": "fantasy"
},
{
"id": 36,
"name": "Slice of Life",
"slug": "slice-of-life"
}
],
"id": "babV0K"
},
{
"id_number": 17955,
"name": "Kobayashi-san Chi no Maidragon S: Nippon no Omotenashi - Attend wa Dragon Desu",
"name_english": "Miss Kobayashi's Dragon Maid S: Japanese Hospitality - Attendance is a Dragon",
"slug": "miss-kobayashis-dragon-maid-s-japanese-hospitality-attendance-is-a-dragon",
"overview": "Special episode bundled with the fifth Blu-ray and DVD volume.",
"type": "Special",
"country_code": "jp",
"poster_path": "bf/34/bf34e5e1396f479323b8e887e68114e1/bf34e5e1396f479323b8e887e68114e1.jpg",
"total_episodes": 1,
"latest_episode_sub": 1,
"latest_episode_dub": 1,
"airing_status": 1,
"aired_from": "Jan 19, 2022",
"runtime": 24,
"rating_type": "PG-13",
"has_sub": 1,
"has_dub": 1,
"mal_score": 7.87,
"genres": [
{
"id": 4,
"name": "Comedy",
"slug": "comedy"
},
{
"id": 10,
"name": "Fantasy",
"slug": "fantasy"
},
{
"id": 36,
"name": "Slice of Life",
"slug": "slice-of-life"
}
],
"id": "tqZ3EJ"
},
{
"id_number": 8959,
"name": "Chaos Dragon: Sekiryuu Seneki",
"name_english": "Chaos Dragon",
"slug": "chaos-dragon",
"overview": "In 3015, the year of Huanli, two countries, Donatia and Kouran, are embroiled in a war of supremacy that is tearing the world around them apart. The small island Nil Kamui has suffered exceptionally from the war, with lands conquered in the name of each kingdom and stolen away from the people. To make matters worse, their deity, the Red Dragon, has gone mad, rampaging about Nil Kamui burning villages and killing people indiscriminately.\r\n\r\nIbuki, a descendant of Nil Kamui's royal family, resides at an orphanage and refuses to take on the role of king. Abhorring conflict, Ibuki desires a peaceful resolution, however the chaotic world will not allow for such pacifism when it is being torn asunder by war. Despite his reluctance, Ibuki is drawn deep into this conflict. Can he rise to the occasion and save his country?",
"type": "TV",
"country_code": "jp",
"poster_path": "92/5d/925d4e2c7a40c4f4e418bbe164badc8f/925d4e2c7a40c4f4e418bbe164badc8f.jpg",
"total_episodes": 12,
"latest_episode_sub": 12,
"latest_episode_dub": 12,
"airing_status": 1,
"aired_from": "Jul 2, 2015",
"runtime": 24,
"rating_type": "R",
"has_sub": 1,
"has_dub": 1,
"mal_score": 5.68,
"genres": [
{
"id": 1,
"name": "Action",
"slug": "action"
},
{
"id": 10,
"name": "Fantasy",
"slug": "fantasy"
},
{
"id": 37,
"name": "Supernatural",
"slug": "supernatural"
}
],
"id": "OcjEpQ"
},
{
"id_number": 17970,
"name": "Super Dragon Ball Heroes: Big Bang Mission!!!",
"name_english": "Super Dragon Ball Heroes: Big Bang Mission!!!",
"slug": "super-dragon-ball-heroes-big-bang-mission",
"overview": "In the Time Nest, headquarters of the Time Patrol, the Supreme Kai of Time informs Xeno Trunks and Xeno Pan that her mystical bird Toki-Toki has disappeared. She sends the two of them to find him, while also being worried about a supposed \"Bird of Catastrophe\" that has been released. Meanwhile, Toki-Toki has appeared on Earth in the main timeline, where Goku finds him while training with Vegeta, Gohan, Piccolo, Krillin, and Android 17. Xeno Trunks and Xeno Pan arrive and are happy to see that Toki-Toki is safe, with Xeno Pan explaining that his existence is very important for the inner workings of the multiverse. Suddenly, the group is interrupted by the arrival of all twelve Gods of Destruction. Champa identifies Toki-Toki and Beerus promptly attempts to destroy him, but Toki-Toki uses his magic to defuse Beerus's attack. Goku asks Beerus what's going on, and Beerus explains that he has received a premonition that a mysterious bird will appear in Universe 7 and destroy the entire multiverse. Xeno Trunks protests that this couldn't be possible, and Xeno Pan quickly escapes back to the Time Nest with Toki-Toki. Quitela, Champa and the other Gods of Destruction are angered by the mortals' defiance, and immediately prepare to destroy Earth in response, but Beerus tells them to stand down, saying that as Universe 7's God of Destruction, he will discipline the mortals himself. Goku, Vegeta, Xeno Trunks and the others all power up and prepare to fight against Beerus. Meanwhile, Fu observes the scene from an unknown location, saying that this is the start of his new experiment. He now possesses a strange, glowing tree, and a strange bird called \"Doki-Doki\", the true target of the Gods of Destruction, which appears to be an evil version of Toki-Toki.",
"type": "TV",
"country_code": "jp",
"poster_path": "44/0f/440f62e68ca62b339b712bd3051e2133/440f62e68ca62b339b712bd3051e2133.jpg",
"total_episodes": null,
"latest_episode_sub": 19,
"latest_episode_dub": 0,
"airing_status": 2,
"aired_from": null,
"runtime": 22,
"rating_type": "PG-13",
"has_sub": 1,
"has_dub": 0,
"mal_score": null,
"genres": [
{
"id": 2,
"name": "Adventure",
"slug": "adventure"
},
{
"id": 37,
"name": "Supernatural",
"slug": "supernatural"
}
],
"id": "TDS6dR"
},
{
"id_number": 4279,
"name": "Dragon Ball Z: Saiya-jin Zetsumetsu Keikaku",
"name_english": "Dragon Ball Z: Saiya-jin Zetsumetsu Keikaku",
"slug": "dragon-ball-z-saiya-jin-zetsumetsu-keikaku",
"overview": "Dr. Raichii is the only Tsufurujin (the race eradicated by the Saiyajin many years ago) thought to have survived. He now is going to take revenge on the only surviving Saiyajin still alive, Goku and Vegita. He uses machines that emit destron, a gas that will destroy all life on Earth. Now the the Z warriors only have 72 hours to find and destroy Dr. Raichii.\n\n(Source: ANN)",
"type": "OVA",
"country_code": "jp",
"poster_path": "94/42/9442447a0c7ef88b17f8edfb4f60c3a8/9442447a0c7ef88b17f8edfb4f60c3a8.jpg",
"total_episodes": 2,
"latest_episode_sub": 2,
"latest_episode_dub": 0,
"airing_status": 1,
"aired_from": "Jul 23, 1993",
"runtime": 30,
"rating_type": "PG-13",
"has_sub": 1,
"has_dub": 0,
"mal_score": 6.82,
"genres": [
{
"id": 2,
"name": "Adventure",
"slug": "adventure"
},
{
"id": 4,
"name": "Comedy",
"slug": "comedy"
},
{
"id": 10,
"name": "Fantasy",
"slug": "fantasy"
},
{
"id": 24,
"name": "Sci-Fi",
"slug": "sci-fi"
},
{
"id": 27,
"name": "Shounen",
"slug": "shounen"
}
],
"id": "LaKYKU"
},
{
"id_number": 4311,
"name": "Ikkitousen: Dragon Destiny",
"name_english": "Ikkitousen: Dragon Destiny",
"slug": "ikkitousen-dragon-destiny",
"overview": "Loosely based on the novel Romance of the Three Kingdoms, modern day Japan sees a similar struggle for power between different rival schools with the three strongest being; Kyosho Academy led by Sousou Moutoku, Nanyo Academy by Sonsaku Hakufu and Ryuubi Gentoku from Seito High School. Together these three tousei, each with their own mangatama, fight for the honor of becoming ikkitousen and fulfilling their fated destiny through battle and conquest.\r\n\r\n(Source: ANN)",
"type": "TV",
"country_code": "jp",
"poster_path": "0d/24/0d247f9e1671a8ddbb5a2473751f776e/0d247f9e1671a8ddbb5a2473751f776e.jpg",
"total_episodes": 12,
"latest_episode_sub": 12,
"latest_episode_dub": 12,
"airing_status": 1,
"aired_from": "Feb 26, 2007",
"runtime": 24,
"rating_type": "R+",
"has_sub": 1,
"has_dub": 1,
"mal_score": 6.82,
"genres": [
{
"id": 1,
"name": "Action",
"slug": "action"
},
{
"id": 9,
"name": "Ecchi",
"slug": "ecchi"
},
{
"id": 17,
"name": "Martial Arts",
"slug": "marial-arts"
},
{
"id": 23,
"name": "School",
"slug": "school"
},
{
"id": 31,
"name": "Super Power",
"slug": "super-power"
}
],
"id": "tLwV8Y"
},
{
"id_number": 1692,
"name": "Dragon Ball Super",
"name_english": "Dragon Ball Super",
"slug": "dragon-ball-super",
"overview": "Seven years after the events of Dragon Ball Z, Earth is at peace, and its people live free from any dangers lurking in the universe. However, this peace is short-lived; a sleeping evil awakens in the dark reaches of the galaxy: Beerus, the ruthless God of Destruction.\r\n\r\nDisturbed by a prophecy that he will be defeated by a \"Super Saiyan God,\" Beerus and his angelic attendant Whis start searching the universe for this mysterious being. Before long, they reach Earth where they encounter SON-Goku, one of the planet's mightiest warriors, and his similarly powerful friends.\r\n\r\n[Written by MAL Rewrite]",
"type": "TV",
"country_code": "jp",
"poster_path": "69/08/6908f85a069414d40530042f2cdd8c8a/6908f85a069414d40530042f2cdd8c8a.jpg",
"total_episodes": 131,
"latest_episode_sub": 131,
"latest_episode_dub": 131,
"airing_status": 1,
"aired_from": "Jul 5, 2015",
"runtime": 23,
"rating_type": "PG-13",
"has_sub": 1,
"has_dub": 1,
"mal_score": 7.46,
"genres": [
{
"id": 1,
"name": "Action",
"slug": "action"
},
{
"id": 2,
"name": "Adventure",
"slug": "adventure"
},
{
"id": 4,
"name": "Comedy",
"slug": "comedy"
},
{
"id": 10,
"name": "Fantasy",
"slug": "fantasy"
},
{
"id": 17,
"name": "Martial Arts",
"slug": "marial-arts"
},
{
"id": 27,
"name": "Shounen",
"slug": "shounen"
},
{
"id": 31,
"name": "Super Power",
"slug": "super-power"
}
],
"id": "xJ5BTj"
},
{
"id_number": 468,
"name": "Kobayashi-san Chi no Maid Dragon",
"name_english": "Miss Kobayashi's Dragon Maid",
"slug": "miss-kobayashis-dragon-maid",
"overview": "As Kobayashi sets off for another day at work, she opens her apartment door only to be met by an unusually frightening sight—the head of a dragon, staring at her from across the balcony. The dragon immediately transforms into a cute, busty, and energetic young girl dressed in a maid outfit, introducing herself as Tooru.\r\n\r\nIt turns out that the stoic programmer had come across the dragon the previous night on a drunken excursion to the mountains, and since the mythical beast had nowhere else to go, she had offered the creature a place to stay in her home. Thus, Tooru had arrived to cash in on the offer, ready to repay her savior's kindness by working as her personal maidservant. Though deeply regretful of her words and hesitant to follow through on her promise, a mix of guilt and Tooru's incredible dragon abilities convinces Kobayashi to take the girl in.\r\n\r\nDespite being extremely efficient at her job, the maid's unorthodox methods of housekeeping often end up horrifying Kobayashi and at times bring more trouble than help. Furthermore, the circumstances behind the dragon's arrival on Earth seem to be much more complicated than at first glance, as Tooru bears some heavy emotions and painful memories. To top it all off, Tooru's presence ends up attracting several other mythical beings to her new home, bringing in a host of eccentric personalities. Although Kobayashi makes her best effort to handle the crazy situation that she has found herself in, nothing has prepared her for this new life with a dragon maid.\r\n\r\n[Written by MAL Rewrite]",
"type": "TV",
"country_code": "jp",
"poster_path": "d6/bb/d6bb5e72c26c2628c2a968980960ff5f/d6bb5e72c26c2628c2a968980960ff5f.jpg",
"total_episodes": 13,
"latest_episode_sub": 13,
"latest_episode_dub": 13,
"airing_status": 1,
"aired_from": "Jan 12, 2017",
"runtime": 24,
"rating_type": "PG-13",
"has_sub": 1,
"has_dub": 1,
"mal_score": 8.05,
"genres": [
{
"id": 4,
"name": "Comedy",
"slug": "comedy"
},
{
"id": 10,
"name": "Fantasy",
"slug": "fantasy"
},
{
"id": 36,
"name": "Slice of Life",
"slug": "slice-of-life"
}
],
"id": "3MoO5q"
},
{
"id_number": 4048,
"name": "Dragon Quest: Abel Yuusha Densetsu",
"name_english": "Dragon Quest: Legend of the Hero Abel",
"slug": "dragon-quest-legend-of-the-hero-abel",
"overview": "Dragon Quest is loosely based on Dragon Quest III. The names and some of the characters are familar, but the world map is smaller and a very different shape. The two main characters are Abel and Tialah. Tialah receives the legendary Red Stone from the Aliahan Village sage Master Yogi. Soon after, Tialah is kidnapped by the evil Baramos who wants to use the Red Stone to resurrect The Great Dragon and be granted eternal life. Abel swore to rescue Tialah and he is given the Blue Stone, which can only seal the Dragon once it has been released. \r\n\r\n(Source: AniDB)",
"type": "TV",
"country_code": "jp",
"poster_path": "2a/1e/2a1ec5220b2d8d1f3b81c7e10ca4c851/2a1ec5220b2d8d1f3b81c7e10ca4c851.jpg",
"total_episodes": 42,
"latest_episode_sub": 42,
"latest_episode_dub": 0,
"airing_status": 1,
"aired_from": "Dec 2, 1989",
"runtime": 24,
"rating_type": "G",
"has_sub": 1,
"has_dub": 0,
"mal_score": 6.88,
"genres": [
{
"id": 1,
"name": "Action",
"slug": "action"
},
{
"id": 2,
"name": "Adventure",
"slug": "adventure"
},
{
"id": 10,
"name": "Fantasy",
"slug": "fantasy"
},
{
"id": 27,
"name": "Shounen",
"slug": "shounen"
}
],
"id": "Hsw5Yr"
},
{
"id_number": 18232,
"name": "Dragon Ball Super: Super Hero",
"name_english": "Dragon Ball Super: Super Hero",
"slug": "dragon-ball-super-super-hero",
"overview": "Years after his father is defeated by an adolescent Gokuu Son, Magenta seeks revenge against Gokuu's family and allies. In his quest to resurrect the defunct Red Ribbon Army, Magenta drafts the services of Dr. Hedo, grandson of the evil legendary scientist Dr. Gero. Hedo embarks to invent a new line of superheroic androids to eliminate Gokuu after Magenta manipulates him into believing that Earth's most powerful heroes are actually alien villains.  While Gokuu and Vegeta train offworld, the alien Piccolo mentors Pan, Gokuu's toddler granddaughter, in the same way he once trained Gohan Son, her father. Gohan himself has forsaken his warrior lineage in order to pursue an academic career. Both Piccolo and Gohan must leap into action when their quiet lives are interrupted by the arrival of Gamma 1-gou and Gamma 2-gou—Hedo's new android creations.  While the Gamma androids believe they are fighting for justice, a more sinister project incubates beneath the Red Ribbon headquarters. Gohan and Piccolo take drastic actions to protect Pan and defend the planet against a new robotic menace.",
"type": "Movie",
"country_code": "jp",
"poster_path": "e3/a0/e3a0c29bf713cc99e35de227eb9c93d8/e3a0c29bf713cc99e35de227eb9c93d8.jpg",
"total_episodes": 1,
"latest_episode_sub": 1,
"latest_episode_dub": 1,
"airing_status": 1,
"aired_from": "Jun 11, 2022",
"runtime": 99,
"rating_type": "PG-13",
"has_sub": 1,
"has_dub": 1,
"mal_score": 7.54,
"genres": [
{
"id": 1,
"name": "Action",
"slug": "action"
},
{
"id": 2,
"name": "Adventure",
"slug": "adventure"
},
{
"id": 10,
"name": "Fantasy",
"slug": "fantasy"
},
{
"id": 27,
"name": "Shounen",
"slug": "shounen"
}
],
"id": "eJG5Sh"
},
{
"id_number": 4740,
"name": "Dragon Ball: Super Saiya-jin Zetsumetsu Keikaku",
"name_english": "Dragon Ball: Super Saiya-jin Zetsumetsu Keikaku",
"slug": "dragon-ball-super-saiya-jin-zetsumetsu-keikaku",
"overview": "Remake of Dragon Ball Z: Plan to Destroy the Saiyajin. Extra on Dragonball Raging Blast 2 game on X360/PS3.",
"type": "OVA",
"country_code": "jp",
"poster_path": "07/f5/07f5f8dadfbee19e3bf964bed4884a77/07f5f8dadfbee19e3bf964bed4884a77.jpg",
"total_episodes": 1,
"latest_episode_sub": 1,
"latest_episode_dub": 0,
"airing_status": 1,
"aired_from": "Nov 11, 2010",
"runtime": 30,
"rating_type": "PG-13",
"has_sub": 1,
"has_dub": 0,
"mal_score": 6.72,
"genres": [
{
"id": 2,
"name": "Adventure",
"slug": "adventure"
},
{
"id": 10,
"name": "Fantasy",
"slug": "fantasy"
},
{
"id": 17,
"name": "Martial Arts",
"slug": "marial-arts"
},
{
"id": 24,
"name": "Sci-Fi",
"slug": "sci-fi"
},
{
"id": 27,
"name": "Shounen",
"slug": "shounen"
},
{
"id": 31,
"name": "Super Power",
"slug": "super-power"
}
],
"id": "9kbLqe"
}
],
"totalItems": 106,
"totalPages": 5
}
}
```

### Get Episode List

```
GET /api/anime/episodes
```
```
https://anicrush-api-six.vercel.app/api/anime/episodes?movieId=cp8ogK
Result : 
{
"status": true,
"result": {
"001 - 012": [
{
"id": 93104,
"name": "Episode 1",
"name_english": "Episode 1",
"number": 1,
"is_filler": 0,
"versions": {
"SUB": [
{
"id": 979865,
"type": 0,
"server": "SH-1"
},
{
"id": 979867,
"type": 0,
"server": "SH-2"
},
{
"id": 1299710,
"type": 0,
"server": "SH-3"
}
]
}
},
{
"id": 93131,
"name": "Episode 2",
"name_english": "Episode 2",
"number": 2,
"is_filler": 0,
"versions": {
"SUB": [
{
"id": 980337,
"type": 0,
"server": "SH-1"
},
{
"id": 980343,
"type": 0,
"server": "SH-2"
},
{
"id": 1299715,
"type": 0,
"server": "SH-3"
}
]
}
},
{
"id": 93194,
"name": "Episode 3",
"name_english": "Episode 3",
"number": 3,
"is_filler": 0,
"versions": {
"SUB": [
{
"id": 980947,
"type": 0,
"server": "SH-1"
},
{
"id": 980951,
"type": 0,
"server": "SH-2"
},
{
"id": 1164175,
"type": 0,
"server": "SH-3"
}
]
}
},
{
"id": 93296,
"name": "Episode 4",
"name_english": "Episode 4",
"number": 4,
"is_filler": 0,
"versions": {
"SUB": [
{
"id": 982009,
"type": 0,
"server": "SH-1"
},
{
"id": 982012,
"type": 0,
"server": "SH-2"
},
{
"id": 1166198,
"type": 0,
"server": "SH-3"
}
]
}
},
{
"id": 93440,
"name": "Episode 5",
"name_english": "Episode 5",
"number": 5,
"is_filler": 0,
"versions": {
"SUB": [
{
"id": 983141,
"type": 0,
"server": "SH-1"
},
{
"id": 983143,
"type": 0,
"server": "SH-2"
},
{
"id": 1168582,
"type": 0,
"server": "SH-3"
}
]
}
},
{
"id": 93578,
"name": "Episode 6",
"name_english": "Episode 6",
"number": 6,
"is_filler": 0,
"versions": {
"SUB": [
{
"id": 984063,
"type": 0,
"server": "SH-1"
},
{
"id": 984064,
"type": 0,
"server": "SH-2"
},
{
"id": 1164223,
"type": 0,
"server": "SH-3"
}
]
}
},
{
"id": 93799,
"name": "Episode 7",
"name_english": "Episode 7",
"number": 7,
"is_filler": 0,
"versions": {
"SUB": [
{
"id": 985488,
"type": 0,
"server": "SH-1"
},
{
"id": 985494,
"type": 0,
"server": "SH-2"
},
{
"id": 1168672,
"type": 0,
"server": "SH-3"
}
]
}
},
{
"id": 93800,
"name": "Episode 8",
"name_english": "Episode 8",
"number": 8,
"is_filler": 0,
"versions": {
"SUB": [
{
"id": 986589,
"type": 0,
"server": "SH-1"
},
{
"id": 986598,
"type": 0,
"server": "SH-2"
},
{
"id": 1168784,
"type": 0,
"server": "SH-3"
}
]
}
},
{
"id": 94025,
"name": "Episode 9",
"name_english": "Episode 9",
"number": 9,
"is_filler": 0,
"versions": {
"SUB": [
{
"id": 987658,
"type": 0,
"server": "SH-1"
},
{
"id": 987659,
"type": 0,
"server": "SH-2"
},
{
"id": 1164266,
"type": 0,
"server": "SH-3"
}
]
}
},
{
"id": 94026,
"name": "Episode 10",
"name_english": "Episode 10",
"number": 10,
"is_filler": 0,
"versions": {
"SUB": [
{
"id": 988435,
"type": 0,
"server": "SH-1"
},
{
"id": 988442,
"type": 0,
"server": "SH-2"
},
{
"id": 1168880,
"type": 0,
"server": "SH-3"
}
]
}
},
{
"id": 94352,
"name": "Episode 11",
"name_english": "Episode 11",
"number": 11,
"is_filler": 0,
"versions": {
"SUB": [
{
"id": 989349,
"type": 0,
"server": "SH-1"
},
{
"id": 989351,
"type": 0,
"server": "SH-2"
},
{
"id": 1168929,
"type": 0,
"server": "SH-3"
}
]
}
},
{
"id": 94486,
"name": "Episode 12",
"name_english": "Episode 12",
"number": 12,
"is_filler": 0,
"versions": {
"SUB": [
{
"id": 990530,
"type": 0,
"server": "SH-1"
},
{
"id": 990531,
"type": 0,
"server": "SH-2"
},
{
"id": 1168984,
"type": 0,
"server": "SH-3"
}
]
}
}
]
}
}
```
Query Parameters:
- `movieId` (required): The ID of the movie/anime

### Get Servers

```
GET /api/anime/servers/{id}
```

Query Parameters:
- `movieId` (required): The ID of the movie/anime
- `episode` (optional): Episode number (default: 1)

### Get Sources

```
GET /api/anime/sources
```

Query Parameters:
- `movieId` (required): The ID of the movie/anime (e.g., "vRPjMA")
- `episode` (optional): Episode number (default: 1)
- `server` (optional): Server number (default: 4)
- `subOrDub` (optional): "sub" or "dub" (default: "sub")

Example Request:
```
GET http://localhost:3000/api/anime/sources?movieId=vRPjMA&episode=1&server=4&subOrDub=sub

Result: 
{
"status": true,
"result": {
"sources": [
{
"file": "https://sunburst93.live/_v7/71f87b4028d27b3ba749bd2029f3248245618a740ca81a9a9863f257784436f85c939482f4d306945639b935dc612f232173cae4f207297dea8798f69741cdadcf03986938ae645355b02ac49101bd99d26dbcacac3e6ab00b678324a21474728d09a70cb4b5086fbc36943efb9f1695c522b23382b639d8f473c8ce9a528151/master.m3u8",
"type": "hls"
}
],
"tracks": [
{
"file": "https://mgstatics.xyz/subtitle/73fd2e74257659a8ef9b9cdd004623a5/eng-2.vtt",
"label": "English",
"kind": "captions",
"default": true
}
],
"t": 0,
"intro": {
"start": 31,
"end": 111
},
"outro": {
"start": 1376,
"end": 1447
},
"server": 4
}
}
```

### Get HLS Link

```
GET /api/anime/hls/{animeId}?episode={ep}&server={id}&subOrDub={type}
```

Fetches HLS (HTTP Live Streaming) links with additional metadata for a specific episode.

Query Parameters:
- `episode` (optional): Episode number (default: 1)
- `server` (optional): Server number (default: 4)
- `subOrDub` (optional): "sub" or "dub" (default: "sub")

Example Request:
```
GET http://localhost:3000/api/anime/hls/vRPjMA?episode=1&server=4&subOrDub=sub
```

Example Response:
```json
{
    "status": true,
    "result": {
        "sources": [
            {
                "file": "https://example.com/hls/video.m3u8",
                "type": "hls"
            }
        ],
        "tracks": [
            {
                "file": "https://example.com/subtitles.vtt",
                "label": "English",
                "kind": "captions"
            }
        ],
        "intro": {
            "start": 0,
            "end": 90
        },
        "outro": {
            "start": 1290,
            "end": 1380
        },
        "server": 4
    }
}
```

### Health Check

```
GET /health
```

Returns the API status.

## Error Handling

The API will return appropriate error messages with corresponding HTTP status codes:
- 400: Bad Request (missing required parameters)
- 404: Not Found (anime or episode not found)
- 500: Internal Server Error (server-side issues)

## Notes

- The API includes necessary headers for authentication
- CORS is enabled for cross-origin requests
- The server runs on port 3000 by default (can be changed via PORT environment variable) 

