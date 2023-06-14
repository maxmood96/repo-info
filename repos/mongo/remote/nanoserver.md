## `mongo:nanoserver`

```console
$ docker pull mongo@sha256:da7ff753c3215523a6fe6d99967753e64200bce55f4185fa720bfd9525416090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1787; amd64
	-	windows version 10.0.17763.4499; amd64

### `mongo:nanoserver` - windows version 10.0.20348.1787; amd64

```console
$ docker pull mongo@sha256:ba596dc2d05f5d913fb34f0e76e133c5c8340c1dd1eba58e14fcb56836fbfeea
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.6 MB (635552638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aab79bfcbb9c9787c2df484bbca7465db20f54119a4d09d78723e48d5ef1ef7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 08 Jun 2023 12:38:25 GMT
RUN Apply image 10.0.20348.1787
# Wed, 14 Jun 2023 18:50:26 GMT
SHELL [cmd /S /C]
# Wed, 14 Jun 2023 19:21:55 GMT
USER ContainerAdministrator
# Wed, 14 Jun 2023 19:22:11 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 14 Jun 2023 19:22:11 GMT
USER ContainerUser
# Wed, 14 Jun 2023 19:22:12 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Wed, 14 Jun 2023 19:30:21 GMT
ENV MONGO_VERSION=6.0.6
# Wed, 14 Jun 2023 19:31:03 GMT
COPY dir:f255d7e00c887e6b06f18133f01bba238bdbaee13791df8bb9e0f4062260c28f in C:\mongodb 
# Wed, 14 Jun 2023 19:31:16 GMT
RUN mongod --version
# Wed, 14 Jun 2023 19:31:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 14 Jun 2023 19:31:17 GMT
EXPOSE 27017
# Wed, 14 Jun 2023 19:31:18 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:f94f5e4cef3f52c830328b87b7298c638fa9ef22a0babf737eda2a2dd6d024c4`  
		Last Modified: Tue, 13 Jun 2023 20:05:48 GMT  
		Size: 120.0 MB (120028549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf26306b7c3ea55d7d8bb15ad1c70de776773883ccc3ce02d9cfac7a8177ccf8`  
		Last Modified: Wed, 14 Jun 2023 19:09:48 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea973e1d3f627a7f78f5f09ff4e4cbe54950ad931a8ac9f6b91800c3f870662`  
		Last Modified: Wed, 14 Jun 2023 19:53:21 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a05d3662d1253cfbf06530db11bb819751c1f3b989def94c06313f77ef96d3`  
		Last Modified: Wed, 14 Jun 2023 19:53:19 GMT  
		Size: 74.0 KB (74005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17495be05e5c0ea68148077f81896256940de4ab199038e806fc1c968454aba1`  
		Last Modified: Wed, 14 Jun 2023 19:53:19 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222a90b2c97562234704d81d4a9fde040d4b926d5878b892f26a2bd3919ea5f4`  
		Last Modified: Wed, 14 Jun 2023 19:53:19 GMT  
		Size: 267.2 KB (267200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d928d18872ba1f1d5759a910103dd579cbe64796fd50c192994afca0688e4d`  
		Last Modified: Wed, 14 Jun 2023 19:59:52 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a14691d8b24416df7dce7e005eead457209b2ccd9193ec9d71c0b7a0c1a8e7c5`  
		Last Modified: Wed, 14 Jun 2023 20:01:11 GMT  
		Size: 515.1 MB (515114155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9991926ac6f3790a66b73e3c22a7c30bb656b875c19767aa2e4a69d559aa911`  
		Last Modified: Wed, 14 Jun 2023 19:59:50 GMT  
		Size: 61.2 KB (61157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d13c7ea935a2bef353c40e1f5bd9af07602c4ed8e7623cfae212cf01848fdb`  
		Last Modified: Wed, 14 Jun 2023 19:59:50 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31edc05e2cdbfe2abfe9488b3f793091ecc656a19db94860c728ce232b3d719`  
		Last Modified: Wed, 14 Jun 2023 19:59:50 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea25bfd97807234cf166a22361d56878a5eff3590296b5d5bcd5e24c70561be1`  
		Last Modified: Wed, 14 Jun 2023 19:59:50 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:nanoserver` - windows version 10.0.17763.4499; amd64

```console
$ docker pull mongo@sha256:acfca76c7372944ef6faeaa597d88113f02deb2ea97aea68d9e9002240a8b9d1
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **619.9 MB (619941702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b682542b794b8468a787ddd2c2c5ccebe348dcf0007c3d0376c3751f88344bfa`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 08 Jun 2023 12:28:32 GMT
RUN Apply image 10.0.17763.4499
# Wed, 14 Jun 2023 18:53:10 GMT
SHELL [cmd /S /C]
# Wed, 14 Jun 2023 19:23:38 GMT
USER ContainerAdministrator
# Wed, 14 Jun 2023 19:23:52 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 14 Jun 2023 19:23:52 GMT
USER ContainerUser
# Wed, 14 Jun 2023 19:23:53 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Wed, 14 Jun 2023 19:31:37 GMT
ENV MONGO_VERSION=6.0.6
# Wed, 14 Jun 2023 19:32:18 GMT
COPY dir:f255d7e00c887e6b06f18133f01bba238bdbaee13791df8bb9e0f4062260c28f in C:\mongodb 
# Wed, 14 Jun 2023 19:32:31 GMT
RUN mongod --version
# Wed, 14 Jun 2023 19:32:32 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 14 Jun 2023 19:32:32 GMT
EXPOSE 27017
# Wed, 14 Jun 2023 19:32:33 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:234d39d9b188e7f36d5a77b0d54990ea826551314b6703c83aef3ef20b1a7050`  
		Last Modified: Tue, 13 Jun 2023 19:06:23 GMT  
		Size: 104.4 MB (104397895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84163792b788702ed02647fa84aaa1ebd7ba0473cb5b5ad12bcaa9a2c6cb5de1`  
		Last Modified: Wed, 14 Jun 2023 19:10:26 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd799c88299e1ebd604eaa844089e95b8f35888e44322cd7da278cf0f9f6de5e`  
		Last Modified: Wed, 14 Jun 2023 19:55:04 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4502866eaaaba58a010f68a9deb71bef8bcc8181d4e895d1822b78614358f4`  
		Last Modified: Wed, 14 Jun 2023 19:55:03 GMT  
		Size: 73.9 KB (73909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f7d3e438ee6e0b29ca19f74c7af5de2b036744543135f66aaca8c7644e300f`  
		Last Modified: Wed, 14 Jun 2023 19:55:02 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:424bb45726be0697e1242142be7739349fa4b7e66e26128ae8b66b0e1795e157`  
		Last Modified: Wed, 14 Jun 2023 19:55:02 GMT  
		Size: 267.2 KB (267201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c8398b5a8bc2565ad8d81663da1c55bc4381de48651d4ad3ac576bd3c28e3f9`  
		Last Modified: Wed, 14 Jun 2023 20:01:28 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec6cec8aa7443588c29cc3ad3e0fc6a659a2e475b8377d589405084d526f3f81`  
		Last Modified: Wed, 14 Jun 2023 20:02:45 GMT  
		Size: 515.1 MB (515114203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4179abceeb8a819e8227ff53b64d15d909d1ffab97f9118141f0400414980c8a`  
		Last Modified: Wed, 14 Jun 2023 20:01:26 GMT  
		Size: 80.7 KB (80724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72cc2d041ad1ea2e454472d53bfb80a4de91b5cb1bb7059b4465390d764959b`  
		Last Modified: Wed, 14 Jun 2023 20:01:25 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4931c68caaa7bcc9746f80a593c049132b9c0e76a41f9cf799facf5bd869b430`  
		Last Modified: Wed, 14 Jun 2023 20:01:26 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460e9318d0ffbdc2dfe7d6ebf6588251a62033001e2cabcd3aff5cac1d0407b0`  
		Last Modified: Wed, 14 Jun 2023 20:01:26 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
