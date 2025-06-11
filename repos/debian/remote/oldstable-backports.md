## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:79b8398a8cca4c46fc6036e6fca7ceb3fe4af548416c1e5d3340c2a16b5adab5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:39e65a963b175b6b95f5d7bc43ebff0e2ff0506183dd87e3a062440fca83e555
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53755005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419e82e67e2cae80c2b0545bda34d8f63726222101306f0fab5ad9bbe05ea7ce`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'oldstable' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:4ee18f5ced79adea7e13b11e73da358acd497842b9198e59e9b8438966057d6f`  
		Last Modified: Tue, 10 Jun 2025 23:24:19 GMT  
		Size: 53.8 MB (53754782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede67acbbee2c69b8d28dc8203610b095ac7529971e48d16739737f312c5d71b`  
		Last Modified: Tue, 10 Jun 2025 23:31:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4e62dfd0693df5d5e979f17e6bffff1500b7d1756d195bf98596b4279822cac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4030155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6432e032c262c417b3f551f6ae08a87e25b46f8e00e159aeb8a0f119784cac`

```dockerfile
```

-	Layers:
	-	`sha256:3667857cbda8ac1d0bd6642740325c36a9c02c5ca4a4b365378ef98b6de93c8a`  
		Last Modified: Wed, 11 Jun 2025 00:25:58 GMT  
		Size: 4.0 MB (4024303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd6ad0f659e827ef7649899fbc2a2f8b186e354035253b10ea3eb910698fafc5`  
		Last Modified: Wed, 11 Jun 2025 00:25:59 GMT  
		Size: 5.9 KB (5852 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:56cf36afa3c7ae9532b1bc4492e7bdabd40686f7fba1ee8ea36a26f8431a3b19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49044180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7d37f6a361290b5e20afcef6c33eed9aceb94ca69c8719ac0eb12a92887c9f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'oldstable' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:792b14bc0dd89bed9371208446f5b38503a0eb4c6c70eb4920ed86331396a6dc`  
		Last Modified: Tue, 10 Jun 2025 22:48:47 GMT  
		Size: 49.0 MB (49043956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71d861fd580b29013c88aeb32a950564edc63686963e264f0b3d25fcb0d6eda`  
		Last Modified: Tue, 10 Jun 2025 23:31:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:75e04874410c35544881fa3e706617fe7614eda826c046cb45526cba7aa58cee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4031769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2b211d759b7d706e61ed455bdd32a16ce7c9c5a70a98a9a89ad5889860eaf8`

```dockerfile
```

-	Layers:
	-	`sha256:2d5d1ad1a5b7ffb35384c56bd57be70b6efb4310a3476cbef73a7249816d772d`  
		Last Modified: Wed, 11 Jun 2025 00:26:04 GMT  
		Size: 4.0 MB (4025865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de70d5126e679f57d1c1c91d4fa588dcc6e26241bce19a04850c5305c67d5799`  
		Last Modified: Wed, 11 Jun 2025 00:26:05 GMT  
		Size: 5.9 KB (5904 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:e3426b0bc2aae73c51a4b38ccb77fff6e05847fb99234ad3048a31085af3aaca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52252527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48741a2360def011a65163ffc758d266670ab1ee136a3f6d18c98f87156fe61f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'oldstable' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:15d602315552e3daf7ab962b144af01fd7f4ad514a6273cc4f5109ce91648596`  
		Last Modified: Tue, 10 Jun 2025 22:49:27 GMT  
		Size: 52.3 MB (52252301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2119444ff364134ef993f276cb3eb6d9394fe9310d9727a25bd20e7419200bea`  
		Last Modified: Tue, 10 Jun 2025 23:31:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c4be89d538d35824dc38d9af9ea33aa6473ffd20bc46778b871ee0b26e9efed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4029804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0c5c27be3d93765a28092e66d27b02aa8218f343fa61d5ff8ffcae0d149354`

```dockerfile
```

-	Layers:
	-	`sha256:ca81aba1e1f852cdfd180200b3f147ae8330db6c38c630f84269248b3c492c33`  
		Last Modified: Wed, 11 Jun 2025 00:26:11 GMT  
		Size: 4.0 MB (4023883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66c648aafa2d788b9eaa37418d0d3e32437c0b14828ba92044fd99d40503a0aa`  
		Last Modified: Wed, 11 Jun 2025 00:26:12 GMT  
		Size: 5.9 KB (5921 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:38a181f559c7f78f55f005ef4c9159eb2d712feb4e2b04fb90c3b8252c8a735d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54690243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081baf1a4ee83ad39d5cae0b17521d630b26d42c734e41b285521f24d135f61a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'oldstable' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e7fc1b41f58652e3e926e74a7d361fe75e0cfbf7d6599c9cbb0c89b4deeb1d6f`  
		Last Modified: Tue, 10 Jun 2025 22:47:41 GMT  
		Size: 54.7 MB (54690018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d3018db3b8a010f2f2ed13ef0b7fc90e6c69c00c9d58afdfb053f944ba8147`  
		Last Modified: Tue, 10 Jun 2025 23:26:23 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:dba6c1e0bcdbbe4eb3466e617fb9ca80a3a2561324ccc6ca581c1e947eabc2bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4026693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:115b658b89675289962b22775767fbb872ffc38f72e64122f7a25884a65649b2`

```dockerfile
```

-	Layers:
	-	`sha256:c6577b816f59c8380adbceeef7ecaf5ee7c9c4ab5a2251133b576461226e05ce`  
		Last Modified: Wed, 11 Jun 2025 00:26:16 GMT  
		Size: 4.0 MB (4020857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bc5442b5f790a19fd2d926790d9c148fe6e1389908c122e55aa6983aa9ecdeb`  
		Last Modified: Wed, 11 Jun 2025 00:26:17 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json
