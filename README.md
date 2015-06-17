FFMPEG
========

Installs FFMPEG from source code with the following libs:
- libfdk-aac
- libspeex
- libopus
- libvpx
- libtheora
- libvorbis
- libmp3lame
- x264
- yasm

Installation
--------------

`ansible-galaxy install palkan.ffmpeg`

Role Variables
--------------

`defaults/main.yml`

| Name                        | Default Value | Description                                                      |
|-----------------------------|---------------|------------------------------------------------------------------|
| ffmpeg_source_dir           | /usr/local/src | Sources path                                                    |
| ffmpeg_build                | /usr/local/ffmpeg_build | Build path                                             |
| ffmpeg_bin_dir              | /usr/local/bin | Binaries path                                                   |
| ffmpeg_env                  | PKG_CONFIG_PATH: "{{ ffmpeg_build }}/lib/pkgconfig" | Environment vars           |
| ffmpeg_flags                | ... (see source) | FFMPEG compilation flags                                      |

Example Playbook
-------------------------

    - hosts: servers
      roles:
         - palkan.ffmpeg