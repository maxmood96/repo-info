## `golang:1-nanoserver`

```console
$ docker pull golang@sha256:9677ae102d63cec43cd9279a293b4593c6a4e9fcd49d22ed89b05eec19e80725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `golang:1-nanoserver` - windows version 10.0.17763.1217; amd64

```console
$ docker pull golang@sha256:3bdc6e2eadd75fd9a3099109ec7101946a4ed45766de52713407c0d01900844c
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234174205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6225130324c1736b47ef995f0e0841c833fc254d7e85959d087912dfeffe073`
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
# Tue, 02 Jun 2020 01:34:54 GMT
ENV GOLANG_VERSION=1.14.4
# Tue, 02 Jun 2020 01:36:57 GMT
COPY dir:79141300d8757e9df6bce16180e905d9ccf2155e9a1263e19d03686a5c1d4794 in C:\go 
# Tue, 02 Jun 2020 01:37:13 GMT
RUN go version
# Tue, 02 Jun 2020 01:37:14 GMT
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
	-	`sha256:150e7565d5638e248f69ea2beeb5a73652b42b22300fd3a2d3995f5211cf4036`  
		Last Modified: Tue, 02 Jun 2020 01:48:32 GMT  
		Size: 863.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19a9ab8aac2ca844f6714139bcdabfb901204e3c09b0630d18b20c9221845ba2`  
		Last Modified: Tue, 02 Jun 2020 01:50:57 GMT  
		Size: 133.0 MB (133010286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe4000fbed592ed24bd6c7981485fe7af0ec882369d9161c4cb90dcd51487d1`  
		Last Modified: Tue, 02 Jun 2020 01:48:32 GMT  
		Size: 71.8 KB (71826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578ab3352d6a850161518931c5b4c75ac98a24ee54ea61cd3fdcc173e511bbf8`  
		Last Modified: Tue, 02 Jun 2020 01:48:32 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
