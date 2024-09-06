## `golang:1-nanoserver-1809`

```console
$ docker pull golang@sha256:49d0d6a97229bc0d778228da8db98250896226741c6ad91543ec990df47c07e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `golang:1-nanoserver-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull golang@sha256:1251f469a3233cea9c3a12cd580b9a495b0d5365e439e637d121543899d9a61b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232163068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7fa08b6bef5d793b9b59de66043919d3b32c01df45e14ad09b5a9889bdf4732`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 11 Aug 2024 06:47:40 GMT
RUN Apply image 10.0.17763.6189
# Thu, 05 Sep 2024 23:06:10 GMT
SHELL [cmd /S /C]
# Thu, 05 Sep 2024 23:06:12 GMT
ENV GOPATH=C:\go
# Thu, 05 Sep 2024 23:06:13 GMT
USER ContainerAdministrator
# Thu, 05 Sep 2024 23:06:32 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Thu, 05 Sep 2024 23:06:33 GMT
USER ContainerUser
# Thu, 05 Sep 2024 23:06:33 GMT
ENV GOLANG_VERSION=1.23.1
# Thu, 05 Sep 2024 23:08:33 GMT
COPY dir:3148b20efd35f18b5a0e13c6e7eabd669161775894572897e562dc60e9ffc1b0 in C:\Program Files\Go 
# Thu, 05 Sep 2024 23:08:36 GMT
RUN go version
# Thu, 05 Sep 2024 23:08:37 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:c4e5a6832ff8986e5f371e5f5a2454121f006cc4c98cbfefb8bb0445da2a9431`  
		Last Modified: Tue, 13 Aug 2024 18:40:28 GMT  
		Size: 155.1 MB (155083093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4576164241d9f95ef857a78bab5f662b9caee025c2c2040f82d5dae9dfe25f70`  
		Last Modified: Thu, 05 Sep 2024 23:08:41 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3cea9f4717a0c23d7a1d75200c7a562fab0266f78cc0893100f2a3a86109a7`  
		Last Modified: Thu, 05 Sep 2024 23:08:41 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2581c57e4daa4fbbc0a17c47b1ce8ef752295ea646356af6e9f7da79c47de503`  
		Last Modified: Thu, 05 Sep 2024 23:08:41 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5faba33117d0f76b69e23cc4ff53bbbeb4da68563686e685393d9c4ce32467d`  
		Last Modified: Thu, 05 Sep 2024 23:08:41 GMT  
		Size: 66.1 KB (66140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:757518685f15b358de118801b57aa325c13e7f9d7f3cfb5cd4075fbddeb0855b`  
		Last Modified: Thu, 05 Sep 2024 23:08:40 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b244c6577522359189ff524a4093970d6041b301ca27106d0da833465e31bb00`  
		Last Modified: Thu, 05 Sep 2024 23:08:40 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c53901dc1ad6f8629484689c1324d3c5fb5d719f1422ed96b18e7c18cbb5cd9`  
		Last Modified: Thu, 05 Sep 2024 23:08:51 GMT  
		Size: 76.9 MB (76939706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc5c33058cb3d1b29835d9acc1d19daec1ead92ae49ff1608531fa191358a7e`  
		Last Modified: Thu, 05 Sep 2024 23:08:40 GMT  
		Size: 67.6 KB (67587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad75add4b68ad19ea503f2ccb0c5dbea2ad100e82ae45a254ba9ee48cab46f09`  
		Last Modified: Thu, 05 Sep 2024 23:08:40 GMT  
		Size: 1.2 KB (1249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
