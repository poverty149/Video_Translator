# Video_Translator


## Dependencies
1. ffmpeg
2. whisper
3. python


## Usage

The following command will generate a `subtitled/video.mp4` file contained the input video with overlayed subtitles.

    python cli.py /path/to/video.mp4 -o subtitled/

The default setting (which selects the `small` model) works well for transcribing English. You can optionally use a bigger model for better results (especially with other languages). The available models are `tiny`, `tiny.en`, `base`, `base.en`, `small`, `small.en`, `medium`, `medium.en`, `large`.

    python cli.py /path/to/video.mp4 --model medium

Adding `--task translate` will translate the subtitles into English:

    python cli.py /path/to/video.mp4 --task translate

Run the following to view all available options:

    python cli.py --help