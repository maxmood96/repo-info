## `golang:nanoserver-1809`

```console
$ docker pull golang@sha256:c1b85c07f059b3a9622ea153dac9c19f8695b95819fe918a2e07478f415371ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `golang:nanoserver-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull golang@sha256:faf9970d047c3e65987a965b7aa39c0940b4701b7800ed7eaeb63da747f6570b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.9 MB (188873656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9776b1044398a520904bf27c10d481fa315b33642ebd893acd6cc3f7d0b5e20a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Tue, 04 Mar 2025 21:57:58 GMT
SHELL [cmd /S /C]
# Tue, 04 Mar 2025 21:57:59 GMT
ENV GOPATH=C:\go
# Tue, 04 Mar 2025 21:58:00 GMT
USER ContainerAdministrator
# Tue, 04 Mar 2025 21:58:14 GMT
RUN setx /m PATH "%GOPATH%\bin;C:\Program Files\Go\bin;%PATH%"
# Tue, 04 Mar 2025 21:58:14 GMT
USER ContainerUser
# Tue, 04 Mar 2025 21:58:15 GMT
ENV GOLANG_VERSION=1.24.1
# Tue, 04 Mar 2025 21:59:17 GMT
COPY dir:1c8a5df65fcdbd0ad306edfb20884d0712989c03ff01d990889cdc983af886a3 in C:\Program Files\Go 
# Tue, 04 Mar 2025 21:59:21 GMT
RUN go version
# Tue, 04 Mar 2025 21:59:21 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c381b10c70eb7825fac4ff06a9bebd4c3aef41802c387c465de0ad24fb8afc1`  
		Last Modified: Tue, 04 Mar 2025 21:59:25 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ebf1c184b2d6ec966f45957dc2a34cfda788482b888be1ded90c85cee65d86`  
		Last Modified: Tue, 04 Mar 2025 21:59:25 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cccf8153226e97e7fb4a918d1b659c34670bced0a2631c7a0d8d2952995f96e`  
		Last Modified: Tue, 04 Mar 2025 21:59:25 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13f48efe68d506c6ed3f1183d947d9fa7bf7d35b50435051b0674026ee286de`  
		Last Modified: Tue, 04 Mar 2025 21:59:25 GMT  
		Size: 66.4 KB (66415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ed5b383f514b157fc9f2e070f534e80ff07b3f4b351b9a71c3d4d380d1a77d`  
		Last Modified: Tue, 04 Mar 2025 21:59:24 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8091b3790c62d35c76897fabdca59190193acebaf34954e13ab4d5aed8e300dd`  
		Last Modified: Tue, 04 Mar 2025 21:59:24 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11263cfb8ac4306eb388259fc1a6236dbfa44fc2344d138acfd113caed002981`  
		Last Modified: Tue, 04 Mar 2025 21:59:36 GMT  
		Size: 81.8 MB (81819038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4b2f9a3a4b1559a0fb0e589415a7f99ceca02136d5dfa7b2f5522099248451`  
		Last Modified: Tue, 04 Mar 2025 21:59:24 GMT  
		Size: 66.2 KB (66213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cccd9fff9c9f864ad17f4dc9b6607cc8a595eead6d90c5daf1d29f1cc5e56ef`  
		Last Modified: Tue, 04 Mar 2025 21:59:24 GMT  
		Size: 1.2 KB (1243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
