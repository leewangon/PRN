# PRN
A path-based relation network for knowledge completion



## 1. Sentence Builder

    > python sentenceBuilder.py {kb_path} {relation_list} {pra_output_path} {sentence_output_path}

> **Output Example**
Jeanne_Moreau	/people/person/place_of_birth	inv_/people/person/places_lived./people/place_lived/location	inv_/people/person/nationality	Germany
Albert_Wolsky	/people/person/place_of_birth	inv_/people/person/places_lived./people/place_lived/location	inv_/people/person/nationality	Germany
Roman_Polanski	/people/person/place_of_birth	inv_/people/person/places_lived./people/place_lived/location	inv_/people/person/nationality	Germany
Catherine_Deneuve	/people/person/place_of_birth	inv_/people/person/places_lived./people/place_lived/location	inv_/people/person/nationality	Germany
Charles_Baudelaire	/people/person/place_of_birth	inv_/people/person/places_lived./people/place_lived/location	inv_/people/person/nationality	Germany

## 2. Story Generator

    > python storyGenerator.py {relation_list} {sentence_output_path} {story_output_path}

> **Output Example**
> 1 Robert_De_Niro inv_/celebrities/celebrity/sexual_relationships./celebrities/romantic_relationship/celebrity inv_/award/award_nominee/award_nominations./award/award_nomination/nominated_for inv_/film/film/language German_Language
2 Robert_De_Niro /people/person/nationality inv_/film/film/release_date_s./film/film_regional_release_date/film_release_region inv_/film/film/language Vietnamese_Language
3 Robert_De_Niro /people/person/nationality inv_/tv/tv_program/country_of_origin inv_/film/film/language Italian_Language
4 Robert_De_Niro /award/award_winner/awards_won./award/award_honor/award_winner inv_/film/film/executive_produced_by inv_/film/film/language English_Language
5 Robert_De_Niro /people/person/nationality inv_/film/film/release_date_s./film/film_regional_release_date/film_release_region inv_/film/film/language German_Language
...
21 Robert_De_Niro /people/person/languages ?	English_Language	4 9 10 13 14 

## 3. A path based relation network learning for knowledge completion

    > python linkPrediction.py {target_relation} {target_story_path} {output_path}

> **Output Example**
> david_j /people/person/nationality ? united_kingdom -> united_states_of_america (X) 
terry_crews /people/person/nationality ? united_states_of_america -> united_states_of_america (O) 
william_h._macy /people/person/nationality ? united_states_of_america -> united_states_of_america (O) 
morgan_freeman /people/person/nationality ? united_states_of_america -> united_states_of_america (O) 
david_spade /people/person/nationality ? united_states_of_america -> united_states_of_america (O) 



