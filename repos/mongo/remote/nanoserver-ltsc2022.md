## `mongo:nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:0b97fc08182af1a8782d108106f86b71f08b9d76ea658bd887557970fb5ba090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `mongo:nanoserver-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull mongo@sha256:b5a5b571779bf9a0f46127853417d91964cac6769684fb624e2ae4c1b3d860d3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **728.7 MB (728728238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2255ee481a02376998cdf797618902a43cddb8a6e1a7f5f948c068684950967`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 10 Aug 2024 19:28:00 GMT
RUN Apply image 10.0.20348.2655
# Tue, 13 Aug 2024 21:08:40 GMT
SHELL [cmd /S /C]
# Tue, 13 Aug 2024 21:08:41 GMT
USER ContainerAdministrator
# Tue, 13 Aug 2024 21:08:43 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Tue, 13 Aug 2024 21:08:43 GMT
USER ContainerUser
# Tue, 13 Aug 2024 21:08:45 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Tue, 13 Aug 2024 21:08:46 GMT
ENV MONGO_VERSION=7.0.12
# Tue, 13 Aug 2024 21:09:06 GMT
COPY dir:f0b5fa50aabc110faf03295e6346b9d39d589dd155d9a16877c392688d63cd36 in C:\mongodb 
# Tue, 13 Aug 2024 21:09:21 GMT
RUN mongod --version
# Tue, 13 Aug 2024 21:09:22 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 13 Aug 2024 21:09:23 GMT
EXPOSE 27017
# Tue, 13 Aug 2024 21:09:23 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:695cae91f2de8dadf81c8b3a95f4942533ef064a72ad8fa7843cca84a839bfba`  
		Last Modified: Tue, 13 Aug 2024 20:02:51 GMT  
		Size: 120.6 MB (120554921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aae38f92f1a90502ab29667a6e8b666659ff65ea1ad20440782fb8e275f5574`  
		Last Modified: Tue, 13 Aug 2024 21:09:31 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6f249d1261c6d799d6c415ecd9d12e2aebb578a77d8795d9d6f46bf2225d817`  
		Last Modified: Tue, 13 Aug 2024 21:09:31 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d70826cc1803011adf3f501ef4f7191c4cf599914cac95fbc69181928c8fc1a1`  
		Last Modified: Tue, 13 Aug 2024 21:09:29 GMT  
		Size: 77.5 KB (77527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe376c5f473c16815b109649d2b1849e6aba962a92c314ad06dcf8a4f51f20e`  
		Last Modified: Tue, 13 Aug 2024 21:09:29 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2eafc69f6fb1f56360e9610f4241ec8f4ccd8a1fc3249a225ed9efeff3699cb`  
		Last Modified: Tue, 13 Aug 2024 21:09:29 GMT  
		Size: 275.2 KB (275159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc902612c73722f14ccd9e220904bb8b5663c3ee955a49fddae58f8166ec6607`  
		Last Modified: Tue, 13 Aug 2024 21:09:29 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5e7832bd3498640ab416ab35be74f3db58d92d0f42d05dd441ddc8b9c8f7b3`  
		Last Modified: Tue, 13 Aug 2024 21:10:14 GMT  
		Size: 607.7 MB (607714596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9828e71e9f685521bd20a04ee54ffc61a2926f5325869b0ef21e78a359f1b8b8`  
		Last Modified: Tue, 13 Aug 2024 21:09:27 GMT  
		Size: 98.8 KB (98815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b1331af1c415def0e7fccbe8fad9c79b591974106a3d8184690c6d291a3598`  
		Last Modified: Tue, 13 Aug 2024 21:09:27 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356f9ee76f76bdce39f50a20508ccad71265f311eabe538eaa733ba120f06cba`  
		Last Modified: Tue, 13 Aug 2024 21:09:27 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71857d3c4da70254690d9a27240b5f081bd94da21c3171b9743aa3634b41c4ce`  
		Last Modified: Tue, 13 Aug 2024 21:09:27 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
