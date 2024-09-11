## `golang:1-nanoserver-1809`

```console
$ docker pull golang@sha256:d4005ccb1a6b1ac4c6b961e1dcc10661978f8da2f54073d59375cbeddd6b3d90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `golang:1-nanoserver-1809` - windows version 10.0.17763.6293; amd64

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
