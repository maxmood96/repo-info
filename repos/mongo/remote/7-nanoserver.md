## `mongo:7-nanoserver`

```console
$ docker pull mongo@sha256:6e290028b937f81c82a4f92595095555f21251f1210f9562d683cd2fd36c3704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7136; amd64

### `mongo:7-nanoserver` - windows version 10.0.20348.3453; amd64

```console
$ docker pull mongo@sha256:a122eadb0720cb5e6f8d2b68c061c099c4ac47d1c43d578bef3db98cf43c001a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **732.8 MB (732782085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0064048fc560da4cc653007f7bf4f19908733f402716a75c7a00b5e2e238dac5`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 04 Apr 2025 22:57:50 GMT
RUN Apply image 10.0.20348.3453
# Tue, 15 Apr 2025 00:15:17 GMT
SHELL [cmd /S /C]
# Tue, 15 Apr 2025 00:15:18 GMT
USER ContainerAdministrator
# Tue, 15 Apr 2025 00:15:21 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Tue, 15 Apr 2025 00:15:22 GMT
USER ContainerUser
# Tue, 15 Apr 2025 00:15:23 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Tue, 15 Apr 2025 00:15:23 GMT
ENV MONGO_VERSION=7.0.19
# Tue, 15 Apr 2025 00:15:46 GMT
COPY dir:9c112edd2ccbf73f54eccbe10e51c93e720a60d4adf79e8d4bde4396b3fc6121 in C:\mongodb 
# Tue, 15 Apr 2025 00:16:04 GMT
RUN mongod --version
# Tue, 15 Apr 2025 00:16:05 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 15 Apr 2025 00:16:05 GMT
EXPOSE 27017
# Tue, 15 Apr 2025 00:16:06 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:5caa30147a287e99992660f7f85276c53fe3299503a06c47d476387410721453`  
		Last Modified: Wed, 09 Apr 2025 01:13:36 GMT  
		Size: 120.7 MB (120736312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5940d350ea2085cf1c459c77ba028a05de1bed6448ba73a4cd0cbd1e93dbae8d`  
		Last Modified: Tue, 15 Apr 2025 00:16:13 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c670d49e86ec6360bffc6d42c5a3cd2a37de01af38043e8105b92eb6fa296c4`  
		Last Modified: Tue, 15 Apr 2025 00:16:13 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90c54217a57c0220d8c979431c56cd160a8f6d3c14f40dddb999a17a8a4ccc3`  
		Last Modified: Tue, 15 Apr 2025 00:16:12 GMT  
		Size: 75.6 KB (75632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78aed1d230df505e8ee1e0c4037f5fa00834ee473334121e90db5302d7e73068`  
		Last Modified: Tue, 15 Apr 2025 00:16:11 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf3ed99c70d6c3fe10f2990ae93ebe3283b6a5cfb99528a0e05c747e6daf7ce`  
		Last Modified: Tue, 15 Apr 2025 00:16:12 GMT  
		Size: 275.2 KB (275159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43310731929f2021a24cff3914b96032932d8c76ca2ffecad8b998d62f4bea1`  
		Last Modified: Tue, 15 Apr 2025 00:16:11 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ea42638cb216e0d7a88da28ca3f23bd18503856c0a5149c6992a8a1bf42fde`  
		Last Modified: Tue, 15 Apr 2025 00:16:57 GMT  
		Size: 611.6 MB (611592107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ee809847614fd64c8301a0fe9d7fc3e7514d6d7aab30f0823391e0ddeb06e5`  
		Last Modified: Tue, 15 Apr 2025 00:16:10 GMT  
		Size: 95.7 KB (95672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc9b2dff69d37bacffd08acb0158110982d8f1fad2ac6e392b93f7fd3048c05`  
		Last Modified: Tue, 15 Apr 2025 00:16:10 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed31ba170263ab91dd189f5300d4e109fcaa590b7bc6423a2f9820d5f4dbe523`  
		Last Modified: Tue, 15 Apr 2025 00:16:10 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd6d85832029da193ecebb736f7e8477e7683a3cf62f3a4e3439964307bac05`  
		Last Modified: Tue, 15 Apr 2025 00:16:10 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-nanoserver` - windows version 10.0.17763.7136; amd64

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
