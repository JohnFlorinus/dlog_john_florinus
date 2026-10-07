# dlog

dlog keeps your Downloads folder tidy. The script `dlogd` watches `~/Downloads`
and moves every new file into a folder based on its file type. Examples:
~/Downloads/beautiful.jpg   ->  ~/Downloads/images/beautiful.jpg
~/Downloads/notes.docx      ->  ~/Downloads/documents/notes.docx

## Usage

No installation needed, only bash.

./dlogd              # watches ~/Downloads
./dlogd ~/somedir    # watches another folder

Every move is printed:

watching /home/john/Downloads
beautiful.jpg -> images/
notes.docx -> documents/
awesome_1.mp4 -> videos/

Stop it with `Ctrl+C`.

## Testing

Split a tmux window in two with Ctrl+b %. Run ./dlogd in one pane and create files in the other:

cd ~/Downloads
touch test.txt
ls -R