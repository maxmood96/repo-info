## `mongo:7-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:64d174d38171b1149ed725aaf3f02a60b842b0f088203421e4eebbd2737c86f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `mongo:7-nanoserver-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull mongo@sha256:6244772f14027e3bdd33153583231d196fcae3f04fd8f48731fd8e323ab9bf94
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **737.8 MB (737844526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014a07dea6b694a349b20ddd999dbed66124fe87d3d1b1c367a03f429b5c7768`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 05 Jun 2025 00:43:46 GMT
RUN Apply image 10.0.20348.3807
# Tue, 10 Jun 2025 22:20:37 GMT
SHELL [cmd /S /C]
# Tue, 10 Jun 2025 22:20:38 GMT
USER ContainerAdministrator
# Tue, 10 Jun 2025 22:20:40 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Tue, 10 Jun 2025 22:20:41 GMT
USER ContainerUser
# Tue, 10 Jun 2025 22:20:43 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Tue, 10 Jun 2025 22:20:44 GMT
ENV MONGO_VERSION=7.0.21
# Tue, 10 Jun 2025 22:21:05 GMT
COPY dir:6becbf78ea59b54f2ec6d0930e08b1dc344a9130079de3866a6f2a985cca81f2 in C:\mongodb 
# Tue, 10 Jun 2025 22:21:21 GMT
RUN mongod --version
# Tue, 10 Jun 2025 22:21:22 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 10 Jun 2025 22:21:24 GMT
EXPOSE 27017
# Tue, 10 Jun 2025 22:21:25 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:96acbf1c6d5b6cc37517502ecbb6a1d2eb55b7615b696401ead868c97a971964`  
		Last Modified: Tue, 10 Jun 2025 20:17:56 GMT  
		Size: 122.5 MB (122540534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70ce26221080b67fb51d76674f4aa0924464011b493a930410c611b53602c2af`  
		Last Modified: Tue, 10 Jun 2025 22:22:48 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dda0c34cb83045a332a699c3818ac2ead33f61f39c4aed886a34274c014b97c`  
		Last Modified: Tue, 10 Jun 2025 22:22:48 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a1138a39ac0eb78e7379e36ee71ea39db588312fddc30f59a63c53a82a7c8a9`  
		Last Modified: Tue, 10 Jun 2025 22:22:48 GMT  
		Size: 77.7 KB (77731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e26731bf78ec4d3b9265c59097281b337b3e885154bd3cf42fef21d097cb34d`  
		Last Modified: Tue, 10 Jun 2025 22:22:48 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0923743687b874bb895920de8c57bb16f26568a201089852cb23956c6bacefdd`  
		Last Modified: Tue, 10 Jun 2025 22:22:49 GMT  
		Size: 275.2 KB (275175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ab1ef76f62280d3792ba1c721f2ff02e658b6fa079aa9bf4d031dd0b53f54a`  
		Last Modified: Tue, 10 Jun 2025 22:22:49 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669ee3f3a6a642b197fbffae56483e853e419fbf58536f09d1b3a8a0d1682d0c`  
		Last Modified: Wed, 11 Jun 2025 01:08:57 GMT  
		Size: 614.8 MB (614848869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8512b39ecd8daf9cbae2493917ae85c7ea17802fb6528259df8978fb72ffe487`  
		Last Modified: Tue, 10 Jun 2025 22:33:09 GMT  
		Size: 95.0 KB (94957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc843306a7415622b5362d2cc135e181eaa451c36eb6a980892a60321cd6a80`  
		Last Modified: Tue, 10 Jun 2025 22:33:14 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe2198ad57eb617ee03e481d5ea97b6bd7918f832420b4dcac41ba5af46d92f`  
		Last Modified: Tue, 10 Jun 2025 22:33:17 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d408f4ca11493d8574af8baba699de445f3d876f14cde34b549c6e4d2b358457`  
		Last Modified: Tue, 10 Jun 2025 22:33:20 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
