## `buildpack-deps:hirsute-scm`

```console
$ docker pull buildpack-deps@sha256:fd1909c610d4669f53eb60263e8751a9a3eac421cb518b59c6f5d039805b6955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:hirsute-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:69a1afd79969a2b3ecb464f3df968aa2cc3beab0f1495e9bede89f09ac95f27f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84338360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9c8d0198a6a8352b0fd8a85b5869bf53af91c497868670db4b65df2af5ccb3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:25:37 GMT
ADD file:cfcb96e25bf4af2949d0c04953666b16dca08216ded8040ddfeedd0e782c6ddc in / 
# Fri, 07 Jan 2022 02:25:38 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:11:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:11:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 07 Jan 2022 03:12:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:318226705d6bf4f94a70707b917c9bea2190a83f512b1c257dffbb691859831e`  
		Last Modified: Tue, 14 Dec 2021 13:10:17 GMT  
		Size: 31.7 MB (31703311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:667d72c9494cdc9bc5e6e7a580bcecde40eb7a16e7a4c41edc1fe489777182a6`  
		Last Modified: Fri, 07 Jan 2022 03:23:54 GMT  
		Size: 5.4 MB (5428552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6069191775651f25c106da8afc7eaf4f45a50d8b3eb5297919a55d422a2906f`  
		Last Modified: Fri, 07 Jan 2022 03:23:54 GMT  
		Size: 3.7 MB (3661779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396aa8e411f33b10d4eca2b45f27a1465828f7bc8bca691c060fe8aa86d81160`  
		Last Modified: Fri, 07 Jan 2022 03:24:12 GMT  
		Size: 43.5 MB (43544718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:hirsute-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b3124d19edb167b0c3fc5e73a2bc783af182ac47d890a70d16ccfc20ad5f0b6e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74813106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c567fcbc04b3a91f70c022d150de1ab1337517961d65059e95e6dc991693d23b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:26:48 GMT
ADD file:b5bafdb9006674a167988c876664fe5c9986ad3472147327f21401be96959a6c in / 
# Fri, 07 Jan 2022 02:26:48 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:59:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 07 Jan 2022 03:00:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f72a97c294933ef5ddaab06415361fb5ebd9a11c5a2652c06e97c5c7e6ebefaa`  
		Last Modified: Tue, 14 Dec 2021 13:11:38 GMT  
		Size: 26.9 MB (26860386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3277394abdbd97a032d5030e64fbf0c4d66e68fa2bd73f13e9db50f1c1d578`  
		Last Modified: Fri, 07 Jan 2022 03:17:35 GMT  
		Size: 4.9 MB (4859364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c788c48d6b28a3708429f2a4d38683ec614ea0e400a23423ee1c428fafcf99`  
		Last Modified: Fri, 07 Jan 2022 03:17:33 GMT  
		Size: 3.1 MB (3138881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dafef7ab4ca009713965146724e2a98c47ee81df7793a143c7d86b4dea38f393`  
		Last Modified: Fri, 07 Jan 2022 03:18:14 GMT  
		Size: 40.0 MB (39954475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:hirsute-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:76f6e63a7f4f923d787cd4f9e0cea2697fc9ac999a8311c1144c7f71a15d2c01
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82542411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a799b41fce3cbe2328db1181d3a3b06e98e5b2238b96369b91ae5a59e92709`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:53:53 GMT
ADD file:53760a4a864d7c22beaf50ceaaceb7114cf6e4d285c9c4e41bddcb4ee83a71cd in / 
# Fri, 07 Jan 2022 01:53:53 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:22:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:22:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 07 Jan 2022 02:22:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a2edff5d3cccb200e40a203e356b5409a32f6982fc3cb50d5dfa39ecb3402d0f`  
		Last Modified: Tue, 14 Dec 2021 13:11:05 GMT  
		Size: 30.2 MB (30175274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31962c7a0c42f9a633a42d699ae0804bb7a2c41af84d17c2c05bfb484d764139`  
		Last Modified: Fri, 07 Jan 2022 02:30:14 GMT  
		Size: 5.4 MB (5401501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03777fa5f65f5eadb5c1582407dee053ea4f82f736924b111656d23be4b41c37`  
		Last Modified: Fri, 07 Jan 2022 02:30:14 GMT  
		Size: 3.4 MB (3432097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a32b07510544c269582c542e5a31c6dbeda6f738f9e6ae11630680ad53ee21`  
		Last Modified: Fri, 07 Jan 2022 02:30:31 GMT  
		Size: 43.5 MB (43533539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:hirsute-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:a791c0b0166313a207d5a49ccc58d4a62e2a3a2ca79eff33a7062880f6efbbc2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.4 MB (97385974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528e5ddca30e12835808044c29a609bdacc890ce0dc522ef29eacb03cf36ec11`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:20:30 GMT
ADD file:9356fd6fd5fe8e2698a7935a4f9e731784a123135fbbac56c0a64aba4ff055d8 in / 
# Fri, 07 Jan 2022 02:20:34 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:54:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:55:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 07 Jan 2022 02:56:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9e0f94572fe4babd7bb8b4026de5bab1243bfc425d3ef7113aab8ad7c891c73f`  
		Last Modified: Tue, 14 Dec 2021 13:12:16 GMT  
		Size: 37.3 MB (37256256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2212a7e701dccfe85f6420d6aca09f1ff394ab0937774e0bebd52230534dd4eb`  
		Last Modified: Fri, 07 Jan 2022 03:11:58 GMT  
		Size: 6.2 MB (6154815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559dad0985e62d3f24058dac581cc0c0b66b02c48da87c36de4efdc5eee32cfe`  
		Last Modified: Fri, 07 Jan 2022 03:11:57 GMT  
		Size: 4.5 MB (4523566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be97f8c528ce8fb34533212d2dd7a34be2fcc9b2f941e1be0ae3f9878d744fe7`  
		Last Modified: Fri, 07 Jan 2022 03:12:19 GMT  
		Size: 49.5 MB (49451337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:hirsute-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:e1d6da7ee78574de9c37442c506601ee07c28f63ecb9a4f5dd709d3b25817330
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75594097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:977e6e5b9957345b6ddc84e884dcb20aed98055fb903166feb06641f99027ea9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 02:18:08 GMT
ADD file:88bfbe1378489e66f6bc7226898a5fbf2fa4921a2a9f8368035d39f3f9e7879e in / 
# Fri, 07 Jan 2022 02:18:09 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 03:09:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 03:10:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 07 Jan 2022 03:13:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a42cee3150e09146966460b6ef66d449ef9ab179df8c79c79444cbf84185ca45`  
		Last Modified: Tue, 14 Dec 2021 13:12:53 GMT  
		Size: 27.1 MB (27142124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389220f2d755d833a1bd50839fb34a27ea51d43c416b72fb22b47cd1a722e28f`  
		Last Modified: Fri, 07 Jan 2022 03:50:06 GMT  
		Size: 4.9 MB (4944481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b9a26a93f46a4255ee80af820d9ecbb928cf6ea3ea2d8691b706011ef7771b`  
		Last Modified: Fri, 07 Jan 2022 03:50:03 GMT  
		Size: 3.2 MB (3177901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1c1eb132e2137abcee4240cab0f3dada4e7825f5ded5652f905673986b7cd9`  
		Last Modified: Fri, 07 Jan 2022 03:52:03 GMT  
		Size: 40.3 MB (40329591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:hirsute-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:431f00ff6c4e76b8bbfcac16f2631c71e0c63df334732d3a259335765ebf6874
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.9 MB (89895673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14385196855949ddeb27eb912e7daa49a4893e60a9177c800bd9da164723317b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 07 Jan 2022 01:42:31 GMT
ADD file:0ab8d0c606111287c48ef013f6e2c33f36b1f35018d55a975462a5bd8a3ba1d7 in / 
# Fri, 07 Jan 2022 01:42:33 GMT
CMD ["bash"]
# Fri, 07 Jan 2022 02:05:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 07 Jan 2022 02:05:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 07 Jan 2022 02:05:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d7416c72715444586e1570693d4643393f777728e1eebec0c79ccefc15b81acc`  
		Last Modified: Tue, 14 Dec 2021 13:13:27 GMT  
		Size: 32.5 MB (32506835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf665ad123cb3baa74f17cff930e68da839c4edc09fa7e6ea0835e3d0504b33`  
		Last Modified: Fri, 07 Jan 2022 02:13:17 GMT  
		Size: 5.8 MB (5801283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0848f444c8f31a00cf6a98c8ee0c2f3c99196cb7fcfcf7ee620c48097d9200f`  
		Last Modified: Fri, 07 Jan 2022 02:13:17 GMT  
		Size: 4.2 MB (4185250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da65a952aaad2359a9e37da775e4141ca4a0dde6a7cac3b41967a079025ec62`  
		Last Modified: Fri, 07 Jan 2022 02:13:30 GMT  
		Size: 47.4 MB (47402305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
