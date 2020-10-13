## `buildpack-deps:unstable-scm`

```console
$ docker pull buildpack-deps@sha256:148f616a503e2d104e4bb8a386d310d660f0d12b00bb4cc85c5b25079584c1f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:unstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8b663c336c6f27ee8028294339f22471745a996fcf20061316c06f47935f0a8d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130142597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a98bf89580a9a6c1ed6ecfc55a3c351a4469fabeee99d44571edc9a31f73c8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:42:22 GMT
ADD file:9463b73933c9a0f2df3bbfaa2805027794a0e3a0cca69453b066ebc4644b6f06 in / 
# Tue, 13 Oct 2020 01:42:22 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:22:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:23:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:23:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ead5025e4e59e53184c941889a91b90e4e7af750b6f2e005952c8484512851fe`  
		Last Modified: Tue, 13 Oct 2020 01:49:57 GMT  
		Size: 52.6 MB (52587404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a50bcb11b150787afba1f3af7ebbb7af8259b2b8b14121b74a6d0b01551ad97c`  
		Last Modified: Tue, 13 Oct 2020 02:30:25 GMT  
		Size: 7.9 MB (7879844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455355c490cedd80caaa467646ef3389e55170d8520f80248b97232c03d34b5f`  
		Last Modified: Tue, 13 Oct 2020 02:30:25 GMT  
		Size: 10.6 MB (10628194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0e82f26a95e6e817a52816fabb1c5164fea5eb51bdf5a55955277dc5d11381`  
		Last Modified: Tue, 13 Oct 2020 02:30:42 GMT  
		Size: 59.0 MB (59047155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:354778dfa3077cbf979fb703ae7551f7cfc9b9efda57ad894c8f53be225d3fc9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.7 MB (124673089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c8b50041487f03fb7f35744f34a345cb1cc11c329d3879b28fe78f2c8394a6a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:55:34 GMT
ADD file:58fae6653444e7013acac8c8b5dfaf08005d4d143891d739c3d3054778fef031 in / 
# Tue, 13 Oct 2020 01:55:37 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 03:54:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 03:54:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 03:55:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1f0f5ab7eed797403be4921ebb3d1c13327fe3d6d4a586c0bb2f4661bf647503`  
		Last Modified: Tue, 13 Oct 2020 02:03:52 GMT  
		Size: 50.5 MB (50504754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df38c36ffcf1ed5e05b47278687eb424e5f086d52c07d18e347f65db5cc3f69c`  
		Last Modified: Tue, 13 Oct 2020 04:10:06 GMT  
		Size: 7.4 MB (7438960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362f9d379e753d7558113cff6099afe40e5d24024073d4516e5d92be7fd2a982`  
		Last Modified: Tue, 13 Oct 2020 04:10:06 GMT  
		Size: 10.3 MB (10316002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0102362b274a4e9e6bfd5756e0eb1af7b07e5deb73c4a0cce590073ed342e25e`  
		Last Modified: Tue, 13 Oct 2020 04:10:32 GMT  
		Size: 56.4 MB (56413373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9b0c03d8a1fe3da202380f6c7de94297ee3ce83dbcb25adb3e1f6ed10bcf26d7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.3 MB (119344235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a40382015a21e049b58f533a6746ba22730b58382f8948694fb21e2fcda7958`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:02:25 GMT
ADD file:6b1218c9574b91ad91309c12b66b8a83d37f3a3ead47d7fc3a16e3c498e6e102 in / 
# Tue, 13 Oct 2020 01:02:27 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 01:43:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 01:44:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 01:45:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:107486c9309dafb8e1d046960e1dca3c02d5aae566c72f8113cbb0f1ed15f9ab`  
		Last Modified: Tue, 13 Oct 2020 01:11:07 GMT  
		Size: 48.3 MB (48255653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb01673e64e8a48d10056720613123aae28172bfeb11020a3aba43cbbac68876`  
		Last Modified: Tue, 13 Oct 2020 01:59:15 GMT  
		Size: 7.2 MB (7183442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e3439ff31f32aefcdeeaf2b053e0f8857776f05392e92baaa254c5446d40fc`  
		Last Modified: Tue, 13 Oct 2020 01:59:15 GMT  
		Size: 10.0 MB (9959277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ce14a99f926f046b0d2295b27dd91ff454c774130961e9dfc7dfe01ee57ad6`  
		Last Modified: Tue, 13 Oct 2020 01:59:39 GMT  
		Size: 53.9 MB (53945863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:522b03728e61a055176b183c87f2dda5c2d70feb88794e37220cc7e97a703d60
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129159085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d6b888ba92ba75072de6cc9126aa8a2d6ed9be7a15c8829bd12aa238322060`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:42:15 GMT
ADD file:af62f3e6ea7fec61b2823188f91b0f3419596dad24e9f9303c3305a3747d4350 in / 
# Tue, 13 Oct 2020 01:42:19 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:36:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:36:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:37:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:77774dc39e62096b335ade088d1f9f15b9cfba84ef4b0106507ec53b4bd6290e`  
		Last Modified: Tue, 13 Oct 2020 01:49:29 GMT  
		Size: 51.5 MB (51483868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7d9ffc760782b4e9e54ad713a8d51c982bb91d4571cbcdaddfd15199b58c4f`  
		Last Modified: Tue, 13 Oct 2020 02:49:10 GMT  
		Size: 7.7 MB (7745936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3602bebd6bd88919236d9b8aaed761e14585cf0d0129ae39141683ca7678c032`  
		Last Modified: Tue, 13 Oct 2020 02:49:10 GMT  
		Size: 10.6 MB (10636757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac51bff55f8abd95fb04d6b1b6c83ce20aa95d629d93a8dfe0528a765db3cda`  
		Last Modified: Tue, 13 Oct 2020 02:49:37 GMT  
		Size: 59.3 MB (59292524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ea9366aeb8d79c594427b39d2accfb06b13e56dc032b4c094090a0c5cfdd29ed
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133671932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29356c2e5c6b47284485f7bd29638261e71b78ac1285f421cfc1397f4105200c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:43:42 GMT
ADD file:71e92b8b05766d1d5d02c013ee4e6bfd49cfe21c2bd5ab2182af02e5e2493796 in / 
# Tue, 13 Oct 2020 01:43:42 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:31:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:31:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:32:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:04671281ee1c9a57e6e56404219f6ae19ebe375e509c240cbdce889f052d441b`  
		Last Modified: Tue, 13 Oct 2020 01:50:52 GMT  
		Size: 53.6 MB (53624141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47de0273945f6e2c47e2f3f03a477c27bd73945f6ad62e80267ca45b1bd029e0`  
		Last Modified: Tue, 13 Oct 2020 02:41:40 GMT  
		Size: 8.1 MB (8053959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b0b6fad1e883cd355dcce25d38d601d02eefec153ce528a98d0b38d4a84f4a`  
		Last Modified: Tue, 13 Oct 2020 02:41:40 GMT  
		Size: 11.0 MB (11015595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd96c2e2dd5b064c3f2b4644f9c8fdf61eb3eb5e96cf1c4f144aa8bde2b402e1`  
		Last Modified: Tue, 13 Oct 2020 02:42:09 GMT  
		Size: 61.0 MB (60978237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:623072dae44800710e2423a6d5b2eec38d479104171f16d15c52ac1eb7193775
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127235141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d129fb712a3c30dd9e967c82b6ee4ad285956103101cc252c08f974ac9adb3f3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:10:19 GMT
ADD file:ec8eebd9c015be5ae41233496690d158f5f7d31b3dbece81b6474018168d339d in / 
# Tue, 13 Oct 2020 01:10:20 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:15:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:16:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:17:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:acfd16a511fbf47ee6caac9e14f0361f1b2a477e4e410835a21a56951f404ee0`  
		Last Modified: Tue, 13 Oct 2020 01:17:27 GMT  
		Size: 51.3 MB (51292191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c8c36fecc594af5a0fcd22383157160ab20328027a9a7aafcc7876e036c074`  
		Last Modified: Tue, 13 Oct 2020 02:26:36 GMT  
		Size: 7.4 MB (7400523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07514ca8c30d4614bc9d748c8ca9dec4b2481d32639fe54cfc45cc2d68aee7a`  
		Last Modified: Tue, 13 Oct 2020 02:26:37 GMT  
		Size: 10.6 MB (10639538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ed89d809ac68ebf4610853e2f5f0dc9ef101c69abe8a4dc2fdb558e07ad9c2`  
		Last Modified: Tue, 13 Oct 2020 02:27:30 GMT  
		Size: 57.9 MB (57902889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:481ab70cab70e48cd98e4d4d98597e1b924d466e0d76f3efae514429cf9a4de2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140947145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:537c7cb938d258ba2d0abaee1743d13aacf0e6c732804ea5809693e4234b35b7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:39:24 GMT
ADD file:7998a5d3f49a86501eb252e7dc54464d086e8239a5f918b15cd85dd11e7341bb in / 
# Tue, 13 Oct 2020 01:39:30 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 09:10:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 09:11:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 09:12:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab405c79eb283d457b4f978511bbef215699b366c926b3450f2a7cbc6a56e33b`  
		Last Modified: Tue, 13 Oct 2020 01:51:11 GMT  
		Size: 56.5 MB (56495338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38962ab4f4d37e5644006dc2c9a5a9b270448a5ea5ea29a387f4c7955497875d`  
		Last Modified: Tue, 13 Oct 2020 09:38:29 GMT  
		Size: 8.3 MB (8329668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8ecae68ecea0d3add456e8b38f9eef46b95731e6dfca00f430a45a774f2a19`  
		Last Modified: Tue, 13 Oct 2020 09:38:30 GMT  
		Size: 11.4 MB (11392727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dfde9fce3dd7addbd894e0669be922a792dc5fa95b3ee33ffbaad4ac26cb393`  
		Last Modified: Tue, 13 Oct 2020 09:39:33 GMT  
		Size: 64.7 MB (64729412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b0a3bc284401613824f404d81de9fc3aea597c8b5bac0ca5e1bfbce97ae20526
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127395555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d530295fa6020b82a7867bc0402d0a1f1797441d9d053c1096829d11513f671e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:42:39 GMT
ADD file:8ae741412fc2632b17f3119be3f00db5ac9da9165ec6ba803cecb706cca2e10a in / 
# Tue, 13 Oct 2020 01:42:41 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:07:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:07:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:08:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2f8a9ab7d8c65b5068769e112907fa3def6a9a81b79ba5632dcc28f6bc45c59d`  
		Last Modified: Tue, 13 Oct 2020 01:46:00 GMT  
		Size: 51.1 MB (51120285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c6c2e1d37a743e5cb89bea0fbf288f3c97c58bd5e1e111a310a1968a8fa789`  
		Last Modified: Tue, 13 Oct 2020 02:12:16 GMT  
		Size: 7.6 MB (7552593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d9d2e85355b3a65546bae45dcf206bd44a3e26e29009a1fcaaccec7cbdc9062`  
		Last Modified: Tue, 13 Oct 2020 02:12:16 GMT  
		Size: 10.5 MB (10505631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450cd2a37bc042631c0485843fea47b52793d6012a3c58241d6cbdca704d0c23`  
		Last Modified: Tue, 13 Oct 2020 02:12:31 GMT  
		Size: 58.2 MB (58217046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
