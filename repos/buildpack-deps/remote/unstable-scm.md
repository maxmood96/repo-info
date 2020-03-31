## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:c4e9d3e046b77e439f00a2471d98a31265f76dc8d50e8ef87c18c73d95bbcd3b
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

### `buildpack-deps:unstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7f7f185300585e2de635f25e390588673c87d450a424e57b25d257c57e6acaee
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.8 MB (125787750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9d81d9cf55a0acc03e455d864a0d8a3638b84abf1dd1c7e25cee850612bcb4`
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
# Tue, 31 Mar 2020 02:05:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:d14b2afe7eba2a0d3afe523ef0cfbd8492e331f5114b35c8cc6dbee1c196889d`  
		Last Modified: Tue, 31 Mar 2020 02:12:00 GMT  
		Size: 55.6 MB (55609845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v5

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

### `buildpack-deps:unstable-scm` - linux; arm variant v7

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

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

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

### `buildpack-deps:unstable-scm` - linux; 386

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

### `buildpack-deps:unstable-scm` - linux; ppc64le

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

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f122a24abf200ebce46efe03cb21a1c29c16cb3c97db0283453d4583031fa9ea
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.2 MB (123196397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c40475846f7806e02e9ca34d11f8c48a2e1e57051a2f1e1d43e369c0a7604854`
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
# Tue, 31 Mar 2020 02:23:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:a3e51fa7629c7a4c3615d5a8fbc92d2dd9d5a1cc4b2af9704ba63068c647a3bb`  
		Last Modified: Tue, 31 Mar 2020 02:29:49 GMT  
		Size: 54.9 MB (54868890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
