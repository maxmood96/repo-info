## `golang:1-nanoserver`

```console
$ docker pull golang@sha256:e35c3934dfc59c15b03c92ca9d7494819ffc29c6f4ac3fb4848a9042a5ddf649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `golang:1-nanoserver` - windows version 10.0.20348.2762; amd64

```console
$ docker pull golang@sha256:9028f20281cf72f97219621676910b20f57eb6df485940047712c69d72e6f770
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.6 MB (197599135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b607ef710c4cb1a2fed7fe4500442317dcdba9675e245038d3a8d3a0b67b84`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 06 Oct 2024 04:41:34 GMT
RUN Apply image 10.0.20348.2762
# Thu, 10 Oct 2024 00:08:31 GMT
SHELL [cmd /S /C]
# Thu, 10 Oct 2024 00:08:32 GMT
ENV GOPATH=C:\go
# Thu, 10 Oct 2024 00:08:32 GMT
USER ContainerAdministrator
# Thu, 10 Oct 2024 00:08:35 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Thu, 10 Oct 2024 00:08:35 GMT
USER ContainerUser
# Thu, 10 Oct 2024 00:08:36 GMT
ENV GOLANG_VERSION=1.23.2
# Thu, 10 Oct 2024 00:10:17 GMT
COPY dir:c6fb990fe30b997cadb6a7ba3c4a7d5a2c2077f37e11b2dbb8f33ee41ec246ca in C:\Program Files\Go 
# Thu, 10 Oct 2024 00:10:20 GMT
RUN go version
# Thu, 10 Oct 2024 00:10:21 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:4a74766ac776b275376a07d5357fd928f8b871c9e3d409729ed7e1ff0c1e608c`  
		Last Modified: Wed, 09 Oct 2024 13:26:44 GMT  
		Size: 120.5 MB (120511000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6766fd5bc5763e107fb765ed8b366e69d7266ab5c3e57061fdade2e12d4cd1`  
		Last Modified: Thu, 10 Oct 2024 00:10:25 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b593263d40bbbfcf77fe343d1fe27a17b3eeb355831ef23ab2ce9b0bcffd0780`  
		Last Modified: Thu, 10 Oct 2024 00:10:25 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada6cf9e1810645eab37f16f5a18eca0e56e08684959cde3c5e84b51782febd7`  
		Last Modified: Thu, 10 Oct 2024 00:10:25 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b3dbd729a283c1fe5dfa176140bf61ca33e56f1e98f9d88c1f87082cd4b0b18`  
		Last Modified: Thu, 10 Oct 2024 00:10:25 GMT  
		Size: 78.2 KB (78231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f34df5c1411ddf02eaf99c2e415e87eda51eb12d99ae1552a7c95a7b7311e8`  
		Last Modified: Thu, 10 Oct 2024 00:10:24 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa83b1d6489d121f508ce11d5cf818b506619c8ed87d7953d4db853dcdaf22ad`  
		Last Modified: Thu, 10 Oct 2024 00:10:24 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dd01dbf243bc45c9b652a86dfee012fc62d31dc3f1aeba6445f737334ea8545`  
		Last Modified: Thu, 10 Oct 2024 00:10:35 GMT  
		Size: 76.9 MB (76921951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6361995a9c48e443e858e40feb67aecf5b3717a2ba564ae6223f86f5dcaf7863`  
		Last Modified: Thu, 10 Oct 2024 00:10:24 GMT  
		Size: 81.5 KB (81533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b284561aa035faaa7794641af1d83e138546fa04905e093be8e499101a2d8f`  
		Last Modified: Thu, 10 Oct 2024 00:10:24 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-nanoserver` - windows version 10.0.17763.6414; amd64

```console
$ docker pull golang@sha256:348ecf955fa4dcbeb0030ca735535c08222623095d15bba0cc1f3ba1e380141e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232183734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d944aeaead6a4c6a5ae5f20b62dc5c1c263d2f8c375ce42f7944adcc4388cb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 04 Oct 2024 21:34:09 GMT
RUN Apply image 10.0.17763.6414
# Thu, 10 Oct 2024 00:03:57 GMT
SHELL [cmd /S /C]
# Thu, 10 Oct 2024 00:04:01 GMT
ENV GOPATH=C:\go
# Thu, 10 Oct 2024 00:04:01 GMT
USER ContainerAdministrator
# Thu, 10 Oct 2024 00:04:04 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Thu, 10 Oct 2024 00:04:05 GMT
USER ContainerUser
# Thu, 10 Oct 2024 00:04:05 GMT
ENV GOLANG_VERSION=1.23.2
# Thu, 10 Oct 2024 00:05:06 GMT
COPY dir:c6fb990fe30b997cadb6a7ba3c4a7d5a2c2077f37e11b2dbb8f33ee41ec246ca in C:\Program Files\Go 
# Thu, 10 Oct 2024 00:05:09 GMT
RUN go version
# Thu, 10 Oct 2024 00:05:10 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:361c9b9fb81cb50150f4deebc9faf195fc69734bc9c24694485fdec906c8f29a`  
		Last Modified: Tue, 08 Oct 2024 18:11:37 GMT  
		Size: 155.1 MB (155093579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f997371c5f088e21b32ac1ca6d7b77c77ff6b025d62575ecbd734f7c51bf7e5`  
		Last Modified: Thu, 10 Oct 2024 00:05:16 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e4d89491eb09e682fe06006541163def88bfb1a04486092c297690d2e772a1`  
		Last Modified: Thu, 10 Oct 2024 00:05:16 GMT  
		Size: 1.1 KB (1095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9fa2b9aa26e07e794fe331730d8e1e0caa650b08f7f5c4a3dba12784956ad64`  
		Last Modified: Thu, 10 Oct 2024 00:05:16 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c20a8fb93e4e363c26fca8a9a8b5cf04f384359a28ccbc4cab86cc7df1822cd`  
		Last Modified: Thu, 10 Oct 2024 00:05:16 GMT  
		Size: 84.2 KB (84222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f8d4437084acde3eea2a65b26232039bdc50b63dc41f7233f0d6a1afb40174`  
		Last Modified: Thu, 10 Oct 2024 00:05:14 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77bf1382b6e99bfd34c9c9973470345fefbdd72ac36dca11e031077f24c979b`  
		Last Modified: Thu, 10 Oct 2024 00:05:14 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded386b6930721adc9d7073f7c90917d24803bf393f989df5649091172a83b97`  
		Last Modified: Thu, 10 Oct 2024 00:05:26 GMT  
		Size: 76.9 MB (76922816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c92e34ff08e5088c2082c1fd7922bae8cece0a2f9c3e1663cf1005aece249f0a`  
		Last Modified: Thu, 10 Oct 2024 00:05:14 GMT  
		Size: 76.4 KB (76429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1981b0e9ac387503bf0e3e346ebb9e15a72c98a6529a281eced15a2197f3775`  
		Last Modified: Thu, 10 Oct 2024 00:05:14 GMT  
		Size: 1.3 KB (1252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
