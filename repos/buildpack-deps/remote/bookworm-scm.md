## `buildpack-deps:bookworm-scm`

```console
$ docker pull buildpack-deps@sha256:bb1d47dae922db48203179f51e2ec4d5be7b2c0e7d8461dfe89630f44a8a9537
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

### `buildpack-deps:bookworm-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:d49eed763642f3a8ece4fbbd2b03a7cb51380e9c2ff44ba2f6235c9ea716450a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129797383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f61a067b7cb013d8dfd5530de56e770a288ce76454e647cdbf9a91b7ec80384`
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
# Sat, 28 May 2022 02:39:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:382e92fdb71925d6bd27ce2b56e500157d771af41de9acecd3517fb9e466c750`  
		Last Modified: Sat, 28 May 2022 02:48:21 GMT  
		Size: 57.6 MB (57585777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:3f49f0cf1d0b037d6be639b7b2be1faf4b015c13cfe39e925e53e4c93f917d20
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.4 MB (124373541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28b5404ddb2a8f1cb5f34fc17e6bd17a89fb1ddee73787fa4c7e3a7b27e74a1d`
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
# Sat, 28 May 2022 03:03:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:28d389a3875812c86b94085d0e0466b0416949eec9f33a61dea888cf39f8c419`  
		Last Modified: Sat, 28 May 2022 03:28:19 GMT  
		Size: 55.2 MB (55173534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5e7991b7303a25429ce297415ecda6a894cec9f08395b1f8ed058ffd264c9bff
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **119.5 MB (119497958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ced32d06bee9061d5c074d8bcf8039431977948ef2e91a19eb912d99b7714b`
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
# Sat, 28 May 2022 02:39:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:e21dd0c806bffa44c59273211fcf9fdb67feabfaa2c4c33867f7d24f3e25078d`  
		Last Modified: Sat, 28 May 2022 03:06:56 GMT  
		Size: 53.2 MB (53179627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:00d4bb71c5456bd7e5e9f5eb3c21b8daa322b6375176b02ba82fc82d34688556
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128543394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:145cbb7c7d9b2ceeffa9d8e4bf42b590d1342f8d0457c6e45850e08ad80b64b3`
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
# Sat, 28 May 2022 11:04:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:4c7240c05d864234a8bf0a46fa1b226ad031fd529f5820ed8ab06d958e9aeb48`  
		Last Modified: Sat, 28 May 2022 11:16:13 GMT  
		Size: 57.6 MB (57605229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:0facb667030f056b56d5ec0f20138666ea4d9afbcc3a2290bae1ed4c549db899
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.6 MB (132581486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47fc36136411b36061fb8c3db105d455b75b670d3c0c1d9f0ff073d1183c759a`
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
# Sat, 28 May 2022 01:09:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:1cbe8878cdce718f0b7deab1bba8c2471c5e61e909f442fce25f4d619d2ab8be`  
		Last Modified: Sat, 28 May 2022 01:20:31 GMT  
		Size: 59.0 MB (58992104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:2fbcbff2b0be3f39b471d6f4928fc7d4f8f60b1e05862d0397e7f6c557ff17c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.9 MB (126900500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3265967bc77b10d1668cc679298029da1e42a76714bf5e55f6059f59b1bfa80`
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
# Sat, 28 May 2022 01:47:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:5addbbcd3adf2891ddf68850f2a8a25112410557e4531d8e3918d9c5ea011ff1`  
		Last Modified: Sat, 28 May 2022 02:21:54 GMT  
		Size: 56.3 MB (56313089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:8b8a7628da9a3ed25f28a98ec4b903cbb4e04e15fa618f3f019f415c84bda771
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (140032643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2961524c3678feb536c9fe2b14e9e7ef72b6c894516e6511e76ff0900cbbd5`
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
# Sat, 28 May 2022 02:58:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:4dc921ec2a90bafbecfdbc02278b617a2c8851e6e9596febb515ab7f43e0860f`  
		Last Modified: Sat, 28 May 2022 03:34:27 GMT  
		Size: 62.3 MB (62313539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bookworm-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:15576eacd9dc926e32cc0213a3c2257a5c2ccad0c011ea0c22f738a8dd49987d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127201194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2871e93339d8397b5082c97bf1bd9e31cfd871d71a10216ba1d728ff34051bba`
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
# Sat, 28 May 2022 02:21:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
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
	-	`sha256:eb7881263aae598e496a174ca6809ac1657096989286b9533de93d9151065f0e`  
		Last Modified: Sat, 28 May 2022 02:34:28 GMT  
		Size: 56.9 MB (56890824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
