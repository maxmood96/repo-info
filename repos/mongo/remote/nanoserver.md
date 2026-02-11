## `mongo:nanoserver`

```console
$ docker pull mongo@sha256:e8e5094c5747ea36a461fea373ecc78d054215de0b87024551958d23bc3ef11b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `mongo:nanoserver` - windows version 10.0.20348.4648; amd64

```console
$ docker pull mongo@sha256:c18f128db0e8f7639d4604d692542bb6bffe45618223cb7df7ed9f04ac03639e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **941.6 MB (941590008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffa0f51b32c9879cbe9694b2d7aa558ebdb1116256e949e56622ffaaaaada6f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Tue, 10 Feb 2026 21:13:44 GMT
SHELL [cmd /S /C]
# Tue, 10 Feb 2026 21:13:47 GMT
USER ContainerAdministrator
# Tue, 10 Feb 2026 21:14:03 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Tue, 10 Feb 2026 21:14:04 GMT
USER ContainerUser
# Tue, 10 Feb 2026 21:14:08 GMT
COPY multi:540d6dd70b1e7484f1958dc08b337aeb56cf8a92fe38be4c279dd406990d6935 in C:\Windows\System32\ 
# Tue, 10 Feb 2026 21:14:10 GMT
ENV MONGO_VERSION=8.2.5
# Tue, 10 Feb 2026 21:15:34 GMT
COPY dir:a0b1e52802eea6e71b140810e76e3ccf3bfdb8657e849479e93df0cd3a9bf7bb in C:\mongodb 
# Tue, 10 Feb 2026 21:15:57 GMT
RUN mongod --version
# Tue, 10 Feb 2026 21:15:58 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 10 Feb 2026 21:15:59 GMT
EXPOSE 27017
# Tue, 10 Feb 2026 21:16:00 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4acba92e930621aa066243dc804cb79601d3950ee96d913d0b2138d82a8db70`  
		Last Modified: Tue, 10 Feb 2026 21:16:09 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d3f95e776cc4dae3b464e0eb8a283a4057279cbee749584752de3c915785b5`  
		Last Modified: Tue, 10 Feb 2026 21:16:09 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a112e1ba715fe6866ca82ed86d3bf3157810c50009e480a0c3852d11724bcc`  
		Last Modified: Tue, 10 Feb 2026 21:16:07 GMT  
		Size: 74.5 KB (74464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95e589cdfd0573ed3ecdd231e440e03ea7034c257388372381dfe55cf735006`  
		Last Modified: Tue, 10 Feb 2026 21:16:07 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c1ed3ef74ed8b6b476640b4e0cfcba9320e86a933e184a61c2c74b0a1015b1`  
		Last Modified: Tue, 10 Feb 2026 21:16:08 GMT  
		Size: 275.2 KB (275208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6fb6cd7156ae770a143d4d85f719e521f0200c6918ae4edb86358f98037624`  
		Last Modified: Tue, 10 Feb 2026 21:16:07 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4cd0cb7369d251252be5f307baa2097b63b368bda7340925a0fca34fa975c6`  
		Last Modified: Tue, 10 Feb 2026 21:17:19 GMT  
		Size: 814.4 MB (814448500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51cceaacb9b80efdcb0aba5b50ebbb200e9d461e77b6df72cf8932498e3c7263`  
		Last Modified: Tue, 10 Feb 2026 21:16:06 GMT  
		Size: 87.6 KB (87565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bea885ca1c3157dba88c9637cc75bd274b737ea9fbf8488dbe43e264b6a5f1d`  
		Last Modified: Tue, 10 Feb 2026 21:16:06 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f8ad6b0f00e174c727c1150d3f24f772b54567d56fb4d55cf15a916c624742`  
		Last Modified: Tue, 10 Feb 2026 21:16:06 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ca5cd3cb25b14172c2917bf4fd497de5e0385009c6d1188774a2f28b223914`  
		Last Modified: Tue, 10 Feb 2026 21:16:06 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
