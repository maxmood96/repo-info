## `buildpack-deps:testing-curl`

```console
$ docker pull buildpack-deps@sha256:e2e46d1f7d594193601a8f8104eb9fa2e50249d6a9b38b8a4d5a4f6d0e7694f3
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

### `buildpack-deps:testing-curl` - linux; amd64

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

### `buildpack-deps:testing-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:14d18c92d6f3e0e50521f4af9a0af22dac6557ee7765d5ff5ed7387c23a70aea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69200007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e14d2d75b2028e203fe991dd648ba6c5fd934cd4529b766c52fa826fb26d9a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 02:01:33 GMT
ADD file:2980a4070352ee6798cd5240bc8b6e068815aed3d8bbf85b426005ece7d9872b in / 
# Sat, 28 May 2022 02:01:34 GMT
CMD ["bash"]
# Sat, 28 May 2022 03:02:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:02:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:234035d78cc15d2308af9cee32306959cb61c14372c60047e93d7b747c05b2db`  
		Last Modified: Sat, 28 May 2022 02:16:30 GMT  
		Size: 50.7 MB (50735045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0923a0d0cdbaffd32ad4dcaea3669e9e3de65fa60085e77bb3b3e8d4b4eb3fa0`  
		Last Modified: Sat, 28 May 2022 03:27:27 GMT  
		Size: 7.5 MB (7537455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d2efe917b364518c9ef6d14325dc6cfd07776bdf28eec8971d46617ff1d524`  
		Last Modified: Sat, 28 May 2022 03:27:28 GMT  
		Size: 10.9 MB (10927507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; arm variant v7

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

### `buildpack-deps:testing-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:276811035b5b20e167ae1dbe98b6e2837b32d99aee74ffaadc6c62f6dd7312ea
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70938165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d593f33508039437d6adfc984a530902a765782c9a115f0680362b9729a5278`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 00:39:58 GMT
ADD file:ae47b859bfb40c803f02c28e3f96af8bc788772728d65e218948bb1eaad3bde9 in / 
# Sat, 28 May 2022 00:39:59 GMT
CMD ["bash"]
# Sat, 28 May 2022 11:03:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 11:03:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:f24ab7edee1353b240b401789e816aa26f6557c18b9a3ac7edd79407f8347c7a`  
		Last Modified: Sat, 28 May 2022 00:46:24 GMT  
		Size: 52.0 MB (52042792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45ebc1dcce8b8aec912befdb6c05e70847b8b6f78e252e30840bd72b965323b`  
		Last Modified: Sat, 28 May 2022 11:15:53 GMT  
		Size: 7.9 MB (7853521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c57a1416128a1d581da45226cd01828d2ad7c0a1efd7b4428c15b7d4efda428`  
		Last Modified: Sat, 28 May 2022 11:15:53 GMT  
		Size: 11.0 MB (11041852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; 386

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

### `buildpack-deps:testing-curl` - linux; mips64le

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

### `buildpack-deps:testing-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:dabfccf228f22a9f7f439443f8d6173db05c7c2d2562dac53e278787e4ed1f00
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77719104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c873ba8e29a4af2b0f8f0eb39e52bad7c9fed1c6b8cf73e7f67ac31bdf740086`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 May 2022 01:21:20 GMT
ADD file:af4ab80f98b1cc5089a94e2932d676aad92fb52c2f59476cc64955602ea3d330 in / 
# Sat, 28 May 2022 01:21:26 GMT
CMD ["bash"]
# Sat, 28 May 2022 02:55:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 02:56:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
```

-	Layers:
	-	`sha256:b80d749a1cbc85d39c24118acb8615cd7c0ba93c2cb7561974f0473b9863a264`  
		Last Modified: Sat, 28 May 2022 01:30:55 GMT  
		Size: 57.2 MB (57161586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2dd070dcaaf036f25496b09532c660455f3a5920ee198f04d6d52e2a7b95ea`  
		Last Modified: Sat, 28 May 2022 03:34:04 GMT  
		Size: 8.5 MB (8492248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a898ca31e1ca70ebebfed2a003df2baad8dd1bf696095a848f745e93a3706aa7`  
		Last Modified: Sat, 28 May 2022 03:34:04 GMT  
		Size: 12.1 MB (12065270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing-curl` - linux; s390x

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
