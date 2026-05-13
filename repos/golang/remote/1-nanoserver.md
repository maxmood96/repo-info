## `golang:1-nanoserver`

```console
$ docker pull golang@sha256:4bf4cad7d61e18397c506c33701880660685717eb1248cf09e9f09b9cac75eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `golang:1-nanoserver` - windows version 10.0.26100.32860; amd64

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

### `golang:1-nanoserver` - windows version 10.0.20348.5139; amd64

```console
$ docker pull golang@sha256:5fd4670c3c45a5c8968258d6970145b5f07bedcdac4c75dcab8aeb6e75dae874
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196445607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:162cf6ef830ec038ea0acab5d39432fba39162df3fb8e5c9a7935b6682e2d1d0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Wed, 13 May 2026 00:26:17 GMT
SHELL [cmd /S /C]
# Wed, 13 May 2026 00:26:18 GMT
ENV GOPATH=C:\go
# Wed, 13 May 2026 00:26:18 GMT
USER ContainerAdministrator
# Wed, 13 May 2026 00:26:20 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 13 May 2026 00:26:20 GMT
USER ContainerUser
# Wed, 13 May 2026 00:26:21 GMT
ENV GOLANG_VERSION=1.26.3
# Wed, 13 May 2026 00:27:19 GMT
COPY dir:425bf7ab617c1ef424fac196b0ce6e63a039ad3cb892a60d419e334d4175bd77 in C:\Program Files\Go 
# Wed, 13 May 2026 00:27:21 GMT
RUN go version
# Wed, 13 May 2026 00:27:22 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f7e64b3d2fa107420bd27c4496d658d3de3cea8dd60de344f850118f17c0a3`  
		Last Modified: Wed, 13 May 2026 00:27:34 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406f72ff2321643d190f0ae919c3cca285853488fa4ea92d1e88386ae8b764e6`  
		Last Modified: Wed, 13 May 2026 00:27:34 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936530891d96d1a420a14f0bfd2e8ded1d172a92038b1c68a9b76a032df7c842`  
		Last Modified: Wed, 13 May 2026 00:27:34 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6466a8979d2b93968c1608395ee2f67af24b25e2b8c84eff909f2606e7a84630`  
		Last Modified: Wed, 13 May 2026 00:27:34 GMT  
		Size: 78.9 KB (78915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e04d99c6e6d7eb60de6bbc989ef5307caa535f912c56b269fd2510985acf89`  
		Last Modified: Wed, 13 May 2026 00:27:32 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0360807804f81554f9558ce1351793544acfe74d85adba2ea0dcb2f757f41658`  
		Last Modified: Wed, 13 May 2026 00:27:32 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d8490fd4a84272436cf285d2639b15c9acd9fff3482aaf542f0abbbea75800`  
		Last Modified: Wed, 13 May 2026 00:27:44 GMT  
		Size: 69.2 MB (69234385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a79c018e6944dadc6ae735638a012475c7b53758a918531eb48eaa630590bfb`  
		Last Modified: Wed, 13 May 2026 00:27:32 GMT  
		Size: 86.9 KB (86917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfa9a1d5544b7b6352f37238c96ad6fde2ad019d9eba648929774ca6562ac59`  
		Last Modified: Wed, 13 May 2026 00:27:32 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
