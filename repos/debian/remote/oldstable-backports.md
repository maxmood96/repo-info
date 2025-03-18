## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:6bcad5ceb19cc639a4a9eeb71b15adfaab00a71e931a65fa4f32a59c3619e968
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
$ docker pull debian@sha256:c9e03eeb727b9e20a595ad356b275a634ec991aee214ee5482736196065119b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53741621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c827407f1296b7770024f6004d47ba5ae8634dba85bc0755ef8ea67d461e31c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'oldstable' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1c1bb87b23cc30a6c7d26e68d050c8fc458e6bda092afaf2ee868dc1b489026f`  
		Last Modified: Tue, 25 Feb 2025 01:29:48 GMT  
		Size: 53.7 MB (53741398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1699a25d2fa3bd1d16d94115f3e69fbfae62d18fe3e23cd4c9c0ac4d5ab400d2`  
		Last Modified: Tue, 25 Feb 2025 02:11:51 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:230909b3b7e7fffd0f02a762bb7eeebd7b6d44e02ffa52ab316bbeb14c17a23d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3923371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0ddb482fedee753e1711b3e1c9b4b7da886059ac7252f4d316fb0c60cf1db7`

```dockerfile
```

-	Layers:
	-	`sha256:9128ebd8f8a6198536b5f255e06346db99a393e3ee6e3542da193aea1845456f`  
		Last Modified: Tue, 25 Feb 2025 02:11:52 GMT  
		Size: 3.9 MB (3917518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b5156eb298bce1e69d1203a6843d4f5e1226f864e43cfb35d08e2c696544d65`  
		Last Modified: Tue, 25 Feb 2025 02:11:51 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:895ac53d43613544e12fd7098844785274dc3c3e0540c5f556d64b95b20b5d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49026959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfaa715b18f1802069aedee14859882e8b3e0a57018aa620adedd775db2a659f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'oldstable' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:41b3c0e18c9315651c24575105ca09b81f294c7cf69c17c2f9fe94fc342d706b`  
		Last Modified: Tue, 25 Feb 2025 01:31:40 GMT  
		Size: 49.0 MB (49026736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c283c3391caab77b639b1b82fbf262a4800241a5827e231cd9651fc9ca06eaad`  
		Last Modified: Tue, 25 Feb 2025 02:16:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:d23ee1fa4a52c73f4986c9400cc3c1a8d6c3dfde1b6f835770b74171d978ef9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3924984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423e08ea9aafa234c9dc9609dbe1ae546728b6d80a713d63e2600a4313d46cd4`

```dockerfile
```

-	Layers:
	-	`sha256:5b9c5e141269beecc338b028eee831dfb847283ae108a8bcc2125a974538914b`  
		Last Modified: Tue, 25 Feb 2025 02:16:03 GMT  
		Size: 3.9 MB (3919080 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9c844ff487c6d19edb056c7748707ff2d2bc611cb5690b570c9dd0a7cc8b12a`  
		Last Modified: Tue, 25 Feb 2025 02:16:03 GMT  
		Size: 5.9 KB (5904 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:37460b6c5e9dd7a19d04c2e64f528514ff180302ccc25a03f70f968c7e6e8364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52248867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a9fa503b00e4ebb3e97703029d75f80f3723ac19ef7cced29e880dae8c13085`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'oldstable' '@1740355200'
# Mon, 24 Feb 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:b5ffff8e0cb89d4cfaae5f4ee9fe724788dcda5eda828b8d0ae1bbebdb5e810d`  
		Last Modified: Tue, 25 Feb 2025 01:31:47 GMT  
		Size: 52.2 MB (52248644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3046c40e83a7a973aa4bfaede1960cbceff6ae4e461c55bb8547499cbc32dc`  
		Last Modified: Tue, 25 Feb 2025 11:25:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4836c62173e9a60ef64443666a6729b7394a1b98892dfcbf8f7a70528601a04c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3923019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e73732d5530d3fd5f0a723d48bc8fbf9a181fb7697524c13a95eadfda5f748de`

```dockerfile
```

-	Layers:
	-	`sha256:c9a3639023c4040bd71d502acf592904ddcfcfefcaf5bbe33dd59d36caafcf2b`  
		Last Modified: Tue, 25 Feb 2025 11:25:32 GMT  
		Size: 3.9 MB (3917098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9bbd0ec025315a2821976ed00b0cbee08f11197117b3886abc96cf3ada03ca6`  
		Last Modified: Tue, 25 Feb 2025 11:25:32 GMT  
		Size: 5.9 KB (5921 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:3f7be803d6c1db344f6b5428d7cf43880832d5f3b8f9793ab9e720b836a8ceba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54678841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7f4319262792fbc03abc6d6360e6c0230e84c48bc91489e017a3c37a64ae6bf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Mar 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'oldstable' '@1742169600'
# Mon, 17 Mar 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:ff654f4f86bd5f54c9ea16833c0d64fd810ffbddd628768cae4d932256f0a126`  
		Last Modified: Mon, 17 Mar 2025 22:17:48 GMT  
		Size: 54.7 MB (54678617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e8a58fa780a4d3a2a359bb93840b3a41b677d7f9875ab1afe3e4328e9f4eee`  
		Last Modified: Mon, 17 Mar 2025 23:24:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ae0856f11580c8aac11917d9c159914ce8aa3e5c0b7cda3db9e978ba2c753207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3919861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a19a02bfc14b942e4dc0fb4ecc1751da2d8619a6bc2335a342cd7dc34aa295f`

```dockerfile
```

-	Layers:
	-	`sha256:97d4b1eef6cb277d6d82f07a35884a87ba5944c1edbd5f30c5e156f456cfc62e`  
		Last Modified: Mon, 17 Mar 2025 23:24:57 GMT  
		Size: 3.9 MB (3914025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46d72cef649eb2020f513cc0c6d820f26aafd6f5c8a97b0f94074cf1192a45e1`  
		Last Modified: Mon, 17 Mar 2025 23:24:56 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json
