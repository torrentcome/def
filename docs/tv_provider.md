# Tv provider
The TV Provider database stores the channels and programs from TV Inputs. The TV Provider also publishes and manages the associated permissions so that TV Inputs can see only their own records. For instance, a specific TV Input can see only the channels and programs it has supplied and is prohibited from accessing any other TV Inputs’ channels and programs.

The TV Provider maps "broadcast genre" to "canonical genre" internally. TV Inputs are responsible for populating "broadcast genre" with the value in the underlying broadcast standard, and the "canonical genre" field will automatically be populated with the correct associated genre from android.provider.TvContract.Genres. For example, with broadcast standard ATSC A/65 and program with genre 0x25 (meaning “Sports”), the TV Input will populate the “broadcast genre” with the String “Sports” and TV Provider will populate the “canonical genre” field with the mapped value android.provider.TvContract.Genres.SPORTS.

### Schema
<figure>
  <img src ="../image/tv_provider.png" />
</figure>
