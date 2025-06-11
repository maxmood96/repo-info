## `buildpack-deps:trixie-curl`

```console
$ docker pull buildpack-deps@sha256:1336d50a9dbd4899139228a50074d315732f8ccdd1b3dc13592eca5fb7db1dfe
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
$ docker pull buildpack-deps@sha256:a4c4524cf0a35057762c54346f1421c78d690525a63d46c728ce78c1d9250cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71772206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce98a44a7d44307bff605999e92b1aa745e51432911540c1f724a10ea8e4fd9b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:0b3435ddf0421631c0396c34acfc4d54793f2c51e2a8b92677402c8f9e0513af`  
		Last Modified: Tue, 10 Jun 2025 22:50:33 GMT  
		Size: 47.4 MB (47445410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3be3896271877b3e95aedbf07f86334bdb2f5374ed0d8dca30695208865ab49`  
		Last Modified: Wed, 11 Jun 2025 03:14:18 GMT  
		Size: 24.3 MB (24326796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:3373997a2b95beb78ca2bb6cf7a05c067b8efa8aee2ccc709d7b3a419fa5fef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4131423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:410de526bd1d6bf05cfd282f0cbb4a4904c4062580f30aef2aed9a8a44edfe96`

```dockerfile
```

-	Layers:
	-	`sha256:e3c408323f62458f04aba7eacab99facaaa861287bf036cbea1a2e2280cc98a0`  
		Last Modified: Wed, 11 Jun 2025 04:21:24 GMT  
		Size: 4.1 MB (4124542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90a9441034dbf63c8a844febb4bc8c0f8aa23dbe16948dfa5c3171aeec71cc10`  
		Last Modified: Wed, 11 Jun 2025 04:21:25 GMT  
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
$ docker pull buildpack-deps@sha256:91f921e9ac6db87ba836c96321c3a736884a8d9a413f5b2b37350e9ee9afb254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74615737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee201c7a25cc687bda114aac2aa4f9a8fbd349ff201703be98ad4852c332085`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:546a427a0109bbde3a869c6a4ff1ed90ec74768e7fd82dd00441608d83416632`  
		Last Modified: Tue, 10 Jun 2025 22:52:49 GMT  
		Size: 49.6 MB (49621528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1439ee882f07f6b24af6e46850d9521759d30430f3be41cdca454de5566ec0ab`  
		Last Modified: Wed, 11 Jun 2025 02:57:26 GMT  
		Size: 25.0 MB (24994209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:d9df3c0b997b4f677740658e772e78c961c2d5c039c388152a85695707021b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4120738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8967f4d31a292bdaab1afe30ce0b6d93f08a4744a0d3794b222534f48be8918a`

```dockerfile
```

-	Layers:
	-	`sha256:97321f2aed4f95657be9cad1245e3f112d505ce97a3077fe4d4b372b8763ebbb`  
		Last Modified: Wed, 11 Jun 2025 04:06:55 GMT  
		Size: 4.1 MB (4113837 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efa388c7db70a880bc5ddf7d9206e980cec5271edb2deae1011da52412e8e2c5`  
		Last Modified: Wed, 11 Jun 2025 04:06:53 GMT  
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
$ docker pull buildpack-deps@sha256:477fad43bdd6a2f82b63d3e9e76db9663226c146741e5029bb79197139de488e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76097193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb152ae3bb1affb848ee8f59609a009ec22a96dec9911d7ebdc92f6d615a6ed`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1749513600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1ffa7429d410cb8e2162450d6c2fc3a21121304db16d73a6b9feaa05000dde5c`  
		Last Modified: Tue, 10 Jun 2025 22:53:14 GMT  
		Size: 49.3 MB (49329768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588affbec95a011eae8d19fbc59b872f3d6089f972f16713469d6820e2e3fe6f`  
		Last Modified: Wed, 11 Jun 2025 02:51:36 GMT  
		Size: 26.8 MB (26767425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:trixie-curl` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:18de74f2e1840dce3b34f2675bd0fb2beebecf4e788b1638cb675f461b540d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4129791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:182d98dd9a6569e32b68f57db9c4d3db7ad0f369aca14911ce4710cfb4ea9751`

```dockerfile
```

-	Layers:
	-	`sha256:a29239fc5b7e0538fcda15659222d5569b3524d660be286c6c23c6ebdaf927d3`  
		Last Modified: Wed, 11 Jun 2025 04:21:48 GMT  
		Size: 4.1 MB (4122970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0457ff2a4cb7e3374085d8f52d17723e6c449c34e1586db5b77296ae8bc2df6`  
		Last Modified: Wed, 11 Jun 2025 04:21:48 GMT  
		Size: 6.8 KB (6821 bytes)  
		MIME: application/vnd.in-toto+json
