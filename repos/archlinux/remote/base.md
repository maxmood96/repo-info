## `archlinux:base`

```console
$ docker pull archlinux@sha256:18dd035ceaa7e7296ef7c1e2cd52022ea95fbdccdc42650b13c0a995b5db3034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `archlinux:base` - linux; amd64

```console
$ docker pull archlinux@sha256:2b4240d03b28657720bd5a026aadf9bafbfb63974c5b5cfe58cfc7ed896bf407
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139833470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e19cbc14c6050a2a209dfec1701753ae4bcba95663b7319f93ead8cb1dbbda7`
-	Default Command: `["\/usr\/bin\/bash"]`

```dockerfile
# Tue, 11 Oct 2022 17:21:56 GMT
COPY dir:8221a8d871ad5057bb0ff188462660aa58db316f541130a892d8975e953a7cab in / 
# Tue, 11 Oct 2022 17:21:58 GMT
RUN ldconfig &&     sed -i '/BUILD_ID/a VERSION_ID=TEMPLATE_VERSION_ID' /etc/os-release
# Tue, 11 Oct 2022 17:21:58 GMT
ENV LANG=C.UTF-8
# Tue, 11 Oct 2022 17:21:58 GMT
CMD ["/usr/bin/bash"]
```

-	Layers:
	-	`sha256:20c953421269c919c94f629133e9b16eaf0df270150da4387643c8ac48a9b0b7`  
		Last Modified: Tue, 11 Oct 2022 17:23:45 GMT  
		Size: 139.8 MB (139825580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0ba93012fc23bd8ed38c02285afe6695ba7ae51aca9474a0a263d7ae7cb4a8`  
		Last Modified: Tue, 11 Oct 2022 17:23:24 GMT  
		Size: 7.9 KB (7890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
