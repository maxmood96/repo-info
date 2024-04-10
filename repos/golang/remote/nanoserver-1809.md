## `golang:nanoserver-1809`

```console
$ docker pull golang@sha256:54ed276098c5e66510a89db5824ded35147bea61b627dc0b4950adbfc39611a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `golang:nanoserver-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull golang@sha256:f1706960d8007e6e03cbf0c59e5cc9d1868c08fb7c5a0e6d765da929b2997fac
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.4 MB (176432895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa758437167d60e18ef5bd1d083b3f2649f5573bdccadfe408cc83adc0f1dccf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 06 Apr 2024 02:05:27 GMT
RUN Apply image 10.0.17763.5696
# Wed, 10 Apr 2024 01:20:05 GMT
SHELL [cmd /S /C]
# Wed, 10 Apr 2024 01:20:06 GMT
ENV GOPATH=C:\go
# Wed, 10 Apr 2024 01:20:06 GMT
USER ContainerAdministrator
# Wed, 10 Apr 2024 01:20:17 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 10 Apr 2024 01:20:18 GMT
USER ContainerUser
# Wed, 10 Apr 2024 01:20:19 GMT
ENV GOLANG_VERSION=1.22.2
# Wed, 10 Apr 2024 01:22:13 GMT
COPY dir:6a3197bc56362ded96b0930f47b7684fc93e6ac6a350b0206d0452f8fb599246 in C:\Program Files\Go 
# Wed, 10 Apr 2024 01:22:34 GMT
RUN go version
# Wed, 10 Apr 2024 01:22:35 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:a9b4234352dbe48c2ab26f66b300829ca94d2fc63738ee6d4221f9962d33cf5c`  
		Last Modified: Tue, 09 Apr 2024 20:38:39 GMT  
		Size: 104.9 MB (104889083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcbc22137e8bec78cc562f6e5ea99543a7a0a8e9da2a641f333f2363fe1dcd89`  
		Last Modified: Wed, 10 Apr 2024 01:36:29 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456844b7ca82c547f7ab11f3e90de37eb3c5d97fa67719f9e410e440713de59a`  
		Last Modified: Wed, 10 Apr 2024 01:36:29 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:689ea0dff33b4cdbbab3b9fd19d416b1f38d22aa9f3755e7a976b414b5c045ad`  
		Last Modified: Wed, 10 Apr 2024 01:36:29 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4835ced22260031d04592970b9337ed60542e56b6c2aa31a239d2d4f1bbe4219`  
		Last Modified: Wed, 10 Apr 2024 01:36:29 GMT  
		Size: 66.2 KB (66221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d5e2f5ce7618906cb0c792ce8d9fe2c1736b69b8b0e61810a7d7a83cd60510`  
		Last Modified: Wed, 10 Apr 2024 01:36:28 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa99397efd2c6d8ca598ec530f19fa07979e26ea7e6bdbb7b23817778f3f6a6a`  
		Last Modified: Wed, 10 Apr 2024 01:36:27 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea5d1060cb43df95c55beea21e94497f428da5f9f808a52e4db527868dc0731`  
		Last Modified: Wed, 10 Apr 2024 01:36:47 GMT  
		Size: 71.4 MB (71398692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8161a552042f72d347adb8fe0e0b3828df1c6eba91c6d58c3fadbbe4c446f48`  
		Last Modified: Wed, 10 Apr 2024 01:36:27 GMT  
		Size: 72.3 KB (72252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18583bfa4de362e8eed0ebab79d01c99aa8651624a6c85b9c2645e5176147c8`  
		Last Modified: Wed, 10 Apr 2024 01:36:27 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
