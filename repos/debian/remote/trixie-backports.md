## `debian:trixie-backports`

```console
$ docker pull debian@sha256:1e45698b8553ad4b2e074f59f14c579194aa9b003f5c7b4a3d8704087954909b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `debian:trixie-backports` - linux; amd64

```console
$ docker pull debian@sha256:a2d7bb6aeedbbec273667be43c64ac5ee45e3b1770fcced06bad2f457fd033a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49278504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbea855352e9b90e0da8a59f0b8bd13236785d14852ef47c122163407437396`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba877eb7acc22b5aff4c813b9c6e42f4c068b58ee3feb5e0cdbabca966840ce`  
		Last Modified: Tue, 12 Aug 2025 21:10:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0c69abf9b3ea57211efc1c815368c7aa3b5d73786667a1c6b8bc8b9c44bed13f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3174316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2303fa75878e4cb2ed1f9ac69c92faf540e8a63cd547cca9027614900e56471`

```dockerfile
```

-	Layers:
	-	`sha256:fd35a287a0d1c7297921863787910b9f644fe97f4b9c23355ea3002f4945a666`  
		Last Modified: Tue, 12 Aug 2025 21:29:42 GMT  
		Size: 3.2 MB (3168489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9365863b38b13025d932c16ba22f5355f3492d980a6e685b22318d105eb04bb`  
		Last Modified: Tue, 12 Aug 2025 21:29:43 GMT  
		Size: 5.8 KB (5827 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:c76161dd8b177de723e90ae23fda1ed80cbf923cd44902bf13e579d83e72bca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47442648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eca53a44788cf72dbbdd40cbee55ebecffb9d2b2b871b6da997b4a5831acf047`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:49b34b9ef926ce7ed8f011fe61446ff5495accfded522a04a8414730759ac407`  
		Last Modified: Tue, 12 Aug 2025 20:49:02 GMT  
		Size: 47.4 MB (47442425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4948e1d7562ad77f5fcd0ca320bbce5528af7abbd3865bb1ada6e330ee09e38d`  
		Last Modified: Tue, 12 Aug 2025 21:11:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:4673e9e1e7be1da3afb8b29be9d27c3e4cf5f5176cb97ad0bbf760623d6f2a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5d0bd3d4a7105b76cf06c47ebdc9c728174cb48f55f685a6604ec2dd005b9b`

```dockerfile
```

-	Layers:
	-	`sha256:37219700734470072ebd989b353df26705941cfe71b421942d78ca4dbc979fac`  
		Last Modified: Tue, 12 Aug 2025 21:29:48 GMT  
		Size: 3.2 MB (3171426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6429fd21acd0cfc9d1ed395963cea672cb174d8f4ee57656728005689fcdaf7b`  
		Last Modified: Tue, 12 Aug 2025 21:29:48 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:4d16e3d7ec032dd404f92da15ac77435ba4053246e9ff1ae57563daaa4990dab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45712855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2949d30e0d23dd2c49c0a6c62287f9fde9442ab38dcac3b9c821f51d649f1645`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:58382c67f397ebdc005890f56dc436f7798aeeee2e0d603ba02e89d6243c138b`  
		Last Modified: Tue, 12 Aug 2025 20:51:59 GMT  
		Size: 45.7 MB (45712631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f50e5b3071e26a886f1e92a549e7962a45a7df9350915e635d9403b207d8e15`  
		Last Modified: Tue, 12 Aug 2025 21:11:41 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:658c302f9e545a2476556e2410fb90cad4e7a93e0937eaca65a00716ff8d59bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a39275ee8a2d09cdfbf6413ec003324574505f87cbed9410485bfe7b06b6dca`

```dockerfile
```

-	Layers:
	-	`sha256:109825c64dd213a6861c5c705bde67e5aae113bc5d9a8d0ca84cd143a31cd314`  
		Last Modified: Tue, 12 Aug 2025 21:29:53 GMT  
		Size: 3.2 MB (3169863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07ecb99353883d373cf9d3675cdefb738ae0bded163d64e360fd4c8c567849b8`  
		Last Modified: Tue, 12 Aug 2025 21:29:54 GMT  
		Size: 5.9 KB (5879 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:59c8e3971306d05597759fb5e87fe5387cfb1f0fe866f26e320123a78784484d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49641825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d0f5a4cb42c13b0b0192621532d762a6969d42020c53c32b693b6b46a1b6f3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5c1a14c6c0903a472ce0454fbf5a543696b4e5dc20c04dade76970c365f97d`  
		Last Modified: Wed, 13 Aug 2025 01:51:31 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e9d538c2689f96797307ebc67052bf4f4481e14f0469fa629b53f3bb0df7224a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc68c01a22a6f20a7ffe6c0f183e504013a364ea47de5eaeecc252c3bfa820d`

```dockerfile
```

-	Layers:
	-	`sha256:0d8018a62741eb0d01d2d8df7e391c8cec3f70639775c0b7b05ad8aaf8904f5a`  
		Last Modified: Wed, 13 Aug 2025 03:25:52 GMT  
		Size: 3.2 MB (3169970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd521f6a4da3dd82f39dc064c6c9b4a1da2ed4476f57789770ed8366757f6d8a`  
		Last Modified: Wed, 13 Aug 2025 03:25:53 GMT  
		Size: 5.9 KB (5895 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; 386

```console
$ docker pull debian@sha256:43cae0cc561abc8092e5c9785a9c14810f3bb4207f2ea9ee7a02667388f25716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50794481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e48a0a22c0fec456c8068f58412d778fdb922384742b27f40a49795e68497c7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:3d9f8c7ff550056ffe2cca57d7110ae0306e74220a891574e97ddc10ba49823d`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 50.8 MB (50794258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea299110d9e91d139cb013fd8ede401750536818406c99696f9b751ee7288b6`  
		Last Modified: Tue, 12 Aug 2025 21:10:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:c131eb9b73488d6bfbcc2dc0efa5490373a47d86bc613837b6ee635eeb6650ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3171502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a772f7cd13fc9d29f32503c164d124baa644b373e10b8ecd73392965964db9f`

```dockerfile
```

-	Layers:
	-	`sha256:d37ca75ce1e0238d9837e98eee77b314ddbf163e220876d0aac418a87cd40ea5`  
		Last Modified: Tue, 12 Aug 2025 21:30:04 GMT  
		Size: 3.2 MB (3165692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2282144f2b3f21436229a76b02dd2593f32718c37ab48b1c64aa8b82aeb6733f`  
		Last Modified: Tue, 12 Aug 2025 21:30:04 GMT  
		Size: 5.8 KB (5810 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:b8b0f809fa84ffd80e4361c6835b5d3882034c2643eaf9b7d73c51db938133a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53103609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1349b9e815da62816531915ce9e71df2f39d8cad37d48c6f62538e0dd30264`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f27474d15761c4d7a825a5a2444f990c74bfddf084dbb7553dcb75b7589bf0`  
		Last Modified: Wed, 13 Aug 2025 05:16:37 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:a31db19e3b1d4d81059cbcf6fa11ce328a7a5bf1556b0ae077604da6b3a970a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3177853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6601434c79aeda3950b98510ccc22b46729c2ab2fa832d395bf87a3706691dc9`

```dockerfile
```

-	Layers:
	-	`sha256:14a47540bcc3c7de4abdb9986d371923946a30ef53a1a5b93f974ca2fdc9b78a`  
		Last Modified: Wed, 13 Aug 2025 06:25:11 GMT  
		Size: 3.2 MB (3172000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d7f008ddab632bcb57758280dc7695afd68eebfd155285aa946b5a2f0d0586a`  
		Last Modified: Wed, 13 Aug 2025 06:25:12 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; riscv64

```console
$ docker pull debian@sha256:d14d511e7ca7e29a49cccfbe2807de3a3817b31311f1506135f0b6b0d5d0d7ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47764527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37ad0314003294970c6a161c24ceb3b2effeb2cdd7d9d42ddee63588eb14650c`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:59f3e0adb655cb03f7d489f3cc57e302e249916bbb076c78008f9329238bfb20`  
		Last Modified: Wed, 13 Aug 2025 01:13:55 GMT  
		Size: 47.8 MB (47764303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9922d12d83d8a1ee926484bb2f4d4f9bf5ef4bf644407ed650ded4f03e96f9d8`  
		Last Modified: Wed, 13 Aug 2025 07:44:41 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:6b70564d735dbdf31f58f4bf1ec9a5e27aecf9d6abdbdf2769a331220923d455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3166665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf3f1af4abb95c040120ef175afcd3af0bc19c5908f4cfcd4202208e43acb09`

```dockerfile
```

-	Layers:
	-	`sha256:4c93b1e0af7705f0992a075377fad278ed1360641405030991ec5a9d154577ab`  
		Last Modified: Wed, 13 Aug 2025 09:25:13 GMT  
		Size: 3.2 MB (3160812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c43c2225757812be8636bc062c79a7624bf183c0a8527e5ad2290d5dcd21346`  
		Last Modified: Wed, 13 Aug 2025 09:25:14 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:trixie-backports` - linux; s390x

```console
$ docker pull debian@sha256:346351f66c2f65dda0d81e4ac569545bb50fbbce69b3c308e7bd612d8f7b8f77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49345384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d34eb90e984a5a980e4a5489d4b59bf07f70ec00636cb2dc50d6d2ff9f618ebf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Mon, 11 Aug 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian trixie-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:c3b791adea90b39bc59919a9959b7f44f65aa3364a03dd0271a5ff658488877f`  
		Last Modified: Tue, 12 Aug 2025 20:59:03 GMT  
		Size: 49.3 MB (49345161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03ad70d20867caf802bdccae4051e96a1852281232763e52bd509e558a97bf5`  
		Last Modified: Tue, 12 Aug 2025 23:15:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:trixie-backports` - unknown; unknown

```console
$ docker pull debian@sha256:0fb634f8d73ec244d6d23d8f561a2d8cc69dc2c08a681b3df42fd4fad2cf584c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3175762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef2ca5d7ec0165fa07342b87e1bdce8b10830e0d9c40732f36f68105093597ba`

```dockerfile
```

-	Layers:
	-	`sha256:03bc4dc76045fc584caae645b2e16f6d6d8162e46c118a933be3af8742617c0f`  
		Last Modified: Wed, 13 Aug 2025 00:27:37 GMT  
		Size: 3.2 MB (3169936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e61c5eef7f63f11fb9e9e239d7b2cb93d5cc7739ad9482754fd490b202ebbd11`  
		Last Modified: Wed, 13 Aug 2025 00:27:38 GMT  
		Size: 5.8 KB (5826 bytes)  
		MIME: application/vnd.in-toto+json
