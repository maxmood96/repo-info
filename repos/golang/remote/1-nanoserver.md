## `golang:1-nanoserver`

```console
$ docker pull golang@sha256:e96bdd2a33889d0ca54e93bf43298707f1caa76c45ae49e88ad71e234548dcd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `golang:1-nanoserver` - windows version 10.0.20348.2700; amd64

```console
$ docker pull golang@sha256:c737a09cd531caeecaa7728ef57fe7dd452a5a0b2164c79d4cb93e8fa9d10b57
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.6 MB (197611428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c724e61f6fb60c3d80bcae0d91776ad552027641ba43d5045302df7e6681105d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 05 Sep 2024 23:48:03 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 02:06:28 GMT
SHELL [cmd /S /C]
# Wed, 11 Sep 2024 02:06:28 GMT
ENV GOPATH=C:\go
# Wed, 11 Sep 2024 02:06:29 GMT
USER ContainerAdministrator
# Wed, 11 Sep 2024 02:06:31 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 11 Sep 2024 02:06:31 GMT
USER ContainerUser
# Wed, 11 Sep 2024 02:06:32 GMT
ENV GOLANG_VERSION=1.23.1
# Wed, 11 Sep 2024 02:08:06 GMT
COPY dir:3148b20efd35f18b5a0e13c6e7eabd669161775894572897e562dc60e9ffc1b0 in C:\Program Files\Go 
# Wed, 11 Sep 2024 02:08:09 GMT
RUN go version
# Wed, 11 Sep 2024 02:08:10 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:a447243899be39b01c34fc7e1bcecb47ce42b14668876fdd121f8b5e2d4d4a86`  
		Last Modified: Tue, 10 Sep 2024 22:28:02 GMT  
		Size: 120.5 MB (120509521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a75803e420378eef9fa4db3e12b4eb8c4257a0b018f1ff0daf2fea0218f0f5`  
		Last Modified: Wed, 11 Sep 2024 02:08:16 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd22ad6292ee625c8354e8c51054e05429c629f00565d8a63d3143e58b6e2c1`  
		Last Modified: Wed, 11 Sep 2024 02:08:15 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad56646d1db92a9d3deada2029a5c4560776f988c9dd20fa34613c4459f0bba`  
		Last Modified: Wed, 11 Sep 2024 02:08:15 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1a4af5bab3b7a99ee4bb75b4e99f28a2c7fc03a9c5c3aed390810d2301abc0`  
		Last Modified: Wed, 11 Sep 2024 02:08:15 GMT  
		Size: 76.2 KB (76207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c5469691005306875ef8adc8f06979fbf66847dd854ae29fb95ab40c7ba1cb`  
		Last Modified: Wed, 11 Sep 2024 02:08:13 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51ad5eab8579942958e3a5a69d6a22cb1129672ef8f26a5ee23ba72324aa85e`  
		Last Modified: Wed, 11 Sep 2024 02:08:13 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d120fad411156d0d30b6216bd832d725510ea921564c55a7cf892327afc752`  
		Last Modified: Wed, 11 Sep 2024 02:08:25 GMT  
		Size: 76.9 MB (76924724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa4a92927a246f410520e9ad8d2c29e33b8c5512566b999a35ab09a16889671`  
		Last Modified: Wed, 11 Sep 2024 02:08:14 GMT  
		Size: 94.6 KB (94594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba6037ca9df1f26f2728ec847f7e1ef50004a900c0185cfc836124e9fd0ab71`  
		Last Modified: Wed, 11 Sep 2024 02:08:13 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-nanoserver` - windows version 10.0.17763.6293; amd64

```console
$ docker pull golang@sha256:e2bfa632669e99cfa46ba8bf9be29ac72e3ccf301694f62f1317fd0720194b0c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232152169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b90a25eee095a69191a1d3ec64a29122e200aff7e9fc386b09c3f7c85479b5e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 06 Sep 2024 01:02:10 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 02:07:44 GMT
SHELL [cmd /S /C]
# Wed, 11 Sep 2024 02:07:45 GMT
ENV GOPATH=C:\go
# Wed, 11 Sep 2024 02:07:46 GMT
USER ContainerAdministrator
# Wed, 11 Sep 2024 02:07:48 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 11 Sep 2024 02:07:49 GMT
USER ContainerUser
# Wed, 11 Sep 2024 02:07:49 GMT
ENV GOLANG_VERSION=1.23.1
# Wed, 11 Sep 2024 02:08:48 GMT
COPY dir:3148b20efd35f18b5a0e13c6e7eabd669161775894572897e562dc60e9ffc1b0 in C:\Program Files\Go 
# Wed, 11 Sep 2024 02:08:51 GMT
RUN go version
# Wed, 11 Sep 2024 02:08:52 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:a8b325bcb6d89afa770bc0d80d724a7529f3c8bdf940ab5418ad8d6b94fb07f0`  
		Last Modified: Tue, 10 Sep 2024 17:40:58 GMT  
		Size: 155.1 MB (155080848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02779c55d1c14ca4325cce02534a5bf299ee29243591e3fc8ece463f2c1e57e3`  
		Last Modified: Wed, 11 Sep 2024 02:08:56 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed3683ace83b8f316c622f98076c8668d8dd736e428ea2f9dddd96a7356bbb2`  
		Last Modified: Wed, 11 Sep 2024 02:08:56 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd3f59eca2bb98239fe91c9b3b1ca7801f27abac3326360f0bceae2d2fa83ed`  
		Last Modified: Wed, 11 Sep 2024 02:08:56 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fdc472c7a75a7bd22813d788f8874eeff78a84721aee4ddd528c6e5b32542ce`  
		Last Modified: Wed, 11 Sep 2024 02:08:56 GMT  
		Size: 72.3 KB (72267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cb1f6ffcaa8d625b5aac5e6ba28bdcc65d7e9e98d6ee82e301aab0ed960ea7`  
		Last Modified: Wed, 11 Sep 2024 02:08:55 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f107b4fd0526cb39991a5e95588f5b6bfb048005f328d3b2c80c4ac44aa78f8`  
		Last Modified: Wed, 11 Sep 2024 02:08:55 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53538aaa4274e569156575669ae9f26c69e269295062fa7852bdf6805154538d`  
		Last Modified: Wed, 11 Sep 2024 02:09:06 GMT  
		Size: 76.9 MB (76920665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0abe5c5a9e3e7f93231d85e2a3366f5c4f0c82add4d49a6a8848bb755b651c18`  
		Last Modified: Wed, 11 Sep 2024 02:08:55 GMT  
		Size: 72.0 KB (71953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be166b89ad2cf131e50b8c872a275b6ddfa0d9f1829f8d4d1bd6ed3457d30b6`  
		Last Modified: Wed, 11 Sep 2024 02:08:55 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
