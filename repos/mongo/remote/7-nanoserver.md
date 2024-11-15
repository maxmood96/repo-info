## `mongo:7-nanoserver`

```console
$ docker pull mongo@sha256:da0aca320d73dfded021ff98c56c44f1db1983ac607d60b386da8a5cdf2e40ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `mongo:7-nanoserver` - windows version 10.0.20348.2849; amd64

```console
$ docker pull mongo@sha256:5e17aca1fe9ad007144039eec7f0c3316f2f35daa138497de37a09661fe7000e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **731.4 MB (731399713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d311f294508709da8bf1edad72ba72f972f36c23c7502e5043736daf630861`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 02 Nov 2024 23:34:35 GMT
RUN Apply image 10.0.20348.2849
# Thu, 14 Nov 2024 21:22:17 GMT
SHELL [cmd /S /C]
# Thu, 14 Nov 2024 21:22:18 GMT
USER ContainerAdministrator
# Thu, 14 Nov 2024 21:22:21 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 14 Nov 2024 21:22:22 GMT
USER ContainerUser
# Thu, 14 Nov 2024 21:22:24 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Thu, 14 Nov 2024 21:22:24 GMT
ENV MONGO_VERSION=7.0.15
# Thu, 14 Nov 2024 21:22:43 GMT
COPY dir:420a97257b8f41b5187b8c509722525c37efef8c1a1591fc20aa57d257fef5d8 in C:\mongodb 
# Thu, 14 Nov 2024 21:23:02 GMT
RUN mongod --version
# Thu, 14 Nov 2024 21:23:03 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 14 Nov 2024 21:23:04 GMT
EXPOSE 27017
# Thu, 14 Nov 2024 21:23:05 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:815d6b7f925aef8327c34c34073ae54cc1c82120f1058682eac4c8c14ca21c70`  
		Last Modified: Tue, 12 Nov 2024 22:44:32 GMT  
		Size: 120.6 MB (120604951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ba30c0fa58985266375e1770c7b466080f6681611a2119b18de91191c7f064`  
		Last Modified: Thu, 14 Nov 2024 21:23:09 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4acbf45343e86c086f6910e99f445842ff59ba2a358f51c861ef146d8bf42219`  
		Last Modified: Thu, 14 Nov 2024 21:23:09 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2454bd08ee3959ece2ec23f5029b4b8ccf96c0cd5b2742fc37bf4cad8acb79`  
		Last Modified: Thu, 14 Nov 2024 21:23:08 GMT  
		Size: 76.4 KB (76447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d163a00f544caaa1758ad3a9d1fffcdef69274a62625c33a921716d76aeaee`  
		Last Modified: Thu, 14 Nov 2024 21:23:08 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afea89ff9fb2a936bbc67f3612439e0780045854db32bd52a5cc8e5cb51328f7`  
		Last Modified: Thu, 14 Nov 2024 21:23:09 GMT  
		Size: 275.1 KB (275150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83413be95c54b91ab42269237d685562640b6e89b4182e6294fc525dc5d9856`  
		Last Modified: Thu, 14 Nov 2024 21:23:08 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04caebcd0649ce0ef82163f54f31b3113ef603e4c24debcd42d0485342cf14d0`  
		Last Modified: Thu, 14 Nov 2024 21:23:56 GMT  
		Size: 610.3 MB (610337550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0340f6daa041af39b82c13bea3156d97ab78a3c5e2cece68ed4ca55ac6c20f52`  
		Last Modified: Thu, 14 Nov 2024 21:23:07 GMT  
		Size: 98.4 KB (98370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4aaede47c1df29d5023e716b16fe4bddf452c8f781d35ceedb7d97fc42805b8`  
		Last Modified: Thu, 14 Nov 2024 21:23:07 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b76ee1b6d6817a2bbb3c56b351875a88d2d357275d3d00875a6dba2677c8050`  
		Last Modified: Thu, 14 Nov 2024 21:23:07 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb286e77d12096755479323c8c9d87772d2985b418b6cc542a1ce041eafa1e3`  
		Last Modified: Thu, 14 Nov 2024 21:23:07 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-nanoserver` - windows version 10.0.17763.6532; amd64

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
