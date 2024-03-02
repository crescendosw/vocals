# vocals
Cantamus vocal parts.

Files imported from [Google Drive](https://drive.google.com/uc?export=download&id=1Ojw5hAKdWjjJcAcpK0wk-BbzcJpTdc6j). 

Script used to import songs from Google Drive into "vocals" repository is in [scripts](https://github.com/crescendosw/scripts) repository under `./import_vocals.sh`.

Vocal parts are integrated into the [hymnals](https://github.com/crescendosw/hymnals) repository via the script `./server/manifest_gen.py`

# Instructions

## Inject Vocals into Hymnals

1. Add desired song directories to local "vocals" repository
* Optionally update `availScores.json`
2. Open Terminal (Cmd+Space, type "Terminal")
3. Download latest version of the scripts & hymnals repository
* `cd ~/dev/crescendo/scripts`
* `git pull`
* `cd ~/dev/crescendo/hymnals`
* `git pull`
4. Run script to inject new vocals into hymnals
* `python3 ../scripts/server/manifest_gen.py`
5. Verify changes made to hymnals repository (bug Mike if unexpected)
* `cd ~/dev/crescendo/hymnals`
* `git status`
6. Push hymnals changes up to Sing Your Part
* `cd ~/dev/crescendo/hymnals`
* `git add .`
* `git commit -m "<meaningful message>"`
* `git push`
7. Within 1-2 minutes, look for changes in app (may require restart)