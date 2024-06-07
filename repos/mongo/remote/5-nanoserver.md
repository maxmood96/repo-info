## `mongo:5-nanoserver`

```console
$ docker pull mongo@sha256:012f301f956d99925d4f840cb6f5629b2c81f4dc50e46e12234f3da99abd201b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `mongo:5-nanoserver` - windows version 10.0.20348.2461; amd64

```console
$ docker pull mongo@sha256:5be823c8d06beb579db98e861915805f5ac06544a38b6e80f7a5dd06dea217cd
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.3 MB (432336092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71964523211c9d724ff76cca23c173eeaaafa7c504a9d43be4303b3b4a3899f5`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 10 May 2024 20:16:48 GMT
RUN Apply image 10.0.20348.2461
# Fri, 07 Jun 2024 01:57:28 GMT
SHELL [cmd /S /C]
# Fri, 07 Jun 2024 01:57:29 GMT
USER ContainerAdministrator
# Fri, 07 Jun 2024 01:57:57 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Fri, 07 Jun 2024 01:57:57 GMT
USER ContainerUser
# Fri, 07 Jun 2024 01:57:59 GMT
COPY multi:c5f0fbe231f542d852dcd0a8e1790eb7694672a9238df11d11d4dd7ca117b6a8 in C:\Windows\System32\ 
# Fri, 07 Jun 2024 01:58:00 GMT
ENV MONGO_VERSION=5.0.27
# Fri, 07 Jun 2024 01:58:14 GMT
COPY dir:a6cc57be35b0b4e87dfd208aad2e6306c874b8418531c7b4d2f073d45bf72812 in C:\mongodb 
# Fri, 07 Jun 2024 01:58:25 GMT
RUN mongo --version && mongod --version
# Fri, 07 Jun 2024 01:58:26 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 07 Jun 2024 01:58:26 GMT
EXPOSE 27017
# Fri, 07 Jun 2024 01:58:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:90b3a5622f8d62905d0a3029df4f91b934558ad375bef25c596214df31acac88`  
		Last Modified: Tue, 14 May 2024 17:22:15 GMT  
		Size: 120.4 MB (120425316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969b3e568885a70369d698a357f1e7b7a04fe001c4dafc989c0d2884b1797c4f`  
		Last Modified: Fri, 07 Jun 2024 01:58:31 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db82f224261f78a61ff3ca0c7410d6040f1ec194fafee5dbfc926490fb45544a`  
		Last Modified: Fri, 07 Jun 2024 01:58:31 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2734c02de86d4d997fa713a3b313f2bafde2b874227f4ff7a230a630145da15e`  
		Last Modified: Fri, 07 Jun 2024 01:58:31 GMT  
		Size: 87.3 KB (87304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a499f28049f948591fb3452a05b7f3fbe689e704920e135f215bc21a98eb26`  
		Last Modified: Fri, 07 Jun 2024 01:58:30 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a0b8dfa8f4723de37843638e7862c7777a2a8f5fecf971b3f4b23f536de8a6`  
		Last Modified: Fri, 07 Jun 2024 01:58:30 GMT  
		Size: 267.4 KB (267450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3092c4a4ac3f3f94c321a6eb7bae0ab1d5241ca2bdc8524c3c5b5db68e5cea4`  
		Last Modified: Fri, 07 Jun 2024 01:58:30 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3405dcdcc2a1a01c004557ab602bd535626c1193c388179530baaba758a1a30d`  
		Last Modified: Fri, 07 Jun 2024 01:58:59 GMT  
		Size: 311.5 MB (311452645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32288af22894b796d25127390d5d27f98780ea14d8fa4060fcb10a8edc4ffdfa`  
		Last Modified: Fri, 07 Jun 2024 01:58:29 GMT  
		Size: 96.1 KB (96090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9fabb68bd2ea689ab3894a6e6b23201b9e1cac3d3afd92c8379e95f3f0aa27c`  
		Last Modified: Fri, 07 Jun 2024 01:58:29 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a30b98d51557c2762302e59e735549c3876f14a8bcd99cbd2067d5fc5b2471`  
		Last Modified: Fri, 07 Jun 2024 01:58:30 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e00bfe54d250dbfb7cb07d4c0c3bd9b3acc33958a30d40c65dc5126e86599d`  
		Last Modified: Fri, 07 Jun 2024 01:58:29 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-nanoserver` - windows version 10.0.17763.5820; amd64

```console
$ docker pull mongo@sha256:834246cbc53286d3351b27d2236197d4887787bc2798d4bac737581e4ec9112a
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **467.9 MB (467934376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48d357732271906aef04a92762a3b4f5edc50af58d42170f926462e4136fcae2`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 10 May 2024 20:21:42 GMT
RUN Apply image 10.0.17763.5820
# Fri, 07 Jun 2024 01:56:27 GMT
SHELL [cmd /S /C]
# Fri, 07 Jun 2024 01:56:28 GMT
USER ContainerAdministrator
# Fri, 07 Jun 2024 01:56:39 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Fri, 07 Jun 2024 01:56:39 GMT
USER ContainerUser
# Fri, 07 Jun 2024 01:56:41 GMT
COPY multi:c5f0fbe231f542d852dcd0a8e1790eb7694672a9238df11d11d4dd7ca117b6a8 in C:\Windows\System32\ 
# Fri, 07 Jun 2024 01:56:42 GMT
ENV MONGO_VERSION=5.0.27
# Fri, 07 Jun 2024 01:56:59 GMT
COPY dir:a6cc57be35b0b4e87dfd208aad2e6306c874b8418531c7b4d2f073d45bf72812 in C:\mongodb 
# Fri, 07 Jun 2024 01:57:15 GMT
RUN mongo --version && mongod --version
# Fri, 07 Jun 2024 01:57:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 07 Jun 2024 01:57:17 GMT
EXPOSE 27017
# Fri, 07 Jun 2024 01:57:17 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:9c038b4bf25cd1f54740808f4833a1b0a5374e056c34a484aa49bc28455a30df`  
		Last Modified: Tue, 14 May 2024 20:05:50 GMT  
		Size: 154.9 MB (154941366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884dd7241c4a14a8a7b01feb31a505ff2aea975ee817e3f13da1c5a5438fc56e`  
		Last Modified: Fri, 07 Jun 2024 01:57:22 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0e6f526124d6fb225c6065faeb2a0586a5954419ea4c18e1cd15b35cb54ac4`  
		Last Modified: Fri, 07 Jun 2024 01:57:22 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc595ec4ad7482ef09a2347534dffe3ebfef8b3e3dcc658c931569d81bcdcc3`  
		Last Modified: Fri, 07 Jun 2024 01:57:21 GMT  
		Size: 67.4 KB (67427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4212cb8c3082f4089546713ed5a306cc7d2d0b8bb05325279d9bcd0548404fe4`  
		Last Modified: Fri, 07 Jun 2024 01:57:21 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f72c656a8b76bddadc807ab26525c055a85077051b4fedf629bbca8cd32af82`  
		Last Modified: Fri, 07 Jun 2024 01:57:21 GMT  
		Size: 267.4 KB (267444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b4955ee50352a731dd8ac22522d47809c666459e56d6ce6ed4881f856b81b9e`  
		Last Modified: Fri, 07 Jun 2024 01:57:21 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a349444331babfa8e6adfbb334b032849643857b35041e80f1fb1a90a9c421ca`  
		Last Modified: Fri, 07 Jun 2024 01:57:51 GMT  
		Size: 311.5 MB (311452676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083806f191e03350f187dfc95599b47c2ce9fa507a6204731a62eaa892051346`  
		Last Modified: Fri, 07 Jun 2024 01:57:20 GMT  
		Size: 1.2 MB (1198203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c561e82a4eb4bc680017ad581aab4c8c3d637a496fd4a35f010ac23b7392daae`  
		Last Modified: Fri, 07 Jun 2024 01:57:20 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1335d51b1134c7fb83edfa1770652190819c665a1c99e095504ae6354b9c5333`  
		Last Modified: Fri, 07 Jun 2024 01:57:20 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eb614935551ab82beb5434c1ecbc92150fa47df5da5a10f082f5f1c1aaadc50`  
		Last Modified: Fri, 07 Jun 2024 01:57:20 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
