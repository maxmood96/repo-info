## `mongo:5-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:5f97ea95c7afcc2cb1f8cfc9f931359423d41b54306c319e6f29be51069b9719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `mongo:5-nanoserver-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull mongo@sha256:048a3ba0e3e213e0df5bfad23045c9dd403e7687d1fbf3fdeba379e74179955a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.4 MB (433381227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff7ce0edef7b6995fe782cfb87fc2fa74fcd21cda8fb9aa140f63b69fc591cf`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 05 Dec 2024 01:18:54 GMT
RUN Apply image 10.0.20348.2966
# Wed, 11 Dec 2024 21:48:57 GMT
SHELL [cmd /S /C]
# Wed, 11 Dec 2024 21:48:57 GMT
USER ContainerAdministrator
# Wed, 11 Dec 2024 21:49:01 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 11 Dec 2024 21:49:01 GMT
USER ContainerUser
# Wed, 11 Dec 2024 21:49:03 GMT
COPY multi:241155f1c943760aaa62762c3091531649e347eeddd5ad65cf07160763241a3d in C:\Windows\System32\ 
# Wed, 11 Dec 2024 21:49:03 GMT
ENV MONGO_VERSION=5.0.30
# Wed, 11 Dec 2024 21:49:16 GMT
COPY dir:fd2d6ad81427e0643ec75c35c5a2885caf2411f586ffac83d1ecef0ad3256227 in C:\mongodb 
# Wed, 11 Dec 2024 21:49:23 GMT
RUN mongo --version && mongod --version
# Wed, 11 Dec 2024 21:49:24 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2024 21:49:24 GMT
EXPOSE 27017
# Wed, 11 Dec 2024 21:49:25 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:f9d5d5ca3244fc2c429a892cbe6066394790f649f32d59acfdf012e490896378`  
		Last Modified: Wed, 08 Jan 2025 02:30:35 GMT  
		Size: 120.6 MB (120601318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775f8ecc24cec198786b17b7cf62600d80343606610ad8596ca04407a429abd6`  
		Last Modified: Wed, 11 Dec 2024 21:49:33 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e489932a2126528ae01811a1ecc33494b77578473ce3b7167344d10493bed8a`  
		Last Modified: Wed, 11 Dec 2024 21:49:32 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d50f10ef4c9c9c7b78d3759c8118356c6c7e5e235d2d194cd87c00b0db621b`  
		Last Modified: Wed, 11 Dec 2024 21:49:31 GMT  
		Size: 75.5 KB (75472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949b6e1f900a00389f1ec844b7165c0623be2ae51b18bd74432b3bce4c10ae20`  
		Last Modified: Wed, 11 Dec 2024 21:49:31 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cec3c4ff275022e649cb0b91ae4aa3117b049024686092e02baf1e10a361e1d`  
		Size: 275.3 KB (275347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820030c8baa0436318e4b94bd77570df495046351f5fb54defadc5ed751c5191`  
		Last Modified: Wed, 11 Dec 2024 21:49:30 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae6a3c078d5a85b6181ee9c2ade08470da6778bcb3c4e640bb245382dad5e7d`  
		Last Modified: Wed, 11 Dec 2024 21:49:58 GMT  
		Size: 312.3 MB (312323762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b6218c9f212ce67ef7faed5f2d5dae740d654dd0f22716e53feed22e3252b6b`  
		Last Modified: Wed, 11 Dec 2024 21:49:29 GMT  
		Size: 98.1 KB (98112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc54370e8115294c6883026707b9bd235ac65b237768a4e8b9947e184e22178b`  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c8cef14860fc6b966fc57816b9e1274b7486f0795f485b129a9a1421785c30`  
		Last Modified: Wed, 11 Dec 2024 21:49:29 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa6a489071f2fdf61d849cf4ece7ad1f52a0da06fcce5460b7fa80ddfc4df66`  
		Last Modified: Wed, 11 Dec 2024 21:49:29 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
