## `golang:1-nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:c73fab6ffb521fec789641a6e30ba3ce4c262dd9f562a063acfa26a4d66b8e33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `golang:1-nanoserver-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull golang@sha256:53783efd0eee9cfd4a41529b7129ae114f45e3a1682c4ed35be9307bb56104be
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196368444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08435efe035641b10e1c4090eefba62ab7eaaef17952ec4193f6e3aa73422cf2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Thu, 07 May 2026 19:22:08 GMT
SHELL [cmd /S /C]
# Thu, 07 May 2026 19:22:11 GMT
ENV GOPATH=C:\go
# Thu, 07 May 2026 19:22:12 GMT
USER ContainerAdministrator
# Thu, 07 May 2026 19:22:32 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Thu, 07 May 2026 19:22:33 GMT
USER ContainerUser
# Thu, 07 May 2026 19:22:33 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 19:24:58 GMT
COPY dir:425bf7ab617c1ef424fac196b0ce6e63a039ad3cb892a60d419e334d4175bd77 in C:\Program Files\Go 
# Thu, 07 May 2026 19:25:02 GMT
RUN go version
# Thu, 07 May 2026 19:25:04 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b39e327d9de6a823c24964cd3d3b351682fb4f41c90058496be55f7923bef4`  
		Last Modified: Thu, 07 May 2026 19:25:18 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63075918086f2befef41dc35ded6c70aa3c300054f313babc23ba17172fe5ae1`  
		Last Modified: Thu, 07 May 2026 19:25:18 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3288bce93c26951ba5ceda945f2c7581dca4d9b0a5b39a47c20598e06bb46fd`  
		Last Modified: Thu, 07 May 2026 19:25:18 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:331e5d809c1a2a59d43107480032dae1bfb57941428e5504fc7adc1482ab4aa2`  
		Last Modified: Thu, 07 May 2026 19:25:18 GMT  
		Size: 76.1 KB (76060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed24b42d577d5dda516f2ad0da3e2497218cad8a13a0658bb3f08d4795ab4a40`  
		Last Modified: Thu, 07 May 2026 19:25:16 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd05151fadd7d6c37dc52069c9b608081335cb1e8c8a81dbe146d8a6acc9b246`  
		Last Modified: Thu, 07 May 2026 19:25:16 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba50e6513a33034f923998d120cbb538b1e3ae24f22eb69092d2cec43545a4fb`  
		Last Modified: Thu, 07 May 2026 19:25:28 GMT  
		Size: 69.2 MB (69235593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6faf2896414d978257612ee319d9cbfb25850f484e162ce7eba4096fb1f32bd4`  
		Last Modified: Thu, 07 May 2026 19:25:16 GMT  
		Size: 94.2 KB (94187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4e96bb4a623c7d1f681652c8f92fae116af23af39964abaf65c559f654d2b1e`  
		Last Modified: Thu, 07 May 2026 19:25:16 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
