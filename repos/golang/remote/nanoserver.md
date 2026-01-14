## `golang:nanoserver`

```console
$ docker pull golang@sha256:b2541110b3944c3e5e78f88e2758d931cadc1630fd14d5f2c863aa557d60cea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `golang:nanoserver` - windows version 10.0.26100.32230; amd64

```console
$ docker pull golang@sha256:194efc304154fd3a3166e83da8f808c731078b0db3252fafcfaf2e36e9f933c1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261146006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e98594614ea268b420ca57ad0ac87ddbf3998291efbcdadf0740b266257c124`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Tue, 13 Jan 2026 23:41:03 GMT
SHELL [cmd /S /C]
# Tue, 13 Jan 2026 23:41:03 GMT
ENV GOPATH=C:\go
# Tue, 13 Jan 2026 23:41:04 GMT
USER ContainerAdministrator
# Tue, 13 Jan 2026 23:41:05 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 13 Jan 2026 23:41:06 GMT
USER ContainerUser
# Tue, 13 Jan 2026 23:41:06 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 13 Jan 2026 23:42:12 GMT
COPY dir:88c362617e5a6c2a31b1694bcf871ea0c6e4eea9f08403024fec2c23b6b3826c in C:\Program Files\Go 
# Tue, 13 Jan 2026 23:42:15 GMT
RUN go version
# Tue, 13 Jan 2026 23:42:16 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:56 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b1d29c65427c975161333fe831880eda9f50278d25028e6a1135a5e6f22b34`  
		Last Modified: Tue, 13 Jan 2026 23:42:37 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:688a69da73107a160420b3e0805c7263d4d2f99acf61092e41307643d75ef26e`  
		Last Modified: Tue, 13 Jan 2026 23:42:37 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9958ae6ca2a74167e2c86c38490c92ba119857c94f2a307cbf0419f5faeba5`  
		Last Modified: Tue, 13 Jan 2026 23:42:37 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0880d441a705ae7280254d0c88cbe9ff1990b0449bc73f09de775cd852085b8`  
		Last Modified: Tue, 13 Jan 2026 23:42:37 GMT  
		Size: 71.8 KB (71826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ac5a4a7124b29268f70c1be6401328d6e4a73e99e550b804bdaf805dbeba42`  
		Last Modified: Tue, 13 Jan 2026 23:42:37 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5ec327033e9d982a0f79cd91687f61b6612df9e7fa987a8e174c4d590182c4`  
		Last Modified: Tue, 13 Jan 2026 23:42:41 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33cda91bd96f314536be464aa5164ea69beb3a62bc4ed968fc61a48259aa73ff`  
		Last Modified: Tue, 13 Jan 2026 23:42:45 GMT  
		Size: 61.9 MB (61904194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c812c7598eb60fd8f7b7ccf129ebdd1f326b75ad68f58fb62174fe9dfbd9f1`  
		Last Modified: Tue, 13 Jan 2026 23:42:37 GMT  
		Size: 86.8 KB (86829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daacc8f0bd77fb93601bc44259e0dc142563df5e69b1542131e524bbc3c3cb21`  
		Last Modified: Tue, 13 Jan 2026 23:42:37 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:nanoserver` - windows version 10.0.20348.4648; amd64

```console
$ docker pull golang@sha256:f26df32d504f6148562b843e3090e21c21f33e5f9f4a3ed561120e0cd85883c1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188764921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe65d068d57a8e0fdd05d9bfe527428b1f15deeb13f37a17ed08a5b75a11473d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Tue, 13 Jan 2026 23:36:41 GMT
SHELL [cmd /S /C]
# Tue, 13 Jan 2026 23:36:42 GMT
ENV GOPATH=C:\go
# Tue, 13 Jan 2026 23:36:42 GMT
USER ContainerAdministrator
# Tue, 13 Jan 2026 23:36:44 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 13 Jan 2026 23:36:45 GMT
USER ContainerUser
# Tue, 13 Jan 2026 23:36:45 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 13 Jan 2026 23:37:42 GMT
COPY dir:88c362617e5a6c2a31b1694bcf871ea0c6e4eea9f08403024fec2c23b6b3826c in C:\Program Files\Go 
# Tue, 13 Jan 2026 23:37:44 GMT
RUN go version
# Tue, 13 Jan 2026 23:37:45 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:12:21 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b181878eecbb581fb608cca6fd3c8366df3a941307647d600b3202f2c884d70`  
		Last Modified: Tue, 13 Jan 2026 23:38:14 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e5bedb1dc64d7d920429bba8afa254fcd29ff6f955a41f228b491d84a98c88`  
		Last Modified: Tue, 13 Jan 2026 23:38:14 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8122ec73fce831709140bc13a4c0aa6a75905609a19da8df763dff36b8df1c98`  
		Last Modified: Tue, 13 Jan 2026 23:38:14 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f20b251155c1a551bee7bd3b28e3951e513926086e8d97368895a27cbfb04ca`  
		Last Modified: Tue, 13 Jan 2026 23:38:14 GMT  
		Size: 76.7 KB (76718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd7c8346c910cecf5bdc4d7320941888d44c6daf6c08d7ae3594c225de520a7`  
		Last Modified: Tue, 13 Jan 2026 23:38:14 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e42bce27433690334865e5bdf9a1961c1491dfc8e913acf5850698ba55aa8d`  
		Last Modified: Tue, 13 Jan 2026 23:38:14 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f8b679fdd882226a6e484fbee18965c36ee6126dbfa763f7188919b216e6cf`  
		Last Modified: Tue, 13 Jan 2026 23:38:19 GMT  
		Size: 61.9 MB (61898783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf880a122acf0a2fa23612735c37c0f65d2828bc761321e2eed81e116afe96c3`  
		Last Modified: Tue, 13 Jan 2026 23:38:14 GMT  
		Size: 86.0 KB (86011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab95ff189aee144d9b0fe26cf355504d3fd8344d7d2adc8622086824fd165c5`  
		Last Modified: Tue, 13 Jan 2026 23:38:14 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
