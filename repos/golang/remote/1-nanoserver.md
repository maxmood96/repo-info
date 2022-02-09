## `golang:1-nanoserver`

```console
$ docker pull golang@sha256:7ece298c1b5ee84aceb5f2ece90638599e8de8049da5dd6285715799ee37316b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.524; amd64
	-	windows version 10.0.17763.2565; amd64

### `golang:1-nanoserver` - windows version 10.0.20348.524; amd64

```console
$ docker pull golang@sha256:5107e6435698c4d97c4bce4421a460e2ed759513638e3f4fdff3df6be0696f8c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262696442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70945021806e8da2f428961895d7eaa9dd2dd60173b87e9dbe9844b5631e910d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 01 Feb 2022 02:25:40 GMT
RUN Apply image ltsc2022-amd64
# Wed, 09 Feb 2022 13:48:34 GMT
SHELL [cmd /S /C]
# Wed, 09 Feb 2022 13:48:35 GMT
ENV GOPATH=C:\go
# Wed, 09 Feb 2022 13:48:36 GMT
USER ContainerAdministrator
# Wed, 09 Feb 2022 13:49:22 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 09 Feb 2022 13:49:22 GMT
USER ContainerUser
# Wed, 09 Feb 2022 14:04:34 GMT
ENV GOLANG_VERSION=1.17.6
# Wed, 09 Feb 2022 14:07:00 GMT
COPY dir:7d325dd3c7e81bd29326c5fb7b320ff307098f97c2703658681dad899622f617 in C:\Program Files\Go 
# Wed, 09 Feb 2022 14:07:51 GMT
RUN go version
# Wed, 09 Feb 2022 14:07:52 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:3ab33c1d9cc1eaef56d5617b87373ead45d8a4ff7ab7da384afe612ba569a524`  
		Size: 117.5 MB (117457656 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d52811c4b439c00c93423790e004fc266374135015625d93ffb80def500d7b64`  
		Last Modified: Wed, 09 Feb 2022 14:34:32 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:263041b42d7aee90b2defa92fc60f7db99cbbb4686f589864f236b46225ac2a3`  
		Last Modified: Wed, 09 Feb 2022 14:34:31 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0167ac52d6f1254de3c047db124eaa082939ef069a8951247813c10025676d6b`  
		Last Modified: Wed, 09 Feb 2022 14:34:31 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95619fbd5e91dcd251f92bd790e401d548ac0352fc1c7ec9b7a17fd0e46cfdf3`  
		Last Modified: Wed, 09 Feb 2022 14:34:32 GMT  
		Size: 87.2 KB (87240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c044d79e4b1aeb1f8dfdb389f38af55837434f7ff54f3b66176470da6c2c8c`  
		Last Modified: Wed, 09 Feb 2022 14:34:29 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec33e49583534f8de106c8930b8621ea95150e7d5cb227ad216f7b4e6b189cf`  
		Last Modified: Wed, 09 Feb 2022 14:46:29 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38740887ab45281a3dc07f69fe5165b54fde8c4f9551b26ff10b9f4ffcf5a09a`  
		Last Modified: Wed, 09 Feb 2022 14:49:01 GMT  
		Size: 145.1 MB (145096694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7e3e2f4a382cb048643f62f327db3194db6bf179b9ca54b9d5dd9ef0d9f04c`  
		Last Modified: Wed, 09 Feb 2022 14:46:29 GMT  
		Size: 47.7 KB (47714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddddc294528b9f75d305a1180a4c6bd97cf315128e111e1d4459fd5ab78827b`  
		Last Modified: Wed, 09 Feb 2022 14:46:29 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-nanoserver` - windows version 10.0.17763.2565; amd64

```console
$ docker pull golang@sha256:df507fe950fd6aefb1a457c4c1d7828533e4fe810f4efab8df4c76474c8073ae
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.3 MB (248340320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb28922f80ad23575306645a342f25e7081bc7207d9b727c6321d48f84dc8cf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 13:53:17 GMT
SHELL [cmd /S /C]
# Wed, 09 Feb 2022 13:53:18 GMT
ENV GOPATH=C:\go
# Wed, 09 Feb 2022 13:53:18 GMT
USER ContainerAdministrator
# Wed, 09 Feb 2022 13:53:36 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 09 Feb 2022 13:53:37 GMT
USER ContainerUser
# Wed, 09 Feb 2022 14:08:02 GMT
ENV GOLANG_VERSION=1.17.6
# Wed, 09 Feb 2022 14:10:19 GMT
COPY dir:7d325dd3c7e81bd29326c5fb7b320ff307098f97c2703658681dad899622f617 in C:\Program Files\Go 
# Wed, 09 Feb 2022 14:11:09 GMT
RUN go version
# Wed, 09 Feb 2022 14:11:10 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4cc9ef1ef09cb03b1e0bcf4dd4f522871216249d6274e1708e2d4ac554954f34`  
		Last Modified: Wed, 09 Feb 2022 14:37:35 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5779598c13bb3e08d7f4d935491fb18f653c01203f588ca53b5b7cfbad87853`  
		Last Modified: Wed, 09 Feb 2022 14:37:34 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ed348d246f1144e12e763bcccfe197870daa37a206e81fda25e13da6216d2c`  
		Last Modified: Wed, 09 Feb 2022 14:37:33 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a586a7e6e6c370d20a3b167c8aaf3fe683d12d23e8fbb17581c8abc4bf8b0c`  
		Last Modified: Wed, 09 Feb 2022 14:37:33 GMT  
		Size: 71.3 KB (71275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d22d16652ddca955c0d35dcfa5f7485e68e36021e320dbff745d0b025700e3`  
		Last Modified: Wed, 09 Feb 2022 14:37:31 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e13770aa248904ab77f57da834b68e650f6dedc02320085a35704c86a5555d`  
		Last Modified: Wed, 09 Feb 2022 14:49:17 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29034f053051cfb37fb9fae96ce93fc8fb3c63b5be06ff44ec3e4413cc305e5b`  
		Last Modified: Wed, 09 Feb 2022 14:49:51 GMT  
		Size: 145.1 MB (145100880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14083e947fb54ea11a3e729218bbe545261ebee460d31d1d79e6d4c19c90d9e9`  
		Last Modified: Wed, 09 Feb 2022 14:49:17 GMT  
		Size: 74.0 KB (73981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e58015c6124d78995d89d8b46b53052f93f3d1ca53bc638261c9610e52d01d5`  
		Last Modified: Wed, 09 Feb 2022 14:49:17 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
