## `buildpack-deps:unstable-curl`

```console
$ docker pull buildpack-deps@sha256:90d38ab30c9b50e48931e72bee869056a0f493b924a15d3fce0f7ebb96efa334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:unstable-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:5e4438a4660fff39ff4671bc5ecfaea3e639dafe61d5c19c735335c96d61c1e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77224544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810a6c7341783cb46e4dd6dfd3619ce659ebdab997fb5297a3baaa9a9d90e94d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:22:38 GMT
ADD file:3a737ad8ab65fe5ad068d6094fbf99ce9ed2b5beff9c86daceee8c2c50182bde in / 
# Tue, 12 Mar 2024 01:22:38 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:58:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:490d250d3b2798e2c88a398b87b4162c8ca53e579e4e79b47fc41c2c2aaca6fb`  
		Last Modified: Tue, 12 Mar 2024 01:28:23 GMT  
		Size: 51.5 MB (51512918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:355c7ca394663c3c42de69370984f58c9ec1386fb7bf3892311813e2a6b72eff`  
		Last Modified: Tue, 12 Mar 2024 06:05:25 GMT  
		Size: 25.7 MB (25711626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:b839041109743d570e5b781207c8b6dd0d83f7a02c1312c39b3abb5859206ead
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72475557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f0f7d477c9f33dfcd2679ea280f5c1a52efe266dd8936b0206e4796fc5b1727`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:09:36 GMT
ADD file:624f450cf1c3fdf8774bf8313557baecef902871c3ad8dff4410f14122f8c507 in / 
# Tue, 13 Feb 2024 01:09:37 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:46:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:24aea175239943bb2adfa7be646a8e0c040383dec937faf220aee85a3f296298`  
		Last Modified: Tue, 13 Feb 2024 01:15:26 GMT  
		Size: 49.4 MB (49423639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c530646f760ee121e031a3cfc99e5f7b580df8596f51a1f5e30e10af689119c`  
		Last Modified: Tue, 13 Feb 2024 01:56:34 GMT  
		Size: 23.1 MB (23051918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d6b8be762fd7b820a830a3321642176df58972875bda564d8ab9992399b21a19
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69289468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:847f66994b4f16318f221a7a1e0bfc18624e296073c3f43d158ff2b83d9c8b0d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:22:33 GMT
ADD file:fd66e10084783208c7cc3adad23d5c975d8f5be56c462c5a37d7a50fffacb677 in / 
# Tue, 13 Feb 2024 01:22:34 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:20:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a9ce49138215d345df26ba8499250bd7c71ec90f1afb15a8ac29dcd7248b188d`  
		Last Modified: Tue, 13 Feb 2024 01:29:59 GMT  
		Size: 46.9 MB (46928854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bed3d75f3913415a967fa0e909adbaf536b4d7ca377cf97730e2135c92b5c0f`  
		Last Modified: Tue, 13 Feb 2024 04:30:48 GMT  
		Size: 22.4 MB (22360614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:dee95caf6b0c1b455dab609a6e0282663050236260541b469810fa55162fb004
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76787782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ff7c840b9981f6f0fd6b0e70d260740b6df8d7a5768f5f7731a3c93d639fd8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:46:41 GMT
ADD file:1202a56d8723ce5bee3f68e3d9488cef88889fe8b2bb138cde766ff787577a7b in / 
# Tue, 12 Mar 2024 00:46:42 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:29:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8e7b106821c007c3c67e9a4d248bd2f87194491ad746f2aa752c5b0ba2fca099`  
		Last Modified: Tue, 12 Mar 2024 00:51:35 GMT  
		Size: 51.4 MB (51353263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa13c84a803d4b150b717babd5d0b89e39ce55a7c4c07cfbc3d34a5e4ce85a3`  
		Last Modified: Tue, 12 Mar 2024 01:37:43 GMT  
		Size: 25.4 MB (25434519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5a308728d3b203f524e96e1e51691b47168168b7318136b03ff137e66eb6ee7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78457588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345b0696be583a4588b82ce28f76fa3e2241256e439d3cf9a96e63c5314f54a2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:38 GMT
ADD file:4189b090bbf8678fcabd8dabb56450346892e68ce7343823f5a1de966a7cfba7 in / 
# Tue, 13 Feb 2024 00:40:38 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:24:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:986c70cdc0585f2b2041c18972cf24b00e1384bf0ae25efa4ed418df60c27f39`  
		Last Modified: Tue, 13 Feb 2024 00:47:09 GMT  
		Size: 53.2 MB (53166067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5992ae92ecc708d9f7dbc50c93a7a44033fbb23286817ad552428376a53b6b21`  
		Last Modified: Tue, 13 Feb 2024 01:33:35 GMT  
		Size: 25.3 MB (25291521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:9ae3abcadf151f05e161d783db0ae32a1ad48e966b277f47310cf428182810e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76380859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff73139fa14bece8576ebddae00b3237b2a6b33f4af5a7b06f7e087928e41036`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:09:20 GMT
ADD file:19ebc3428f26cc4bc4aed9fbd4cf7f5f3ee4b77b9740ca3ad10c77626e14bc82 in / 
# Tue, 12 Mar 2024 01:09:25 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:21:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:38f59bdee9eac9fb953df0852a9bf0458844eaf90c474ba863879a284671eca6`  
		Last Modified: Tue, 12 Mar 2024 01:21:04 GMT  
		Size: 50.6 MB (50572329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a77dad95891fc49c3987711b4646cb679c4a443baceb97ed9b60ab673bd2cbc6`  
		Last Modified: Tue, 12 Mar 2024 02:48:12 GMT  
		Size: 25.8 MB (25808530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:f4d801f38cacd0f7e8238d9fa9b555397d005871c797600a236673a8f1009a78
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83231257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76df9f8d1769ffd0312ec0f89c5d0a0d872c9c014d7599bb90d44c845764aacd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:32:08 GMT
ADD file:5a26866ec93cd672e68eb3b6408e2d78eb1ceb2804d316ab9e215bb248c396ea in / 
# Tue, 12 Mar 2024 00:32:16 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:51:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7d54e43a79af3d6c46553326fe893093beb487d05a53a78510db1edf5ad46734`  
		Last Modified: Tue, 12 Mar 2024 00:40:01 GMT  
		Size: 55.3 MB (55261063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b06e7f021e50f240952103e6d889ea6a36f09aeae1132a71b34e28c7e5d70c0`  
		Last Modified: Tue, 12 Mar 2024 02:22:32 GMT  
		Size: 28.0 MB (27970194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:e92f86976a5cd03080f3085c1e3b01120ea86bcdb7b626462007d6404ad1cefb
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74382105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d59d38898e1d4062b30c25a537ea543f591df07098a4bf01ce7cab34e3154aef`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:08:51 GMT
ADD file:ad62fb7e744226b84b9b87b22c6b1e797cb2a179f4f2c7295e0db14b95dcd84a in / 
# Tue, 12 Mar 2024 01:08:54 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:30:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9c2efbfef38bc6f28418aabddc7ba24be7bed3ebbd2673ebc8db7533e9ae8c47`  
		Last Modified: Tue, 12 Mar 2024 01:11:24 GMT  
		Size: 49.7 MB (49682014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ab338dc4eeec296303efc67a955dedb7028ccf69f05896a788076dbc0a4108`  
		Last Modified: Tue, 12 Mar 2024 01:41:00 GMT  
		Size: 24.7 MB (24700091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b1495b19a1aef63cffb7ed02e326d62ebe3f7a8302e9dc9078de88cdb0138cec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77423194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6080271906badcffc8ea612ac576254148c13a27b420400e2e28096aaf192f4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:02:33 GMT
ADD file:5d186ec2d875f4307a34d264914243316106515ef9072abb7cf5e80c252da588 in / 
# Tue, 12 Mar 2024 01:02:36 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:21:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ec6259c8a823fea482e8e351d24e5f493bd9f11e76074191518e50ac63335314`  
		Last Modified: Tue, 12 Mar 2024 01:22:34 GMT  
		Size: 50.9 MB (50889351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d95670fd7000d49d11835682e227fc4e48c87caf6a3e9e49895a14def51b2b0`  
		Last Modified: Tue, 12 Mar 2024 02:49:09 GMT  
		Size: 26.5 MB (26533843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
