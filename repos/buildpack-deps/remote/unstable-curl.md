## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:aed9083a94462542e6ec7fbc421cf827839ed0154a01c944156b6f4aee2a8082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d4940b76f809da1197d06e221d76a16f154fd99910005a1c2f7651772d7125a0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77459604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd0377e771a8165686d7b01131699352a03f3100e1b93531a23ed77ab1db9361`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:29:36 GMT
ADD file:b10a84e4e404c6ca6a1a6782f9040f24bb7bfbb95055e8cd39600ef22a4a9284 in / 
# Tue, 14 May 2024 01:29:36 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:59:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a79fdf356ad40501c2429368bf029e9f2414f18b03d6fa40ddac5cebf750f95c`  
		Last Modified: Tue, 14 May 2024 01:35:04 GMT  
		Size: 52.6 MB (52642897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc1cdf2f53eab47078fb369ea2ed0807107650f4e0c9a7ff1cae9e9467eba2d`  
		Last Modified: Tue, 14 May 2024 03:07:13 GMT  
		Size: 24.8 MB (24816707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4a75e40ac7a1fe630bb010eb3eeaf49603ae42baa21a3fbd326475234464e0cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (72965445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faaa2fe6d5fb2ae8d118ecaf4966363c8704473c7d63ed143f17bab082e3ba3f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:49:14 GMT
ADD file:48ad2cec46f0edaca758532e477d58141198d71874a7a659465c7778bc242f0e in / 
# Tue, 14 May 2024 00:49:15 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:16:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:96c71f057932ff03c2e4c9ce93dc6ca864ede3a6ed0a0a4316465b6b244a70e6`  
		Last Modified: Tue, 14 May 2024 00:53:10 GMT  
		Size: 49.7 MB (49745150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3dc2b7166580d8b48f65e06b51724e39b263522cf4d0680077e2d9bb25bf55`  
		Last Modified: Tue, 14 May 2024 01:24:03 GMT  
		Size: 23.2 MB (23220295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3de2ae46aa0b2efb8696e5a9518df923fe96ce320e76ce36f19c5d315d084012
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69777812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f146c6bbfb73005fb9997c30d19b9aea16b5834cc583044ee0135a5c149cd786`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:10:01 GMT
ADD file:02154de0dc9450545487c68904a4e760ff1ce6b2170e0658abc5f63881b61f8e in / 
# Tue, 14 May 2024 01:10:01 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:41:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bdb66c06bd7989a8ebc0daa12fd841f7fcee2541fcb911169e2813963f822a18`  
		Last Modified: Tue, 14 May 2024 01:15:24 GMT  
		Size: 47.3 MB (47253384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189169cb3c2ae8c9630343a69b9fbd4a22a6c652a99ce0018ad4752718803357`  
		Last Modified: Tue, 14 May 2024 01:50:06 GMT  
		Size: 22.5 MB (22524428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7165d54684c4135ba4a78cc0fc078fb33baf96064b640e8d0337ec23cea6faf2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.0 MB (77025435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff9ae8d4cf485ec5646645406fa50958b32c6cc7774922b204289e5fba65e031`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:40:41 GMT
ADD file:65d77d3f6289af1318c696652b600f022ddbc3a1daaf105602e348ad91d2c41c in / 
# Tue, 14 May 2024 00:40:42 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:48:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:66334a1d5d0f0597e9440b0db265b333533e2fce7f5bb2d1fba09c85ef6cd21d`  
		Last Modified: Tue, 14 May 2024 00:45:15 GMT  
		Size: 52.9 MB (52930287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699aafb7efe9505bddcc73d0e5a54c28cf53e16271eae78e8e83cbc483d6a6bf`  
		Last Modified: Tue, 14 May 2024 01:55:32 GMT  
		Size: 24.1 MB (24095148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:096d378e86e558488df51202ba86ecc1f693252d82b109d16765688f522ec6f2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79483123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:263f53c61d9d563d5029e8cfb1ff491ef9403e36c79b25d2cdc90e928b6e7763`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:48:47 GMT
ADD file:e7eb6b079b0eae2716a306dfd153c88de0766961cbb0cbc2499648abc3b7bb7d in / 
# Tue, 14 May 2024 00:48:48 GMT
CMD ["bash"]
# Tue, 14 May 2024 09:07:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:241b052c0f57772eb9a56c460c88c133545f781291832042a8e20e0fd5b01591`  
		Last Modified: Tue, 14 May 2024 00:54:59 GMT  
		Size: 53.5 MB (53539918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137fcf033ffeba23f126575a61f0568479824add57544692806db0ea178f1a88`  
		Last Modified: Tue, 14 May 2024 09:17:13 GMT  
		Size: 25.9 MB (25943205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:eb7ac57ab97d938af38f1cc8b2bd22f98e562de90d4159c142197de225d2bac8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76341580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ea2c8543abcfddfd53575d84fa053c68b83b5134803bce1db79832d8e08232`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:17:23 GMT
ADD file:6ee5f04f14b1e874e152ce4477f27a16f4f4f6e4e49473d9e0d4f54bc8c7736d in / 
# Wed, 24 Apr 2024 03:17:28 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:04e21b74f69d4354ef0e677ec5dab4b460bf993f23d559662b8fd1e622263e43`  
		Last Modified: Wed, 24 Apr 2024 03:28:44 GMT  
		Size: 51.5 MB (51498447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9270daa8a7463a9ee3bd00970502d053092f544e14318daa6b1a128a03093d`  
		Last Modified: Wed, 24 Apr 2024 04:36:52 GMT  
		Size: 24.8 MB (24843133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:72b8bf372c37c39dcaae15721f9c6d237a4250a1b3a8d04880cdc1902f51f608
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83521460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a38354e5205110f751d5ab3755278ac1fb0a1b00900e2badecc806ced2ad3a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:21:02 GMT
ADD file:48cc1541210c6108c0251f6f008cd7e9eb30330f4f7a0e4ca8f13863de6afe2f in / 
# Tue, 14 May 2024 01:21:05 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:01:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bae7d269c4dd7d40de29faa635851f1c684cc32fdc792af4ff32efd2461c744f`  
		Last Modified: Tue, 14 May 2024 01:25:52 GMT  
		Size: 56.5 MB (56538197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba953fb3ef8f77266c250f5f1e3517eaee2b356a1467463a6aa091c29b3d81e`  
		Last Modified: Tue, 14 May 2024 07:12:49 GMT  
		Size: 27.0 MB (26983263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:2d71e44099f4aa392d0cf642f5fee30969cb1f140e417bb191651e88288a9ed6
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74993402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa00d9e6291279d45ac74db77b396697e9458d7d76fe4f9bfe1080541b518ec2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:08:59 GMT
ADD file:18cb19ec2784efee4339c923ec316987819836eb7aad9280180eeca7729ae78c in / 
# Tue, 14 May 2024 01:09:01 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:30:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e438edd6428d670b6cea990c6caad079c8929366cc17e63aaad3fad6d8aaa661`  
		Last Modified: Tue, 14 May 2024 01:11:42 GMT  
		Size: 51.0 MB (50961424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e0d23029d29d3802db61889c19c99463249e5cb15c8c9edcf99017419bbf7b`  
		Last Modified: Tue, 14 May 2024 01:39:45 GMT  
		Size: 24.0 MB (24031978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9d13b3b3fed7a5c88446c55e87f4cd26f81127cfada2b0a78434a934ed4c967e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77840902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd13938e979998201bdf409e7fd9c1432696ae28a2c50a7e76e28090a4625142`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:43:54 GMT
ADD file:34bf2264b5be5e585bc909c05f313cebb02329e956459b02e719a727804b5ef1 in / 
# Tue, 14 May 2024 00:43:57 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:23:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d8beb42479d9c358247f3312313f4b01304d06a9f4350f46669bc0340b164395`  
		Last Modified: Tue, 14 May 2024 00:48:47 GMT  
		Size: 52.3 MB (52293312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe716d1139dcfb0e4a0ac4867ff5d98684c037b80d0741511a7238159f33b964`  
		Last Modified: Tue, 14 May 2024 01:31:04 GMT  
		Size: 25.5 MB (25547590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
