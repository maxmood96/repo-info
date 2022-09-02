## `buildpack-deps:kinetic-scm`

```console
$ docker pull buildpack-deps@sha256:acb0852335a3ebd50b51b14fbfb92eb19a1b99f55dcc4bdfadb2195e8ee5939c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:kinetic-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:828ba173c64d2b06cfab5015d103cacabaf810768a3edebde3bc29cbdc44e5b4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77570973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdf0e5aaa1e96e04823419e7cc270da44b5ef7482b69063331a8f8dc4851ba7f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:43 GMT
ADD file:d5de90ac61ee7027aa0900efb669efa73f611463cf73ab2cfdacadf5ab9fee19 in / 
# Thu, 01 Sep 2022 23:46:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 02:32:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 02:32:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 02 Sep 2022 02:32:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0b78030514e08aad79cb596ba84b18b9579e90eac0b8e0c2dec483c3da8dbee8`  
		Last Modified: Thu, 01 Sep 2022 23:48:15 GMT  
		Size: 27.4 MB (27428015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71363ea1301988ddf4ef6039b34a05a19b44a70e1ba2764e95fa0f47b3585c12`  
		Last Modified: Fri, 02 Sep 2022 02:39:23 GMT  
		Size: 6.8 MB (6779788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d261ea038a7743d40031459e01e57001571ca5986a617d9e2d3174c66d98187a`  
		Last Modified: Fri, 02 Sep 2022 02:39:23 GMT  
		Size: 3.6 MB (3633660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dee5c450c1549fab83f54e9138820f82132ebf0b50a52e7ffb97b6074e98c1b`  
		Last Modified: Fri, 02 Sep 2022 02:39:39 GMT  
		Size: 39.7 MB (39729510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:cfd3f516f9db19a7d0a3397bd2a4556f9fe1196d887519954a604ed38c08ae24
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78188598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6c836955c987cb709f3f744b01bd49e876b7dfdfddb548a7b840351c8452b0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 02 Sep 2022 06:08:44 GMT
ADD file:6fea481ddc80754c10680e7c291055af82ef815eb0fdaf745c49c4f4cdf2afa1 in / 
# Fri, 02 Sep 2022 06:08:44 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 09:35:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 09:35:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 02 Sep 2022 09:36:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1f63be4c3b8fca43746377bd8a99dd9b04acdd942d8464feaae1671e6363d920`  
		Last Modified: Fri, 02 Sep 2022 06:10:58 GMT  
		Size: 25.8 MB (25845683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c94aedbe9250aab4e90e8e88c1f2af520548789812f567b90a81f67dc9145e`  
		Last Modified: Fri, 02 Sep 2022 09:43:15 GMT  
		Size: 5.9 MB (5948408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78166495a53038ebe64fd164f5d7e26607173735e8a0e096424b99f947d93cb`  
		Last Modified: Fri, 02 Sep 2022 09:43:14 GMT  
		Size: 3.8 MB (3801422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28471ad57cdb7e9e4d1bd803eae0208867737111fd76d4143f4b6120903361b7`  
		Last Modified: Fri, 02 Sep 2022 09:43:34 GMT  
		Size: 42.6 MB (42593085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e3b5b4e76e7beab59040a6636f56d76d7503606a20e63a3e2f9ea2a8bb6ac29d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76174117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b653827e5a547aa259b9c8b69823046c120471f9a42d4cb3c39bfce50ac697`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 02 Sep 2022 00:58:02 GMT
ADD file:1b9e898b22915c14e3d83959e989e2a653148ff82c8e2a1b3dfa8035256219aa in / 
# Fri, 02 Sep 2022 00:58:02 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:42:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:42:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 02 Sep 2022 04:42:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7c0b344a74c2d365a9a57a618f4a544c4e8e70f341f67973d3a22aee52a267b9`  
		Last Modified: Fri, 02 Sep 2022 01:00:04 GMT  
		Size: 26.7 MB (26663798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b21ff0107faab8a809cab0821df6c069bdc690f3cda610960915bb07f0c47780`  
		Last Modified: Fri, 02 Sep 2022 04:48:55 GMT  
		Size: 6.6 MB (6603091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62edf58fe3260c89e551263ca83a26aead51b89196e35322ead3ba9023c23aed`  
		Last Modified: Fri, 02 Sep 2022 04:48:55 GMT  
		Size: 3.4 MB (3390812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df24de8e3685677e98d7d3aea7263fa8e11665eb30549c733d0760b8bdd6a28`  
		Last Modified: Fri, 02 Sep 2022 04:49:12 GMT  
		Size: 39.5 MB (39516416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d1a0061871614fa08a0672d33b54065a27d2ac2e6fddb89f4b8d50f90beebb10
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88355729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4218919910d1defe9ce53d3c83bc3ee4351f723a43693566be868052037c8d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:50:26 GMT
ADD file:79183abf8a1f4a6d4d04d73bcbe47e66f08bea9796acebd37d515855a459d132 in / 
# Thu, 01 Sep 2022 23:50:28 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:46:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:47:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 02 Sep 2022 03:48:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ff717d18c49d9ec97ec3efef7dd73fe40829e1902f57d95a91516a42f69a091a`  
		Last Modified: Thu, 01 Sep 2022 23:53:03 GMT  
		Size: 32.1 MB (32082633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76c734e70f580a1e1db27a87020a89cba5ca648c7e9c85068bd42b1e3126ebe`  
		Last Modified: Fri, 02 Sep 2022 03:58:49 GMT  
		Size: 7.8 MB (7750570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09098d7e8658181028c27fff2df2b67293550987d175c5fab78075ddec7dd8ac`  
		Last Modified: Fri, 02 Sep 2022 03:58:48 GMT  
		Size: 4.4 MB (4361359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc897ebe25a803a066f6b1910e20dec6fc0162253745894a729850d1d32c57c8`  
		Last Modified: Fri, 02 Sep 2022 03:59:13 GMT  
		Size: 44.2 MB (44161167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-scm` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:0ecd3a16684ad715fdc64797dcb67e50a578b932508e659b89877e29aeb60c31
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78259290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eebb88c0344c66b13bb1996a4cd968b97228457505a37dac024aed53fc270e0`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 02 Sep 2022 00:14:23 GMT
ADD file:7c2ab85ecb4dc221c58ed92c05acad8d0b2ad90e46ec34c0a45fd5a5c3a9f7e2 in / 
# Fri, 02 Sep 2022 00:14:25 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 01:16:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 01:17:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 02 Sep 2022 01:20:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:26010bd634bfca42373b6c36c189031dcce89570ea1226e9462a48d7a684240c`  
		Last Modified: Fri, 02 Sep 2022 00:32:57 GMT  
		Size: 25.6 MB (25594334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0826196a5d14cf0f019090771814dce885e1420c992b36ab31bfed7b28d86cf5`  
		Last Modified: Fri, 02 Sep 2022 02:00:23 GMT  
		Size: 5.9 MB (5930253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add19389e79fd75d5e3421d12568767855677a99cc4cfe5d50d5590034851237`  
		Last Modified: Fri, 02 Sep 2022 02:00:18 GMT  
		Size: 3.9 MB (3881273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f04e7e633bdcb9ab785ebbaa03714ef1fb30b6e9341369572e7eb655916151`  
		Last Modified: Fri, 02 Sep 2022 02:02:44 GMT  
		Size: 42.9 MB (42853430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:kinetic-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f129e4299698e3c5c9ab8769330e17dd80fdc69e682f5705ef355e75dfc32ff8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75653148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:505a854970b8539945a41a684cd6895a2b377733c46184f17c584767122c2b75`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 02 Sep 2022 01:03:38 GMT
ADD file:61a0b983796cf76453cbc73a44968b8cefb9f90cc922075728432bdbdaaeb854 in / 
# Fri, 02 Sep 2022 01:03:40 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 02:09:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 02:10:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 02 Sep 2022 02:10:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a51274124ed15147344e4d31d9378a33521faff1de175e551081c34c14db1b9f`  
		Last Modified: Fri, 02 Sep 2022 01:05:17 GMT  
		Size: 26.0 MB (25995506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18a9727cdfe9e4d0ad02573de5f42a04ee40c70d014fcdffb4b684522e06d667`  
		Last Modified: Fri, 02 Sep 2022 02:17:04 GMT  
		Size: 6.5 MB (6470487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd626668509bf2d37bfd328fa211e8e7ad57c719072d9c7f1fc379bc2c187745`  
		Last Modified: Fri, 02 Sep 2022 02:17:04 GMT  
		Size: 3.6 MB (3625387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1947234f2c6685065fd711d09a80a70640e7a9c3b7521b8bbdd0c52afb85d8b5`  
		Last Modified: Fri, 02 Sep 2022 02:17:16 GMT  
		Size: 39.6 MB (39561768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
