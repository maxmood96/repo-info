## `golang:nanoserver`

```console
$ docker pull golang@sha256:53d53ab976fccd3c7097775bab2775cd5af35868be6f11a5ec89107b2345058a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `golang:nanoserver` - windows version 10.0.26100.2894; amd64

```console
$ docker pull golang@sha256:1d3430a75acfc3142a372085ac724c53158d575e33c252d5cf3a6b5d2d2b37ef
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.2 MB (276190505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09aa2547b5e352eb3aaf07a13ace0387d61fd3fa0cadaca8df519e262a9d597b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Mon, 13 Jan 2025 02:49:59 GMT
RUN Apply image 10.0.26100.2894
# Wed, 22 Jan 2025 00:31:45 GMT
SHELL [cmd /S /C]
# Wed, 22 Jan 2025 00:31:46 GMT
ENV GOPATH=C:\go
# Wed, 22 Jan 2025 00:31:46 GMT
USER ContainerAdministrator
# Wed, 22 Jan 2025 00:31:49 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 22 Jan 2025 00:31:50 GMT
USER ContainerUser
# Wed, 22 Jan 2025 00:31:51 GMT
ENV GOLANG_VERSION=1.23.5
# Wed, 22 Jan 2025 00:32:58 GMT
COPY dir:686423f35bba4280be244c38d9d939799b38be8e943dabfe1a129b187496242a in C:\Program Files\Go 
# Wed, 22 Jan 2025 00:33:02 GMT
RUN go version
# Wed, 22 Jan 2025 00:33:02 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:3c572c5b651b10d04181f97ce4c0938b69ad43912e8c0bf19f77a4ea9a8f72e8`  
		Last Modified: Sun, 19 Jan 2025 13:02:58 GMT  
		Size: 199.1 MB (199054258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6afe8090e9a89a6ffec74070c2fcbfa84db43403b27412f7ee5928939d44211c`  
		Last Modified: Wed, 22 Jan 2025 00:33:08 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6d0be54ddccf801ad3d03d9c9f9d70d02cff13a8d6d1f9c4883679b85261fd`  
		Last Modified: Wed, 22 Jan 2025 00:33:08 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cc6707b7c3e4bcf83362a7014b4dcaf9e41000100c429fcc80bde0ac6263f4`  
		Last Modified: Wed, 22 Jan 2025 00:33:08 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c47a9f8c72e6b9a7c49b7af035a007de89ff80b262feadaa7eabacfe380a8e3`  
		Last Modified: Wed, 22 Jan 2025 00:33:08 GMT  
		Size: 76.1 KB (76117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05994658523b1f7f0562fc779452ab5ff12bdb93b8fd412c2573ad6b9f054865`  
		Last Modified: Wed, 22 Jan 2025 00:33:06 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199954f1cd39d3b03523484fd919499a03bd0d48b2c6d9a4725a78e961fd51a6`  
		Last Modified: Wed, 22 Jan 2025 00:33:06 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abae5adfeb63bd097c0c7bac52621925064713c74a985ad61b21e2b8e508dd30`  
		Last Modified: Wed, 22 Jan 2025 00:33:18 GMT  
		Size: 77.0 MB (76965544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85f32c1e4e868f02687c68148e3e49ad66ee2b934c4365578f23e808f85f681`  
		Last Modified: Wed, 22 Jan 2025 00:33:06 GMT  
		Size: 88.1 KB (88100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d5d6b9428163c5301a7cc1fb3c87ec43f7b8bd3108eb6e401f8abf143abd53`  
		Last Modified: Wed, 22 Jan 2025 00:33:06 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:nanoserver` - windows version 10.0.20348.3091; amd64

```console
$ docker pull golang@sha256:abd2ff423b6cab9ba824904827850786201036edaf7a6cccaa573607fd2c5aba
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.8 MB (197782527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0f8f969f49d36d27c4059f99ea799852131e3f38eb86cb17a7553b78625286`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 12 Jan 2025 09:54:50 GMT
RUN Apply image 10.0.20348.3091
# Thu, 16 Jan 2025 22:56:45 GMT
SHELL [cmd /S /C]
# Thu, 16 Jan 2025 22:56:46 GMT
ENV GOPATH=C:\go
# Thu, 16 Jan 2025 22:56:46 GMT
USER ContainerAdministrator
# Thu, 16 Jan 2025 22:56:48 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Thu, 16 Jan 2025 22:56:49 GMT
USER ContainerUser
# Thu, 16 Jan 2025 22:56:50 GMT
ENV GOLANG_VERSION=1.23.5
# Thu, 16 Jan 2025 22:58:54 GMT
COPY dir:686423f35bba4280be244c38d9d939799b38be8e943dabfe1a129b187496242a in C:\Program Files\Go 
# Thu, 16 Jan 2025 22:58:57 GMT
RUN go version
# Thu, 16 Jan 2025 22:58:58 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:fd3058b29fbd287119a2fa4d2d36a46fdee3bbada5fd9ef6f02f2d7d4cc143ab`  
		Last Modified: Tue, 14 Jan 2025 20:27:35 GMT  
		Size: 120.7 MB (120661554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a74ff023c34672bc6342d9a966e984a037cd0ce1c5685fcb949eb067e7e201`  
		Last Modified: Thu, 16 Jan 2025 22:59:04 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec0c2f0693957324ea78289b63acf0c296a57524c788d3d2e3411346cf08e129`  
		Last Modified: Thu, 16 Jan 2025 22:59:04 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991c43c51ce7a881e54c74bb6d249075c2757904c585ff1bfdb40699f14708d5`  
		Last Modified: Thu, 16 Jan 2025 22:59:04 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c533d930dd50f36824c5c08269e0646d5d36cbb655a9593b17b7197edf9f66af`  
		Last Modified: Thu, 16 Jan 2025 22:59:04 GMT  
		Size: 77.3 KB (77311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea82bda638fa607f137d1cb6d9662b41aa492105c6658eb60e0a931577f3340b`  
		Last Modified: Thu, 16 Jan 2025 22:59:02 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c55ec2070dff390df3fc65fb9ec22b639bd982693f28ca362cb36c5bfca977`  
		Last Modified: Thu, 16 Jan 2025 22:59:02 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e724dfb3c501f4565bf97ad56d9af43db99472e70f5089e8d3a95a7326eedc4`  
		Last Modified: Thu, 16 Jan 2025 22:59:14 GMT  
		Size: 77.0 MB (76951270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468df26272102c6f9c541ff36441c37d8fc8f6c20cedd854cfe56c05693ee27f`  
		Last Modified: Thu, 16 Jan 2025 22:59:02 GMT  
		Size: 86.0 KB (86006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f02f2f82d6d41bfa154523d613bb7e66dabceee24c0d25d76568b6c87cdb42b`  
		Last Modified: Thu, 16 Jan 2025 22:59:02 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:nanoserver` - windows version 10.0.17763.6775; amd64

```console
$ docker pull golang@sha256:329bfbcba3acf181ccc95d4a039e5a5bf5a8f4f742d1cdce8d73ac2af326f873
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.4 MB (232368955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2e3b702c90512300dac156f8a762123444fc2b3f107c638dd7a4aa7175ae07`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 09 Jan 2025 09:30:10 GMT
RUN Apply image 10.0.17763.6775
# Thu, 16 Jan 2025 23:11:22 GMT
SHELL [cmd /S /C]
# Thu, 16 Jan 2025 23:11:23 GMT
ENV GOPATH=C:\go
# Thu, 16 Jan 2025 23:11:23 GMT
USER ContainerAdministrator
# Thu, 16 Jan 2025 23:11:26 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Thu, 16 Jan 2025 23:11:26 GMT
USER ContainerUser
# Thu, 16 Jan 2025 23:11:27 GMT
ENV GOLANG_VERSION=1.23.5
# Thu, 16 Jan 2025 23:12:26 GMT
COPY dir:686423f35bba4280be244c38d9d939799b38be8e943dabfe1a129b187496242a in C:\Program Files\Go 
# Thu, 16 Jan 2025 23:12:30 GMT
RUN go version
# Thu, 16 Jan 2025 23:12:31 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:3a71a517ad886518458023f01614036e271bdcdb366b9c2c64b1b5dd7737a6b0`  
		Last Modified: Tue, 14 Jan 2025 20:45:12 GMT  
		Size: 155.3 MB (155267564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:821d23661c1c15acbbccbaa4abd76058a575aee7bf928077a3413667b7f6e4e6`  
		Last Modified: Thu, 16 Jan 2025 23:12:37 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6446a7058982c34cc27fa32f8cb9c56bb631cb5388676f7cd7ba07ec4fa566`  
		Last Modified: Thu, 16 Jan 2025 23:12:37 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ecca87bb743c62448e4cc6f747cc13b946834031298ce745b6a5899e9d6f6fa`  
		Last Modified: Thu, 16 Jan 2025 23:12:37 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb451ac0154ac1dd2c7f13e06f032679745e2081ad33575156a3f3e5f5d8b2f7`  
		Last Modified: Thu, 16 Jan 2025 23:12:37 GMT  
		Size: 74.1 KB (74077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a2bdeff3a119565141c55a3098a631307b70f8582ccae332dc877c392fe0ad`  
		Last Modified: Thu, 16 Jan 2025 23:12:35 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c32f3de7fce820a1841bfa5ee459b870cb2bd83a84fd1b0138ea8081fbfcff`  
		Last Modified: Thu, 16 Jan 2025 23:12:35 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3ace88ca08359f38e6afece8a1ca6c5bb41476505f4dc124bd6dda25e1e95d`  
		Last Modified: Thu, 16 Jan 2025 23:12:47 GMT  
		Size: 76.9 MB (76949677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b5f349a4a464efc1c9bd312408b205204274c38813646b4d28a496f160a144`  
		Last Modified: Thu, 16 Jan 2025 23:12:35 GMT  
		Size: 71.2 KB (71173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa225549ddea29f41e597bea9dfa4d564f26fba7ff8154f7e177c8610392dd5`  
		Last Modified: Thu, 16 Jan 2025 23:12:35 GMT  
		Size: 1.2 KB (1247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
