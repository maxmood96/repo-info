## `golang:rc-nanoserver-1809`

```console
$ docker pull golang@sha256:7e8348315d256db14081ad67aae121eb5675e305663a323ee9472d4c5e62f42c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `golang:rc-nanoserver-1809` - windows version 10.0.17763.1339; amd64

```console
$ docker pull golang@sha256:0893d0efa470806c8ca251f4b0eadb1e396f47fad90ab373a8d763e47f1d0c1d
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234881984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7010299313e730a65c01055fa803c04c312d64a0378f82ea874cf7a7514555`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 07 Jul 2020 13:50:07 GMT
RUN Apply image 1809-amd64
# Tue, 14 Jul 2020 19:16:55 GMT
SHELL [cmd /S /C]
# Tue, 14 Jul 2020 19:16:56 GMT
ENV GOPATH=C:\gopath
# Tue, 14 Jul 2020 19:16:57 GMT
USER ContainerAdministrator
# Fri, 24 Jul 2020 23:23:29 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\go\bin;%PATH%"
# Fri, 24 Jul 2020 23:23:30 GMT
USER ContainerUser
# Fri, 07 Aug 2020 23:22:39 GMT
ENV GOLANG_VERSION=1.15rc2
# Fri, 07 Aug 2020 23:24:52 GMT
COPY dir:520e8e34eaa283084724f61d40f9dbde7ab11d4453c32cfc5834ad1cb47763d1 in C:\go 
# Fri, 07 Aug 2020 23:25:12 GMT
RUN go version
# Fri, 07 Aug 2020 23:25:13 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:dc95608099543221ef539391bfece5c1ce37b97af9da457f5990349cab028a12`  
		Size: 100.9 MB (100895619 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f19104f608aa61eccae7875d2fbe58c4c2831d21fadc4e8c6d1216898f3cfa9d`  
		Last Modified: Tue, 14 Jul 2020 19:43:44 GMT  
		Size: 889.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e422aa8935c83cc478814657d80109c6d8542988c85afee27c5affa60bb51e6`  
		Last Modified: Tue, 14 Jul 2020 19:43:43 GMT  
		Size: 891.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6485f028429f96efadd8e965b6c594850f8b6bd968565e0e7bd1bbe413968948`  
		Last Modified: Tue, 14 Jul 2020 19:43:43 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0e60b8a687035c9781fbac4abf37176dd8eae89ec16fc95f42f11c5f70ad84`  
		Last Modified: Fri, 24 Jul 2020 23:31:14 GMT  
		Size: 67.7 KB (67718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70b750dd29ada9534382d7fe259ed67c4ec1599835a2926b8656e28f65a2948`  
		Last Modified: Fri, 24 Jul 2020 23:31:12 GMT  
		Size: 890.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20b90651344e36ed87aaddf9bf396466b541707df63cd1e3b9a468fa3aa56e6`  
		Last Modified: Fri, 07 Aug 2020 23:28:38 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4c6f0a0c3e9c0ac673413d09759e69ecdf40ed573b4233c0c12f3273dbbc94`  
		Last Modified: Fri, 07 Aug 2020 23:29:16 GMT  
		Size: 133.9 MB (133875560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dcf38a6feb25b452481fa9c5b0cca0e846fb94699fae9fa131c454a77eb6b4c`  
		Last Modified: Fri, 07 Aug 2020 23:28:38 GMT  
		Size: 37.5 KB (37532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706f7b502d702e4844e3d10ff01ae629ffadc9b75e2aa48a5a0d1473f291f5d1`  
		Last Modified: Fri, 07 Aug 2020 23:28:38 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
