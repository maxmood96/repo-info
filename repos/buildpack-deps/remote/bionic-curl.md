## `buildpack-deps:bionic-curl`

```console
$ docker pull buildpack-deps@sha256:c85f85a3eaa8f708be0c4ef31c11a083d2c1a3bd466820693dc5eea775835002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bionic-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:e1d8c4faf8376dd4483913b372086027b131dc7be7d4675692597fc0a5966678
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 MB (36372771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1129fbf08223c38de16bf8bc67c4b46cf546cee23a07897342a6b06bb8c10ebf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:26 GMT
ADD file:f554512cb0acad99508554656767804e4821ece488fac0e46fd2c643a39f7021 in / 
# Fri, 18 Mar 2022 05:30:27 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:38:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:38:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:11323ed2c65349758e68a03a8e43825ec263dc9790daea93cf83b18ad0703109`  
		Last Modified: Thu, 17 Mar 2022 11:55:05 GMT  
		Size: 26.7 MB (26708634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222ef3f2ac944896d21cb971be4b7ec028ac826242cd0451df060b0b4412b92f`  
		Last Modified: Fri, 18 Mar 2022 07:08:55 GMT  
		Size: 6.6 MB (6641832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3f005ad8fda9d934f3bab809914d7cf447e57835543823c59da423475b8f58`  
		Last Modified: Fri, 18 Mar 2022 07:08:54 GMT  
		Size: 3.0 MB (3022305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6f391663368344db81086792af6820993bd3b16ac14ef974f1b7de89a299087a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 MB (30605088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5780ee29340d6934bbe79b88fee887bd917a237cd8351b858b8f8cb78d32057`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 07:32:19 GMT
ADD file:05014e7be574a8703e7ca668f8ff20d708f1860234bc44e3ef9e9a15193ea2c2 in / 
# Fri, 18 Mar 2022 07:32:19 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 03:07:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 03:07:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d423dfb8c4fe22914d518a0a7c648903c4159e75b2ddd41c2d7dd27c5af71078`  
		Last Modified: Fri, 18 Mar 2022 07:35:55 GMT  
		Size: 22.3 MB (22308133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59dd41a6c49eacf0df81b34978f371986d045163bc627fc8cc72de7188772b43`  
		Last Modified: Sat, 19 Mar 2022 03:40:45 GMT  
		Size: 5.7 MB (5712348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd796a264aa4c81e3c709b9f64a9058add3ff5a5d6182545c52efe99ffacdc7d`  
		Last Modified: Sat, 19 Mar 2022 03:40:42 GMT  
		Size: 2.6 MB (2584607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2a58612831945616a0bca6b4b6858c38c8bdfcec7eadea2fe0577d91285bd342
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.4 MB (32382303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734b8511b29340aced3d2bfca203681e7237f9c172642a586bc0337315bd7cb2`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:40:54 GMT
ADD file:4e0e00a64dd88d531092dae4e900f36acb9c48c652d278ec0cd32aef9fffb42b in / 
# Thu, 03 Mar 2022 19:40:55 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:06:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:06:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:20d796c36622ded7b79b53bfa23d7db4140fde7ea3842825f9aca4070b429317`  
		Last Modified: Thu, 03 Mar 2022 19:42:21 GMT  
		Size: 23.7 MB (23729651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b00c8ed3e482790555b6ba75dc2fe88a431898579874f982bd42af6e94adaca`  
		Last Modified: Thu, 03 Mar 2022 20:16:15 GMT  
		Size: 6.1 MB (6082527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:355a1859624fa4241536a77dd88b7f379d0cfcecb8c9d1647065d1fce7976682`  
		Last Modified: Thu, 03 Mar 2022 20:16:14 GMT  
		Size: 2.6 MB (2570125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ce2dac3e85153fabaaab1097f98ad0ee178203f6acb8668db724e6732f86b031
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37344500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5d7542bbb25c7bf7d167963ad6ff61209be96d0899ae23fd503fb4d741eef2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 10:41:23 GMT
ADD file:72f05c1b10aca0acb5e79b003217b981354d67a2f72a45a5a48a74d5a22d8a52 in / 
# Fri, 18 Mar 2022 10:41:24 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 14:35:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 14:35:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:2ae2a3052b0bf32822826824df976f36386fcf8a79f3777f41da7a64101a1603`  
		Last Modified: Fri, 18 Mar 2022 10:42:30 GMT  
		Size: 27.2 MB (27162241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7b56172011c8d88198bee93c2bf6f3b33ad52348cb1380b5cbb47138aa4044`  
		Last Modified: Fri, 18 Mar 2022 14:49:48 GMT  
		Size: 6.9 MB (6930126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed6e7f33485b705fec685d6fbe7cb0623696f9ffab68a00b24fe2dc017b4eff`  
		Last Modified: Fri, 18 Mar 2022 14:49:47 GMT  
		Size: 3.3 MB (3252133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:38fc2634989953421c3f9bf864043f697ad36cfd216bd51037a86bd3dc8b57f0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.2 MB (41213952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf25a66da5f1a356e0181d69942adcfd10fefcb7f65d63b03c72df2f4a2481d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:47:57 GMT
ADD file:512f577cb3b73f892801365276edc7835b0fbed63fe39c4e98c86264d363163b in / 
# Fri, 18 Mar 2022 00:48:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 06:09:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 06:10:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:37a959c2edf986d1489b0000a2dbfecd72195cde6524f2a6545bf3c5d66f6bac`  
		Last Modified: Fri, 18 Mar 2022 00:50:57 GMT  
		Size: 30.4 MB (30438056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1830b6c456b7475c45d963eda213b02483fc132dc1a3a8a912694395f1556c6`  
		Last Modified: Sat, 19 Mar 2022 06:49:09 GMT  
		Size: 7.1 MB (7056588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f35c7c52bcdc240668649aeed659e09476496c4c7a0fa05fcbdb7bed19e76d`  
		Last Modified: Sat, 19 Mar 2022 06:49:03 GMT  
		Size: 3.7 MB (3719308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bionic-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:949c57c8c8fafc767f055de2cbe1ca35df62bc3c7ada393592c30484a5da8531
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.7 MB (34672987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6b0eaee4e991ed0d5187499e72de418fac57c6a11f5776637749564be8520cd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:37:02 GMT
ADD file:ca83c77547f5f41417a9bcad24827780f3cecda3aadc05e3ea075ef651e7a96c in / 
# Fri, 18 Mar 2022 00:37:05 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 17:05:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 17:05:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:19966aaba2fa737074d039f29b54f413d837daaa9d85f02bc54eddd7d645b73c`  
		Last Modified: Fri, 18 Mar 2022 00:38:33 GMT  
		Size: 25.4 MB (25365461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f707de7995f967781fe849ea5a655fcb09a909fd6fb0b137984e23c20e247748`  
		Last Modified: Fri, 18 Mar 2022 17:14:33 GMT  
		Size: 6.3 MB (6332555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b377478018a8c1dec3ff1d3e1c0d8db2e042e1ab1fe80f7f615a0f777ad6d4`  
		Last Modified: Fri, 18 Mar 2022 17:14:32 GMT  
		Size: 3.0 MB (2974971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
