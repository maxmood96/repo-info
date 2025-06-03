## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:b5eb2e8cfa7c6d43bc178dc0ddd86ace9840bf6dcf8aff7c5b7cf17d757d08b8
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

### `buildpack-deps:trixie-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7068a13c401f297719a4c15b8bc738c13a16505f90d3e4cee3cccb491c095a8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74830659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83644fa2676c0f077a7f4b2854fc68303a8932ef031bba8c91f818a9a5fa66ae`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073c3e094f775042a2296ed99ca159904c7ae19127cddd6dc0e02dfeff3ac66b`  
		Last Modified: Tue, 03 Jun 2025 13:35:19 GMT  
		Size: 25.6 MB (25583751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:30dce5b86276ea1ab5a19122afb9965a92bb003e8a6663e32bce716ada2de982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4003262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc63778a9addc9223df451d73e626c40d5d433c7fe93fb8147a7adc496e8483`

```dockerfile
```

-	Layers:
	-	`sha256:127f75efa84446233bf62d055f1a5ef2c037fc1d489ef29ca240502a2cbd59db`  
		Last Modified: Wed, 21 May 2025 23:20:51 GMT  
		Size: 4.0 MB (3996441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd056a7aa68ae459a1319b4aaf16f5c0dcecec2360a0ee6e62da52ac4c9da77a`  
		Last Modified: Wed, 21 May 2025 23:20:51 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:585a429b1204e8d5322950a627ba98ae5c626c4dd86b819038ee4399d3eccce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71765703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:323b1460368e6acb22678b90dd050e10118f26a05bb717e3d55c033026f4ff12`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9616f5c2624aa57711d4d3a917ef21ea33c33b9e29ed21732abc6456aa133801`  
		Last Modified: Tue, 03 Jun 2025 21:52:52 GMT  
		Size: 47.4 MB (47438143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fced245b3861daa32a8eb96fca42f40c6b8763a3cff659d7638f85cead39fe0`  
		Last Modified: Thu, 22 May 2025 01:15:18 GMT  
		Size: 24.3 MB (24327560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:7238573960e402a673ce8f7d7d70b385c16ac8441e80177f2f5ec46cc32ffeea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4012676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d960dd9bcf376f59f433e8f50ecff15b165bcc313710ee74e616156b9be57f2b`

```dockerfile
```

-	Layers:
	-	`sha256:6dcd3432a4cd69297ddd334b9125cc7b5e9fac39bbc7cf0256772534b0e71e4e`  
		Last Modified: Thu, 22 May 2025 01:15:17 GMT  
		Size: 4.0 MB (4005795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:361c69732df08ef18feba6299346bcd61b7c58a79906c84bb42cd1c40688b1d3`  
		Last Modified: Thu, 22 May 2025 01:15:17 GMT  
		Size: 6.9 KB (6881 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f43b438d47b3e1d34325502886cb7fed2ffaa769b91299237732697fcec0dbe5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69283408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fd834e6423fa8b2c1c204f34480295e808f8d4501c52436228bd9cd10fc841`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d82ad715078dca1bd38ac71d3c9c872661d1bdfae377c84300033db7bf3581fc`  
		Last Modified: Wed, 21 May 2025 22:32:07 GMT  
		Size: 45.7 MB (45690818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e80b8be2756aeb2756ee1709c45d1af8640bfca2b89a56244b22bcddaa053da`  
		Last Modified: Thu, 22 May 2025 02:30:07 GMT  
		Size: 23.6 MB (23592590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:eebd1a442b4be1c560d43e383d800ca22975a5b236fd89c5bb34f47a19aee2ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef129aa5f2e40c2312060618a4ea6e9040d936af49c1af63e6e62c6735c46da5`

```dockerfile
```

-	Layers:
	-	`sha256:cf8853896c79dc745e5b6db111fa374eb9c18a8f16e0a9187ae8a7249d9d5d68`  
		Last Modified: Thu, 22 May 2025 02:30:06 GMT  
		Size: 4.0 MB (3997934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ea7f6782e17917fae44dcdb021df86f0aa1da87dd1bda0fa429347c7d66efcc`  
		Last Modified: Thu, 22 May 2025 02:30:06 GMT  
		Size: 6.9 KB (6880 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:964673d1a4e5048d51c5b04eeccbb8250986440ffe36105c5e9633f7dfb92f05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74600134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e10ff222af52107ffea11d64987f45a1e1e7f241baade80f4579327acf23122`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:397826b9fe635f12caff1a603eb12c37426a5b3dc563e0adff2debff0c68a6b0`  
		Last Modified: Tue, 03 Jun 2025 13:47:15 GMT  
		Size: 49.6 MB (49618294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b925a0b1aba64c2f9934b5b752199fa927f08300fc82c456fa922c4303a06f43`  
		Last Modified: Thu, 22 May 2025 02:48:53 GMT  
		Size: 25.0 MB (24981840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:460e6eb8e7f905b05bf7aa9ecc5f19b8da1a8eb0cf29443650083be15134e8bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4004872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f0ecedc0e4fbacb56fcad42199f1f48fd4d4cd0186ea5f00603ca6e446fc02e`

```dockerfile
```

-	Layers:
	-	`sha256:5b22c33ffa4b71ceb6b8699d45585d127a84a8ae42c137be1a434f29a4fa1b3a`  
		Last Modified: Thu, 22 May 2025 02:48:52 GMT  
		Size: 4.0 MB (3997971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7588e9a0b59c73be12308c6303e11330aa24e938154df39edfe2114c3d892f3`  
		Last Modified: Thu, 22 May 2025 02:48:52 GMT  
		Size: 6.9 KB (6901 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:08e20e1b6588b122c336608d933dc24ea4ced2196252f951a6e7483d186814f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77507096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10e4bc89d31ad4149e68349c67fc4f470f8b8a8968f5b0d125510f8aefdd47c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7e1acd19dab9f7ab62b7570b85e71035e78cd9d9b9bff975df4b0a635578c7be`  
		Last Modified: Tue, 03 Jun 2025 14:04:15 GMT  
		Size: 50.8 MB (50761280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24ada90c6b3f67e8ac11f8d9700e1fbeb5f64ed848c2ef5d89e89c3d1161d7e`  
		Last Modified: Wed, 21 May 2025 23:19:58 GMT  
		Size: 26.7 MB (26745816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:f994515d62f455ad16004599055fea85c1f2770a865b115ed127f4223e8c3946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4000359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1825fbe5843560a58ffa256a21502d84e39f841c9210dec5d074591cb746f761`

```dockerfile
```

-	Layers:
	-	`sha256:528b64fdacca13a43986cd6a12b8350a7c594980265fbc2c6da4314dd6e78380`  
		Last Modified: Wed, 21 May 2025 23:19:57 GMT  
		Size: 4.0 MB (3993560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9191f35729fd8c05e8ed6adadd9d57acd0b16adb56917cd1175ac13468b4f462`  
		Last Modified: Wed, 21 May 2025 23:19:57 GMT  
		Size: 6.8 KB (6799 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0b4c18fe55aec475f12ef6cbe6a6e74286ed2c605db9d1aed09ff0878cc6cf7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80046521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6232cd1f7b3b204a55f9ddf72fc3cce5c2bed6f1eaccca5885c408b36dba6f20`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:25dfffa4126a91eb76c700c90bfdc9a9e15f34c7438a81f16c8a6999bbde6e45`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 53.1 MB (53080544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e139263efe3c22e2cdab37e8ebc2c1a1759b3b3d0c9c98b6becc0fbbd0bcf2`  
		Last Modified: Thu, 22 May 2025 07:33:02 GMT  
		Size: 27.0 MB (26965977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2a3708d4be3e1e1d018c135baec5906a710f5b0f1089627f069b54891ac7aee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4013494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8509cfacd4f2fe750be6633184bb693054abadeef660550094f81495a4b8a4f`

```dockerfile
```

-	Layers:
	-	`sha256:c66a374556073b845864b8f7b3f37a4f16dfec5346268bc1a3d52f27bffebd3c`  
		Last Modified: Thu, 22 May 2025 07:33:02 GMT  
		Size: 4.0 MB (4006641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3de3ea32636e3959cd8ea1d19e29ba953b268320ff6214959ad5b73fe33dc8c`  
		Last Modified: Thu, 22 May 2025 07:33:01 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:5e8a6323c6da70a665a0c5413e28153899e4eccb896a92780e805a909a31b8a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72649005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f38352c775944087262b83841025b54d353ec9df223192ad78af9a2823a9a9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:c83c5fa20952cc8610d790073e97537e7832127593042fa9c620fa910fe6f6b9`  
		Last Modified: Tue, 03 Jun 2025 15:26:09 GMT  
		Size: 47.7 MB (47731411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bd8670e232ca11355ffc7ddcb280e00c712f98c6d6ef1c601d041012816cfa`  
		Last Modified: Wed, 21 May 2025 23:26:24 GMT  
		Size: 24.9 MB (24917594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:5487b90124b64172b4b3d78de8b5dcfb51550c1f4b37ed19ae645c9944640e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3995786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db71767e7116d80a232e4589f034c8fb7cc0c683632bd7e748dcb1ff2d4bb730`

```dockerfile
```

-	Layers:
	-	`sha256:e2303bcdbed8af296176ca76f8b7599e01489b002661f6f2609b5d1b2b3cefcb`  
		Last Modified: Wed, 21 May 2025 23:26:21 GMT  
		Size: 4.0 MB (3988933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29bd6042780dbc076d553ea25fac1ab9123c28b90ba1e9e716e1787509280f7c`  
		Last Modified: Wed, 21 May 2025 23:26:20 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:c66a6d2cb9e68f7743bd7e1da2ef77c7db87a118095fbd97745f32fe93bd1eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76080001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25b4691d06221580f5c9c32e241d67816f5d76f5408e4c7ba86299c8d4f268dd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:71c8524b25c34592c256fbae9045d0ade48f5e9889d37c5b2190092fa9017d48`  
		Last Modified: Tue, 03 Jun 2025 15:34:07 GMT  
		Size: 49.3 MB (49322227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8645228c4b06e89bef4ee7caae64a6417dc0f102985c8d7902876a160465531e`  
		Last Modified: Thu, 22 May 2025 01:03:11 GMT  
		Size: 26.8 MB (26757774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:36255b67745ead1c05946b6042f04c536df6efbd23e60ebb3c83c2efc06a480c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4011044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834bbb46505a035638d988c7819373ca265e810e1312b46cdf5a63d1bef69db8`

```dockerfile
```

-	Layers:
	-	`sha256:762de580b6a9b2edb3a75913673b034bd358822166034a7291b84d3c76880b80`  
		Last Modified: Thu, 22 May 2025 01:03:11 GMT  
		Size: 4.0 MB (4004223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2117ab1c8672cbd22c49e401d4a08c4185fa2a670856291dd82a15b5024cca88`  
		Last Modified: Thu, 22 May 2025 01:03:10 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json
