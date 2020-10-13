## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:25343d30490794b1cc8739d36dfa2c6f93a2a3e9fa085325e4680eb40be5fa02
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

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:eba2f36b648ff2a8895f58fa445152c80dd28e16d7ba0c904970a1e62ed1deb0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71095442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456f607a08d80280ad597c44011acfad66a5e247d845eab4bbcfd1410b3ec333`
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

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:1a77ff20d02968fde8be5502c6c6b33ca0f20bfb6362dfca7198368cbb3a06a4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68259716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4c896059f63609dd44e378b2c3ce92e78770aaceb93e7305ff5af44ea89144`
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

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:96680ba947df80eb7a989e122b00b8ca541c1fb1fa47d70106e0e9ce346e8863
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65398372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:297e1959f21f55471007cd2a3b9a7ca5f24a90324a52bf066a7aaa92713a8d76`
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

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ce9a383efcdc7da657e4ca9272c8de85a8e807fab8319243ed34606986d36e20
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69866561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bd52e4253127416a3103784d58579cd5a21bccc3bfe1dcb42d8ff69fb8e881`
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

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:af6a3ecd94beae3361fd06fc9bcedac893fb49826df4fea4a65c86000f96bc83
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72693695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28100a860870b5983338b534120ebd746e2c880a1ca715450ef3cea3ffde103`
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

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:daa8a6e7697b85b87940004cf2a34c7459e65d261df3f5a3213d3d453a406a6c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69332252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2de2df8aa9c1fd6e6fb637c565f51b794ccad5ff6d07e5677ea8e6969206aca`
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

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4c78cba5a674d0117a0549c11318b3cb7baffd79ee69d9a8f747d5a6de2e8a73
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76217733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cc7cfbf8882871f1e3f7c1728ee24886a7f593bfbed8a590fa23cd9bd41f0b5`
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

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:2d3c38a3281d5f714f75b1dd9e3cd5e628aa706cfbbbfb1a9a9d9afe5ae7e32e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69178509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82b1e87d0c212ce378d8aad7b3f9b2ea12f39f4da511dfec5a8d12712b3d289`
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
