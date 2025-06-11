## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:4939eac334ad0636e4a39f509fd83d0ae4202ed93ab1771f30182b6aeea21022
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

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:42767b409e08aefede925540fd05dced7d67d117c9516e3c5e6af0a322780fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53755008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4e798e4400d65df5a9bfe9fee3979687837d164a55ace5b0004f8adfeb1ee6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:72049b7b8f2615e8b5167a09158b78d10a3b79a1ac60ce60cb5528a8c7723090`  
		Last Modified: Tue, 10 Jun 2025 23:24:16 GMT  
		Size: 53.8 MB (53754782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689e3d92809bafbea28040a3692cbd00780642dd3a26aa55be976ea7429c6d2b`  
		Last Modified: Tue, 10 Jun 2025 23:24:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:94121a30180ee1e6c882b3265be7682b982bc5481a85ad0c8aaf6d8b643a2828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4030147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7980efe98586b11c9f5355461e6aad34f77f36cfa5b955ea111f29b0bcd23c42`

```dockerfile
```

-	Layers:
	-	`sha256:f185fc326081221e0442d9713030f2b779cd6eb17194c555a2314be5686bd840`  
		Last Modified: Wed, 11 Jun 2025 00:24:57 GMT  
		Size: 4.0 MB (4024301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1fd1925914d5cd46514ec21e5923bae27be82cb8036b11cece61e3050cf1d52`  
		Last Modified: Wed, 11 Jun 2025 00:24:58 GMT  
		Size: 5.8 KB (5846 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:f77c8b9604d4b722e12cac43ffa87a9dda27577ee922ba0027aa4a1a88b1c33f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49044181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5301e507297fc6cb9a2fbba8773da8f272aad569b8f9442757ec62d5ed207c6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c43258def9bd93af20e1c5bd4e42a71d9db281a9fc468bbb5eb78d7a51c6472a`  
		Last Modified: Tue, 10 Jun 2025 22:47:56 GMT  
		Size: 49.0 MB (49043954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c12bdd4ca6de465c09f65b3d6b35ba2f656501533e8f202e2ac1e68250aa08`  
		Last Modified: Tue, 10 Jun 2025 23:25:28 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:ebcb18552cd1e7bad5ca416be375cd83b4094ced304375959ec2cd808cc84e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4031760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c157084f8d502e9d440117d9e60d9c15c94c2abb399af7317909b1a71070665`

```dockerfile
```

-	Layers:
	-	`sha256:465608f213d50015569a2d7459e5c901dc6562ff628a53d4862ecc9b322084ee`  
		Last Modified: Wed, 11 Jun 2025 00:25:03 GMT  
		Size: 4.0 MB (4025863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5682bcdf7008acd168b57563792d2481288e6a01b809f42994c25c3b7c86ea26`  
		Last Modified: Wed, 11 Jun 2025 00:25:04 GMT  
		Size: 5.9 KB (5897 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:0d6a0aad6a5a536afd63bfbaa62d2a5cc2f32bf709ebe021eebb6f0a5dc83309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52252526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb08bfa909b6dc8b6916c8c89fb469cc549f8d01b240cae0a2aefab65ecee011`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:01b9f05048bbb73f25cf8fdb677f6390611ed20f4945645387ddce6122b5075e`  
		Last Modified: Tue, 10 Jun 2025 22:49:07 GMT  
		Size: 52.3 MB (52252301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b85383dbc7bcda1038d86f0b06555a07e7311c872b05768367c285a8bda3a32`  
		Last Modified: Tue, 10 Jun 2025 23:24:14 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b006db088650b372e49a444488996e4298fea08b529929bd7ff73b04f13277f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4029796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c971972b3f47a270e21f4876f49cdc09d9b4375fd9a8dc04a4677ab5496e3a7e`

```dockerfile
```

-	Layers:
	-	`sha256:d4c145cfabe5f4d1b34e507f36ba9c09ac7b4c8084bf81201da12542ed2d856e`  
		Last Modified: Wed, 11 Jun 2025 00:25:09 GMT  
		Size: 4.0 MB (4023881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56c1b4a3ca7090550157fc50ed5e8168d2d944ebc0ff4941c7e387c8e7ce85db`  
		Last Modified: Wed, 11 Jun 2025 00:25:10 GMT  
		Size: 5.9 KB (5915 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:f0276b278cb9d3ee08494cdee8354e97af6b4e9d4134f785078eba0e19aa23c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54690238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6063ec240da3c41bf38d5cb5b5e8f8653242deea91911a62efbc950c2a0914c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 10 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1749513600'
# Tue, 10 Jun 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:e516fc486459913e83d7e1f35cc45b6e3bed5cabe1eab9f1598665e153a14d6f`  
		Last Modified: Tue, 10 Jun 2025 23:24:19 GMT  
		Size: 54.7 MB (54690012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5144c301fec2775c4d4f45dd22d7f475eea9f2543e9a1f54cebc79b253f98fe4`  
		Last Modified: Tue, 10 Jun 2025 23:32:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:bullseye-backports` - unknown; unknown

```console
$ docker pull debian@sha256:1d332e97488f55dd1a8e71c98a7bb683152452306ccdf4764928dd7283f4e852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4026685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:757fdf4b9a2d551a6552d193dd5adf8c2c440bb89cccb6d930e117a8ace4bd4f`

```dockerfile
```

-	Layers:
	-	`sha256:ebb304e3bfd78be53e21dca2dfca379ccbe5f81520898c8f49f4e0101e343882`  
		Last Modified: Wed, 11 Jun 2025 00:25:15 GMT  
		Size: 4.0 MB (4020855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a11e4572497d7137771bfb222aecde4e47ff2716410bcf3745d1b705a4d81e4a`  
		Last Modified: Wed, 11 Jun 2025 00:25:16 GMT  
		Size: 5.8 KB (5830 bytes)  
		MIME: application/vnd.in-toto+json
