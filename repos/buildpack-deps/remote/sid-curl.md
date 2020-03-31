## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:e718732f86bdf9aeb9050ab4cd80caabecd695a18f06d34fe7dbdd0d7e610d31
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

### `buildpack-deps:sid-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:75370b107b116d7c4e8ba71d5c09afbafe0f0d17bf3514e73bf36ed4aced2bf2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70035499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4612f747713456c5691f382594eef42af7b4701540a3a3e726fe540c7247b7`
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

### `buildpack-deps:sid-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:3e04457d160417ed5b84d9bcc8bd27638a9efae98e4363fcb872ec6af9ce60ba
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.3 MB (67331268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41493ca79b5f5a37cfbe4e2830cca7adbc0f608da2685e7b2867bc8fdfcbab7c`
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

### `buildpack-deps:sid-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9b473de0976fa6b4ec77bdc5e52d70745d88ed0ff7065d80f0606ab5c3f605b9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64464718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99d2cdc9a34935f2b2bc7ebaafab56f0969b41c3d97a4c14e71729a446bf039`
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

### `buildpack-deps:sid-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2412dfc45b4de4df93f27c61fe89d75d45bff581845a5f71e83df66dd56d425b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68878452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:082114cf0f4f2c2ebed027129e4e98be476b66ed622aac665994bdb78670d77e`
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

### `buildpack-deps:sid-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e3d675e579b9f52fef7e68f45107793961b279aa8f16e43f7d0045a825f9f02d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71851656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4259ecce0a5e2f27ce63931f19b2e6827d1248a1b0036dbf6df3e2c6d4aca4e4`
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

### `buildpack-deps:sid-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:0defc4746eadb2c0fe1e87e6147992a5bbce4e92e5ad5cc200adb7b9b39c3887
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74977431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9febb774dd31dcacd88ca4a9e27c26a07f7b6bfee6bd1b547029a019f749b9a`
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

### `buildpack-deps:sid-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b82407f404d6049563eb3a6dfe81ad07fb41a3ff2cc87ea85b06d00c372932d6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68231027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698e114ca6c21cb85ca2f06b512c9d5cdbd4d0e6644b64b84c24506a6324dc90`
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
