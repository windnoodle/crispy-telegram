# crispy-telegram

## twilight zone
Determine if a time is in the magical hour of the daylight savings time shift.
In the Spring, the magical hour will be skipped.
In the Fall, the magical hour will repeated. On the first occurence of the hour is where the magic happens.

*Usage*
> magicality = twilight_zone.get_magic_shift(now_utc, candidate_time) \
> assert magicality == twilight_zone.SPRING_AHEAD

> magicality = twilight_zone.get_magic_shift(now_utc, candidate_time) \
> assert magicality == twilight_zone.FALL_BEHIND \
> assert bool(magicality) == true

> assert twilight_zone.FALL_BEHIND.timedelta == timedelta('1 hour') \
> assert twilight_zone.SPRING_AHEAD.timedelta == timedelta('-1 hour')
