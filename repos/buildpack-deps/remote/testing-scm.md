## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:28354ee27c9eb4ac359a24d05c6739da60d9425997ea05d5492f064bc5719cf8
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

### `buildpack-deps:testing-scm` - linux; amd64

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

### `buildpack-deps:testing-scm` - unknown; unknown

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

### `buildpack-deps:testing-scm` - linux; arm variant v5

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

### `buildpack-deps:testing-scm` - unknown; unknown

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

### `buildpack-deps:testing-scm` - linux; arm variant v7

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

### `buildpack-deps:testing-scm` - unknown; unknown

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

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e68ba4155d2ba86fde8d389332d35fb57b219ab388c52083fb2444efe918ea4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.5 MB (140474976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e64285bc4c8d47537d83d55000ab224324b279033ab7b8bc92945167abfa6f6`
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
	-	`sha256:4de57c6718ff0fb4c76cd3ff1a33db2bde24e482395a89d0d4f6c7e6b3c20f53`  
		Last Modified: Tue, 12 Nov 2024 01:03:14 GMT  
		Size: 53.7 MB (53669977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27cb33ae9e17116eb9be8382614725b619742aeedfb992b4bc26c5d5efa717e`  
		Last Modified: Tue, 12 Nov 2024 11:17:43 GMT  
		Size: 20.3 MB (20252075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebb08f62c15bea658c57ae9f96fa28c800a3f5d9e56db394a67684608bb7764`  
		Last Modified: Wed, 13 Nov 2024 02:44:37 GMT  
		Size: 66.6 MB (66552924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8ffcccd6c472db2ad16e7472dde5590c02d9ae19978f59bb583c24f2d9d38810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7634144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f591844f361615941dcdc296cd5300c1afd784c436186b2cd88cb1d7213e5a5a`

```dockerfile
```

-	Layers:
	-	`sha256:318f9c03404ac143438a39d4002624ef9668934df3300c4c327c325e35130c59`  
		Last Modified: Wed, 13 Nov 2024 02:44:36 GMT  
		Size: 7.6 MB (7626750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:794ac960c7af0f044e1c0e47cb50a4e5b4790c29b0b6a81c475c748bca1007bf`  
		Last Modified: Wed, 13 Nov 2024 02:44:35 GMT  
		Size: 7.4 KB (7394 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; 386

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

### `buildpack-deps:testing-scm` - unknown; unknown

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

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:a57aad00feecb8edf6a531a3b2273b38be5782fd4b5c2fa686bd3ffb7bb477d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.5 MB (138504731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe7cb8809cd8d0bb5c836f77e402319e5b8174742ad7ca2deaac8446abc8c79f`
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
	-	`sha256:e85824c3ce994136e0b1f6545ca38052c56e3faf7dc4ab5102ef2c2e357cee02`  
		Last Modified: Tue, 12 Nov 2024 01:08:01 GMT  
		Size: 52.2 MB (52200415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40c4cfa8a0eedb22460a31984d56495095c0e6d072ab4be3aa70aec30584cf7`  
		Last Modified: Tue, 12 Nov 2024 18:05:03 GMT  
		Size: 21.0 MB (20951814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174684d328adb3f37db85b256c1516f8c1ae147bdb5b13929af1a4f6ef492496`  
		Last Modified: Wed, 13 Nov 2024 02:09:28 GMT  
		Size: 65.4 MB (65352502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aeb383292ed98f4e95e7bed23e796ac6667a5b32d7643ec0320d200b94f1584d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7d0367030e0511dcd2d0554cb412a467c40ddd6bcc39f900c52198c48b5a46`

```dockerfile
```

-	Layers:
	-	`sha256:a57a9024738cef4b7c03619301631a79b8697a908e20800b4364f7d9cab9d9d9`  
		Last Modified: Wed, 13 Nov 2024 02:09:21 GMT  
		Size: 7.1 KB (7147 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; ppc64le

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

### `buildpack-deps:testing-scm` - unknown; unknown

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

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:46ddd549b8448668973dc627a780c9ebe569e18b458f0a20f70fe4d66912c066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142162888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:921deb515dbff867d2486af1ef5ba583576dd60170a1c95da6f0f4957e8b7e1c`
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
	-	`sha256:a54a131d29bb2d4a9258476cdcb51efa9314272b8894e2474e100e5d38d85679`  
		Last Modified: Tue, 12 Nov 2024 01:05:54 GMT  
		Size: 52.9 MB (52885488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a20f0f48b3016dae43f5b6fa4b9b89a2e08fbca4da340a0b01b79f3c8a37e0f`  
		Last Modified: Tue, 12 Nov 2024 09:03:50 GMT  
		Size: 21.7 MB (21709127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428dd13bafc8a0c841ef38af6a389113eb680c47f53aaa14b18f49ab9df90a04`  
		Last Modified: Tue, 12 Nov 2024 23:35:08 GMT  
		Size: 67.6 MB (67568273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:566987c32caf861482277ccd9fa0937719940b4d69a2ec1fa494dc66159335b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7623460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71ea321e1420a23fdd06266b4dd7711a895b6a4b2d48ff6d1c4594a918d96a74`

```dockerfile
```

-	Layers:
	-	`sha256:49b05a5282b415b42c65eb29b028a0afdb93f9bd733af2ac2334c63c3ba641d0`  
		Last Modified: Tue, 12 Nov 2024 23:35:07 GMT  
		Size: 7.6 MB (7616146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a92489f5ba67540e64af974444993423515914a349bbae13e078ee5f73af31a7`  
		Last Modified: Tue, 12 Nov 2024 23:35:06 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json
