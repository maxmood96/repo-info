## `golang:1-nanoserver-ltsc2025`

```console
$ docker pull golang@sha256:e877a3866a55fb58a100fb707023325489c88abb719b51abbd3046de272d952f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `golang:1-nanoserver-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull golang@sha256:d4bcceb315a1662952d7421ed623026b6fd6a030890aa2d6fe08e28b8c43f999
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269137556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:361d8bdf33e12f86bbd599852f52a786d243a5fa07e6b7ddc90c9b16868b496c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 10 May 2026 09:46:02 GMT
RUN Apply image 10.0.26100.32860
# Wed, 13 May 2026 00:30:21 GMT
SHELL [cmd /S /C]
# Wed, 13 May 2026 00:30:22 GMT
ENV GOPATH=C:\go
# Wed, 13 May 2026 00:30:22 GMT
USER ContainerAdministrator
# Wed, 13 May 2026 00:30:24 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 13 May 2026 00:30:25 GMT
USER ContainerUser
# Wed, 13 May 2026 00:30:25 GMT
ENV GOLANG_VERSION=1.26.3
# Wed, 13 May 2026 00:31:27 GMT
COPY dir:425bf7ab617c1ef424fac196b0ce6e63a039ad3cb892a60d419e334d4175bd77 in C:\Program Files\Go 
# Wed, 13 May 2026 00:31:29 GMT
RUN go version
# Wed, 13 May 2026 00:31:30 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:34ab6476d71f2d23d05a00ac439000ba4c19d17e5c66f15efbe329ed79bba2bf`  
		Last Modified: Tue, 12 May 2026 22:29:47 GMT  
		Size: 199.7 MB (199739001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56e374292e12697ac816c9c662ab09ee1df4987feaf7423acd4b89a78c1b2c1`  
		Last Modified: Wed, 13 May 2026 00:31:38 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85fa805ee8b2132067342d9c512573f8441f67dc4f148a2798c2e782bdc3df4d`  
		Last Modified: Wed, 13 May 2026 00:31:39 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeca096267113463db51a6b6af16216e699ad83db5e7c65cbc2fd3b0ca3ddf5e`  
		Last Modified: Wed, 13 May 2026 00:31:38 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d13e2c9d5e1e8b8eeef15902964df98bbf368d7b3383bde3bd714b73f0143a`  
		Last Modified: Wed, 13 May 2026 00:31:38 GMT  
		Size: 72.8 KB (72775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad98b806ff9a0d8f3b60f47744394cde5131658a7911df5390ff3620b496c31`  
		Last Modified: Wed, 13 May 2026 00:31:37 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6d1eba91588bcf0dadde19d20de012b0757715e2c5f6730e7d007f43fffefd`  
		Last Modified: Wed, 13 May 2026 00:31:37 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1218fd31853ce1b0e2958f42a9d3c3a37e247688bb20015c9369178eb97ae7`  
		Last Modified: Wed, 13 May 2026 00:31:48 GMT  
		Size: 69.2 MB (69237458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c948aacda1153c100f76d7c5b0f9999daeeaa8a73c8469f078a856291614bc`  
		Last Modified: Wed, 13 May 2026 00:31:37 GMT  
		Size: 81.8 KB (81763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65d44da02d125ed94d8ee24a31ff68c0a06f9de94534cb0b0e5a0862b7ff99b`  
		Last Modified: Wed, 13 May 2026 00:31:36 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
