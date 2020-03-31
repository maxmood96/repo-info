## `buildpack-deps:sid-scm`

```console
$ docker pull buildpack-deps@sha256:5ad28b903d9996ac5eb6a758aaa5b73a6068add81431e9405ff27a8e2bd8bbdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:sid-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5dc86e27860ded32525d666822429ae0640923aa182ae919d5e5417d4d40fd3b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125288125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4874fbd401accf81e6b2260d2b4cacb601f7941a6ad8b512a6cb2fe25d233bc6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:40:05 GMT
ADD file:bec180e92743e5024fcf273019085a4de227f49fe65e76828b9c7f740fafacce in / 
# Wed, 26 Feb 2020 00:40:05 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:15:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:15:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 01:15:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8ea0d19362f06fe2b59b222ce913ba48c67c375897c1011c35ae714403602dae`  
		Last Modified: Wed, 26 Feb 2020 00:46:06 GMT  
		Size: 51.9 MB (51852485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2dd00a16259f5ef437d658e1c9a35286e86c1b1e57ee707e76e7f633f9addcf`  
		Last Modified: Wed, 26 Feb 2020 01:22:25 GMT  
		Size: 7.9 MB (7923560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd95542fd67b65c74ba330b9fbc3a0338708e71af91f677f4c837e08e89f590c`  
		Last Modified: Wed, 26 Feb 2020 01:22:25 GMT  
		Size: 10.3 MB (10259454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040bc7d271e35c9971c628f49f18ba318438168e369228977edd9f27c6c65cbb`  
		Last Modified: Wed, 26 Feb 2020 01:22:43 GMT  
		Size: 55.3 MB (55252626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:ea1f4024cfda705bde9a8bf267c132f256662fc31faaf8a36f8f5c6c8e67ca2d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120240406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9d8b2f30cdf42b24fd89dabbde57bb8aa9e94ae54b339a004bbd81f903a30f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:50:40 GMT
ADD file:6f5d17638043fb7ef05ca0f1c1d20b54cc5e6b65f1c56dddffa5c9b9a0c499d8 in / 
# Wed, 26 Feb 2020 00:50:49 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 03:48:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 03:49:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 03:50:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9cc5a3f6ff999f547ce2337a1307b1bdd7bc19f327358e69994e1d288b2e95aa`  
		Last Modified: Wed, 26 Feb 2020 01:02:02 GMT  
		Size: 49.9 MB (49854601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c3c5021d94167dd69f630d803a6d0eced6e577ad4645c38b09339ae8699386`  
		Last Modified: Wed, 26 Feb 2020 04:03:55 GMT  
		Size: 7.5 MB (7501600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3042081863acbc3c403980506dacbfb08207c794e8dca78c7aec29e279d805c9`  
		Last Modified: Wed, 26 Feb 2020 04:03:56 GMT  
		Size: 10.0 MB (9975067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b8fead3d31aa63fd9ad9f20353d249eca80b40be5e6dc2930e56673cf2372e8`  
		Last Modified: Wed, 26 Feb 2020 04:04:21 GMT  
		Size: 52.9 MB (52909138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:8957ee7b9269eeced997e647990bac302f34ebf952e59ed11160cd3dc9a316a6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.1 MB (115084202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:774cebeb5ece1a8b92091c7e3439f6f2fdcb51fd1355b8423b14a1eda413bea4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:56:58 GMT
ADD file:30aa400682ef7dfcd135a9f9a7ce18e83290a6cfc96893e530b1601d79691bd2 in / 
# Wed, 26 Feb 2020 00:57:02 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 02:22:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 02:22:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 02:23:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7565e2c5d4e7edc07eae55400f5a90bb7e3cbadf4008fb3f77acfcb3c9cf3cdf`  
		Last Modified: Wed, 26 Feb 2020 01:10:06 GMT  
		Size: 47.6 MB (47586966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41118136e87d29bef0a68251f8642bb1356a3d2e3f47a2f27be5762226d865a7`  
		Last Modified: Wed, 26 Feb 2020 02:36:03 GMT  
		Size: 7.2 MB (7238491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1fe1d11ac7f4f8e86fd0b1041300173ac89c0fbb2ff4d8a7d84c5ac366cf5b`  
		Last Modified: Wed, 26 Feb 2020 02:36:03 GMT  
		Size: 9.6 MB (9639261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe0babdd479b6b3ac0feadc47ae9366120adf2cc38672b176b234776b828c9f`  
		Last Modified: Wed, 26 Feb 2020 02:36:27 GMT  
		Size: 50.6 MB (50619484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d6c0db61738709aea92d1ae6f5ca452ec5cf3ee20148bf6c99efde39bbe645b3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124323133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d2e066acc063c05fe4b135443a0ae3de9505f5b7db30bb499cf5425683c7f94`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:48:15 GMT
ADD file:dd5929937313448ee9b3d8640f7868a744a021a2795207ffb95b84e16f7af7f3 in / 
# Wed, 26 Feb 2020 00:48:20 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 03:55:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 03:55:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 03:56:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:39684676301c5f1b4bd75510ba0132ffcf4cb0d41ee99702ffef900f06db4fe3`  
		Last Modified: Wed, 26 Feb 2020 00:57:14 GMT  
		Size: 50.8 MB (50825108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27a4d3ca3fe90120d925f3e4e10e613078f4130d5ce9a4dab2addbab99a69d3`  
		Last Modified: Wed, 26 Feb 2020 04:07:00 GMT  
		Size: 7.8 MB (7799823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273e8497f8b87f730468a98640fb9e0328f1d1eefcbe99c52ca4815168f8d8d0`  
		Last Modified: Wed, 26 Feb 2020 04:07:01 GMT  
		Size: 10.3 MB (10253521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251d262a68f1f17e515885845941b1d0b80a806be8b751151a8470bdece99101`  
		Last Modified: Wed, 26 Feb 2020 04:07:25 GMT  
		Size: 55.4 MB (55444681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:84bf66b1fa99892160d3ec742ea4dc743df694f9dd3a620241419c5024da3646
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.3 MB (129338846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa4eda296a398179e2e4633d1bc19af0b9649d7a462a15eff7c9113dd86a064`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 00:41:33 GMT
ADD file:013e2e45d880a5e5d3c8ac0fafc140790ca1cefd17f2567b30509c07e6bd04d9 in / 
# Tue, 31 Mar 2020 00:41:33 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:22:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 01:23:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 31 Mar 2020 01:23:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6b4a325a89fc0cab2f3ade12182ef3b2b0d777b725c55ef166a7d8e1d80d7425`  
		Last Modified: Tue, 31 Mar 2020 00:47:26 GMT  
		Size: 53.1 MB (53085713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3da8b75e1598f9c9c1768e28dd5414741333f37655c91c43cf6d35fd9a2f8e0d`  
		Last Modified: Tue, 31 Mar 2020 01:31:35 GMT  
		Size: 8.1 MB (8108721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6053a7232909f13050253bad2d64e10fc1f0cdd4d248a794a99c4f71ae186c1`  
		Last Modified: Tue, 31 Mar 2020 01:31:35 GMT  
		Size: 10.7 MB (10657222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540a37aecc444b244c1b92d817cbd18b62937c7a451261c81a129ebee7d922e6`  
		Last Modified: Tue, 31 Mar 2020 01:31:57 GMT  
		Size: 57.5 MB (57487190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ff306acb183a175e9fcd1a86800ebdf2454ae43abf9f6e6b7395a28527bf69b4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.6 MB (135577936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98b1fbee005bf98e69f06a1b1dbdb6c0e9476aa0e6d9b6a6c6c38dbf7e6fc8a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 01:33:32 GMT
ADD file:e8ad38a3aa62a68656015c5a2194c52db73148c61283b8bbdbe2cc1115779a67 in / 
# Wed, 26 Feb 2020 01:33:40 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 08:16:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 08:17:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 08:19:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b5d07ca9f794960ebb8121371afbe7629c826a4e13ca577db10e90088136c145`  
		Last Modified: Wed, 26 Feb 2020 01:57:40 GMT  
		Size: 55.7 MB (55686176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4513973fe5f313717ebc29953fa459565167466bd449ad3fb2eb647af093b56`  
		Last Modified: Wed, 26 Feb 2020 08:51:55 GMT  
		Size: 8.4 MB (8355278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b25cfebebe7381513eeeeb97185df1f6c63f7c0b67ba21182ec14e4dd8bfdc5`  
		Last Modified: Wed, 26 Feb 2020 08:51:56 GMT  
		Size: 10.9 MB (10935977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4065f029ed2c98c2cddf01e1b8e2581e6ddf26412640c1fbd58200e52e39475b`  
		Last Modified: Wed, 26 Feb 2020 08:52:43 GMT  
		Size: 60.6 MB (60600505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4d6f6610a68f0d0852a4bcd9b0cc4909bdcf68e12184296bbb3edd57e91b4cf4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.7 MB (122731854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62df09e969d0dfe4b183754c9e6f97f4907ac144095cc80f8a0f3f0b84aabaa4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 26 Feb 2020 00:43:32 GMT
ADD file:fcda88ea9095d27648ef2b20dcb0fa0d26132f30445c10f3bdd53215b61af4af in / 
# Wed, 26 Feb 2020 00:43:36 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 04:37:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 04:37:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 04:38:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:76bea0f8034c37ea3ba91754ddb1ae9c546d61083532c54e8b98a250873a7444`  
		Last Modified: Wed, 26 Feb 2020 00:48:23 GMT  
		Size: 50.5 MB (50488540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aae2b518ca19378772cf8b419c04c707233cb7ae1004654e819a1c10ff73dc5`  
		Last Modified: Wed, 26 Feb 2020 04:48:26 GMT  
		Size: 7.6 MB (7594585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d07bbb87470a5f46649b849ac7b2b4798c2e6c26d497529bf23a7c04df123f`  
		Last Modified: Wed, 26 Feb 2020 04:48:27 GMT  
		Size: 10.1 MB (10147902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4117172dbd4e7f9ae675b6fd91c6bba514dfa610f62357d36f7aa71c0c570a`  
		Last Modified: Wed, 26 Feb 2020 04:48:43 GMT  
		Size: 54.5 MB (54500827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
