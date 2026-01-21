## `mongo:nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:12a9da113a4fc6bbc73c4e3c57292b9ea2396e7d04c971369ee99e374e755a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `mongo:nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull mongo@sha256:2117f0f87afc6ec99a5051a6ba72857b3911691db80a025a8be413f619edd631
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **941.4 MB (941371322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee39697089c74f0bf16e348f217c422cff685e81f9137059fcd5a8a9c5202c7d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Tue, 13 Jan 2026 23:36:27 GMT
SHELL [cmd /S /C]
# Tue, 13 Jan 2026 23:36:27 GMT
USER ContainerAdministrator
# Tue, 13 Jan 2026 23:36:29 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Tue, 13 Jan 2026 23:36:30 GMT
USER ContainerUser
# Tue, 13 Jan 2026 23:36:30 GMT
COPY multi:540d6dd70b1e7484f1958dc08b337aeb56cf8a92fe38be4c279dd406990d6935 in C:\Windows\System32\ 
# Tue, 13 Jan 2026 23:36:31 GMT
ENV MONGO_VERSION=8.2.3
# Tue, 13 Jan 2026 23:37:10 GMT
COPY dir:e4a7b73dcd7a2e9245c6f81881a690dd19d71f8235112b80871c1a7931621cbe in C:\mongodb 
# Tue, 13 Jan 2026 23:37:38 GMT
RUN mongod --version
# Tue, 13 Jan 2026 23:37:38 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 13 Jan 2026 23:37:39 GMT
EXPOSE 27017
# Tue, 13 Jan 2026 23:37:39 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:12:21 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f4f3621828e36d1eb188643fcedf11b030c9396334d2f106e6d68db92acd816`  
		Last Modified: Tue, 13 Jan 2026 23:39:05 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6039f686b41ffe6869ade167872640c637482fb300cb84c4b6ef356adce3fddc`  
		Last Modified: Tue, 13 Jan 2026 23:37:46 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec4dcc9859372638101c3ae1bb0272043b537f13270a70adba6c0a98a1b16a88`  
		Last Modified: Tue, 13 Jan 2026 23:37:45 GMT  
		Size: 77.5 KB (77538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a6804c3e686ebb7966222f4e91e115ab749b974c7a1503d18299ee83cfc41d`  
		Last Modified: Tue, 13 Jan 2026 23:39:05 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f3dad23ad562c83386d5baed676d4b9af1419346ad1a40307bf9b3de1973ac`  
		Last Modified: Tue, 13 Jan 2026 23:37:45 GMT  
		Size: 275.2 KB (275199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f323c2c3364ae54b1e68089b19d1766cba920cd17afbc77b1d35b57d9713e63d`  
		Last Modified: Tue, 13 Jan 2026 23:37:45 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be30c7da0d55623fd83f926089d32fba523fa182622ad3ae175eeedd539b212`  
		Last Modified: Tue, 13 Jan 2026 23:41:09 GMT  
		Size: 814.2 MB (814228410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0831285cf6ec1d0c0191f55dd105b933c8e81d8d7311b24576b193d21394dc65`  
		Last Modified: Tue, 13 Jan 2026 23:37:43 GMT  
		Size: 85.9 KB (85861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f751d2f15361b6207416ef7e1817f89a13b7838f30f7d7df533ef6da7251b9a`  
		Last Modified: Tue, 13 Jan 2026 23:37:43 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46572c100b9bfb051267dced25c55e6e2591c78b8962f8ad3289ff4da1471d00`  
		Last Modified: Tue, 13 Jan 2026 23:39:05 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eed69cbf5b2402add91a332d7273b12f8784f9db190c2d2e04986e517ccca54`  
		Last Modified: Tue, 13 Jan 2026 23:37:43 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
