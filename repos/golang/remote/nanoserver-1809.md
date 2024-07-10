## `golang:nanoserver-1809`

```console
$ docker pull golang@sha256:e4eb5ffc13ff916b070c5c5ca95ffb79bb68ccdd53392bd444466e7fc5793abb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `golang:nanoserver-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull golang@sha256:025c7a355f8582cc599b15645edc83f8de46514b8069b3e6d2a0e64dffda43a6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227738649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:030f676b27d7d17805e1dc57e898ed6da10d5d42d7af296d30f520b42858b00b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 03 Jul 2024 00:02:58 GMT
RUN Apply image 10.0.17763.6054
# Wed, 10 Jul 2024 18:13:09 GMT
SHELL [cmd /S /C]
# Wed, 10 Jul 2024 18:13:10 GMT
ENV GOPATH=C:\go
# Wed, 10 Jul 2024 18:13:11 GMT
USER ContainerAdministrator
# Wed, 10 Jul 2024 18:13:13 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 10 Jul 2024 18:13:14 GMT
USER ContainerUser
# Wed, 10 Jul 2024 18:13:14 GMT
ENV GOLANG_VERSION=1.22.5
# Wed, 10 Jul 2024 18:14:14 GMT
COPY dir:df9ea26aca7559ebf2412d95343abd7f451e9742ee3cc83124365ec0b4f8b5ea in C:\Program Files\Go 
# Wed, 10 Jul 2024 18:14:20 GMT
RUN go version
# Wed, 10 Jul 2024 18:14:21 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:53308e1345e8a502fe824770c132f9d645d42108fee87a0708ea8814c901e40d`  
		Last Modified: Tue, 09 Jul 2024 17:42:24 GMT  
		Size: 155.1 MB (155081383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40bf8b52bed009e91977d36a3803cfbc92c311c06b874df08fc8c1fe5c1a9276`  
		Last Modified: Wed, 10 Jul 2024 18:14:27 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d64e7686e7c6be3e68fc891f8fe1a21adce2abd1ece7058ea71f741a0ca95796`  
		Last Modified: Wed, 10 Jul 2024 18:14:26 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca77fdd2fa76526336a36f9c5fc458e97ebb4adbf7e900ec68ef816eda701040`  
		Last Modified: Wed, 10 Jul 2024 18:14:26 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed9dbb4024907fdf92d71e5154725fdad69211fc3b2c1a07127b0e720b5d25c`  
		Last Modified: Wed, 10 Jul 2024 18:14:26 GMT  
		Size: 73.2 KB (73200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90afd3d6b00447aea74f5f8ff5bcd1090504489e0fee4265b966275f57086247`  
		Last Modified: Wed, 10 Jul 2024 18:14:24 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2298a271982893d87c5e9fb749288c424cae471c79b1aeb51ce03b5faad4c2ea`  
		Last Modified: Wed, 10 Jul 2024 18:14:24 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65044f62cc229fdadf8408b4695a78a8be91caf55bc953d9d4d6dcc6280df2ae`  
		Last Modified: Wed, 10 Jul 2024 18:14:35 GMT  
		Size: 71.4 MB (71366645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6eb5d0ba1375d34154b2a4ab80fb48226b1e742dc26f859e5d27ff08b9f1d19`  
		Last Modified: Wed, 10 Jul 2024 18:14:25 GMT  
		Size: 1.2 MB (1210931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b516bd4dd3d9c8dc3fba4b87a7824906c35d37118abaff9bb728489b97ab8d2f`  
		Last Modified: Wed, 10 Jul 2024 18:14:24 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
