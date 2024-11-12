## `buildpack-deps:trixie-scm`

```console
$ docker pull buildpack-deps@sha256:b4b757d748fa726c2bd2cf871ddcb888abc2629d4d810d39f96d38a8459f2f64
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:trixie-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2a1bd17b9e1179e78a37cda2c95e93951c6eb4a1124428a1956a423ea7e13d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140355694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543cc9466a8dcd1ed3904970a2c6b3a94865825d52f80c81fd62f72298710c59`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:723f7d6ce61509bbccf2af45aa75a4c5cd83b188d6e85822321cdc68268417bf`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 53.2 MB (53226763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1538514cb923497c68c854e6f9e45945ca05f4a0f5a179472e7f81b1ee0cfbb`  
		Last Modified: Tue, 12 Nov 2024 02:38:24 GMT  
		Size: 20.6 MB (20597910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa039132691ce2d5258743dd8ecefd941d85955a38506ba77c3fb6d2f554298`  
		Last Modified: Tue, 12 Nov 2024 03:18:08 GMT  
		Size: 66.5 MB (66531021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:006c1a4f157ca8332c37cfc903f51fe99c90c9e534a72cac860f9fb8365b84af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7623030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e23d95e10f0fa5f7d7bb7c419adb4b4efc852e89db69d30cfe318be44e81af`

```dockerfile
```

-	Layers:
	-	`sha256:f66b32ff82c0df69c59a686e88a8d08a6ae82c59c9462bd2249d9876a847eaca`  
		Last Modified: Tue, 12 Nov 2024 03:18:08 GMT  
		Size: 7.6 MB (7615716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6de0676f525b54096e36412a85f3c6647ed8bc777fe9cf6dbc7352a34d09c157`  
		Last Modified: Tue, 12 Nov 2024 03:18:07 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:8d8e3fdc5829aed1b63ea33f435469be1517cd603483aabe32fe43e31b9b84e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133665306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16cf4cc1b27f69e3f63ac0b103f60c88fafda72f2853563fccebf54e71da792d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4ff391534f557bd19067799d6e6b7e386e43cbf7d061a795a182546eb2145e99`  
		Last Modified: Tue, 12 Nov 2024 00:58:57 GMT  
		Size: 50.1 MB (50091523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d129d70e5af0f50e5354ff02342f42eba97458b43a0df2209f72566f664a4a`  
		Last Modified: Tue, 12 Nov 2024 06:29:56 GMT  
		Size: 19.6 MB (19607774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a342b984b6752601eb44f7fa9cc6f866d747d925571f5c63f8db143a85f2fc46`  
		Last Modified: Tue, 12 Nov 2024 11:32:48 GMT  
		Size: 64.0 MB (63966009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:55cb1fe2158d176fa5dcb4daeac857818c62b2e9366dc456933b6f31765d4469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7623355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5037e5aaa8ca5213b9ca8057df32fbe8e1b104c09243d715658e4a29226b356c`

```dockerfile
```

-	Layers:
	-	`sha256:cb82e81672aacf72d387cbc2f43da98514547c58c1480ebf7b5835d0e3fb28c7`  
		Last Modified: Tue, 12 Nov 2024 11:32:47 GMT  
		Size: 7.6 MB (7615982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d98118b2ef6e507ba56174c04789b05d0d96599c8d4772447261b2491bdffb5`  
		Last Modified: Tue, 12 Nov 2024 11:32:46 GMT  
		Size: 7.4 KB (7373 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:da6fdb925b5de7f3beaaf9f7138cfab36ec0cbfdcdabf72cdad10c36ca194511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.9 MB (127859410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:290b778918d3f0776bc82777549e9e66202608ae29931c36c3a39cb680f69433`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:7b183110c42f24584c122a8e76db1e925d5fd8b3489ae273dbca0b0cc3bc0090 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a5589eaa1616610f1da5585cd04faf9e418fe913dd4e9ef827abdbe93f8caa5b`  
		Last Modified: Thu, 17 Oct 2024 03:10:29 GMT  
		Size: 47.7 MB (47659640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a052304c7554ffebe70b582d4e2eb7d1d61098f5f96c8c9603940278d081561`  
		Last Modified: Sat, 19 Oct 2024 00:58:30 GMT  
		Size: 19.0 MB (18971211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfcca10ec23fe707cc08f7ab790838065704861f60c0f678095482cc25ef593`  
		Last Modified: Sat, 19 Oct 2024 06:40:45 GMT  
		Size: 61.2 MB (61228559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a9757a6eef12d8e4457f63d8128b0b8c16a0230cee675ce2af94935916d16c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eea98d047064758984f353ad89edcd13307d0700c40c376b60bdac9d397af66c`

```dockerfile
```

-	Layers:
	-	`sha256:7a93cf475e613ba4986581169e51da296f5eab2d1af2eec23ca1a4ebddd8c326`  
		Last Modified: Sat, 19 Oct 2024 06:40:43 GMT  
		Size: 7.5 MB (7486524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20c2dfc26ee7918a49826fed2ffc0d36d6dd4dab8b3cc5d2ec3b13523d04f02c`  
		Last Modified: Sat, 19 Oct 2024 06:40:42 GMT  
		Size: 7.4 KB (7386 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3b629d663679a2b2b40868852c5dfbda509fd66bd6f901cdf256592706f0da24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.3 MB (140280895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6f779d0370a31853b4d9b6ad68485f28d2bdeb59641df30882b6ee54f6a915`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:5d91cfda460a83c91802e918bddf6951978599b67dbd5e3c0a492a53f20d6ad6 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:6f4ac25c892a8a547634a70e67af9f356a5f2b1f34e7c78d52074f2a21999111`  
		Last Modified: Thu, 17 Oct 2024 01:17:18 GMT  
		Size: 53.6 MB (53599725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b74f65518d0117b47b1d80b0bf8981ebb7ddb04cdeeadd261af699b6e5d50`  
		Last Modified: Sat, 19 Oct 2024 01:12:15 GMT  
		Size: 20.4 MB (20382473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b125c1d7d6d0668d3d31049e15ed26c5f15741a45a407eab00423ec50972be12`  
		Last Modified: Sat, 19 Oct 2024 05:20:09 GMT  
		Size: 66.3 MB (66298697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:981b9d0b27672f9ae58a479116f2d44a4372d329f9e65910623c50857c7f2012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7499825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83b16a06a55282321f67d9ada42e21d02d811ecc3a3fc386acf84684d93a15b`

```dockerfile
```

-	Layers:
	-	`sha256:e31fe82ca59e0b11c21807625cd32304cb7c70ed6c502b0b98468e11df80130f`  
		Last Modified: Sat, 19 Oct 2024 05:20:07 GMT  
		Size: 7.5 MB (7492419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:859f0a00775cceb04089b3a21a3466d9b86a3ba87b410318a08e54198cb54287`  
		Last Modified: Sat, 19 Oct 2024 05:20:06 GMT  
		Size: 7.4 KB (7406 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:17f77e1c82b223cf3f38382724d4a83f63a07ca65e77321db1ec9ea444466eb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.2 MB (144160990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558df670cd95356ddd37034014ece4572b6e5b0c6d1d40dda1c173413f7e507c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a04f0591b5521dc9360454fa2fd6b21d9b7d989bb4c88327ad94f8282af3b267`  
		Last Modified: Tue, 12 Nov 2024 00:55:13 GMT  
		Size: 54.1 MB (54095157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914cc5c9bed5c786b85a6e40864cd3fb4af442dea3455ca88a01cfa26707d8df`  
		Last Modified: Tue, 12 Nov 2024 02:38:04 GMT  
		Size: 21.7 MB (21722460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c207d20a70d18f9e95ac6b10fd58bbc5d2a036845c50cdab8e2fa983066a990`  
		Last Modified: Tue, 12 Nov 2024 03:14:35 GMT  
		Size: 68.3 MB (68343373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a7af66e9bf190aefa86e1f76abfec0fe4c44a04ddbc03d55ff18c4ef7c863f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7617759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3fbadbc2198b4e131475280b87df5241639ec83a1ca1198e19eb4022f3dc1a`

```dockerfile
```

-	Layers:
	-	`sha256:cb12d5a0477c96ee0bf9ebe5630d302496423079ffd94280db676664955ca33a`  
		Last Modified: Tue, 12 Nov 2024 03:14:33 GMT  
		Size: 7.6 MB (7610468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:534ad46e5e83d3c45f05ba6b7886be6e67993ce4f589506783f49296f2c60595`  
		Last Modified: Tue, 12 Nov 2024 03:14:32 GMT  
		Size: 7.3 KB (7291 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:78d50bdb37e5bb8ce65015b943145de8356d61c7bf9ac0d2b70b5bb19d61592f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.2 MB (138151112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c40a1f4ab862506927452bfc655b5b498b376a47d0ebbd5c7fe468eb7a88db`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:7540ed5b693bb419df5aaa69483f55c19bc0566d076c5e65757a0a6fe38375a3 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bd6795a0a311ac784071ff263d2b83d646956234334d40fe908b91a1dde11378`  
		Last Modified: Thu, 17 Oct 2024 01:22:22 GMT  
		Size: 52.1 MB (52128468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bde6977c24ffe15c007c6606184010ccb92606e6158cbd76d8e770997debfa`  
		Last Modified: Sat, 19 Oct 2024 01:01:31 GMT  
		Size: 21.0 MB (20966640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdea9feeed917171d6d06a6129bb34f0f75c8fdb0fc8f9755f248adca6eee285`  
		Last Modified: Sat, 19 Oct 2024 02:14:28 GMT  
		Size: 65.1 MB (65056004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:81190818ed7d83b0f92ee66dc853e7c6f22b9535d8e52f4f00fcfdc4354973ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 KB (7159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f37bae74959741f2259d72bed0704bd028bbb2ff4414f68912774344bbdbf3c`

```dockerfile
```

-	Layers:
	-	`sha256:c02dd3eab5f5e9db4c0f38c6e763e61d6cf4e72819705f3060c07ec5c7819c76`  
		Last Modified: Sat, 19 Oct 2024 02:14:21 GMT  
		Size: 7.2 KB (7159 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fccf093e3bb36008832e5ec58a51f1ac32d0d886c98f75c4f37ebb863d6885a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (151013309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebeec5bc9376d17e01d51bb7962444e7575f3df8a16e27526ab9a4ffac838a4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:554b3bf5ec10b22cc962f7afc042e96c50635c0e2b0d817544a202afc2a52711`  
		Last Modified: Tue, 12 Nov 2024 01:05:47 GMT  
		Size: 57.2 MB (57193598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08187472bfe4fce6e3b2fc2951e231ce30c71f70be1dc829ad73735e312d479f`  
		Last Modified: Tue, 12 Nov 2024 08:31:04 GMT  
		Size: 22.0 MB (21983916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5445db0db78751088bfd85b5a3ee628352f9d78288ca29fed636c550e50e6235`  
		Last Modified: Tue, 12 Nov 2024 16:12:54 GMT  
		Size: 71.8 MB (71835795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:e94f6be5b6eddf231fce0e6606fd38a9209523a97cc3e95f0c1f15a4652074c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7629581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46fa744652a5277bf95624921ad212b186a9d9c17913d20b62f2bbb489029e5c`

```dockerfile
```

-	Layers:
	-	`sha256:1dc404b8f0d7ebf05e25893e3c6825872d16ff0cae8abaaf48f9a7649d8bff42`  
		Last Modified: Tue, 12 Nov 2024 16:12:52 GMT  
		Size: 7.6 MB (7622236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b0339d7f4b34fc047dba3dca04265fd1aa21572185158b43c3d4d366e80585d`  
		Last Modified: Tue, 12 Nov 2024 16:12:51 GMT  
		Size: 7.3 KB (7345 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cb2e75552a2d042a659ba547ccb0609e06f697798884a74c6805ee8b1ab38d65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141797604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9b44ffe80f44627eca35eaa520ed53a92ed54585062c43ba93198f9ec59a05`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
ADD file:fe7c88cb45fa7097d71f60ba00c0d6ad76dd030e8e34771e5ee3735b59a4d6e6 in / 
# Wed, 31 Jan 2024 23:01:46 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:53440987c87b8deb9090e5298bf822ffc945f186eb4c81cecc0ebf58717ca549`  
		Last Modified: Thu, 17 Oct 2024 01:51:55 GMT  
		Size: 52.8 MB (52808844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3816f9124671541da45f7e11a0a925de47e719482f5bcd085247ecdcb8c613`  
		Last Modified: Sat, 19 Oct 2024 00:59:12 GMT  
		Size: 21.7 MB (21656188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cc2aa2fcdc4addb1b596c3dbc6f3699d60107644fd49f54f3050356c21437c`  
		Last Modified: Sat, 19 Oct 2024 03:48:52 GMT  
		Size: 67.3 MB (67332572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:b270aaa7768e4a2d159ff7b5f42829b62c59d4ef131517f86c9ae12564beddae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7494252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:942bb4de50d03290e36368d5b3922ed61f5adbe88b45bdc98fe4f5ece352669e`

```dockerfile
```

-	Layers:
	-	`sha256:be9cc770647715d3212ab0a996c38d93ff0e416f9d91de05c1000fc1ed5dc2b7`  
		Last Modified: Sat, 19 Oct 2024 03:48:52 GMT  
		Size: 7.5 MB (7486926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dd9a3268144974562f1606345489a7a1d2317d957179ab65d447e065d5173d3`  
		Last Modified: Sat, 19 Oct 2024 03:48:51 GMT  
		Size: 7.3 KB (7326 bytes)  
		MIME: application/vnd.in-toto+json
