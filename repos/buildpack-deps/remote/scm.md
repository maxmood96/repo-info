## `buildpack-deps:scm`

```console
$ docker pull buildpack-deps@sha256:8f8b5f31a0bdfa2a6975e72a366ba2a3768cc6b974dde304db675046346f36a5
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

### `buildpack-deps:scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:63f8cc622484d4919c8efa1a709873c3a4b7efa45c49397b808982c998314b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142680809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b00b7c6f2392505f8719a98ff2f6ef8bd616ae75ef7033bfcb8442dcccb6a2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:23:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:281b80c799ded5b9a390d2e8c59930db01ee395ab809dd34259897c660751f4e`  
		Last Modified: Mon, 29 Dec 2025 22:31:07 GMT  
		Size: 49.3 MB (49289587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f14138abe4f09d3ef3953105144728056046ae469ae21e8e42749bacd67cca`  
		Last Modified: Mon, 29 Dec 2025 23:47:42 GMT  
		Size: 25.6 MB (25613989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378c64c4458002be86f2d86c5768ae9ec0cff69afac7d1444e50206dc4566fa9`  
		Last Modified: Tue, 30 Dec 2025 01:24:00 GMT  
		Size: 67.8 MB (67777233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:021dadb2adf7f142f52a3b87e9527c6ae5410bbfc99709f18919770f7bcce486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7774675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12102b232575087daec3456b81415b1010576ac0e45300cd0a5421d63f6121a8`

```dockerfile
```

-	Layers:
	-	`sha256:e6766b0f7138d64adf4ff5cb6023cbcf5e681d5c7c60f094212fbdcf9052261a`  
		Last Modified: Tue, 30 Dec 2025 04:25:42 GMT  
		Size: 7.8 MB (7767098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:facd45e8947218a737261140ebddca5599bdc71412a292dae28b67ce6a7c77b5`  
		Last Modified: Tue, 30 Dec 2025 04:25:43 GMT  
		Size: 7.6 KB (7577 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:00f4339ae846dc8d72349295bf5ebe475fe5bd855a7ba521bda76aea8d09c870
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137112408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63fb1df76de89cd9d8c3f44a56de61ddda6148e31fb84ffc9bc01a46dcb63214`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:29:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:50:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:34295e8c92d32055cf38cee5aec380c4d26fb9f87d9d69deffe81403a9d5a203`  
		Last Modified: Mon, 29 Dec 2025 22:26:50 GMT  
		Size: 47.4 MB (47448770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cf1b0fd719c142e9016b7b007d0d982443d9aeedfc75f9de33d17efc3342d9`  
		Last Modified: Tue, 30 Dec 2025 00:29:32 GMT  
		Size: 24.3 MB (24345729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a515687a5a3da2827aa6a3b8071d1f515ed0d5cba1dbfad9af02797c060c18`  
		Last Modified: Tue, 30 Dec 2025 01:51:10 GMT  
		Size: 65.3 MB (65317909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:57d68bcb77bbe9f10bdd6d8bb08f52cb153996c2af0d30138374fc84ca2c0add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e53e0f95ee2532231410d1abd27bb07089be41314f4d7fc54e208fecdad9892`

```dockerfile
```

-	Layers:
	-	`sha256:95665755aba303d45b66107b450547aef680d875aa0739a2b4889e4018b5f828`  
		Last Modified: Tue, 30 Dec 2025 02:21:54 GMT  
		Size: 7.8 MB (7768136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e726e8b358215e37277138c929245d328fab46fcba9a13cbc3d63c54f57ac2a0`  
		Last Modified: Tue, 30 Dec 2025 02:21:55 GMT  
		Size: 7.6 KB (7649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e9173e66cc789c7d22b9a1203b233727450f7816db16bb0118a25aa55d18a0b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132051890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4635ff2f59f4de314c6b4d7614ca540da6c28b13053ddc26f4766e6b624797`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:35:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:07:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d20050ceedb84a03f8a4208462819500ff366fe1a69cdbba74b118aa8a38a87a`  
		Last Modified: Mon, 29 Dec 2025 22:28:10 GMT  
		Size: 45.7 MB (45718317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1468c2ee0f43e81d6e097b24054de66ae95db50d77cef08d1eabe51a5dab43cd`  
		Last Modified: Tue, 30 Dec 2025 00:36:02 GMT  
		Size: 23.6 MB (23619911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa494d16bf7a563003db4c95fa508ca504a77c791075afbc16c7f5a1be17761`  
		Last Modified: Tue, 30 Dec 2025 02:07:44 GMT  
		Size: 62.7 MB (62713662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ce4edf7172b6f99521524b3967911df3792316257e84ddc2f1282a3ed31e94df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3943b7627c8906d99e3b3e003f021d91de0e15b2839154e134d941d0ff3d9b`

```dockerfile
```

-	Layers:
	-	`sha256:bd8cb70fc0a8410f3677b42aa093100885acc69ff04cb1a7b2d191e3016fa37f`  
		Last Modified: Tue, 30 Dec 2025 03:27:58 GMT  
		Size: 7.8 MB (7767605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b69ef4cf4ac1e60509823cc3b831649961c8444c37bedfce99218c60b267d492`  
		Last Modified: Tue, 30 Dec 2025 03:27:58 GMT  
		Size: 7.6 KB (7649 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8119ab350578420190116327ce38e9226fed560a819b506976d4916c4361e74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.3 MB (142255022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e276557c308bf61abcfc36346ee60d4addef22f06f34c33aee4f54a5759ab9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 01:25:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5785abec2864dcd8d343ccd872458a50ffb2a61739bc46a79709c68c455cb8fc`  
		Last Modified: Mon, 29 Dec 2025 22:30:57 GMT  
		Size: 49.7 MB (49650193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce2d1ead36d47118631ae52b25fc39c1aa005c68093dd34e456927908318c52`  
		Last Modified: Mon, 29 Dec 2025 23:47:57 GMT  
		Size: 25.0 MB (25021045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d9404781930ac9b1a80bc4d3e616b480ed1eeab70b8545e9988a3a11d00783`  
		Last Modified: Tue, 30 Dec 2025 01:26:07 GMT  
		Size: 67.6 MB (67583784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:07bd2f4efc761637e2a36f2786027888067b46db13bb374246ba54834b251371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7782442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:937eb4e9195af3fc59a307e4faaba355a986702a5b78ec703e955c1363cc9a52`

```dockerfile
```

-	Layers:
	-	`sha256:239e86fac866c26929a9222835aea5e9d8d3f3cb912d715f30daeb41398f01ee`  
		Last Modified: Tue, 30 Dec 2025 04:25:43 GMT  
		Size: 7.8 MB (7774773 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80ad4db7e7e58aba8a75a580c9daff8586372d78e7d220f430868c4128b3f265`  
		Last Modified: Tue, 30 Dec 2025 04:25:44 GMT  
		Size: 7.7 KB (7669 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:f2b6283001cd4d5d581129ece1ba4da31e84f747dde66300eb1c2b93aa7706d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147372851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7fde892580f2257f3ce88107d9793fdc6fa7c2e32cced7a52a6a7cae5d717b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:47:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 00:34:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7ba68d5e03a08e607fe00d0a9f5d3925adc34700fc401165e5513c0d55ae9d2e`  
		Last Modified: Mon, 29 Dec 2025 22:27:39 GMT  
		Size: 50.8 MB (50801684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabb00c990eb2d1ca8a4037bb0b9c6e0d0d8b6c6fb47372c8ec75cd65588cdd8`  
		Last Modified: Mon, 29 Dec 2025 23:47:40 GMT  
		Size: 26.8 MB (26776375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc67c159b6d502873d04e7b21d326f226b1fd89576f5d5cd1b817d74d68fee4`  
		Last Modified: Tue, 30 Dec 2025 00:34:34 GMT  
		Size: 69.8 MB (69794792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:db57e4717828025dd65b68e8f5180e596cc4b38ee18d81541377db5e13f7ff99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7770783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e66d0796a8dd250a8f4f572c99ddbba377c7976ba390790b485e49c22e2703b8`

```dockerfile
```

-	Layers:
	-	`sha256:9217446bb82851e3a4c4fbf55177d6fe76e985e6ac89e23db290f46fc2b1d74c`  
		Last Modified: Tue, 30 Dec 2025 03:26:46 GMT  
		Size: 7.8 MB (7763233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d70802c911e7cacd168c279a1630587d04e0e6a1137e5cd58e637debb4fc7d01`  
		Last Modified: Tue, 30 Dec 2025 03:26:49 GMT  
		Size: 7.5 KB (7550 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:9be638afc4cb836aebc740382a2c5fdcb2e2f9c516855273f3768fdc81adb845
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153127339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31355cf61aaf7c221b5bfd3e2125f67c7f70a2149bbd8d85eb216459631c04fd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 02:12:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:fb00391cdf4b5dc5fe2e67e0bee3770076e9af9efed48ba15cb306902e36c78c`  
		Last Modified: Mon, 08 Dec 2025 22:52:23 GMT  
		Size: 53.1 MB (53108478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e79cf54a8287f03b9105a7213ef3a99e05832db0bdcaf506dd64b872bddfd7b`  
		Last Modified: Mon, 08 Dec 2025 23:23:25 GMT  
		Size: 27.0 MB (26996775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbdd943d24ee93fc3b0013d3315e9ace0f4529c7fcae39b318579723e579b6d`  
		Last Modified: Tue, 09 Dec 2025 02:13:21 GMT  
		Size: 73.0 MB (73022086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9b65a039736fa0712f8adeae612d6c130342741ab1d1235b4920d70a19b841b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7781836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:417182257df48eeeb32025e981cb561778957cee4821e6dcaa0081e53d1d3d56`

```dockerfile
```

-	Layers:
	-	`sha256:837d7ea9030b359fddae4bf5b73777bd28084f48c7cecc7e257caf34a8d97827`  
		Last Modified: Tue, 09 Dec 2025 05:22:06 GMT  
		Size: 7.8 MB (7774221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dcd6abd7def16fdf778efd1e76f1bc398d9fecf4d4c826152d42141b8b7653b`  
		Last Modified: Tue, 09 Dec 2025 05:22:07 GMT  
		Size: 7.6 KB (7615 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:62aff9aa14b0d04c3649e4da037546a3e6c8c0b46efcbfb685ded435ad6b580e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139385468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9732a86b45c58daeeaeade83d8dff902e254602761779c23da27c4640fb160`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 08:39:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sun, 14 Dec 2025 08:46:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e8961870af39130e72e5dc66bd3574bb074dffc7989fd5e909f55fefadae8a30`  
		Last Modified: Tue, 09 Dec 2025 02:05:05 GMT  
		Size: 47.8 MB (47771135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2088c9d98910c38f13b1907a28647a9e78cc7ea821df93ab45af07ce2813dcab`  
		Last Modified: Thu, 11 Dec 2025 08:40:59 GMT  
		Size: 25.0 MB (24953834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a60a42ed8727e43dc5cd180abfcc19a18468941394808f724b1f4dc00352352`  
		Last Modified: Sun, 14 Dec 2025 08:50:41 GMT  
		Size: 66.7 MB (66660499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c93fcb9f32640d44c8df15d31786a9d2f5e2f4579feab55a9842fd685f8c8295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7764549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10dab79f9d0f243147e5d6c1bccc8c2653ae45ab741ef6571847cf6b1218ea9c`

```dockerfile
```

-	Layers:
	-	`sha256:dc033af8175d5d3c4bf1ec17d0328ebc9f1fccbe1f9426fff69686c42e9a5fcb`  
		Last Modified: Sun, 14 Dec 2025 11:20:41 GMT  
		Size: 7.8 MB (7756934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7281f6f01552795cd448f271be937c8b751ca95db60e4440b04e62a2394053ad`  
		Last Modified: Sun, 14 Dec 2025 11:20:42 GMT  
		Size: 7.6 KB (7615 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cf5a4571c21f1a0834f8ca434dbd52a07b66a8c841eb98db2d41582d925644ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144756770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2800fa55610b95d68f94c44c804f6b85362bae87facda03ffe29c1ec35b727`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:11:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 01:47:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3f8967bef2f6a8ec916f7d3a0d528a6724093176621c5758addeeece50e41dec`  
		Last Modified: Mon, 08 Dec 2025 22:16:15 GMT  
		Size: 49.3 MB (49345908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98c145469a927f8321c172bcf0ed7919725c5f02b2fea3f4d05ea5083b4b8c0`  
		Last Modified: Tue, 09 Dec 2025 00:12:09 GMT  
		Size: 26.8 MB (26786516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a105dbf5cfcb4e2c38a6c33b07d696009c0c1ce742a7404e87b258f0914a1424`  
		Last Modified: Tue, 09 Dec 2025 01:47:55 GMT  
		Size: 68.6 MB (68624346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1e4f862c71e06995347878d4f7391bd7d9bbab590c29768e96eb728c9408143c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7775588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c637b2a4b6fc11a753f8b8e894c70ba016a47223536032067e2a64adb9d31472`

```dockerfile
```

-	Layers:
	-	`sha256:b3516f174b88fe3a07591f25fa495aaabba3bf7f9888a99f1f2a823b54c98ac2`  
		Last Modified: Tue, 09 Dec 2025 02:24:49 GMT  
		Size: 7.8 MB (7768011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cca90cf7e56a630dff6d199d4421f2fced11652c81d76d616763ccc983768ac`  
		Last Modified: Tue, 09 Dec 2025 02:24:50 GMT  
		Size: 7.6 KB (7577 bytes)  
		MIME: application/vnd.in-toto+json
