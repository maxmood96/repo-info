## `golang:1-nanoserver-1809`

```console
$ docker pull golang@sha256:c4e6431ff332ce68cc8dd115e6b4763ae54f7ad62b934ce26d4de44dff5d50c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `golang:1-nanoserver-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull golang@sha256:63976f04d7b9c07aa0288125096b873a243e3b744f338b132ab6a3e79401f706
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227542314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c5c06405fdae914ff1a535ee12a7f07da7091ba986177dba863b75b0a60e381`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Wed, 15 May 2024 23:51:15 GMT
SHELL [cmd /S /C]
# Wed, 15 May 2024 23:51:15 GMT
ENV GOPATH=C:\go
# Wed, 15 May 2024 23:51:16 GMT
USER ContainerAdministrator
# Wed, 15 May 2024 23:51:19 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 15 May 2024 23:51:20 GMT
USER ContainerUser
# Wed, 15 May 2024 23:51:21 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 15 May 2024 23:52:32 GMT
COPY dir:4d079461b01f7018cdefcf75d79e42082e4956562e5247e8be7d5083d6b6044d in C:\Program Files\Go 
# Wed, 15 May 2024 23:52:39 GMT
RUN go version
# Wed, 15 May 2024 23:52:40 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de8f1966f64b6aa27754b22424bbdcd7b76110f53e298b10fd258191a6a46dd`  
		Last Modified: Wed, 15 May 2024 23:52:47 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:725545ebc70ff54fa3bd0e4fa6407988dcbdffd3bf56c133f1cbddf314a05692`  
		Last Modified: Wed, 15 May 2024 23:52:46 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2d74c3b840c92a885cb83a0038d48f297f1691080d126b481f9aa9d05ca641a`  
		Last Modified: Wed, 15 May 2024 23:52:46 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b9e5281159b87bba5f555e02c8ad0b828d4b49845d81957f86267eef21f6ae`  
		Last Modified: Wed, 15 May 2024 23:52:46 GMT  
		Size: 67.0 KB (66959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7444401d77ac2a840024d94acad56875da51d04985874256a74e661d808ba54`  
		Last Modified: Wed, 15 May 2024 23:52:44 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86b5debcd615c3bec61849bc964f2f93e8dcbd136ed67d84f0794554d7d7d9c`  
		Last Modified: Wed, 15 May 2024 23:52:44 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843c3e165944bf358d38c5548efbdb8cfdba6bddcfa49828fe6cdddf4132a4dc`  
		Last Modified: Wed, 15 May 2024 23:52:55 GMT  
		Size: 71.3 MB (71336454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38cfae732d6d9218d84e45212b98b922e7c6565cc591e9673b19ad37dad54452`  
		Last Modified: Wed, 15 May 2024 23:52:44 GMT  
		Size: 1.2 MB (1191082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06eb3fcd797b2f8ff39f4cdbdb8ec7ae5196ab98a0a6eaaed2738d0c3453d39b`  
		Last Modified: Wed, 15 May 2024 23:52:44 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
