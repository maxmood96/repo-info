## `mongo:5-nanoserver`

```console
$ docker pull mongo@sha256:6d00dbcd5c9cec914ee66bb666525aa5d3c7d30ff7f3e6827a14ab73f3421463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `mongo:5-nanoserver` - windows version 10.0.20348.2340; amd64

```console
$ docker pull mongo@sha256:9f8e556cb962a907e26c2bd98ef4d717a9fe235ffef8e5b754cfbb6924281abd
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.3 MB (432263750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e359f02de6f43b4c97fa213aa49b8a5967880e030eabf4b96703b69d917c9a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 05 Mar 2024 19:20:30 GMT
RUN Apply image 10.0.20348.2340
# Wed, 27 Mar 2024 22:49:38 GMT
SHELL [cmd /S /C]
# Wed, 27 Mar 2024 22:49:39 GMT
USER ContainerAdministrator
# Wed, 27 Mar 2024 22:49:56 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 27 Mar 2024 22:49:57 GMT
USER ContainerUser
# Wed, 27 Mar 2024 22:49:58 GMT
COPY multi:c5f0fbe231f542d852dcd0a8e1790eb7694672a9238df11d11d4dd7ca117b6a8 in C:\Windows\System32\ 
# Wed, 27 Mar 2024 22:49:59 GMT
ENV MONGO_VERSION=5.0.26
# Wed, 27 Mar 2024 22:50:15 GMT
COPY dir:c5a2113c049daa407c2563884632bc242bc44a6af608518dbd20ed2fd2c8f561 in C:\mongodb 
# Wed, 27 Mar 2024 22:50:26 GMT
RUN mongo --version && mongod --version
# Wed, 27 Mar 2024 22:50:27 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 27 Mar 2024 22:50:27 GMT
EXPOSE 27017
# Wed, 27 Mar 2024 22:50:28 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:94ec3b200bababb5c0b6605ad82c23779d8f918fbfe1ef5d1cf51be6f12fa749`  
		Last Modified: Tue, 12 Mar 2024 19:42:37 GMT  
		Size: 120.7 MB (120702694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae4b4bb1d1b8fad9c2cf9197c385fb729d726d0ee955322d06c37a6537ed82e4`  
		Last Modified: Wed, 27 Mar 2024 22:50:34 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b188b7110314e25742704d0cc85239724b49c7fd5123566984a10b1f0f19f3ca`  
		Last Modified: Wed, 27 Mar 2024 22:50:34 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fa3155f576b54d07c39a31a2372ead8ba25b49a7883126e6f2ba748b9cc2f86`  
		Last Modified: Wed, 27 Mar 2024 22:50:32 GMT  
		Size: 72.5 KB (72489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a11bfe1cd1791f083527ac89b418a84a6d980501523933d8be2cfd4a91d469`  
		Last Modified: Wed, 27 Mar 2024 22:50:33 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf19754273f6f11f7c79795a624c1ff72c5a406c860a2fbc4d7e956ecb029cf`  
		Last Modified: Wed, 27 Mar 2024 22:50:32 GMT  
		Size: 267.4 KB (267448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce2ba029ddcc7482eedb02c30670168e0d27b69be9de2e276c7203f66574c59`  
		Last Modified: Wed, 27 Mar 2024 22:50:32 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dfa588030b223df9beaaf9b14b127d140a735e1ee1ee48ecbb46fd75dbd478`  
		Last Modified: Wed, 27 Mar 2024 22:51:01 GMT  
		Size: 311.1 MB (311135484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958fac87a2a7d2fec0312a51e9f0dd646f1c15b11d950309d0433a999063bb8b`  
		Last Modified: Wed, 27 Mar 2024 22:50:31 GMT  
		Size: 78.4 KB (78358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec4f06ff17eeb990ef3fec46b81a5c5c91430379ed7ae1651dbb00c221125c7`  
		Last Modified: Wed, 27 Mar 2024 22:50:31 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee74f0cc1bda42525ed287a90dd3f44ba0419e4a54d8fb2c76fa7b2846184ec`  
		Last Modified: Wed, 27 Mar 2024 22:50:31 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e799cd97db464349b9e049dc3b31529b6ca3aa3100e337adee4c5fd3c0939189`  
		Last Modified: Wed, 27 Mar 2024 22:50:31 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-nanoserver` - windows version 10.0.17763.5576; amd64

```console
$ docker pull mongo@sha256:dec5b34b706cea92fdf90f771293471dca8c17037c7389027630abc746459d4d
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.5 MB (417479248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc638f18356da2a3057b16066d3454289a72ec0a30fe0d5e523883efdf3aa8df`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 27 Mar 2024 22:49:43 GMT
SHELL [cmd /S /C]
# Wed, 27 Mar 2024 22:49:43 GMT
USER ContainerAdministrator
# Wed, 27 Mar 2024 22:49:52 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 27 Mar 2024 22:49:53 GMT
USER ContainerUser
# Wed, 27 Mar 2024 22:49:55 GMT
COPY multi:c5f0fbe231f542d852dcd0a8e1790eb7694672a9238df11d11d4dd7ca117b6a8 in C:\Windows\System32\ 
# Wed, 27 Mar 2024 22:49:55 GMT
ENV MONGO_VERSION=5.0.26
# Wed, 27 Mar 2024 22:50:16 GMT
COPY dir:c5a2113c049daa407c2563884632bc242bc44a6af608518dbd20ed2fd2c8f561 in C:\mongodb 
# Wed, 27 Mar 2024 22:50:29 GMT
RUN mongo --version && mongod --version
# Wed, 27 Mar 2024 22:50:30 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 27 Mar 2024 22:50:31 GMT
EXPOSE 27017
# Wed, 27 Mar 2024 22:50:31 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79065c5095b72b6f80d24b19792625e24772ee7c15d4d6958e295d52c4f9be2c`  
		Last Modified: Wed, 27 Mar 2024 22:50:37 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab41f44ff599539f55d57106158ae30845a717008e9a13800c192f8792a6c45a`  
		Last Modified: Wed, 27 Mar 2024 22:50:36 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb1d4a63802ddff27560369ed28e37311f0e9e683033a06e1c094e4090c3f3d`  
		Last Modified: Wed, 27 Mar 2024 22:50:36 GMT  
		Size: 66.3 KB (66325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63c14a6a01da12dc78857808974fb39e5a03250f88308755461eb94d99baa5d`  
		Last Modified: Wed, 27 Mar 2024 22:50:35 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d918ab68c1c01d645e67a1c5f701d243946846d8ad6c49596bdedfbb39c5680`  
		Last Modified: Wed, 27 Mar 2024 22:50:35 GMT  
		Size: 267.4 KB (267423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2558eab61220cbe8a314f5bd6556af22521f27eced4a55c4b70e6ca5c86f9a3`  
		Last Modified: Wed, 27 Mar 2024 22:50:35 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9fe8a3bd6ce80011252bb0f627a70ba54f3b44c63521a145007e43c182cb735`  
		Last Modified: Wed, 27 Mar 2024 22:51:05 GMT  
		Size: 311.1 MB (311135520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f98a850158f3d09ef4a14e997e8cde979db3d801b37500948f09464273ffd604`  
		Last Modified: Wed, 27 Mar 2024 22:50:34 GMT  
		Size: 1.4 MB (1382631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72907c110e2ead97d463621884d337042a056fc6535aeccf259c13d68efb0ac6`  
		Last Modified: Wed, 27 Mar 2024 22:50:34 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097fdc74b727ac468742eb1e9cd1b668be9ebc9e14b5c43eba14948aea710c5b`  
		Last Modified: Wed, 27 Mar 2024 22:50:34 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5467cca57005020c31ec1c32f3cdf8887f9ddd358023f25dd070c3f3def95c47`  
		Last Modified: Wed, 27 Mar 2024 22:50:34 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
