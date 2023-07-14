## `mongo:6-nanoserver`

```console
$ docker pull mongo@sha256:f76b74d4789d8f2fab5e634b35d3df7fe4bb0abfaae7e3d8fbbd2353909d3cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1850; amd64
	-	windows version 10.0.17763.4645; amd64

### `mongo:6-nanoserver` - windows version 10.0.20348.1850; amd64

```console
$ docker pull mongo@sha256:b82c3cc1a7064e8a290498679b89c69aab6f94b31d4afefe81e3be08fb268a4e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.0 MB (636955256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0bef61a4a7668ce50543f66fb7c62f597a0efe892be1debc9f307bedf1ebe36`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 07 Jul 2023 21:00:40 GMT
RUN Apply image 10.0.20348.1850
# Thu, 13 Jul 2023 20:38:35 GMT
SHELL [cmd /S /C]
# Thu, 13 Jul 2023 22:41:28 GMT
USER ContainerAdministrator
# Thu, 13 Jul 2023 22:41:38 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 13 Jul 2023 22:41:39 GMT
USER ContainerUser
# Thu, 13 Jul 2023 22:41:40 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Fri, 14 Jul 2023 04:16:46 GMT
ENV MONGO_VERSION=6.0.8
# Fri, 14 Jul 2023 04:17:25 GMT
COPY dir:ece1ac4e72523e5445e13262209cd12cb9863d3774981ba252b9a3cd29bf28b9 in C:\mongodb 
# Fri, 14 Jul 2023 04:17:38 GMT
RUN mongod --version
# Fri, 14 Jul 2023 04:17:39 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 14 Jul 2023 04:17:40 GMT
EXPOSE 27017
# Fri, 14 Jul 2023 04:17:41 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:cc0a26bd90fcc4d863317c36d7ffec77a0a82a905697204d4dcbc76ec13b3920`  
		Last Modified: Tue, 11 Jul 2023 20:10:45 GMT  
		Size: 120.1 MB (120056465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262f95c9ffc2400b306c39bdd21ab1ee5e02c305fa1895921355e39b04ef5049`  
		Last Modified: Thu, 13 Jul 2023 21:09:57 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c68dafb672cd72b022af598465e06fd23042d9e29348ccc200530e5b35d9bdf`  
		Last Modified: Thu, 13 Jul 2023 23:27:03 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1171b244f6f6515a32b709bf3ce287a50845db3a64ddc64026d75947c2af63`  
		Last Modified: Thu, 13 Jul 2023 23:27:01 GMT  
		Size: 80.2 KB (80237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943c2ea6e887132d6348c7c470e1eb8c8f31d8de00201b789ae3683c1d616638`  
		Last Modified: Thu, 13 Jul 2023 23:27:00 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4f862bd8d3921ac069f3d77465c09e893240d2097dcf9f298858f17bc60ad4`  
		Last Modified: Thu, 13 Jul 2023 23:27:01 GMT  
		Size: 267.2 KB (267212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce37c93c1e90a37fd970a920a9fb93cb6709b0ab7c426085ebe761f7a2a10e9a`  
		Last Modified: Fri, 14 Jul 2023 04:41:16 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e17236883dcc8590f334e5c6c1ce3e0c5f1fb15edbb2924417a91688a205c5`  
		Last Modified: Fri, 14 Jul 2023 04:42:30 GMT  
		Size: 516.5 MB (516481852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735cd4f9ce74607824303301120762f911153610f047a5580d488d731f9c2c5d`  
		Last Modified: Fri, 14 Jul 2023 04:41:14 GMT  
		Size: 61.8 KB (61844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d580da6b5f4e6f68498009939048d0839e045c6edcb05f760558a5a89b339a`  
		Last Modified: Fri, 14 Jul 2023 04:41:14 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7120bcd8374b8f0336bf315cf08e0eb3cbde5ead5da0944f7c253030403013e7`  
		Last Modified: Fri, 14 Jul 2023 04:41:14 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdc1825a8f563c0f4bb5bb8ff9a145092806f3d0383eaa830c54aff5fb07e60f`  
		Last Modified: Fri, 14 Jul 2023 04:41:14 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:6-nanoserver` - windows version 10.0.17763.4645; amd64

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
