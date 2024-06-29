## `mongo:nanoserver-1809`

```console
$ docker pull mongo@sha256:086d9272acebdc797ca23b865aaa8e3c37fde1f2798eec4e0d7037dab724c92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `mongo:nanoserver-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull mongo@sha256:c4c2d7743696dd81ed6f9b46f1f94d38f687c38bee017feea248afca76980a7b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **764.3 MB (764306587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc6ab0ad06972437a27eaa5c4ffae2dcc0510b467212c02ecfbbb08123da27d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Sat, 29 Jun 2024 00:50:15 GMT
SHELL [cmd /S /C]
# Sat, 29 Jun 2024 00:50:16 GMT
USER ContainerAdministrator
# Sat, 29 Jun 2024 00:50:24 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Sat, 29 Jun 2024 00:50:25 GMT
USER ContainerUser
# Sat, 29 Jun 2024 00:50:26 GMT
COPY multi:a15cb83b582227fb63ddd0661404eaa1493105c6dda1936a8da7d2c4ac1b40ba in C:\Windows\System32\ 
# Sat, 29 Jun 2024 00:50:27 GMT
ENV MONGO_VERSION=7.0.12
# Sat, 29 Jun 2024 00:51:12 GMT
COPY dir:f0b5fa50aabc110faf03295e6346b9d39d589dd155d9a16877c392688d63cd36 in C:\mongodb 
# Sat, 29 Jun 2024 00:51:23 GMT
RUN mongod --version
# Sat, 29 Jun 2024 00:51:23 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 29 Jun 2024 00:51:24 GMT
EXPOSE 27017
# Sat, 29 Jun 2024 00:51:25 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa3c8a83bbe33f5f65ac0bf36cb51756df0dade98f69387672fc91688eab5cf`  
		Last Modified: Sat, 29 Jun 2024 00:51:29 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9bc8da58f5a2e152a5a9593b353d132a3edc5b3a2dcbdd466576acacb0cf8b`  
		Last Modified: Sat, 29 Jun 2024 00:51:29 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfeb5e6833444e262dca35cf82be138403f68b4389c00b57847786db08f03d5`  
		Last Modified: Sat, 29 Jun 2024 00:51:28 GMT  
		Size: 67.1 KB (67122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd1a39daaf9d14df08c8acd2c690428ec8a3b3567ded9c877198de07fbab70b`  
		Last Modified: Sat, 29 Jun 2024 00:51:28 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1edf268b667f3e5703e13c6b87440952578ecb65a3015eb9f73f984a9a5b9bb`  
		Last Modified: Sat, 29 Jun 2024 00:51:28 GMT  
		Size: 275.2 KB (275167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e70ab4456e3e2fd266459474692fa125572719cd81b42c4d4ef3d58a9a4b8c4`  
		Last Modified: Sat, 29 Jun 2024 00:51:28 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb64b8b302d60633e41d36fac84336923b89900c3a5863f4eb2614726d9b5e4f`  
		Last Modified: Sat, 29 Jun 2024 00:52:16 GMT  
		Size: 607.7 MB (607714865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acbd0bc69d4b7228dd22805394527fc023b9e541c2b7ed01944db4a192b8de61`  
		Last Modified: Sat, 29 Jun 2024 00:51:27 GMT  
		Size: 1.2 MB (1208985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6069cd1851d5017f46f5cb1331b6090c725b7d47d3377f959c390bfffc461fe`  
		Last Modified: Sat, 29 Jun 2024 00:51:27 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8c9aa182bece87139ded3e06aaee431470e683242aa1bbbb5db53b7bd80193`  
		Last Modified: Sat, 29 Jun 2024 00:51:27 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756bad67eb3a5163c0ed796a8c04f69233a1e7e52deda8586b86113d0424f646`  
		Last Modified: Sat, 29 Jun 2024 00:51:27 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
