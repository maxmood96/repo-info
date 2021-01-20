## `golang:1-nanoserver-1809`

```console
$ docker pull golang@sha256:a5a347a32f70378c58b9e2e8a916c2bc123b37eac45e001e65cd6e5bd25b135d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `golang:1-nanoserver-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull golang@sha256:883788e1d080658db3e96e88bed0b31c1d56e1a70defbbc517febe6fc7f50c1d
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235229644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5bdb17c8105e5934b007f2c5dbe435320d8defc51306fc1b4a1338b2a67c1d7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 07 Jan 2021 16:14:35 GMT
RUN Apply image 1809-amd64
# Wed, 13 Jan 2021 13:44:35 GMT
SHELL [cmd /S /C]
# Wed, 13 Jan 2021 13:44:36 GMT
ENV GOPATH=C:\gopath
# Wed, 13 Jan 2021 13:44:37 GMT
USER ContainerAdministrator
# Wed, 13 Jan 2021 13:44:52 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\go\bin;%PATH%"
# Wed, 13 Jan 2021 13:44:53 GMT
USER ContainerUser
# Wed, 20 Jan 2021 00:59:05 GMT
ENV GOLANG_VERSION=1.15.7
# Wed, 20 Jan 2021 01:04:17 GMT
COPY dir:b090524ff2924fc89c2ae4f91d41383bcd9eef1a71cb43643d007fcaeb24737c in C:\go 
# Wed, 20 Jan 2021 02:15:36 GMT
RUN go version
# Wed, 20 Jan 2021 02:15:37 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:62239e9aa1a352a20b0d4969c2b508b8a18d10e799d4db72e6f24ccbb2c724d9`  
		Size: 101.3 MB (101340070 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:50358a323c5421695eacfec8cf19b70cfc54a72e6dc491bc2bfd4391d84dcaf9`  
		Last Modified: Wed, 13 Jan 2021 15:13:44 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7b504f15f2836681dc74e6bf27d7be538fe7e6a6f53ea4bf3d8be6bb6545d8`  
		Last Modified: Wed, 13 Jan 2021 15:13:44 GMT  
		Size: 868.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf6648d03a5b65f08b03a3cf89c0de5e57b386f48c5316121c697a7d4f12488`  
		Last Modified: Wed, 13 Jan 2021 15:13:43 GMT  
		Size: 863.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cdc9022e2634f8a89707e4bfa55b2ff2a86865a3d7e5508effdc4abd5e92405`  
		Last Modified: Wed, 13 Jan 2021 15:13:43 GMT  
		Size: 66.3 KB (66267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3d33148024d9121b1452536b9df85f11745d7d415b1537823e481164375713`  
		Last Modified: Wed, 13 Jan 2021 15:13:38 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921c0f5f99237ab770c101e32a17e929f39689f6f5f1ed6e26c458ecad5725e5`  
		Last Modified: Wed, 20 Jan 2021 02:29:04 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:967b6c68d3442797ec4d54fea2c64687eef919572811f8615740d9bf3118a59a`  
		Last Modified: Wed, 20 Jan 2021 02:31:42 GMT  
		Size: 133.7 MB (133737237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f8555e78a5d1cb289d4c527f63008c9071ba1b4d6e17a090a52fb93c0fe7fb`  
		Last Modified: Wed, 20 Jan 2021 02:29:03 GMT  
		Size: 80.2 KB (80173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27634e21c25507f9cabe1b751a7a46adf1f858062f5a81502c3701bd119fd638`  
		Last Modified: Wed, 20 Jan 2021 02:29:04 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
