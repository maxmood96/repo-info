## `mongo:6-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:5e233706f401c85f44b2e963233ad68ef348ddfe99cac6a6ea960040f09fa670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `mongo:6-nanoserver-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull mongo@sha256:062af46b37a723ddf187cc0b72796ddbb8700c222a90c99e95194a8230ccdf9b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.3 MB (647268428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fbe1d0498bfc786befc6b6d073a5f6cfca29d115001f3a5f1fc3a4a496dbd83`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Tue, 18 Mar 2025 17:53:59 GMT
SHELL [cmd /S /C]
# Tue, 18 Mar 2025 17:53:59 GMT
USER ContainerAdministrator
# Tue, 18 Mar 2025 17:54:01 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Tue, 18 Mar 2025 17:54:02 GMT
USER ContainerUser
# Tue, 18 Mar 2025 17:54:04 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Tue, 18 Mar 2025 17:54:04 GMT
ENV MONGO_VERSION=6.0.21
# Tue, 18 Mar 2025 17:54:22 GMT
COPY dir:3e58ecc6221c38d328e962765c65cbae4544929c28b4dc0b7bf576cc4212e36c in C:\mongodb 
# Tue, 18 Mar 2025 17:54:33 GMT
RUN mongod --version
# Tue, 18 Mar 2025 17:54:34 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 18 Mar 2025 17:54:35 GMT
EXPOSE 27017
# Tue, 18 Mar 2025 17:54:36 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf9ce98ee7e81fe133a1f8764cd89a187bcfa05acc9d3689d4613766e34fc7c`  
		Last Modified: Tue, 18 Mar 2025 17:54:40 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0433cd25b78602c549aba95a7d3b0a82cc29f8c4ed5cc35f80b0bdcc7d93e9`  
		Last Modified: Tue, 18 Mar 2025 17:54:40 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994287ff7dc4521401053e1386312587041442df1cc5b918380965fa19e2fdf8`  
		Last Modified: Tue, 18 Mar 2025 17:54:40 GMT  
		Size: 76.0 KB (75963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d987a472de33a9037922366eb79a661454e3ba426cba1505b10af1d53341b8`  
		Last Modified: Tue, 18 Mar 2025 17:54:39 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09da87c4f8ba19371333e49120c454f1b66935b0dca1e2e0d22634a646f07e9`  
		Last Modified: Tue, 18 Mar 2025 17:54:40 GMT  
		Size: 275.1 KB (275138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf6b51571f795496a083c1cb0988dbe6372749acb2c5e4f80f2a2689f0a8d16`  
		Last Modified: Tue, 18 Mar 2025 17:54:39 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52965b31b2f5f6b277566e8c0f50ee555d68dfe786fc1747ad30dab719d7f7bb`  
		Last Modified: Tue, 18 Mar 2025 17:55:23 GMT  
		Size: 526.1 MB (526116277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1260fb8f96719a3d9540dac0e332c493b65014426769fdf9cd4b4f52e189cdb0`  
		Last Modified: Tue, 18 Mar 2025 17:54:38 GMT  
		Size: 98.2 KB (98248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5373239660975f9df87f119767b544aed002bd95ee6c536dc162342d1098640c`  
		Last Modified: Tue, 18 Mar 2025 17:54:38 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50dec9b906bb1a041bc2340af161cd294b8351588addb1379e7135b0053edb14`  
		Last Modified: Tue, 18 Mar 2025 17:54:38 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3be39552beef8ab0428bda320e07b5628bffc30b291b0e0196a6ebd72491b1`  
		Last Modified: Tue, 18 Mar 2025 17:54:38 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
