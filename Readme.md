# jBot

## jDownloader + Filebot = jBot ❤️ 


> Tested only with Synology DSM Docker via Portainer


| JDownloader Config                                      | Value                                 |
|:-                                                       |:-                                     |
| Archive Extractor > Extraction: Custom Extraction Path  | /opt/JDownloader/Downloads/EXTRACTED  |
| Settings > Default Download Folder                      | /opt/JDownloader/Downloads            |

## Docker config
> The variables starting with `FB_` and `JD_` have to be defined as environment variables on the host system

> Every variable listed below is __mandatory__

### jDownloader Docker variables
| Variable name   | description             |
| :-              | :-                      |
| JD_EMAIL        | my.jdownloader email    |
| JD_PASSWORD     | my.jdownloader password |

### Filebot Docker variables
| Variable name     | Default value                                           | description |
| :-                | :-                                                      | :-          |
| FB_INPUT_PATH     | `/volume1/input`                                        | Download folder (has to match with the volume definitions) |
| FB_OUTPUT_PATH    | `/volume1/output`                                       | Video folder (has to match with the volume definitions) |
| FB_SORTED_PATH    | `/volume1/output/*unsortable*/{file.structurePathTail}` | Folder for not sortable files |
| FB_LOG_PATH       | `/volume1/output/filebot.log`                           | Path to log file |
| FB_TVSHOW_FORMAT  | `TV-Shows/{n}/Season {s.pad(2)}/{n} - {s00e00} - {t}`   | How to format TV-Shows. [More details](https://www.filebot.net/cli.html) |
| FB_MOVIE_FORMAT   | `Movies/{vf}/{ny}/{ny}`                                 | How to format Movies. [More details](https://www.filebot.net/cli.html) |
| FB_ACTION         | `move`                                                  | rename action |
| FB_LANGUAGE       | `de`                                                    | language code |
| FB_SUBTITLES      | `deu`                                                   | subtitle language |