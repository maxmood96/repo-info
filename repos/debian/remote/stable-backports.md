## `debian:stable-backports`

```console
$ docker pull debian@sha256:e0ac680df1539c5a69e42903ad9e6ffbe35a3611894be7df46465ebad83e1266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:stable-backports` - linux; amd64

```console
$ docker pull debian@sha256:03dd3ba268eb2c52a2df551134df93e7b92e3df6038469eb686a28138c797f53
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49560616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9229c4a651dec7b5a397dd31de6ae2416f5aeb739ed4dd2265b3af1d8c546c4f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:52:50 GMT
ADD file:9a7cd535c1ee276f3c39bfa94554d79e4962d0fad6f1b2eccffaa7b101523f16 in / 
# Wed, 10 Apr 2024 01:52:50 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:52:55 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c1f78403d4e5ca02554d454e2f2d22a63008e429384e30bce4c96806aab4b3fb`  
		Last Modified: Wed, 10 Apr 2024 01:58:47 GMT  
		Size: 49.6 MB (49560395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1499fa28f86a7400a179c0f7e2c0d65596445fa8b09748f971916832a3dabef8`  
		Last Modified: Wed, 10 Apr 2024 01:58:56 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:c96d7f390903539483bd83005ffc0262f26186a43f5a1e3757b795896e8e056c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47316353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f579ea03f209a82d596c56aeff7b79fc8a5f31345e74728b3b35b23af95a9c20`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:50:59 GMT
ADD file:eeb3d2dbde88edda12fa2e5c064dd853afe929473e6193b643adf66925c634e2 in / 
# Wed, 10 Apr 2024 00:50:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 00:51:05 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:dcffe465e81a44cf7e6977394dcdbb9225df031cff86cbce733b180c4769066c`  
		Last Modified: Wed, 10 Apr 2024 00:57:03 GMT  
		Size: 47.3 MB (47316129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8dbe463be9ab4d9d9947b6c04a2bb197b73d212c7b237bd133a53f450602a2`  
		Last Modified: Wed, 10 Apr 2024 00:57:12 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:92c394c81017e5f7e7a9016ee44a8ef76288855cf2171738c26c43f88db95a9c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45158826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ac98c0fc503ffbc4163391d88077a121c2a7d121783a6ce2c118078898cb180`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:00:57 GMT
ADD file:f5a0b03302f0a5e8c1ec4eedfce83103c010d0ca252de78c1f694f35ddf10675 in / 
# Wed, 10 Apr 2024 01:00:58 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:01:03 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a5fcd6ce54c8e754be55f1c029cf0fd86edf219779922f7311173a5acb4541c1`  
		Last Modified: Wed, 10 Apr 2024 01:08:05 GMT  
		Size: 45.2 MB (45158604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfa161395ff1514b2b1f1dbd038f04da32dcf06801825abc325cece605f10aa3`  
		Last Modified: Wed, 10 Apr 2024 01:08:14 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:3b706b7aea42de94e9c379f15d4b0fda2e7d8480c15258d3d1032d84bac65abb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49596484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:661b9a307693b8d6d9a69a10441364e7f2c738aacdbc96f94c4ad15593f9d584`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:41:44 GMT
ADD file:dca6811bc1b65e1fe54cbd2ebad57417e39ba29bf53af1fe0a5f64ed79912342 in / 
# Wed, 10 Apr 2024 00:41:44 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 00:41:47 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:95cba99d2ecd28260b5e8fd2d88c68996d94c735378ad3e804351a03f15ee7f0`  
		Last Modified: Wed, 10 Apr 2024 00:47:14 GMT  
		Size: 49.6 MB (49596262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05785b146fa382f8df3fd693de4cfa93e29b12b2e26095f7dfe1fa3f99edd00`  
		Last Modified: Wed, 10 Apr 2024 00:47:23 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; 386

```console
$ docker pull debian@sha256:578caa46015198c6a06b3cb8356ca55c991b4c86123b24106bc3ab880c6e89b8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50587426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9958792e95d71b5e32a71648cf987fda470b3047bdc5a8cfe257e4683c1a70d7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:59:15 GMT
ADD file:dc5dde50600aeacbaacfd9026fc58084f6d000773ea0bf0240952459e8c5254b in / 
# Wed, 10 Apr 2024 00:59:15 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 00:59:18 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:85a67818578c6d5ca8aa44d72e8d6d6ad400ec243b5907874661dc497f298dba`  
		Last Modified: Wed, 10 Apr 2024 01:05:55 GMT  
		Size: 50.6 MB (50587204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423183fbf2269d62b95a98da6cd886c376e7e57a01526fe84255595d6e6a47ef`  
		Last Modified: Wed, 10 Apr 2024 01:06:04 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:3a008e722d08dcf5ffe63a5d23b1c5d7774888eee276a79ba85b35e707486ee8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49567476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1557bac1383476cc2172a4d2122a09af2d54808843c1669c9e80e1005ef5d5e0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:14:40 GMT
ADD file:965cdf36b66d7d3e23be4b96b907331aa9fc79c3af011f3f83cd68429ff4767a in / 
# Wed, 10 Apr 2024 01:14:45 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:14:57 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0a4e1cffe6e49645b1aada794cc049caa21111a6867fa893cb64a625295d709d`  
		Last Modified: Wed, 10 Apr 2024 01:26:35 GMT  
		Size: 49.6 MB (49567252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2684858600315653d184a5f58f1e6c4c5a6e5cf183bf85212a23bcd299a60c77`  
		Last Modified: Wed, 10 Apr 2024 01:26:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:b559c07855c1853e649b9de6e2471de1cd7454e4f58423764ac30c70a2bfbfc9
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53562696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:088a2756e43a3854fdb475fd41197bbc7b42f82d29fb85e068156e3275b7e0ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:28:02 GMT
ADD file:89bddebee26a2d6266cfe28d8aad8553d9832c80f30da08f260cfc41781a38a6 in / 
# Wed, 10 Apr 2024 01:28:04 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:28:10 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cc8b4ce6aea8f4c65324996b3a566bb241396abe620d31bad8347930d5196801`  
		Last Modified: Wed, 10 Apr 2024 01:33:35 GMT  
		Size: 53.6 MB (53562473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370afba2f9289c35001470a21dea37e521484aa620cfb202abe4dfecd0c6ba73`  
		Last Modified: Wed, 10 Apr 2024 01:33:44 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stable-backports` - linux; s390x

```console
$ docker pull debian@sha256:4ff46637cd69c0721b4fc99c3e5155faa19b6543c92e6e8efa8d0dbdc6a797d4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47922931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:950dd339917c7515189b5729648025684c279103279ed15f4430207112f6c306`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:29:15 GMT
ADD file:2dd6e7692b9152446536ceb60e09cfa11b5df0394fbde1a3b761d986ce347787 in / 
# Wed, 10 Apr 2024 01:29:20 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 01:30:44 GMT
RUN echo 'deb http://deb.debian.org/debian stable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:22f006b0457239e17302598eb6381c3a0e259a251d47cfd712eaeeee1900e019`  
		Last Modified: Wed, 10 Apr 2024 01:50:02 GMT  
		Size: 47.9 MB (47922706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b70a9bfeb9c551c49df2baa9e25c52f7a07948a011d598806dc219ba2fa4008`  
		Last Modified: Wed, 10 Apr 2024 01:50:08 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
