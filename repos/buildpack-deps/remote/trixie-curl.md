## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:6121190b5899a089459e87634c5fc1cc319a9e904476c676d20e57ff734e644f
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
$ docker pull buildpack-deps@sha256:0f90a9fd5f37ce8b1f3a7d4007ccdf62f7bca4a9a5f91cf6f75fdb2c42033216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74855351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b83e7bd9c5b711dd090aab6ac0fa7a7fe1e1f65da6041bcd6bd76d9265e173`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d8e51f6b7dcdaee60f07f9a13a971abe1be9dc977d52d0849087118f80a1c7d6`  
		Last Modified: Tue, 10 Jun 2025 23:25:45 GMT  
		Size: 49.3 MB (49253859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f807a61ec306a45196094c9a44cffbe9d5d5a283a87c6e5c2469748ac3a19da`  
		Last Modified: Wed, 11 Jun 2025 00:01:30 GMT  
		Size: 25.6 MB (25601492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:af05b169f22ed00897ae9117325cc9076e8fe11c3667b88aef1c82d2a6f61929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4119128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc007121c4391ff7b9f33492683e86bccf6bbfdf6fcd33d60e167b599b07113b`

```dockerfile
```

-	Layers:
	-	`sha256:6695b4b2c73b2fffc05ac11b7d5f1764ebdac67b2a5ec88bb021d54c955dfe02`  
		Last Modified: Wed, 11 Jun 2025 00:07:16 GMT  
		Size: 4.1 MB (4112307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:270578706767bfa2a22a54a0e4aab4534c4589f01747346be6cab69ad3890a6f`  
		Last Modified: Wed, 11 Jun 2025 00:07:15 GMT  
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
		Last Modified: Wed, 11 Jun 2025 01:21:06 GMT  
		Size: 4.0 MB (4005795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:361c69732df08ef18feba6299346bcd61b7c58a79906c84bb42cd1c40688b1d3`  
		Last Modified: Wed, 11 Jun 2025 01:21:07 GMT  
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
		Last Modified: Wed, 04 Jun 2025 00:32:15 GMT  
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
		Last Modified: Wed, 11 Jun 2025 01:21:14 GMT  
		Size: 4.0 MB (3997934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ea7f6782e17917fae44dcdb021df86f0aa1da87dd1bda0fa429347c7d66efcc`  
		Last Modified: Wed, 11 Jun 2025 01:21:15 GMT  
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
		Last Modified: Fri, 06 Jun 2025 09:49:42 GMT  
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
		Last Modified: Wed, 11 Jun 2025 01:21:21 GMT  
		Size: 4.0 MB (3997971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7588e9a0b59c73be12308c6303e11330aa24e938154df39edfe2114c3d892f3`  
		Last Modified: Wed, 11 Jun 2025 01:21:22 GMT  
		Size: 6.9 KB (6901 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:3652ff309a7e5410507ca85ec721ccae8492ec8fda16b7cdf41cd1972a4299b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77520948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4bbe4a850306099dcbcdb090249d0acadcb849d90857f10dcad730682fb4ba0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:f24aa3f80422a60637035cbe1e280f72c031e00f6d803abf75d114fc69f38e79`  
		Last Modified: Tue, 10 Jun 2025 23:26:07 GMT  
		Size: 50.8 MB (50765612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b60bf3250137ff5f937387763b677cbdfc73f6e6d8cb191bcb236dadd350bc3`  
		Last Modified: Tue, 10 Jun 2025 23:59:18 GMT  
		Size: 26.8 MB (26755336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c0c42712feb0e014efd6e3fd92b576d0ab5b4c7071227b1e75e2ba962869017b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4116225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8072c4fd395d0e8559dabf201ee7935f9f9504492f3d656a2fc0939f25ba4a`

```dockerfile
```

-	Layers:
	-	`sha256:35b265ebc0f4b28fe716d076a63adcbdbf2ee042dab4a46d8ccf31b645e1d6ee`  
		Last Modified: Wed, 11 Jun 2025 01:21:27 GMT  
		Size: 4.1 MB (4109426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26b9cb328d990cc71dca701c22ddd299c22e4ea1af684294df329d317e66d924`  
		Last Modified: Wed, 11 Jun 2025 01:21:28 GMT  
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
		Last Modified: Wed, 11 Jun 2025 01:21:34 GMT  
		Size: 4.0 MB (4006641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3de3ea32636e3959cd8ea1d19e29ba953b268320ff6214959ad5b73fe33dc8c`  
		Last Modified: Wed, 11 Jun 2025 01:21:35 GMT  
		Size: 6.9 KB (6853 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:trixie-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:c29470dae93cdfc9a0ae9d5916334ac1e97e5794a14f737e71164f2c8ba544da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72680382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:102a07090901b179274ff19c14553f40824416c7ffd1b0edaa5cd3f63d8af061`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:183a50217c4846c3775204631f79c9cba563face97fcc3de4421f000af401588`  
		Last Modified: Tue, 10 Jun 2025 22:56:31 GMT  
		Size: 47.7 MB (47743345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:821f4f32e32d9aba20b46d2290a43e58210fbeadb10dd55306d3440511ee2020`  
		Last Modified: Tue, 10 Jun 2025 23:38:17 GMT  
		Size: 24.9 MB (24937037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:cc0c2b2fa1ac5e17480fa22983058d235aa3bc42f46dc37a5faf4955712c376c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4111651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c4dddfe249249a47b20cbdd9ed17b37e01eccffab57147174de2ace177dc16`

```dockerfile
```

-	Layers:
	-	`sha256:c0cd7ece6ba3cd31b1426da02d1f41eae73534c105e1d33a494352dacadb0d67`  
		Last Modified: Wed, 11 Jun 2025 01:21:40 GMT  
		Size: 4.1 MB (4104799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f84a662c84d10747289d75a6c0a7bba75eab90ef2fbcf9916759962a8659a13e`  
		Last Modified: Wed, 11 Jun 2025 01:21:41 GMT  
		Size: 6.9 KB (6852 bytes)  
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
		Last Modified: Wed, 11 Jun 2025 01:21:46 GMT  
		Size: 4.0 MB (4004223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2117ab1c8672cbd22c49e401d4a08c4185fa2a670856291dd82a15b5024cca88`  
		Last Modified: Wed, 11 Jun 2025 01:21:47 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json
