YQL tables to retrieve ranking and fixtures information for french and
english championship

# How to use it


Make the xml files available on the web or use the one on GitHub

    https://raw.github.com/ymainier/soccer_tables/master/ranking.xml
    https://raw.github.com/ymainier/soccer_tables/master/fixture.xml


Use the YQL console to test 

1. See how to retrieve the [Premier League ranking table][yql_console_ranking].
2. See how to retrieve [all fixtures for Manchester United][yql_console_fixture]

# How to customize requests

For ranking

_Required_ `league` key, the value can be `'french'`, `'english'`,
`'champions_league_group_a'` to `'champions_league_group_h'`

For Fixture

_Required_ `championship` key, the value can be either `'french'` or
`'english'`

_Required_ `team` key, the value must be a team name. It must be valid
for the championship. See the team name used [here for the Premier
League][team_name_english] and [here for Ligue 1][team_name_french]

[yql_console_ranking]: http://developer.yahoo.com/yql/console/?q=use%20%22https%3A//raw.github.com/ymainier/soccer_tables/master/ranking.xml%22%20as%20ranking%3B%20select%20*%20from%20ranking%20where%20league%3D%22english%22%3B "YQL Console example for ranking"
[yql_console_fixture]: http://developer.yahoo.com/yql/console/?q=use%20%22https%3A//raw.github.com/ymainier/soccer_tables/master/fixture.xml%22%20as%20fixture%3B%20select%20*%20from%20fixture%20where%20championship%3D%22english%22%20and%20team%3D%22Manchester%20United%22%3B "YQL Console example for fixture"
[team_name_english]: http://uk.eurosport.yahoo.com/football/premier-league/teams.html "Teams in Premier league" 
[team_name_french]: http://fr.sports.yahoo.com/football/ligue-1/equipes.html "Teams in Ligue 1" 
