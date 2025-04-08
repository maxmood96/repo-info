## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:4c65957cff56eceed3f59a9be5a8d873614a62f73217c3ac61a76a7ec1e1a8a2
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
$ docker pull debian@sha256:7051e1f57d4b6e2407ab952d784e5d6f624ad3020b2bf478f56c17777746b1ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53748757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e1580d6b4f9455199103e44bff88f885a9b74271ba8182d362f6e8c5c5d0ca`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'oldstable' '@1743984000'
# Mon, 07 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:d733ef6e598b6296fad8c042727c647f5609a6378b68fd6b929231dc45d4e68d`  
		Last Modified: Tue, 08 Apr 2025 00:23:18 GMT  
		Size: 53.7 MB (53748532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a801e434cd398594ff424ee5feb42c3867d3d8c4a2c01ca0df35135725e8696`  
		Last Modified: Tue, 08 Apr 2025 01:11:23 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:b43f3eeb123b402864000b6d984da673f02ff80e02767947eeea5c54a2e21494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3925285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50bbe330e1ed5d3928dfa3fa1b205a6b0922ef3c49638ce72ae86310db8b7f40`

```dockerfile
```

-	Layers:
	-	`sha256:f73b497aa9debce0ede1bd010f747a84ce86bac9f117b2635a85490ebc6afc5e`  
		Last Modified: Tue, 08 Apr 2025 01:11:23 GMT  
		Size: 3.9 MB (3919432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:701c43b697ce308858d817621c9ba6c7a9cc8e6ac48cc98662151a14f01fdbd7`  
		Last Modified: Tue, 08 Apr 2025 01:11:23 GMT  
		Size: 5.9 KB (5853 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:d5f40479fe4610715f6c08ab15ce69aa1025b639ab2549fa137be0de08f1fe28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49031679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5cbf7397a4111bab2f76abab776dce10e696544109f5d0bb31beef8878edfe`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'oldstable' '@1743984000'
# Mon, 07 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5d4a5bd7ce7271c9be3ec90c9d20b6970afa7564be1a2cfdbb2598ac9a76e16f`  
		Last Modified: Tue, 08 Apr 2025 00:24:13 GMT  
		Size: 49.0 MB (49031453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a990c610d8dd843094e85a16144d4f37522adc25b1b426e6e1bc18683b58692a`  
		Last Modified: Tue, 08 Apr 2025 01:12:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:8d9df32fdabcc92a5246f2bc24e6bdd72a95cd8b486bc0abf0aca73c956f6fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3926899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab98c0b3400aa24e13a46496d17ad4be2fc278fc8385175f2262d02b2aa174f`

```dockerfile
```

-	Layers:
	-	`sha256:ec9df5715fb1efd37827dfc4bf4a5fbbca8fecf4becbd7ffe89094172854714c`  
		Last Modified: Tue, 08 Apr 2025 01:12:15 GMT  
		Size: 3.9 MB (3920994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e1541d896e00c4fee98bd2c2d6a2629fbbb78a8e9a82bf51dfc7b5fe35a1079`  
		Last Modified: Tue, 08 Apr 2025 01:12:14 GMT  
		Size: 5.9 KB (5905 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:cff4286faff3ddd12e37276d61068fe8044994681a0a20db41ca327c465f083e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52254449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882c0011272630911be810b3586e41dad78a22f7fa30c1b348e11aa59fb4702e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'oldstable' '@1743984000'
# Mon, 07 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:1c9251e80fc93955222e6efa8b7d02b10199e3bb45186df70d53fb53b04d552f`  
		Last Modified: Tue, 08 Apr 2025 00:23:52 GMT  
		Size: 52.3 MB (52254224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a15f791de7b03be1a78214788220c7972a6cfcfc37eb4c430b99b570dbab56`  
		Last Modified: Tue, 08 Apr 2025 01:12:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:123b4681241ae99a64bcae348fe8202e69dc2a99a05122beae97f93ff3fe7dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3924933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fd7c1dc6266caa3cbd674b85de997e4c5c7e6084e7e1167f5466f38b9d50a83`

```dockerfile
```

-	Layers:
	-	`sha256:3a271da2f5ef9c1293a7b0310937004cd4ad516503e2f714665946492ab8e2ea`  
		Last Modified: Tue, 08 Apr 2025 01:12:07 GMT  
		Size: 3.9 MB (3919012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:faf5c3075aa1088fab0fbccc02540af9ba52360d1741ffff1758f99d69e437f8`  
		Last Modified: Tue, 08 Apr 2025 01:12:06 GMT  
		Size: 5.9 KB (5921 bytes)  
		MIME: application/vnd.in-toto+json

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:84ce9671a765a39df34d8033ff3269b3931af1d8668ac3e9107c234e71800817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54684694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91bfc6088ae7cea09a5a1fb9757f733b05169b88ae7a4e4bb7eadeeeef093ca5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'oldstable' '@1743984000'
# Mon, 07 Apr 2025 00:00:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list # buildkit
```

-	Layers:
	-	`sha256:5135a40bb0dbc419ccef3843425f37048c9d9c55bd778c5a773e87764a4f6262`  
		Last Modified: Tue, 08 Apr 2025 00:23:07 GMT  
		Size: 54.7 MB (54684469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9dffaca902a56d4d5c7763429b13e3304455b413392b81568c1d923c40303d4`  
		Last Modified: Tue, 08 Apr 2025 01:11:59 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `debian:oldstable-backports` - unknown; unknown

```console
$ docker pull debian@sha256:e7589927513945519cd223235c421e9ccbb003b56ce4c77e67e8a91420351b1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3921775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26aa41fe215c2c30336bedd7f91898d51c67a021b026031076cf11de2d598d7`

```dockerfile
```

-	Layers:
	-	`sha256:1d8e25fd956f194a8bf5804c56264c4e323b67d18cbe3dacd211e3ec8985ab49`  
		Last Modified: Tue, 08 Apr 2025 01:12:00 GMT  
		Size: 3.9 MB (3915939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3f9784a7384e36d204ffd1b313d229c16a69886de079805b7fd6a72b1d290fb`  
		Last Modified: Tue, 08 Apr 2025 01:11:59 GMT  
		Size: 5.8 KB (5836 bytes)  
		MIME: application/vnd.in-toto+json
