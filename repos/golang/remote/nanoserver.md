## `golang:nanoserver`

```console
$ docker pull golang@sha256:d32c4dc5c252863b027166ce6c2eec5281f1c47c7a6b0a8cca09d993f4ce70b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.405; amd64
	-	windows version 10.0.17763.2366; amd64

### `golang:nanoserver` - windows version 10.0.20348.405; amd64

```console
$ docker pull golang@sha256:19502033ed95fdd72c31514e4e6205df84aa9477c7f0e13ade2b42c97cbf4d16
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262432458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd44fbdd587d688b5921820235ce29728db0cbab71a01ec928e37212204e5a7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 08 Dec 2021 01:24:33 GMT
RUN Apply image ltsc2022-amd64
# Sat, 18 Dec 2021 00:29:51 GMT
SHELL [cmd /S /C]
# Sat, 18 Dec 2021 00:29:52 GMT
ENV GOPATH=C:\go
# Sat, 18 Dec 2021 00:29:52 GMT
USER ContainerAdministrator
# Sat, 18 Dec 2021 00:30:22 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Sat, 18 Dec 2021 00:30:23 GMT
USER ContainerUser
# Thu, 06 Jan 2022 22:28:50 GMT
ENV GOLANG_VERSION=1.17.6
# Thu, 06 Jan 2022 22:31:56 GMT
COPY dir:7d325dd3c7e81bd29326c5fb7b320ff307098f97c2703658681dad899622f617 in C:\Program Files\Go 
# Thu, 06 Jan 2022 22:32:50 GMT
RUN go version
# Thu, 06 Jan 2022 22:32:51 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:11961e4f2e13a442b572d4bc37edfe94ad6d8c2ed378f0dcae8b880959c4b538`  
		Size: 117.2 MB (117225770 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5f7005dc509dad3c53e79bd72ff76e4dda4a38b2eee2264ceb864eaa233dab99`  
		Last Modified: Sat, 18 Dec 2021 01:23:16 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4e9f3e38224e5b84c429855780b0ef7e6b0a577e925894bf426a73252fe4dd`  
		Last Modified: Sat, 18 Dec 2021 01:23:18 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f2acbfdb66c79b7e8a0b1a4194db1d7d6513ea6cc53dfb4221b786c7c74a8e`  
		Last Modified: Sat, 18 Dec 2021 01:23:15 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40585525152eca561c21db4a5bd8b39d73bf0e6db9a501c19e1aa7c08c6b4014`  
		Last Modified: Sat, 18 Dec 2021 01:23:15 GMT  
		Size: 78.6 KB (78567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f03c4a986705577537ed4bcc508d6c305c7b567c6838dd124f535f59759c36b`  
		Last Modified: Sat, 18 Dec 2021 01:23:13 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79da90077e095b71f83027becccd6c9c8bc4def00cb5a1fa216ffaaf9fa67b63`  
		Last Modified: Thu, 06 Jan 2022 23:04:57 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518e92b2b9c4350db364d67f8f0309a8a6b9c43574f5a9c6b6040799f8e59899`  
		Last Modified: Thu, 06 Jan 2022 23:05:42 GMT  
		Size: 145.1 MB (145068112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2317c01782849c497ab8eb2869fe89cb00bc22791fd15f169133a6a71be741c`  
		Last Modified: Thu, 06 Jan 2022 23:04:57 GMT  
		Size: 52.9 KB (52878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b169f03d7494f6985a74fb4a55018686da941dc2237b80ae86d2a88e7ae5ea`  
		Last Modified: Thu, 06 Jan 2022 23:04:57 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:nanoserver` - windows version 10.0.17763.2366; amd64

```console
$ docker pull golang@sha256:c856d015c818a7ea711a16236bf4f6ab2f986f8b4e3aaa9beada01043eff8f16
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.1 MB (248084830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760787855301be3c99aaa8e958a286d4836cc4fc4b099b1083af9e927a18a751`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 07 Dec 2021 04:37:11 GMT
RUN Apply image 1809-amd64
# Sat, 18 Dec 2021 00:33:50 GMT
SHELL [cmd /S /C]
# Sat, 18 Dec 2021 00:33:50 GMT
ENV GOPATH=C:\go
# Sat, 18 Dec 2021 00:33:51 GMT
USER ContainerAdministrator
# Sat, 18 Dec 2021 00:34:18 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Sat, 18 Dec 2021 00:34:18 GMT
USER ContainerUser
# Thu, 06 Jan 2022 22:33:04 GMT
ENV GOLANG_VERSION=1.17.6
# Thu, 06 Jan 2022 22:35:37 GMT
COPY dir:7d325dd3c7e81bd29326c5fb7b320ff307098f97c2703658681dad899622f617 in C:\Program Files\Go 
# Thu, 06 Jan 2022 22:36:21 GMT
RUN go version
# Thu, 06 Jan 2022 22:36:23 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:034b2f457cdf6a0d3f7024523d40fd6eeb8568e6c76d9fa56f4053fcf3a21d63`  
		Size: 102.9 MB (102904001 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:dac80fcd8aee90ad8a9145e0685b7c90d701307507ff32ffed6c86abc09c0f7a`  
		Last Modified: Sat, 18 Dec 2021 01:24:07 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c14910fae13be585e698e80c191a6ca8b4d4ca7c1cfa7ba6e5839c0ff9d37cc`  
		Last Modified: Sat, 18 Dec 2021 01:24:07 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c585c62725044581c397691e0cc42f23784332757eae6be3ebbb4f8ebf83a9c9`  
		Last Modified: Sat, 18 Dec 2021 01:24:07 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8a4b06c80653b74f6d18b1845aaa0bab0a8234513e2beb5a97a655d96152ff7`  
		Last Modified: Sat, 18 Dec 2021 01:24:07 GMT  
		Size: 67.7 KB (67683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb2867122ac52d3617c048f83a93cca87925a6e5530e20d89648feadbcb23b7`  
		Last Modified: Sat, 18 Dec 2021 01:24:05 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8fc7e97f3ffb911ad49056dfdc6e4bcf1d5397908e1e4a25dc175caf5b1bc5`  
		Last Modified: Thu, 06 Jan 2022 23:05:57 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eaf49beaa7a28dc152a51f95c25379d0ca098f9935b60ec28110fa119f19b80`  
		Last Modified: Thu, 06 Jan 2022 23:06:41 GMT  
		Size: 145.0 MB (145033335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9bb9bb4baa36d17cb03952ee06f620f643907823855ba1428665dbf3bfe5d8`  
		Last Modified: Thu, 06 Jan 2022 23:05:58 GMT  
		Size: 73.2 KB (73167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497d5b53ad2ed5a1edfc542a6beb8512a17698d38c7aa155581a503b57f04b1f`  
		Last Modified: Thu, 06 Jan 2022 23:05:57 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
