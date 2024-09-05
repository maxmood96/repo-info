## `buildpack-deps:oldstable-scm`

```console
$ docker pull buildpack-deps@sha256:45f5e141493a46219849c6f6acce6edc74e5804b4650f0a40ee16adc9bd5baef
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

### `buildpack-deps:oldstable-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4aef53b9a2eae41c83be8f573280b21013c421e704b19b08312173d0e3e35573
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.6 MB (125571750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03b31b3c521a9d88d81aa84171eba30d1f9b198944fdff4b09f8c830a8751dc2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:56 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Wed, 04 Sep 2024 22:30:57 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:56:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:56:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e779000ed269823143d5ce9acd3ef6f6ff7465222482f7b02c10ba21f448cc`  
		Last Modified: Wed, 04 Sep 2024 23:02:18 GMT  
		Size: 15.8 MB (15764398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d691dff6d17d00b0cbbc4772eb805d97e02504d89ea3e5857cb97c943b74462`  
		Last Modified: Wed, 04 Sep 2024 23:02:33 GMT  
		Size: 54.7 MB (54726023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:a86730fc51beab973cb8add78f2a7e58deebff1e672c01d62614821d77a79a90
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.3 MB (120293588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d361f615568448e949e16d27136fe91cd71e9fa15a0c10306291505053e8b45a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:55:37 GMT
ADD file:1ad1c69027cf70fd9e0302f05fa38c8e0ba5f379ea0946e3cf3ff594a009c1c2 in / 
# Tue, 13 Aug 2024 00:55:38 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:21:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:21:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cb69e1e26795dd48d68a798670cc01030e737d07157119437dfe132cdf786177`  
		Last Modified: Tue, 13 Aug 2024 00:58:47 GMT  
		Size: 52.6 MB (52588991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a171b3b8f43de3f72c3eb383b3b8aa78ac532f090de94fed14d7a1aa1e5c63d`  
		Last Modified: Tue, 13 Aug 2024 01:30:52 GMT  
		Size: 15.4 MB (15375126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc22013229b56309440bd8fc1d5ea5676b191eef21e7b46a13f701910c56462`  
		Last Modified: Tue, 13 Aug 2024 01:31:10 GMT  
		Size: 52.3 MB (52329471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:ce3b9e370af68730a4b51563bd8e8bdafce6d4eff06b4c3bab7af18aed7cae97
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **115.7 MB (115737147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7d917904ba0aba7a811d8927b48c9d24febc228111d2b66aeab0bedbedc6ee`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:17 GMT
ADD file:e3043c245364d9fe593e24bbcac51334dca659e8ec7cd42b6368ba7ea83ea087 in / 
# Wed, 04 Sep 2024 21:58:19 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:30:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:30:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3e424c6173543918aac0bf0552ca8359d23f7b7baa2d77fc8e2c9deb6756f39d`  
		Last Modified: Wed, 04 Sep 2024 22:02:04 GMT  
		Size: 50.2 MB (50240273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0451e8e66d2aa4834e6580560eb32abf8bbac64409d70c85811226b651f2aba`  
		Last Modified: Wed, 04 Sep 2024 22:37:06 GMT  
		Size: 14.9 MB (14879935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a810222c5e9f2cbfb1260daae6fe81f9c63f9fa8cad05812e717e0135194dd`  
		Last Modified: Wed, 04 Sep 2024 22:37:24 GMT  
		Size: 50.6 MB (50616939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:25055f990335dc5e442f1da22b05a2229bfa4e780330493c9fc1a0b91c4d36b3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **124.3 MB (124314780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:058d4847d703ccb14c228bd019b880f4a587bdf25cb89d195fc24363bdea5c75`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:59 GMT
ADD file:aad8b86b3a958bc07504985acedcc819faa4f1ed12ca8b46d8d94c4d564cbdfa in / 
# Wed, 04 Sep 2024 21:40:00 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:03:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:03:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d82c4492ee91810a42e0c53e955a661e9a092364bc474c9db559ea5b24b7047f`  
		Last Modified: Wed, 04 Sep 2024 21:42:52 GMT  
		Size: 53.7 MB (53731619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf248fd698830ce7c74f07fb7ca6adac7bea55a16521e9e1f2afe06219e00f6`  
		Last Modified: Wed, 04 Sep 2024 22:08:56 GMT  
		Size: 15.7 MB (15749712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b216df41d3eb392b55b4bb8c654fe024d7c3d00404a7e105f494ef43990fad`  
		Last Modified: Wed, 04 Sep 2024 22:09:10 GMT  
		Size: 54.8 MB (54833449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; 386

```console
$ docker pull buildpack-deps@sha256:2c3044d7a286ae2a788c5b37f5bd2fe6aa0ffbc115851050defffac0fd544962
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128269754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe6dbb003a1a505f2070fde5fd98afdca9b926fea0fee1d727d782182c96a174`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:06 GMT
ADD file:b4823f40fb9693690d7dfe07f6179ae1ea0a288d8912f4f8365d372e27134f0e in / 
# Tue, 13 Aug 2024 00:39:07 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:07:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:07:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c99355adbbcd3ac4e44cd6fb2596fed1658ea87be87df9894ec5aaf076a548b2`  
		Last Modified: Tue, 13 Aug 2024 00:42:55 GMT  
		Size: 56.1 MB (56074104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d740897ef0cfebeecea08cfc67998814e44c45164f9dc7c044e9e2a0507541f4`  
		Last Modified: Tue, 13 Aug 2024 01:15:00 GMT  
		Size: 16.3 MB (16267943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dab982039e3c0ad98af0fa361fb64e7b9635b80923dca6744c230e0994f2bf3`  
		Last Modified: Tue, 13 Aug 2024 01:15:21 GMT  
		Size: 55.9 MB (55927707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:35b801921e609d3209dacf1b5ba52b01de7c3aa9e8aa02c6391d36341e616684
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122356344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcab7119b603616470e424761bd314b03772c99f37bb1c28be22208d5e17e2ae`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:11:45 GMT
ADD file:6c103cf641951f38237d461bf13e5ba7a8b38776409e4443857a95928d972a64 in / 
# Tue, 13 Aug 2024 00:11:51 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:03:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:05:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fbfd53ead15e1f39becdee0e90a399fced0550dcbe1c27017a0256c390b08747`  
		Last Modified: Tue, 13 Aug 2024 00:23:13 GMT  
		Size: 53.3 MB (53310557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975486c9b8367654ca68daf3f98e4da57b660b9ac9788562fa218a38d9db4e6e`  
		Last Modified: Tue, 13 Aug 2024 01:34:35 GMT  
		Size: 15.7 MB (15734788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3b3474926636ee8b68ffaabc4b0327c4331cc3894af8f568c64d5f6f1d8594`  
		Last Modified: Tue, 13 Aug 2024 01:35:20 GMT  
		Size: 53.3 MB (53310999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b24b3a40397e5e4780ec4987a4c5de21b5a10aed81c711c231d6debb8669d609
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134593168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c221000ca1ce797c56fce59ac01ef1cd91a243101b30d6d0fec00980d1226a63`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:22:14 GMT
ADD file:25dc93c8090a0afba4b41321f81883857bfdd6b30ea9f278833c5a5d9d16ad52 in / 
# Tue, 13 Aug 2024 00:22:18 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:23:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dad1c3eca3bf4b2a67cef1dbad507d7a913df7bbe1e3f88044230dd291ada39d`  
		Last Modified: Tue, 13 Aug 2024 00:26:46 GMT  
		Size: 59.0 MB (58954654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b50eef4accfc66462c4cf81c03bb57857b5f3ac891da5b87bfdf1ba826c9677`  
		Last Modified: Tue, 13 Aug 2024 01:36:03 GMT  
		Size: 16.8 MB (16765928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df0e65d951ce5d0b07cbb65477bbb01cfa607241b5c5855f4fb361bedfd1247`  
		Last Modified: Tue, 13 Aug 2024 01:36:21 GMT  
		Size: 58.9 MB (58872586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3946705950289b1cd5ee35a7981aabd8a53eafc5e536516a12c29dcb83bc7205
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.0 MB (123041240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c52f640c0a850aadaaf7abcdfb8230a8322f73ee3c1e5c69a140e8d7e315c26`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:42:51 GMT
ADD file:993091e64467ec0ea9bcecdd744da64284d459b933863322bd011dd2111f47c1 in / 
# Tue, 13 Aug 2024 00:42:53 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:17:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:18:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9c1a2da0ad07de8657187bee6e4fad1ff817bafdbac14fb77a3953cd7f50038c`  
		Last Modified: Tue, 13 Aug 2024 00:47:43 GMT  
		Size: 53.3 MB (53324089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c695efccb58000e04eb154deca02ce22ea52fd05ee4246281c66bb7a42d20a96`  
		Last Modified: Tue, 13 Aug 2024 01:25:32 GMT  
		Size: 15.6 MB (15641934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f3f87ffa253b4cb357637ad56494facf5bf533f6fd3bdf78f1066c6fb0fb23`  
		Last Modified: Tue, 13 Aug 2024 01:25:44 GMT  
		Size: 54.1 MB (54075217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
