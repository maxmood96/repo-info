## `golang:1-nanoserver-1809`

```console
$ docker pull golang@sha256:9a7ce0b22efa5352041057fc178cd029b4da2abb08a583894df77d4565d885df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `golang:1-nanoserver-1809` - windows version 10.0.17763.1217; amd64

```console
$ docker pull golang@sha256:8e3fa021f279f6142bc85e9236c4807610a0cc711eadebd7546236938841ab71
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234157866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd742836bd6dabad4818b9fd5f4e019b48f0b79413f66394898beaeabe3ab7c8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 06 May 2020 12:39:06 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:45:59 GMT
SHELL [cmd /S /C]
# Wed, 13 May 2020 12:45:59 GMT
ENV GOPATH=C:\gopath
# Wed, 13 May 2020 12:46:00 GMT
USER ContainerAdministrator
# Wed, 13 May 2020 12:46:16 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\go\bin;%PATH%"
# Wed, 13 May 2020 12:46:17 GMT
USER ContainerUser
# Fri, 15 May 2020 21:22:14 GMT
ENV GOLANG_VERSION=1.14.3
# Fri, 15 May 2020 21:24:31 GMT
COPY dir:24e54437b4591155a0496ca948d9a9848f82a8c0bfdf6e9c2b799a5e2a614acc in C:\go 
# Fri, 15 May 2020 21:24:50 GMT
RUN go version
# Fri, 15 May 2020 21:24:51 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:b9e6fec25718aef5ed18d499b27e43adb524f9ee4f2eb3f0fffaea018e7e86b0`  
		Size: 101.0 MB (101019852 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:40353fa5ada037c8e7ee420534fa5382bdfbaf02e1076b13aed24281de55c455`  
		Last Modified: Wed, 13 May 2020 13:01:02 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a72d54d9d133d3699eb985ab2185f853990987e9d27b7684a1cc85b1e4b104`  
		Last Modified: Wed, 13 May 2020 13:01:01 GMT  
		Size: 861.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508740f077f04bd716c91abe093629a4f879980cea83d172b1f5f6a4c0e64ba9`  
		Last Modified: Wed, 13 May 2020 13:01:01 GMT  
		Size: 865.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e75b0268a2f057e874739401fafa440f9012b282a6477518fcb223c83a6fe2`  
		Last Modified: Wed, 13 May 2020 13:01:01 GMT  
		Size: 66.7 KB (66723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abe006cd051b4870a7d6b5390952c199763bc0bb76c7885f7ef2ac62a74250b`  
		Last Modified: Wed, 13 May 2020 13:00:59 GMT  
		Size: 930.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05b308b503be2037319c4f0ac3cef18671e24807647aabf06471c3eee997589a`  
		Last Modified: Fri, 15 May 2020 21:38:26 GMT  
		Size: 867.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993e6c44b3713dfb0dd822bf35d1c9e965a74eee71cc15eb05e06c3bb1ee0d73`  
		Last Modified: Fri, 15 May 2020 21:38:53 GMT  
		Size: 133.0 MB (132995486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9a029a863995ca819e451849d332e1904a4e66d5895ce371c386175cb8e2d0`  
		Last Modified: Fri, 15 May 2020 21:38:26 GMT  
		Size: 70.3 KB (70332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a043ad5afeb3389c5c93438b1e1332b79b868124ba5a1fbb5cacc6ea784d7cc`  
		Last Modified: Fri, 15 May 2020 21:38:26 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
