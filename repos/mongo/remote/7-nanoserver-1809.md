## `mongo:7-nanoserver-1809`

```console
$ docker pull mongo@sha256:9af6e2694b64614ed065ee51c1b0fb4c0a50d1da64a1530c19abc0e482df194a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `mongo:7-nanoserver-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull mongo@sha256:febed7d9cb65119b10eb9a22b6d2e3a8ff6b778d638ef590bf82dec3149fb306
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **766.0 MB (765998575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b26dc11a74a215c3d0bb557262a4ea51b987a665730e93f56bc6fd545ae46c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 01 Nov 2024 11:18:21 GMT
RUN Apply image 10.0.17763.6532
# Thu, 14 Nov 2024 21:11:14 GMT
SHELL [cmd /S /C]
# Thu, 14 Nov 2024 21:11:15 GMT
USER ContainerAdministrator
# Thu, 14 Nov 2024 21:11:17 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 14 Nov 2024 21:11:18 GMT
USER ContainerUser
# Thu, 14 Nov 2024 21:11:19 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Thu, 14 Nov 2024 21:11:19 GMT
ENV MONGO_VERSION=7.0.15
# Thu, 14 Nov 2024 21:11:53 GMT
COPY dir:420a97257b8f41b5187b8c509722525c37efef8c1a1591fc20aa57d257fef5d8 in C:\mongodb 
# Thu, 14 Nov 2024 21:12:04 GMT
RUN mongod --version
# Thu, 14 Nov 2024 21:12:04 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 14 Nov 2024 21:12:05 GMT
EXPOSE 27017
# Thu, 14 Nov 2024 21:12:05 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:b79a100b554b1ee5bf83d129fe624c0ddd7754edeaf1a1364fefbbf2ba3095c1`  
		Last Modified: Tue, 12 Nov 2024 20:49:39 GMT  
		Size: 155.2 MB (155214227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb480ddb2b961c373824fcd3b424da7ff662d52a047d75f94a20384a58b8e9d`  
		Last Modified: Thu, 14 Nov 2024 21:12:13 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776c0013f5f05c5fd3c305844f87f030e08519232eed68dfe9ff3866d78ef6c1`  
		Last Modified: Thu, 14 Nov 2024 21:12:13 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff515af8743bbf893a3c482b4384f67f05b21a938b929d2645aa2f04d595012`  
		Last Modified: Thu, 14 Nov 2024 21:12:11 GMT  
		Size: 73.2 KB (73235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5709201e09f44c175e3f671279f4bef2010965afec1b4ff5e4770b2029237410`  
		Last Modified: Thu, 14 Nov 2024 21:12:11 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116bb7163f1a3168b39bc34d422dac75d995d9a99e2740bdc5905de7470a02c2`  
		Last Modified: Thu, 14 Nov 2024 21:12:11 GMT  
		Size: 275.2 KB (275250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9da3b05c23d56bd6837ec8288407bda0b4fcc2e5dd3b6c017dfb496cee4741`  
		Last Modified: Thu, 14 Nov 2024 21:12:11 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c33fcef401a698e49b78e7595b19ac727cc3f573b603ebf6cc23805ace026e`  
		Last Modified: Thu, 14 Nov 2024 21:12:57 GMT  
		Size: 610.3 MB (610337626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678b6dd9c01d07beaa7a3d749cede58980af6e117c7307d86439adb630d9fe14`  
		Last Modified: Thu, 14 Nov 2024 21:12:09 GMT  
		Size: 90.6 KB (90625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:067b8840ceb48b2d7d9db2a28dad155df70a60a13ef9b653d702bb26a10c758c`  
		Last Modified: Thu, 14 Nov 2024 21:12:09 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23753341f04dfefb2ee6dda0a7173ddf6e895dfc16437e7ff85d8ab42c4fad4`  
		Last Modified: Thu, 14 Nov 2024 21:12:09 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4617cb28ec31e37b7f9cc7adacbf587a365fc6a4c63886fad0dd396f5f3f91`  
		Last Modified: Thu, 14 Nov 2024 21:12:09 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
