## `mongo:6-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:47f97a64e375693de47416400bdc675b18af298f9f886ecf2bc1ee34043ba882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2527; amd64

### `mongo:6-nanoserver-ltsc2022` - windows version 10.0.20348.2527; amd64

```console
$ docker pull mongo@sha256:291bcb025090ec4a7af470bd25f26d9c1862ad1e937a276794ba97ed242286a1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.3 MB (637268233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d8563a050f69397a8dde7224bb68719b39f72deb470206e43d1ca995ceb354b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 07 Jun 2024 08:41:16 GMT
RUN Apply image 10.0.20348.2527
# Sat, 15 Jun 2024 00:04:41 GMT
SHELL [cmd /S /C]
# Sat, 15 Jun 2024 00:04:42 GMT
USER ContainerAdministrator
# Sat, 15 Jun 2024 00:04:45 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Sat, 15 Jun 2024 00:04:46 GMT
USER ContainerUser
# Sat, 15 Jun 2024 00:04:48 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Sat, 15 Jun 2024 00:04:48 GMT
ENV MONGO_VERSION=6.0.15
# Sat, 15 Jun 2024 00:05:07 GMT
COPY dir:b68ff258c344bc8aa9f2b0f3549c715c1c93667ff42fef166146a10263a4fbca in C:\mongodb 
# Sat, 15 Jun 2024 00:05:23 GMT
RUN mongod --version
# Sat, 15 Jun 2024 00:05:24 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 15 Jun 2024 00:05:25 GMT
EXPOSE 27017
# Sat, 15 Jun 2024 00:05:25 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:f9825bcd6f9509654677a23b5fa1d32b32e1e32ff51914ebfaa76d5e79c22b50`  
		Last Modified: Wed, 12 Jun 2024 02:27:19 GMT  
		Size: 120.5 MB (120488969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0abbce10e4e5df53c1c59c42c80b150b27de91fc11ccf161e56480478f3dbf8b`  
		Last Modified: Sat, 15 Jun 2024 00:05:30 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d922f8d269082b946a9c0e1cdfb631527ccbd7d765bd24438a7fca8469b0fc2`  
		Last Modified: Sat, 15 Jun 2024 00:05:30 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e65c511bf02ed12926a5b5151af818250347e97fa51078a3a6d7b9a4784f89`  
		Last Modified: Sat, 15 Jun 2024 00:05:29 GMT  
		Size: 79.1 KB (79100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c544c9e37fdde10f09409913f9fa18b606d29295750ad2f772626850235b9c8`  
		Last Modified: Sat, 15 Jun 2024 00:05:29 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd90686a273669c27aa9412681d0befc87f965641132b652acf67d00e303c6d2`  
		Last Modified: Sat, 15 Jun 2024 00:05:29 GMT  
		Size: 275.2 KB (275164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e77a3fb40b7bf91100899119db5f0e3c3a1d47be9ccd52146417f6f0ead78e`  
		Last Modified: Sat, 15 Jun 2024 00:05:29 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad1088273a3076d7dd4ef3a4e51d341afe29678be3898d4c184d98be341fab19`  
		Last Modified: Sat, 15 Jun 2024 00:06:09 GMT  
		Size: 516.3 MB (516321136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42abd8c875114ff93c98e2facc4c9419d6f23dde9cb0b49ade3030c2f09a9d3b`  
		Last Modified: Sat, 15 Jun 2024 00:05:28 GMT  
		Size: 96.7 KB (96652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a195a8941d5e6e331b00437248c0cd4ae3f155eb705dd74450dcdc930d5139f1`  
		Last Modified: Sat, 15 Jun 2024 00:05:28 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d9a854b2900d3203c656375e131fa570b2ee8a358215bc970e600518ead792f`  
		Last Modified: Sat, 15 Jun 2024 00:05:28 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07f69751371c0490bf8b4c7027ead2c68b2f233947b213f7b3660765ef52598`  
		Last Modified: Sat, 15 Jun 2024 00:05:28 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
