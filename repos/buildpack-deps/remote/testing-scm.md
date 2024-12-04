## `buildpack-deps:testing-scm`

```console
$ docker pull buildpack-deps@sha256:1a683724cd1481a99f1be814d9203d1225b731e173089e3e62c046780abf1ca6
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
$ docker pull buildpack-deps@sha256:da06b24525cf008d45f41cb668247eee87a08689df068a618d546916d6ae1c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139771011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ca6d8dd9a27942e7de592f7688c5ce9541beb0071fbb2c608ceb2bef3f6f6f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e4743b5a77e386ff2c8b73b5f4786349b4c3b4a5bba77f60a49c3b94a3b29584`  
		Last Modified: Tue, 03 Dec 2024 01:27:30 GMT  
		Size: 52.1 MB (52113554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4547041a33b6c57d94bf3840b901ad1987b2672b67b1e68ff564d9703716a01`  
		Last Modified: Tue, 03 Dec 2024 02:29:17 GMT  
		Size: 20.6 MB (20599021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46b5387da4a2f31c146885e44d705069d7906eee138ab3588a9fee7bcae723e`  
		Last Modified: Tue, 03 Dec 2024 03:17:15 GMT  
		Size: 67.1 MB (67058436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:a8a576689048442f9285b1e2d3b8e70de8ffdfb4c20c56d6e70985784cd861a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8be949d7ff95df28359fe769be1e7b26f6f2bd935fc6ca92743ef514696ee24`

```dockerfile
```

-	Layers:
	-	`sha256:d392955327241dbd4fa732bf7f7bf2f671035b7dff2ce50e2a7fd0802cc79306`  
		Last Modified: Tue, 03 Dec 2024 03:17:14 GMT  
		Size: 7.7 MB (7673471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68f3b7d42efb398b3cb47bbe501e8f1d88b26d69ba97707db98f4be1d3a213b4`  
		Last Modified: Tue, 03 Dec 2024 03:17:14 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f58998c164b872a995e8c2488d4449c575c973afdd5328339dce33bbaecbb6ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 MB (132678369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996871804936b7a5ef88a59edfb5ff11a638889c5c06ba22cac89fae0dcb7aaa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:5bc3ae687a9226ba4c006ebae837bdf4fc9ce21a92c2280c2fe34aaa801bc170`  
		Last Modified: Tue, 03 Dec 2024 01:29:30 GMT  
		Size: 48.7 MB (48667592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f104f4b59037c21344a76456c37d0109c126d6df42220396b04d3aaad3cdf4`  
		Last Modified: Tue, 03 Dec 2024 05:25:08 GMT  
		Size: 19.6 MB (19608590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b47bb9243d7017922dcc62de48c63d8cfb54c3c1e685c3e38d7cea429218c0e`  
		Last Modified: Tue, 03 Dec 2024 08:42:18 GMT  
		Size: 64.4 MB (64402187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9eac8d18f0d619b921e87fb696ec7ddd1dcd909048886f90f96abca7fef946bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4899ab3a5d47d295306707e3a125b9526e97ba5ee2e8421e14431b21b28ecf7`

```dockerfile
```

-	Layers:
	-	`sha256:24d68fa4daa45f024376e555272bf77b2c06ea5f777b7d93ddb7878d49d60ecb`  
		Last Modified: Tue, 03 Dec 2024 08:42:17 GMT  
		Size: 7.7 MB (7672931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c14de663ae0734d8f5151fdf3a515dceefedcce57432d1cd70a5f5e9a49cc37c`  
		Last Modified: Tue, 03 Dec 2024 08:42:16 GMT  
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
$ docker pull buildpack-deps@sha256:719ff7c42eefa5f6811c72f3d92c194797cadf5b65455e346d3cb3e9b7705616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.5 MB (143544476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1e3ad359f205a750b81d425ca9d2f51cd5eeefadb8cd309a411bc9397fd7e21`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1a5aa91e83fa5cc5d15dce96bbfdc6d2483a659fdee76a341522b60ff87dc849`  
		Last Modified: Tue, 03 Dec 2024 01:27:32 GMT  
		Size: 53.0 MB (52956284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79565d36fc8ccc76d07975f07b5cf916b84627952cb6785e10e8d0301cc2acdd`  
		Last Modified: Tue, 03 Dec 2024 02:14:48 GMT  
		Size: 21.7 MB (21726798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad782586fddb10041571d568c827bae913dd109647631cce2fe893ecfe4b9488`  
		Last Modified: Tue, 03 Dec 2024 03:17:11 GMT  
		Size: 68.9 MB (68861394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:535718f08215a34be3c30316648e76a757427791ab2fd9e70495b1e6a5e58b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7675497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fa66fa78d05f3be959bc718b8f26030aa9c1a00679251a79660446336a3ffee`

```dockerfile
```

-	Layers:
	-	`sha256:d64db0dc614cd414a9d0e4644feae150e0f1e8c7eda3e0b58ee2612315e3f67e`  
		Last Modified: Tue, 03 Dec 2024 03:17:10 GMT  
		Size: 7.7 MB (7668205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c80bd9ae34e9602bb84c05a4ddf8a0caa783edcbe6ea469738ea67b68efdc55`  
		Last Modified: Tue, 03 Dec 2024 03:17:09 GMT  
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
$ docker pull buildpack-deps@sha256:7cbdb5aaa9bdb372290824b75edeb47013f021005307c350766138665edeb373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141874600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a0fb9ae5e7d29b1b0cf491d5393a5ac639936cf966ffa23da517254253e92f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1733097600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:33a597a4ae2eff9c605f460e3e4517cc31e0999c816baef2a6ee6ab3da5c61ec`  
		Last Modified: Tue, 03 Dec 2024 01:31:39 GMT  
		Size: 52.1 MB (52069406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3f8d29d82faa501360f9fefd446cacd0bf557a29588aa4fc37c50e750000a3`  
		Last Modified: Tue, 03 Dec 2024 04:09:18 GMT  
		Size: 21.7 MB (21710113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0425f6ff87e23ba6d559005a68cf32aede99d5bc0259e82af81721ec006b580`  
		Last Modified: Tue, 03 Dec 2024 07:56:17 GMT  
		Size: 68.1 MB (68095081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:39a2f7b3b1fb4e73530d08d088bcd30eafd6d5d786bc9387b653d8f8d8b3ba55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49c702e9c9410935d4299af789c96c665239bfb53818cf765a6699f89a9cca41`

```dockerfile
```

-	Layers:
	-	`sha256:a366d37dc4c5fab3169fa8005fbfd07ec0cdacfc63c176b0074314ab29054942`  
		Last Modified: Tue, 03 Dec 2024 07:56:16 GMT  
		Size: 7.7 MB (7673077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13d3948af2dd637e8a6e5a87efaa2a0c83e3771e6c96a7300299f8a4fa0515d9`  
		Last Modified: Tue, 03 Dec 2024 07:56:15 GMT  
		Size: 7.3 KB (7314 bytes)  
		MIME: application/vnd.in-toto+json
