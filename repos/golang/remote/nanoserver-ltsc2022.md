## `golang:nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:999b600122c632ef39cdc26899228aa7d48641d237b20b9300887ba7e0c7cc42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.473; amd64

### `golang:nanoserver-ltsc2022` - windows version 10.0.20348.473; amd64

```console
$ docker pull golang@sha256:f5069909999ed4cb5ae1b4c09ac86e3ff4e8168bf542539767e9ed39aa7e4a31
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262553165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5afb24c9f0e86a31a9f4afee62dfcb53731f215dbef4e7e2f71a96270429e26c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 16 Jan 2022 04:54:46 GMT
RUN Apply image ltsc2022-amd64
# Mon, 24 Jan 2022 23:22:08 GMT
SHELL [cmd /S /C]
# Wed, 26 Jan 2022 15:16:54 GMT
ENV GOPATH=C:\go
# Wed, 26 Jan 2022 15:16:55 GMT
USER ContainerAdministrator
# Wed, 26 Jan 2022 15:17:36 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 26 Jan 2022 15:17:37 GMT
USER ContainerUser
# Wed, 26 Jan 2022 15:33:52 GMT
ENV GOLANG_VERSION=1.17.6
# Wed, 26 Jan 2022 15:36:29 GMT
COPY dir:7d325dd3c7e81bd29326c5fb7b320ff307098f97c2703658681dad899622f617 in C:\Program Files\Go 
# Wed, 26 Jan 2022 15:37:23 GMT
RUN go version
# Wed, 26 Jan 2022 15:37:24 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:7691725ee3658d154f940d82fd8c3ff07c0dc589a0c9a93df47ed0ede92a76ab`  
		Size: 117.3 MB (117333150 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:af941a54762cda1c0e1e5ddbfe84c7d2f98e61a1f8ac9d819645377dd6d79003`  
		Last Modified: Tue, 25 Jan 2022 00:13:29 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d449ef7adffb330d62595f8aa91af7dfc9595db039cdf7627c421218669ee1`  
		Last Modified: Wed, 26 Jan 2022 16:07:08 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f36b2324645b4e6df6dcb7e33a033ef288a71fce269301658c9a1cb819e460b`  
		Last Modified: Wed, 26 Jan 2022 16:07:08 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6cdbdeefd71a7c39ec088b586875b397426de35f03629b6a7be4a1c7bb8877e`  
		Last Modified: Wed, 26 Jan 2022 16:07:07 GMT  
		Size: 88.7 KB (88672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91b281211874677fb61a9f1208d662dd8fadb27a8c12c2f5ce4359e3022b0e3`  
		Last Modified: Wed, 26 Jan 2022 16:07:04 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d180c51abe4cb6346000ccde8798d496290412bd5a9202ca95575d9de1d76b8`  
		Last Modified: Wed, 26 Jan 2022 16:16:38 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b88fdc75f2cc88104ece6ee1d5fda95739f98543443e983a6ab2059178e5e1e`  
		Last Modified: Wed, 26 Jan 2022 16:19:31 GMT  
		Size: 145.1 MB (145074729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8045e4fc75887fcc23821eef7f66987b2a03785acb1ddaaa9754cec9d146a1e`  
		Last Modified: Wed, 26 Jan 2022 16:16:38 GMT  
		Size: 49.5 KB (49455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874658f629c130fbfc73267f53c83f4c0c0d688b112b225c5582f11e2db338b0`  
		Last Modified: Wed, 26 Jan 2022 16:16:38 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
