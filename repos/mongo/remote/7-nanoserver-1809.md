## `mongo:7-nanoserver-1809`

```console
$ docker pull mongo@sha256:51ba240af929bea42cf228fdf86a3586269e2e0b6101ca8858bb111cd7982149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `mongo:7-nanoserver-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull mongo@sha256:fa65d8a6127ecc57ef8ac2f4da7913ddb024e3291372df48dd336591afbb6254
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **718.9 MB (718938548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a31487ac1884780471dd92935071733814b10ebf3ab98e077002410bca036915`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 05 Apr 2025 01:31:28 GMT
RUN Apply image 10.0.17763.7136
# Tue, 15 Apr 2025 00:09:04 GMT
SHELL [cmd /S /C]
# Tue, 15 Apr 2025 00:09:05 GMT
USER ContainerAdministrator
# Tue, 15 Apr 2025 00:09:07 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Tue, 15 Apr 2025 00:09:08 GMT
USER ContainerUser
# Tue, 15 Apr 2025 00:09:09 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Tue, 15 Apr 2025 00:09:10 GMT
ENV MONGO_VERSION=7.0.19
# Tue, 15 Apr 2025 00:09:49 GMT
COPY dir:9c112edd2ccbf73f54eccbe10e51c93e720a60d4adf79e8d4bde4396b3fc6121 in C:\mongodb 
# Tue, 15 Apr 2025 00:09:57 GMT
RUN mongod --version
# Tue, 15 Apr 2025 00:09:57 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 15 Apr 2025 00:09:58 GMT
EXPOSE 27017
# Tue, 15 Apr 2025 00:09:59 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:a06e0965a0fa3715e629889bd9332aa22aadd75654cac5c9818b67c0264b3ee1`  
		Last Modified: Tue, 08 Apr 2025 20:16:02 GMT  
		Size: 106.9 MB (106922524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:313e04eb098595d5b945067a49c4884144a495cb9c415e7963bb45076c65573c`  
		Last Modified: Tue, 15 Apr 2025 00:10:07 GMT  
		Size: 1.1 KB (1054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4ee417747f03891ede93ab2d6fc1ee2cf23862df7c42bcf8c33cbd653fa492`  
		Last Modified: Tue, 15 Apr 2025 00:10:07 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1529dc33786d088e346cffff16a559e053ddb1c7e6b192654969107fca1890de`  
		Last Modified: Tue, 15 Apr 2025 00:10:05 GMT  
		Size: 68.8 KB (68785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d6aaf920f37e3e86d35be6ff7ff0e101a2c0bf372d9c3285111c37b937f0bac`  
		Last Modified: Tue, 15 Apr 2025 00:10:05 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3367c5aaea3b0120111869ab2e8e73081a5a8fcb2578ba99aed22c72e221a28b`  
		Last Modified: Tue, 15 Apr 2025 00:10:05 GMT  
		Size: 275.2 KB (275233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de91f0d3f2f5e640a00c8ce58867196820d8330c277b602f4bce8e2cc7a8d69b`  
		Last Modified: Tue, 15 Apr 2025 00:10:05 GMT  
		Size: 1.1 KB (1098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2c6aa8aa45bb985988b68c4da798370086bead2fed767b476c05fa94a6f2f6`  
		Last Modified: Tue, 15 Apr 2025 00:10:52 GMT  
		Size: 611.6 MB (611592508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6916f03f581d7388f0a4fa53a7b7b946d45385260d25f481143b2dd1374d2ac1`  
		Last Modified: Tue, 15 Apr 2025 00:10:03 GMT  
		Size: 72.1 KB (72076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4efc4bd95306588ecc1a29d8714040c3d2fc6388cfa9fa2308542ab2a18118`  
		Last Modified: Tue, 15 Apr 2025 00:10:03 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92daf9a8a229625167c4606601ffec30669c60b18bf2a9f96c3de37054c26e8d`  
		Last Modified: Tue, 15 Apr 2025 00:10:03 GMT  
		Size: 1.1 KB (1097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c382a160b24968f19d52aa8e86e63944dee4586774d16fa89c2badeb6f461c4a`  
		Last Modified: Tue, 15 Apr 2025 00:10:03 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
