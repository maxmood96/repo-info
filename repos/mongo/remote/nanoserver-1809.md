## `mongo:nanoserver-1809`

```console
$ docker pull mongo@sha256:68ce9f1041a0ac367722de60739d2d9f6c4a72b5879fa1754f2ba9114ba3c75f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4645; amd64

### `mongo:nanoserver-1809` - windows version 10.0.17763.4645; amd64

```console
$ docker pull mongo@sha256:aa323317ff656b97b550d12f629ffb870f9e6a60f8bb917651d953b953beb896
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **621.3 MB (621314567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccbebaba2da069c31ba63c995fa9fa52fc41405313b8cddb9ff0889d26893d4e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 07 Jul 2023 07:42:59 GMT
RUN Apply image 10.0.17763.4645
# Thu, 13 Jul 2023 20:41:18 GMT
SHELL [cmd /S /C]
# Thu, 13 Jul 2023 22:42:56 GMT
USER ContainerAdministrator
# Thu, 13 Jul 2023 22:43:04 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 13 Jul 2023 22:43:05 GMT
USER ContainerUser
# Thu, 13 Jul 2023 22:43:06 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Fri, 14 Jul 2023 04:17:50 GMT
ENV MONGO_VERSION=6.0.8
# Fri, 14 Jul 2023 04:18:27 GMT
COPY dir:ece1ac4e72523e5445e13262209cd12cb9863d3774981ba252b9a3cd29bf28b9 in C:\mongodb 
# Fri, 14 Jul 2023 04:18:38 GMT
RUN mongod --version
# Fri, 14 Jul 2023 04:18:39 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 14 Jul 2023 04:18:40 GMT
EXPOSE 27017
# Fri, 14 Jul 2023 04:18:41 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:5c5b06ba65934bcf850a1a54ecf4b3da34d3e6d6c8e90dbc897719c3ea377c8a`  
		Last Modified: Tue, 11 Jul 2023 17:31:37 GMT  
		Size: 104.4 MB (104408241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48271163dd58fddb2ff623ae3c53cac64a29148ad84e995c93073602f68793d`  
		Last Modified: Thu, 13 Jul 2023 21:10:35 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25653f1b79488d51860f4c39a7b5cb89dcde67e655debe7f7c2175ac330de2c`  
		Last Modified: Thu, 13 Jul 2023 23:28:43 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9847941203abbe97818feb1f724af0fd19021fcdc2b4bed652803609b6ee4a8`  
		Last Modified: Thu, 13 Jul 2023 23:28:41 GMT  
		Size: 68.8 KB (68839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:257289d6eacacb75cbf84765b6355a008ee35bdf481b5b2b7989bbb19502ddb7`  
		Last Modified: Thu, 13 Jul 2023 23:28:41 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4022eb1ac7f21a3a4d4f640ce85aead9f625653c11bc05eb3929118d0e799544`  
		Last Modified: Thu, 13 Jul 2023 23:28:41 GMT  
		Size: 267.2 KB (267186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e17a653d66ccfa1870304d22198a1100673f7c0e69930a86e97e3c7c02770b0`  
		Last Modified: Fri, 14 Jul 2023 04:42:46 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff31c7349c6ce910d4836610ed683121440b3874abfc6e02fd5fbe4f47b6291`  
		Last Modified: Fri, 14 Jul 2023 04:44:02 GMT  
		Size: 516.5 MB (516482016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d878fab9c8bd28ed453139f5beceb72dfd472365ed5e309f1df4281bf8cb2df8`  
		Last Modified: Fri, 14 Jul 2023 04:42:44 GMT  
		Size: 80.7 KB (80681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b89e0cf044ba736b91e632d854b04b5d5b55e10826015b71966bc8ae7600b5`  
		Last Modified: Fri, 14 Jul 2023 04:42:44 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df0da9d65110646083d85d3b6ec02f1cc88f4fe7ddf177c065f7b007e8429a4`  
		Last Modified: Fri, 14 Jul 2023 04:42:44 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226232f63f504661724d7feeb70940571af37124a03128e58e04e34ee3c00a87`  
		Last Modified: Fri, 14 Jul 2023 04:42:44 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
