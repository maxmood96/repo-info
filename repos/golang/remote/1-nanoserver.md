## `golang:1-nanoserver`

```console
$ docker pull golang@sha256:b317fab0a523b54f5f488f4d96ca13fc28066171d7ba86b2530b4983c8f380dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `golang:1-nanoserver` - windows version 10.0.20348.2849; amd64

```console
$ docker pull golang@sha256:e3a7919c180ac2cf11e3c5d865260dd691b81c3130236f96926f5585dbde0a3e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.7 MB (197706923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2663a2fac2ef4d43dda2d8d1bf8afdf648fa854c8ac367cfcb8eae017f42e56`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 02 Nov 2024 23:34:35 GMT
RUN Apply image 10.0.20348.2849
# Thu, 14 Nov 2024 21:18:04 GMT
SHELL [cmd /S /C]
# Thu, 14 Nov 2024 21:18:05 GMT
ENV GOPATH=C:\go
# Thu, 14 Nov 2024 21:18:05 GMT
USER ContainerAdministrator
# Thu, 14 Nov 2024 21:18:08 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Thu, 14 Nov 2024 21:18:08 GMT
USER ContainerUser
# Thu, 14 Nov 2024 21:18:09 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 14 Nov 2024 21:19:15 GMT
COPY dir:d7d597c32e0f94f5ef9191a04cf49682b3853beb64463026d6a674e969c30a19 in C:\Program Files\Go 
# Thu, 14 Nov 2024 21:19:18 GMT
RUN go version
# Thu, 14 Nov 2024 21:19:19 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:815d6b7f925aef8327c34c34073ae54cc1c82120f1058682eac4c8c14ca21c70`  
		Last Modified: Tue, 12 Nov 2024 22:44:32 GMT  
		Size: 120.6 MB (120604951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e1db33143f8dd679938a1933d56de9e17ec546e0677b38a86f97b1c2078698`  
		Last Modified: Thu, 14 Nov 2024 21:19:25 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b66dc17f2278316b0b60bcb9059da11cca267442d4c5a2afee6e88cd9f2b4f4`  
		Last Modified: Thu, 14 Nov 2024 21:19:25 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d1b41aa64b0a1a4757c2fbb063193d42443e7f470aaa0aeb3060dc96eea835`  
		Last Modified: Thu, 14 Nov 2024 21:19:24 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352b409732532336074d37281ca94e84620b1cc01081557cb59ade724b24184a`  
		Last Modified: Thu, 14 Nov 2024 21:19:25 GMT  
		Size: 76.1 KB (76098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d07d30d3edf8d13cbe5cbd9c9d16a060c887e2af3353c25e527ed9d0cf88203`  
		Last Modified: Thu, 14 Nov 2024 21:19:23 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266fd50553582c14d8623415277535b038cb2d2c1bb72f6028754ddb864ed6a5`  
		Last Modified: Thu, 14 Nov 2024 21:19:23 GMT  
		Size: 1.0 KB (1019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3d9e9abf819bdd6ef401dce0969d0466de0f847e61160a3959252e08deb8ba`  
		Last Modified: Thu, 14 Nov 2024 21:19:34 GMT  
		Size: 76.9 MB (76926755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bbd14069b8eba933658f2fb07e259a1d769754de9c2864b682217e8d31004dc`  
		Last Modified: Thu, 14 Nov 2024 21:19:23 GMT  
		Size: 92.7 KB (92742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c30a557eccd713bd7ca20c82e12982750f997598e7f7ebb2bdaa07ce9b5aa65`  
		Last Modified: Thu, 14 Nov 2024 21:19:23 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-nanoserver` - windows version 10.0.17763.6532; amd64

```console
$ docker pull golang@sha256:92e2d5f8533696fde13f4fc077f867617a1378b29913d6cb26b07a08b0ae67d2
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232294317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c29120bf58c9c50c52cdb6d02836f44b3f2d015d69b8856fa317f98679eb4385`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Thu, 14 Nov 2024 21:17:04 GMT
SHELL [cmd /S /C]
# Thu, 14 Nov 2024 21:17:05 GMT
ENV GOPATH=C:\go
# Thu, 14 Nov 2024 21:17:05 GMT
USER ContainerAdministrator
# Thu, 14 Nov 2024 21:17:09 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Thu, 14 Nov 2024 21:17:09 GMT
USER ContainerUser
# Thu, 14 Nov 2024 21:17:10 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 14 Nov 2024 21:18:13 GMT
COPY dir:d7d597c32e0f94f5ef9191a04cf49682b3853beb64463026d6a674e969c30a19 in C:\Program Files\Go 
# Thu, 14 Nov 2024 21:18:17 GMT
RUN go version
# Thu, 14 Nov 2024 21:18:18 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7a88d5402b73c99a99f016c33d5be89ff782422570faf92a6655a219e03332`  
		Last Modified: Thu, 14 Nov 2024 21:18:24 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39edd594bbebcfcc113c9dca698b961a934f3490db7f4ccb6de83f4b7a847518`  
		Last Modified: Thu, 14 Nov 2024 21:18:24 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc9ab9254d5a4a0947a3e5bbfcb9bb8f64b590f9e3ba17ebccc906c1d1f61e5`  
		Last Modified: Thu, 14 Nov 2024 21:18:24 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e26fa73c24b99795326e027a3f395c3b5d85a95e57d6cb03dcd32196892180`  
		Last Modified: Thu, 14 Nov 2024 21:18:24 GMT  
		Size: 73.8 KB (73795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d296f45cfa1bd1f7756888b493a2a43be0d7d2ab580725166eef7fd1102297f`  
		Last Modified: Thu, 14 Nov 2024 21:18:22 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed6a733e908f09db9ecd56dd0f80664fbd47209b27a01072a74036788957ffd0`  
		Last Modified: Thu, 14 Nov 2024 21:18:22 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d46261c9576b28ebd48fccc84bd7f9ef965942f6c4ba48ce368d650b49079e`  
		Last Modified: Thu, 14 Nov 2024 21:18:34 GMT  
		Size: 76.9 MB (76924615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f690598eb58b7b63b8435313936064e59c474af6610a199fb388239fe75d1ba`  
		Last Modified: Thu, 14 Nov 2024 21:18:22 GMT  
		Size: 75.2 KB (75198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779add5d7c47305470a5856f78beb9408af7fe38804bdd7c6f6125ab563d5b90`  
		Last Modified: Thu, 14 Nov 2024 21:18:22 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
