## `buildpack-deps:sid-curl`

```console
$ docker pull buildpack-deps@sha256:eb3aaa80de74eec09424baafcb3ab2905302f0505bd0a44381ca877bd50a6a44
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
$ docker pull buildpack-deps@sha256:12ba50a46083b7b25c3ea8d426472c984e7deeaf32421e549b68a06ebb54b151
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70177905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe676bf583c6d482304c48d6bdcdfd1d3c84398b633abf58f05d5a5f9a9d5152`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:22:48 GMT
ADD file:7562f01f4040e4f21a40337301dd14e4377f3d101bd0919a96ae05bff37d7087 in / 
# Tue, 31 Mar 2020 01:22:48 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:05:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:05:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:616821eae326bcd1b2974181d172e5949f2c8c091398159b63b0f483913be88a`  
		Last Modified: Tue, 31 Mar 2020 01:28:20 GMT  
		Size: 51.9 MB (51949680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c04e796c39db97cc83b98c665f9d3f60b53540de3aef972a49131d996b2aab`  
		Last Modified: Tue, 31 Mar 2020 02:11:44 GMT  
		Size: 7.9 MB (7930362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e38af22482c0eee10c6177e3f57aebccdca1c6f4050aa653ba0fefcffec7507`  
		Last Modified: Tue, 31 Mar 2020 02:11:42 GMT  
		Size: 10.3 MB (10297863 bytes)  
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
$ docker pull buildpack-deps@sha256:8c74bc18f1236d500f8e18c71bc83c911bd2e8338e9fa2854a67675b8016eac8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68327507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc9ca423a6c31d1df279e47c3d570fe8702e0653f885e4890b65ace16bdd5602`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:09:33 GMT
ADD file:416f205dbbd8311318e69b6a4cd3d5426df0bc88ee4293cc800980d9d95e85fc in / 
# Tue, 31 Mar 2020 01:09:35 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:23:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:23:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:14bc63db6ec21658b800879387ad1a9200b09e59912af2bf8c5fe175da9e5ec6`  
		Last Modified: Tue, 31 Mar 2020 01:13:18 GMT  
		Size: 50.5 MB (50546013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4527654ed18a1f30bed3dfc69b5b6b62d0dd0d886de936b12dc43261ab235c`  
		Last Modified: Tue, 31 Mar 2020 02:29:31 GMT  
		Size: 7.6 MB (7597631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76af75185df23fadda1aa1fce4299d7f85ac601bd6d2e00a3a54023456b0581`  
		Last Modified: Tue, 31 Mar 2020 02:29:36 GMT  
		Size: 10.2 MB (10183863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
