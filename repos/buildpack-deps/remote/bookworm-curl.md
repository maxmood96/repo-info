## `buildpack-deps:bookworm-curl`

```console
$ docker pull buildpack-deps@sha256:5666619850e1f047e12ab2dbc36ce65a5e663e6dcd36e345ea2e81de8480cf2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bookworm-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a770165776050de218e043254b884fc845658ee339f38c2f983006e5177cfe87
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72211606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a1cb561d2445ad364a50b941bd8c730df1a0e80d3b2b0803faaacc9cdf4004`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:19:50 GMT
ADD file:05d40d360d088a73d2d9ea8361742b3b0e7f5ac80923374f84acf3d1be6c7798 in / 
# Sat, 28 May 2022 01:19:52 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:39:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:39:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:1afe78e67a22dc5c619d5518a1d45e8f5ca31628fa6b7caa3b645c4fba19faaa`  
		Last Modified: Sat, 28 May 2022 01:24:12 GMT  
		Size: 52.9 MB (52947713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a14d423114bf1291f01f267de6950924fd08d5221af6a2165d1f4201c7bf04`  
		Last Modified: Sat, 28 May 2022 02:48:03 GMT  
		Size: 8.0 MB (7999256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485b5a45d253cd5d3bdc472baa541897f0b1cdd23ca5be5de99b1a0191168b34`  
		Last Modified: Sat, 28 May 2022 02:48:03 GMT  
		Size: 11.3 MB (11264637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:5377dce73de2174ec38309f94c864746db84bdc0a0010eb8fb4fc171083ee396
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69201021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11b0d9e7ae24c971ec79c92a799784c5ce866e082441d7e847701b79c4eef969`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:49:02 GMT
ADD file:14b16b308b28ed8604a9f98d47e92522f709988224084eb5d2dfd30d3511e4a4 in / 
# Wed, 11 May 2022 00:49:03 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:01:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:01:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:0baf2800ae4e68af843862199b558f14eac2766cea5651c0837cbd8ee827981f`  
		Last Modified: Wed, 11 May 2022 01:03:42 GMT  
		Size: 50.7 MB (50737437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1cacfec2c73325f6ee9727f3ee99a764a10620c61e467c786773e82fac2589`  
		Last Modified: Wed, 11 May 2022 02:26:52 GMT  
		Size: 7.5 MB (7536108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9a878bece2839158834198a327d030c397685382713b32bee43b9de34889dc`  
		Last Modified: Wed, 11 May 2022 02:26:52 GMT  
		Size: 10.9 MB (10927476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:403bfdc01a573b048212df9063afedf5aedde940e885c1ecac6b4692d6fd2d07
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66318331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a68d5d33c79e64651f398ef8f6ab7f4294d2ebd334d8c1c46f849b3bbf7bb6`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:58:07 GMT
ADD file:8f129729b10afccc69a16674ae2d85afe02706c13f7c3177672040ce01dc34a2 in / 
# Sat, 28 May 2022 00:58:08 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:38:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:138713cd49f1253cc6e27f92b0403100f0c5966f7a66077fd4d7c6ab6a6799df`  
		Last Modified: Sat, 28 May 2022 01:13:41 GMT  
		Size: 48.5 MB (48476343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db436db30438e10e5eeb35827787a5b8ed355db8a9ecf271097bb255dc415b5`  
		Last Modified: Sat, 28 May 2022 03:06:08 GMT  
		Size: 7.3 MB (7269071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926a3169136786c87319557ca5d830b8821949450e41d7405b1167918ad0bb4a`  
		Last Modified: Sat, 28 May 2022 03:06:08 GMT  
		Size: 10.6 MB (10572917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2bdb08c18302d24323126613fbd20e3387a995aae955fcd2545cb4ecc2e1835e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70936670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40068327e4941832a318e33dc677f367ed31328bf68e03dd821b2fafa7fff65c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 00:46:19 GMT
ADD file:a50b6ecf9ed84e6e3bb43f96fd036c7ebaad7f94df16c3637d6dd19a6dc91701 in / 
# Wed, 11 May 2022 00:46:20 GMT
CMD ["bash"]
# Wed, 11 May 2022 01:23:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 01:23:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:45306f5029ed7ce5685e65dccfaecf3f4a79040520f3ffb65eac76781218fea1`  
		Last Modified: Wed, 11 May 2022 00:52:36 GMT  
		Size: 52.0 MB (52041343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5de1fe22d36e48b637912dbd432cf236f1d956231296b275af61bc5cc951b1a`  
		Last Modified: Wed, 11 May 2022 01:34:36 GMT  
		Size: 7.9 MB (7853647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f57f959274f20ecbbfac9d0dd7e9dcbbc904e7eaf49a4ff37e3149afcbb2247`  
		Last Modified: Wed, 11 May 2022 01:34:37 GMT  
		Size: 11.0 MB (11041680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:14c0e903cb12f9990d5ac596d7a6603a58a0ff73fe44e6007efac3a9404115ab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73589382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c641f129a26cdbfa75e2af8fe2cf4111faf7b38281b88ac1420898e02cfcd84`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:38:49 GMT
ADD file:ba6ab6618a6fab6f0a1d80573b329e26b602c060d940b76c1774ddab96982cd9 in / 
# Sat, 28 May 2022 00:38:51 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:08:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 01:08:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:d1098d76e3f40923a061abc8c2e6697409b0a2428eab6f37ae394a7b491b1cad`  
		Last Modified: Sat, 28 May 2022 00:45:27 GMT  
		Size: 53.9 MB (53948486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052560f7b1294898c71f369cf5ba0727eeecd6b6ba0e30c151347d6333c1f5e7`  
		Last Modified: Sat, 28 May 2022 01:20:08 GMT  
		Size: 8.2 MB (8176480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee8b2d3f9aaae772a2ef7c3c5860d032dcd57b82cbaba04dcf2e741bf9b5895`  
		Last Modified: Sat, 28 May 2022 01:20:08 GMT  
		Size: 11.5 MB (11464416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:e61a32a45dd117177f3bd708e6cfe446bf20e1d13983d183675b9e93ce7db7d7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70587411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e99adf0a9889992bf5a664282b8b7f8eb05665953ddfb20bb9c15bac4777275`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:09:18 GMT
ADD file:0db9365eff38bea353e789709159951d557685e098127d950e467c83468aadd7 in / 
# Sat, 28 May 2022 01:09:23 GMT
CMD ["bash"]
# Sat, 28 May 2022 01:45:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 01:45:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:409912beaa99ac80f6ec57bce7ac6621f4659f5f43cdaf3152de94639a634798`  
		Last Modified: Sat, 28 May 2022 01:19:34 GMT  
		Size: 52.1 MB (52061634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6976dd6800a501b4f86f988f732f79809a62582465ed0c2a06afe5c24d753b1`  
		Last Modified: Sat, 28 May 2022 02:21:04 GMT  
		Size: 7.5 MB (7506250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c469859fffca391e2318192162949a194958f00b7d4d3e4aaf787a8d79865cde`  
		Last Modified: Sat, 28 May 2022 02:21:05 GMT  
		Size: 11.0 MB (11019527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:82740ab2784f26262948ac13e96b6d92462f1593a8881b27f32b4fbcbf8a9ba8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77712430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7851d7fdcdd6838e60cf8c9f7afaf67fbfd152682acfcb26cfba3324767910d1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 May 2022 01:30:46 GMT
ADD file:151ed5fad83d0b4f27c9bb34e41c649df7b7b9cbe789e3036c44d12cf1f53a71 in / 
# Wed, 11 May 2022 01:30:51 GMT
CMD ["bash"]
# Wed, 11 May 2022 02:07:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 02:08:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:49991d23fb52aaf7937c711b0196364a5011e41402f3ea986702027fadd27e0e`  
		Last Modified: Wed, 11 May 2022 01:41:30 GMT  
		Size: 57.2 MB (57150441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ac162b59dc7eb516878ceab4828d006f42ec802f1755cbd5bc3126bf8d03c9e`  
		Last Modified: Wed, 11 May 2022 03:46:29 GMT  
		Size: 8.5 MB (8496430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f4172550a38e5e5676e20f279186dcd1ebf123a9b2693d032e98814590d62a`  
		Last Modified: Wed, 11 May 2022 03:46:29 GMT  
		Size: 12.1 MB (12065559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:20200fdd521a77d5db95814c744cd9d02f1e1c5cdbd5ea4f739b165f4ca78f64
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70310370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0346180d8eac71017c5f53afb9d9c42b595ac638c69b0727afcb7a0c398a819e`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:41:57 GMT
ADD file:4a6691f8332d56b3f631afa5579acf89d2271614f4a4f77baa24e59c0b2b3016 in / 
# Sat, 28 May 2022 00:42:02 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:20:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:20:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:5c219aa5bd4928fd8e410d747805f6d8a6cede332d701af0c9e39dca3b50c70d`  
		Last Modified: Sat, 28 May 2022 00:48:58 GMT  
		Size: 51.5 MB (51490385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b51eb782be06235f2446e523178fdce20039860905eeef1a177ee2ab9b7b259`  
		Last Modified: Sat, 28 May 2022 02:34:14 GMT  
		Size: 7.7 MB (7662349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077ec432669cf9233ec7c2120b3f33664a5d8ac0f8d2a61de67643c292801208`  
		Last Modified: Sat, 28 May 2022 02:34:14 GMT  
		Size: 11.2 MB (11157636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
