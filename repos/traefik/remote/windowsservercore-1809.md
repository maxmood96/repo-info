## `traefik:windowsservercore-1809`

```console
$ docker pull traefik@sha256:dcbeb6860cd363ffbf75e5bfa4205ca40ac893671edff1de0bebb611a66e7f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `traefik:windowsservercore-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull traefik@sha256:141d2e52601143ef720424f58a829aeb2150d1464d7e544871abde34b3eab3ab
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2425369279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9ae0974a481af0c9c54b77ebb2352bdf28205989dda9280adb21136d160ca6`
-	Entrypoint: `["\/traefik"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 04 Dec 2020 02:13:01 GMT
RUN Install update 1809-amd64
# Wed, 09 Dec 2020 13:30:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Dec 2020 23:57:58 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/traefik/traefik/releases/download/v2.3.4/traefik_v2.3.4_windows_amd64.zip"         -OutFile "/traefik.zip";     Expand-Archive -Path "/traefik.zip" -DestinationPath "/" -Force;     Remove-Item "/traefik.zip" -Force
# Wed, 09 Dec 2020 23:58:02 GMT
EXPOSE 80
# Wed, 09 Dec 2020 23:58:03 GMT
ENTRYPOINT ["/traefik"]
# Wed, 09 Dec 2020 23:58:04 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v2.3.4 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aa4f58cd6da1aaf1a0b44d443bd88e7fbe5b0a6f193995a1a61d6bd63990f314`  
		Size: 672.5 MB (672541583 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a4372d14958dc8a7eaaace9e4774e7f1db524da5eb4474b5e46738848a3a61a5`  
		Last Modified: Wed, 09 Dec 2020 13:54:38 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b374a2371e6098c9d2dba6231dd5668140fa030d0af38ea13f285498aee3a08f`  
		Last Modified: Wed, 09 Dec 2020 23:59:43 GMT  
		Size: 34.5 MB (34490274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76acc5a64fc8176b26de766fb07a28091a8e7c4dce392eda4c5ae498a4adb089`  
		Last Modified: Wed, 09 Dec 2020 23:59:34 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a889f5a061c8bf7d59a6523a397a379c14f579d6b1d14a3853ad22001255133`  
		Last Modified: Wed, 09 Dec 2020 23:59:34 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb7204da2688274f3c5f729fd510dceda6f6ed9b3acd23e2241daf62532c04c`  
		Last Modified: Wed, 09 Dec 2020 23:59:34 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
