## `golang:1-nanoserver-ltsc2025`

```console
$ docker pull golang@sha256:e95dda6f1e74f85b154d2994a601ca22bc23e2146611a994c59f49b29bb0636d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `golang:1-nanoserver-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull golang@sha256:9ccd7501fd24c6d5c6c935d196deb310fe6932db69cac44bee31302281caaefb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273497754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d40f739ef2d915ae8575b3003ba1bd539daaa5767fd160d9ec1f6f5b2848ebc0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 10 May 2025 00:58:48 GMT
RUN Apply image 10.0.26100.4061
# Wed, 14 May 2025 21:14:11 GMT
SHELL [cmd /S /C]
# Wed, 14 May 2025 21:14:12 GMT
ENV GOPATH=C:\go
# Wed, 14 May 2025 21:14:13 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 21:14:15 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 14 May 2025 21:14:16 GMT
USER ContainerUser
# Wed, 14 May 2025 21:14:17 GMT
ENV GOLANG_VERSION=1.24.3
# Wed, 14 May 2025 21:15:20 GMT
COPY dir:11c24136d74cfff65bad471f7cd999b92a92062aeed3b3acc0519a1823e1187a in C:\Program Files\Go 
# Wed, 14 May 2025 21:15:23 GMT
RUN go version
# Wed, 14 May 2025 21:15:24 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:9824510349be04d2eb26f9aaba1d016eddcbed10bdcd6681f4636c948766f3d1`  
		Last Modified: Tue, 13 May 2025 23:02:56 GMT  
		Size: 191.4 MB (191412015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b20a59e1970814df9234ccab3e3042a288705465b09e0c1a6da98da26016edf5`  
		Last Modified: Wed, 14 May 2025 21:15:30 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8595cba111c13eaa7d9fc2289472241dc3e2d47c9217371dd7d4f46e204a23`  
		Last Modified: Wed, 14 May 2025 21:15:30 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec2824be3c42d15d0661bcb1f1be5ebdbabe10e507ba49121375864aea9053e`  
		Last Modified: Wed, 14 May 2025 21:15:30 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d30965497f94ac3e97f9b6d26392628c27294fafa6ad593c0731e496ed2bf4`  
		Last Modified: Wed, 14 May 2025 21:15:30 GMT  
		Size: 76.0 KB (75967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a14114cd125e4c07f6317dadc36c08ce3fe73e676e3875344de874385a9b649`  
		Last Modified: Wed, 14 May 2025 21:15:28 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d8cd6f02d4f80a6ce7948a2446e960bcf97acb518dfcbdaf33fe77012d81f8`  
		Last Modified: Wed, 14 May 2025 21:15:28 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f37c5c3e341d4264b21232fd876f5d0fa635a2b5cb356c9cc549bd21abc479d`  
		Last Modified: Wed, 14 May 2025 21:15:41 GMT  
		Size: 81.9 MB (81915515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0aa8d9ccff1344b7d9a44e8a1e4c80b0c20bea015f4d75b6d45ab7a3d8837ce`  
		Last Modified: Wed, 14 May 2025 21:15:28 GMT  
		Size: 87.7 KB (87695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9524759fda7b5bd89fe0f1d62a3b671ad9f21e56b83240685cb58b2e5c0cb177`  
		Last Modified: Wed, 14 May 2025 21:15:28 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
