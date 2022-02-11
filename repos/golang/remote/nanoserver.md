## `golang:nanoserver`

```console
$ docker pull golang@sha256:244977d945fa63ed07f46e58d9432d7cc8014606f4672c02f160d0e789c5e353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.524; amd64
	-	windows version 10.0.17763.2565; amd64

### `golang:nanoserver` - windows version 10.0.20348.524; amd64

```console
$ docker pull golang@sha256:6511ac890bfc0c2c35758c41c19006f5889e1a8e39f46b2c4281157f5a7d3787
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262725857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7707b21aed483a75b9c8fbaf189b7389674aba1e2a27c112c1d7eda670159e`
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
# Fri, 11 Feb 2022 01:23:29 GMT
ENV GOLANG_VERSION=1.17.7
# Fri, 11 Feb 2022 01:25:53 GMT
COPY dir:3f60b0c715184a0a0eb2fa6d2b3b41854dcbc305dbacfafb652d8009bf879980 in C:\Program Files\Go 
# Fri, 11 Feb 2022 01:26:46 GMT
RUN go version
# Fri, 11 Feb 2022 01:26:47 GMT
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
	-	`sha256:5014f888aaf7f414a1089a86d8c774ab5681d1064297340d3bc4d3346e86d7df`  
		Last Modified: Fri, 11 Feb 2022 01:47:56 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:272d2503dd95cf21e5220c4c88da2c5c7cd60afa24d0d2d9adfabc0691890a54`  
		Last Modified: Fri, 11 Feb 2022 01:50:35 GMT  
		Size: 145.1 MB (145127431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4dae220fbe4a7b51cd89a3b3bdecfc8821c9ff20678b7b4a2320cb8d823c5c`  
		Last Modified: Fri, 11 Feb 2022 01:47:56 GMT  
		Size: 46.4 KB (46389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c262bd2aab80f13708fb767afdf56856e94c310d4b9e3c209eea873cd3c2af92`  
		Last Modified: Fri, 11 Feb 2022 01:47:56 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:nanoserver` - windows version 10.0.17763.2565; amd64

```console
$ docker pull golang@sha256:f91c7df80a0e0f9a736acdcb73cf83a481974d2aec7a76e9c14170ac4f3c8453
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 MB (248364103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86ff54ba389ca169799699ebe3e563c2b0166a397a6e62dc4f147f124b1010c`
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
# Fri, 11 Feb 2022 01:27:00 GMT
ENV GOLANG_VERSION=1.17.7
# Fri, 11 Feb 2022 01:29:20 GMT
COPY dir:3f60b0c715184a0a0eb2fa6d2b3b41854dcbc305dbacfafb652d8009bf879980 in C:\Program Files\Go 
# Fri, 11 Feb 2022 01:30:03 GMT
RUN go version
# Fri, 11 Feb 2022 01:30:04 GMT
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
	-	`sha256:452359048fbed7be890ee04ef4c16c9cf866deb68964f2259cdbddef19143a99`  
		Last Modified: Fri, 11 Feb 2022 01:50:52 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895f4d78198e1fe08798b240238dd6da6cf9491d13a91f8572d0f88778134dec`  
		Last Modified: Fri, 11 Feb 2022 01:53:30 GMT  
		Size: 145.1 MB (145122663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a06a5d41cb9fcdf10b6dba80e69fca65a55256209de18b60a1a7d263e21b37`  
		Last Modified: Fri, 11 Feb 2022 01:50:52 GMT  
		Size: 76.0 KB (75979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a627d949453912c617c9caf0d3164a6eebd095de505873d0322fcae4633d3cc`  
		Last Modified: Fri, 11 Feb 2022 01:50:52 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
