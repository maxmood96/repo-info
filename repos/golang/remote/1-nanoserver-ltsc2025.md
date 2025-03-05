## `golang:1-nanoserver-ltsc2025`

```console
$ docker pull golang@sha256:5f2ee48797826863d872465cf03a4b83c5f5bd0dc221088e08e391131b42fa26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `golang:1-nanoserver-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull golang@sha256:e60e7a04461fee8bed123d1169ebb783f8d7d6265aafa76143e43d95c26c4e64
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.9 MB (287919981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910aa6721978ffc1d7c59825280ecaa64d911801323bc2b91e8d3bd1735a5ab5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 08 Feb 2025 22:31:47 GMT
RUN Apply image 10.0.26100.3194
# Tue, 04 Mar 2025 22:00:47 GMT
SHELL [cmd /S /C]
# Tue, 04 Mar 2025 22:00:48 GMT
ENV GOPATH=C:\go
# Tue, 04 Mar 2025 22:00:48 GMT
USER ContainerAdministrator
# Tue, 04 Mar 2025 22:00:51 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 04 Mar 2025 22:00:51 GMT
USER ContainerUser
# Tue, 04 Mar 2025 22:00:52 GMT
ENV GOLANG_VERSION=1.24.1
# Tue, 04 Mar 2025 22:02:03 GMT
COPY dir:1c8a5df65fcdbd0ad306edfb20884d0712989c03ff01d990889cdc983af886a3 in C:\Program Files\Go 
# Tue, 04 Mar 2025 22:02:06 GMT
RUN go version
# Tue, 04 Mar 2025 22:02:06 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:e075dd07cbf907b7da8dbd8365b73a71ac92a834b78f520bd976cb97e0fcc0a1`  
		Last Modified: Wed, 12 Feb 2025 22:34:59 GMT  
		Size: 205.9 MB (205890263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb938ce7adfa6220edd7579d3708adc7ce8fe8c4a900eb610fbe3e7e52ef763d`  
		Last Modified: Tue, 04 Mar 2025 22:02:10 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a82e6fcfa693026572c37f44c508bde4e0254b1534b60d34553edd41726d449`  
		Last Modified: Tue, 04 Mar 2025 22:02:10 GMT  
		Size: 1.1 KB (1087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016ef6815875ced1d5a6a55351da25231512914d5dcbaaaf8d36bcd5824a377d`  
		Last Modified: Tue, 04 Mar 2025 22:02:10 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a212c2c6c2436b6b9c60c7db5267858a023f61a2fa1a641cf15f9edfc1cfb4f2`  
		Last Modified: Tue, 04 Mar 2025 22:02:10 GMT  
		Size: 76.2 KB (76166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8d73998529977cfe11e6084b9d0a1ba1474bdeee5c61aa09ec1acbeb380ca6`  
		Last Modified: Tue, 04 Mar 2025 22:02:09 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9134d424caaf8bfa895c9d816257ed1c35ec4322f3ff95a614db299b4376f0df`  
		Last Modified: Tue, 04 Mar 2025 22:02:09 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7301298ec9b72c5dd02c500360ee737baaca744ade788d38ffe66aa44ded835`  
		Last Modified: Tue, 04 Mar 2025 22:02:22 GMT  
		Size: 81.9 MB (81858160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb7afee09b383890a533359ebc7b66026b956a5b3afbe60333331b5bf77b4fd`  
		Last Modified: Tue, 04 Mar 2025 22:02:09 GMT  
		Size: 88.9 KB (88871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3d6fea26773bf95f94c231877df55c84044a41d24ee81f4be164d13817607d`  
		Last Modified: Tue, 04 Mar 2025 22:02:09 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
