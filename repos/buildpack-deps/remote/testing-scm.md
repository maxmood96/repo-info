## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:020f3285228ad3f932a303fb118e97cb657b6efa7bc5180405afe6d60bff75f6
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
$ docker pull buildpack-deps@sha256:b8c4d19fcdd5c0b9f7b881512d2a832e0e9c6dcb0708b59a510e64b735bed08e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140637122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeb4a493006e190c0b315afcc48fc4931e5562387cc87da4bd2e85e2b38eb2d8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1734912000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5dc28167de372c586b840aa2cdcf07e2afc8e85b392a5dbb5552be77587eff75`  
		Last Modified: Tue, 24 Dec 2024 21:32:36 GMT  
		Size: 52.2 MB (52212351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfcdb7af4643d9e902826381436aafc5ca852c439990983daa707960060dbc0`  
		Last Modified: Tue, 24 Dec 2024 22:15:33 GMT  
		Size: 21.4 MB (21406167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389a305f06858b3033956e0f308da92fdc18e3e15dddb5afd66e1616ffcfefee`  
		Last Modified: Tue, 24 Dec 2024 23:16:10 GMT  
		Size: 67.0 MB (67018604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7d4871b2ae7aa36acc715a500392660f5689484aceb26b746982b2d288f20a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7637550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751f177fd473369962664cbaf2402763f88ed4ca504f306d73d123f57329aff2`

```dockerfile
```

-	Layers:
	-	`sha256:09688db7c2ddf0451b6758d67daee2d4544615d3d39a28715be92acf490dd5ab`  
		Last Modified: Tue, 24 Dec 2024 23:16:09 GMT  
		Size: 7.6 MB (7630236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82f2e0053dd96bd8cd5b4a230c83c0a7e5257148a9de0bd3d0a3393bdbe84855`  
		Last Modified: Tue, 24 Dec 2024 23:16:09 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:741577e8e26a084526bba4c0ffc323f111b22c4cc35ea9a0cac2ea92e8a1b014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.5 MB (133502308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:258b9e966c898da2cf25bbeaf06417bdb05114c45627dd3333b7ec6d394c3cd2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1734912000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b5a5271e09aab30795789f051d2425121101b650637f36e772bdb80c62bb4833`  
		Last Modified: Tue, 24 Dec 2024 21:35:34 GMT  
		Size: 48.7 MB (48738917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd230c08c2a8f220f4a7754708d43b365ecaa32d038ae6429f10953c7ef0284c`  
		Last Modified: Wed, 25 Dec 2024 01:32:00 GMT  
		Size: 20.3 MB (20299500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0bb5fbe3b18f1821e5711e289a996102173dec864a8442d53c9dfe3b763817`  
		Last Modified: Wed, 25 Dec 2024 04:51:05 GMT  
		Size: 64.5 MB (64463891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7d9dc8b7dd6bb6ee676a4cc75a339fe24989d490c4e4a8c2bac81102a09696be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7637884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1234a4c33cf3dc5fdf65617a8f900b7ca3b63cd99b73997ba1ba047ce4f5d9`

```dockerfile
```

-	Layers:
	-	`sha256:f1bf8f0d44ebba11d199d0b4151d57a847547dad072372a129f88a51d97112ce`  
		Last Modified: Wed, 25 Dec 2024 04:51:04 GMT  
		Size: 7.6 MB (7630510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d4a9013c8d44395229ae2ce70484fc0d89b290409e786de5724759e8247d2e1`  
		Last Modified: Wed, 25 Dec 2024 04:51:03 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8d39deb50460a075e5ebaf45c7b356d7aa6926e0e4f6057a529fdf1828aa0cc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.5 MB (127522538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d34bcfbc7c0a8a66fb81bf7e930bcfc56b7ba0f6804bb489d2094768bd39d3f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:20c73c374f639d431be81d6bb3157ee925cb0c99f0451d2cd165921c444373d3`  
		Last Modified: Tue, 03 Dec 2024 01:31:30 GMT  
		Size: 46.7 MB (46679645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c705f22774d3593ddb8b7b982bc9e82a21362788a9fdc05272e21016ed52debc`  
		Last Modified: Tue, 03 Dec 2024 07:38:00 GMT  
		Size: 18.9 MB (18944460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a431a228225acac55e8846f5426c9cadb4b56af6577e4fc2e206ee3b42a287`  
		Last Modified: Tue, 03 Dec 2024 17:18:35 GMT  
		Size: 61.9 MB (61898433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f20d4b16748272026d508703532e62ad1f72e903aaef04835eddd35e1decfdb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b962f3d7ce0aa2602c4d46b70ba89b538cdeafedebdb91bd90afa6ec3a1251e`

```dockerfile
```

-	Layers:
	-	`sha256:693052ed3df2b83fde4fa0800280114d8462930cdccb7241a2ca16b00cb08dbb`  
		Last Modified: Tue, 03 Dec 2024 17:18:33 GMT  
		Size: 7.7 MB (7672703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db2a8779eafb68a0aed7fc5d3002a09e4385f40c35f0d5b8c3c25910c9afd1e2`  
		Last Modified: Tue, 03 Dec 2024 17:18:32 GMT  
		Size: 7.4 KB (7374 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d49da1c0ab574f1ee82048183744e7c4a20a58e2630de30576536864742e3b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139699926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1edb438449340747f9d5156a2a723ab8c85b0976e68c66f9498ee726545578dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9eb21918436f171705acc6e3469286cf27466cc89ea0d17c1699761c888e169c`  
		Last Modified: Tue, 03 Dec 2024 01:32:46 GMT  
		Size: 52.3 MB (52340851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937167b9612f87af0bddfb5d6d68eeee5ceeb8c8e8837f1f9918d7f613aa06c4`  
		Last Modified: Tue, 03 Dec 2024 05:40:08 GMT  
		Size: 20.3 MB (20251872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5eb80243bfd344e12541595272ea8f33faae6f5a77fc26a37baef8d6c8ea36`  
		Last Modified: Tue, 03 Dec 2024 11:52:25 GMT  
		Size: 67.1 MB (67107203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9b7a4e8e3b0b85db390656b6b8cca5621a23e152efdffe411a8f9d5475cd97dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7690453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bca429ac0be19736a53bcdd86c8110a6b3d096b8578d09b9e8cc4847630157e`

```dockerfile
```

-	Layers:
	-	`sha256:875d04078eea0a2500a40cad84a0a00885b05d146a2b6d2e56489b96860538cb`  
		Last Modified: Tue, 03 Dec 2024 11:52:23 GMT  
		Size: 7.7 MB (7683060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4fb854e6b21f3d5083b4dd91df66eed9eacff04eac2761219dc9f5beb7ad194`  
		Last Modified: Tue, 03 Dec 2024 11:52:23 GMT  
		Size: 7.4 KB (7393 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:f97a4184f96456f9ae21ca643b9d4d7c8c0c80119a619b63aed30aec7cd9b90a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.4 MB (144356587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca78dc99df8f96bd24e7db15afb4798413f6e19843a78587b4d6a008ee99ae88`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1734912000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:099da81c5d3f4771071b424bb19cc8bfc272821672d87e1978f2f206f3040f4f`  
		Last Modified: Tue, 24 Dec 2024 21:32:39 GMT  
		Size: 53.0 MB (53029057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26fe834ebc7804c0441c6204e790d670676126e97ebaad982188f420a6aa9d5`  
		Last Modified: Tue, 24 Dec 2024 22:14:48 GMT  
		Size: 22.5 MB (22510156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deb826681a9ebc8783590b4b5076ad7abcfca5c59d820cfc6e4d1027f2e2804f`  
		Last Modified: Tue, 24 Dec 2024 23:16:11 GMT  
		Size: 68.8 MB (68817374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5a9b37dd3faa1ecacdf995efc5378d4aef76a0e2c8815c78c9adb645c495ceeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7632277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d9c5fc90344a84dc93fd21caf61f753808fa9ca4126954ad266cefbeea3c445`

```dockerfile
```

-	Layers:
	-	`sha256:d4176d3aee41ac8297cff2ec7c65318a223c554c1a53a52c90b590ab98dbc90a`  
		Last Modified: Tue, 24 Dec 2024 23:16:09 GMT  
		Size: 7.6 MB (7624985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2bfdb5ac8660a8546888c6f358a1b17678bc0ed0bc11c382e9e3b8483e278c3`  
		Last Modified: Tue, 24 Dec 2024 23:16:09 GMT  
		Size: 7.3 KB (7292 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:c079df95e76a9a8894714db9abb0277635d739c02b9038af4c21f30993c8cd2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.3 MB (138304433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be3d5dd81e344958a5a800b0939a8ef1c7fc30d9d447fcd4586c175cb5aad950`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'mips64el' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e5a8d7ead1bc1f754b3a65ff28bee76dc2dc6179a698bf1402b64ec3d987e4e2`  
		Last Modified: Tue, 03 Dec 2024 01:30:45 GMT  
		Size: 51.4 MB (51439925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6d7c128c8894ab5647ca7070a8c53cc1626367f0fee2913a8ce5fe2237ac2e`  
		Last Modified: Tue, 03 Dec 2024 15:48:58 GMT  
		Size: 21.0 MB (20951581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddd6435addf48f219bf6a9a7272ed63c493377979c37d721428b6d2c65dab1f`  
		Last Modified: Tue, 03 Dec 2024 23:28:11 GMT  
		Size: 65.9 MB (65912927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ac901c44bfa9f9e8c10c0c7241b6e2071a9ce15aca6b3ff64884cc0a7debc7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 KB (7147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efaf51db1c3fa8cb7c637485809ed264d0f11848e68054597ad746478f6a6130`

```dockerfile
```

-	Layers:
	-	`sha256:67a2e9f6b9101e016ca82f90ddb239e70c70d069ab2d1ff8fe9468b7dfab7232`  
		Last Modified: Tue, 03 Dec 2024 23:28:05 GMT  
		Size: 7.1 KB (7147 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:29106e083d3f0884ff2ab67cab04de54b2948f989c84c1de72a1ceb5d72f2900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.4 MB (150416706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ec1fbf43792ca3ab0d994b9fbdf8d4c8fc7e96b90202e42e6e6c01520a25cb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5e74ce1d603959ee7e791ff530dd1c46ce3dbdbf2d00f3d3917cd370d2c2ca56`  
		Last Modified: Tue, 03 Dec 2024 01:31:51 GMT  
		Size: 56.0 MB (55955673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e3c1d8feca2b36465cdfb5b57d9969f0fb66fe43bf079a81607bc309440b99`  
		Last Modified: Tue, 03 Dec 2024 04:38:34 GMT  
		Size: 22.0 MB (21990810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f35d27e17f5faa7b717fcd51d2689cc9f5f0b57184433a4eae97a42f95da04f`  
		Last Modified: Tue, 03 Dec 2024 09:44:41 GMT  
		Size: 72.5 MB (72470223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d7a5f51f1d75eb637e939fe2c1d001071a9ffca3db92bd98f0f44b1414ddf061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7686565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be05632c83a4dc663ff459ace817ccabda153cf61714e31816283eed707acf41`

```dockerfile
```

-	Layers:
	-	`sha256:e80dad17cad41492690720cb23ab6f99daa18133ee238fccb5bfbdfefd17ab40`  
		Last Modified: Tue, 03 Dec 2024 09:44:39 GMT  
		Size: 7.7 MB (7679219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:413f4d207e490cadfa1567ed05b98441f383ecc08e32f7c8d9168196cbb75d3b`  
		Last Modified: Tue, 03 Dec 2024 09:44:38 GMT  
		Size: 7.3 KB (7346 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ac70c87e9381f52ce776562ae586af2726f3f43cef7a85c16385c81ea668c9b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.9 MB (142930571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192c6e313c3e79056edca61bdb94ec5ab894882dadd45c0b6ca8b7938f823a8b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1734912000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e1fe280a5056c1901421b5598ff050c78aa067b752ad527583fba85c589bb647`  
		Last Modified: Tue, 24 Dec 2024 21:37:42 GMT  
		Size: 52.2 MB (52167537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febb20153a9b4c7c97b49477bb7e12772fe5782559f417bb6517d244a48d7108`  
		Last Modified: Wed, 25 Dec 2024 00:18:28 GMT  
		Size: 22.6 MB (22603773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07fbd06dbc0259f8b92d4683dee4083fe7d2a755f0c0ab5b7d6848714d1ec49`  
		Last Modified: Wed, 25 Dec 2024 03:31:21 GMT  
		Size: 68.2 MB (68159261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1deb1d53abb5b2497f99707bf429f1e7394353b828e6180042524f08a87fcab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7637969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7a963a09f80f77dc5e607efb1fd69a71556171a3b95e2e6349a178eef8228d`

```dockerfile
```

-	Layers:
	-	`sha256:b4acacdb0de60835cf6eb931b0139b18df6c0200b4da3188db08206ba326a551`  
		Last Modified: Wed, 25 Dec 2024 03:31:19 GMT  
		Size: 7.6 MB (7630655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c7aa0c685a441410c3da89e021f02c99785fa3c91ab5cab3f7588232b8d1062`  
		Last Modified: Wed, 25 Dec 2024 03:31:19 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json
