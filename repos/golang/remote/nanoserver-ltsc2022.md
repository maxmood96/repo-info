## `golang:nanoserver-ltsc2022`

```console
$ docker pull golang@sha256:f300ae5bc2cad3e7cedb789cb4c62304b065695f4889665d5b981b5693295cf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `golang:nanoserver-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull golang@sha256:2dc3a3058a982b782052440acb799ce007dff98225ac3b74602791d19d5f089a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184755405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633b268555efcf47cd794ffb8b63f1895151d8a555b47f6e23dfbba0a20d98f1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 22 Oct 2025 21:38:30 GMT
RUN Apply image 10.0.20348.4297
# Wed, 05 Nov 2025 21:14:36 GMT
SHELL [cmd /S /C]
# Wed, 05 Nov 2025 21:14:38 GMT
ENV GOPATH=C:\go
# Wed, 05 Nov 2025 21:14:40 GMT
USER ContainerAdministrator
# Wed, 05 Nov 2025 21:14:56 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Wed, 05 Nov 2025 21:14:57 GMT
USER ContainerUser
# Wed, 05 Nov 2025 21:14:58 GMT
ENV GOLANG_VERSION=1.25.4
# Wed, 05 Nov 2025 21:16:58 GMT
COPY dir:3cd50d34ed67d71dc6ad2837dc9665403756fda3aa14b5be3225998e6b9c9021 in C:\Program Files\Go 
# Wed, 05 Nov 2025 21:17:03 GMT
RUN go version
# Wed, 05 Nov 2025 21:17:05 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:2ac1abee018ad49a2f67a19d7f82901aac546affca76c86382db1a855dfcdaa1`  
		Last Modified: Fri, 24 Oct 2025 03:12:47 GMT  
		Size: 122.7 MB (122684063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d87428036e29944b836a81eb0158af17d3da226b65f33e0a9f3fb3403912f7`  
		Last Modified: Wed, 05 Nov 2025 21:17:27 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec04db77061f1b5511d687a659e1be5521d5de8f9b899d67750b6098aa93d78`  
		Last Modified: Wed, 05 Nov 2025 21:17:27 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af135193fd5d7eb988368fb9072638093225159f7976c7394537621c509aeba`  
		Last Modified: Wed, 05 Nov 2025 21:17:27 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136198900115c19ea4499fff99f491e56aaf7ccd61cea251de31c93e4ef6099c`  
		Last Modified: Wed, 05 Nov 2025 21:17:27 GMT  
		Size: 80.2 KB (80208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d872fb07936d456348ac275a7e5970ef076dae5ab9cad8f6695e4d36a4fb6a74`  
		Last Modified: Wed, 05 Nov 2025 21:17:27 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b2cbd5498a091d98011cea2a32fd0f8261c65f630c1ee0df0b4a26b7bfccca`  
		Last Modified: Wed, 05 Nov 2025 21:17:28 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2682fee6cefe9c9c1b67f7dce190943ab0009a2baa233fc88bb0341de3ab3dc`  
		Last Modified: Wed, 05 Nov 2025 21:17:33 GMT  
		Size: 61.9 MB (61900843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7381707e431834ccc8dd6b22802dd4be9dfe3b5055b6c0568169fad880e600`  
		Last Modified: Wed, 05 Nov 2025 21:17:28 GMT  
		Size: 83.7 KB (83701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc1a88e51f6a0f099f439cd9f656b767cf9a969355457565ffce87d98723f14`  
		Last Modified: Wed, 05 Nov 2025 21:17:28 GMT  
		Size: 1.3 KB (1251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
