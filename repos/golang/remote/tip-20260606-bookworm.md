## `golang:tip-20260606-bookworm`

```console
$ docker pull golang@sha256:380dc6c56c60564e516e98d937d44867734d25a4c0f0689180590fa5f575152b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-20260606-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:8ade52416f2ae50461b0c7b91c3ec6ab785664c2237cd5f8d96bd316f8b6dc29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.5 MB (331484065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17cb4055f4552bcf500174b8b5ce63e19db4a5aef91f919d994639067867fff8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:42:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 04:17:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 04:19:24 GMT
ENV GOTOOLCHAIN=local
# Thu, 11 Jun 2026 04:19:24 GMT
ENV GOPATH=/go
# Thu, 11 Jun 2026 04:19:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 04:19:24 GMT
COPY /target/ / # buildkit
# Thu, 11 Jun 2026 04:19:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 11 Jun 2026 04:19:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da31edd9efdb812e66d13819903973ea6b188d2e7358547676d33d1e3f706f2`  
		Last Modified: Thu, 11 Jun 2026 00:42:23 GMT  
		Size: 24.0 MB (24044000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbaeeb62b9d03a1204b85c3b257aa3e1ce2c4ccfeea479fb2e659211019c29d`  
		Last Modified: Thu, 11 Jun 2026 02:24:43 GMT  
		Size: 64.4 MB (64404116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bad0ceafa428d8443ea6b999370f6c6caf4913f53d36d194a7ed51ca74e9b7`  
		Last Modified: Thu, 11 Jun 2026 04:19:51 GMT  
		Size: 92.5 MB (92481378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9caf2b5917603f564e8b31c080871596acbc699caf5fd0fec4940c836746ec3`  
		Last Modified: Mon, 08 Jun 2026 22:46:13 GMT  
		Size: 102.1 MB (102052370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee129a9fd3fc8202c8d7e6a9548f270cb82dd9749dc72e458b7bd48a6a46da6`  
		Last Modified: Thu, 11 Jun 2026 04:19:48 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260606-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:3584317db16f9b3fee769efbb1adb0bae83bf1f8ff1e5e61b86262cbc04ba393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c12728c14a151eace97ba662058847820d5139f440c72d466e22ebd73b4f74e`

```dockerfile
```

-	Layers:
	-	`sha256:4a35ae5bba582d5301277b3201590047104665e1e36d60362764b3524e74c963`  
		Last Modified: Thu, 11 Jun 2026 04:19:48 GMT  
		Size: 10.5 MB (10497073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a97bce89e40e411b95a92b0edf3043b13d81e46a3d9e8c07cc554175a46ab937`  
		Last Modified: Thu, 11 Jun 2026 04:19:48 GMT  
		Size: 28.4 KB (28390 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260606-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:aa34b0b87e32b5c925c25914af2df2852aeb11b98c0528b035c63d756638db0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.9 MB (289893672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5217c6171ba8c5777042a673017494e3bf05a3d604cf4208d9b9dc59915460e1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:23:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:43:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 05:03:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 05:06:39 GMT
ENV GOTOOLCHAIN=local
# Thu, 11 Jun 2026 05:06:39 GMT
ENV GOPATH=/go
# Thu, 11 Jun 2026 05:06:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 05:06:39 GMT
COPY /target/ / # buildkit
# Thu, 11 Jun 2026 05:06:42 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 11 Jun 2026 05:06:42 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c0213091aa87e4be7caed06dd364889c231dab5ba50fa1e54365eb7a94390261`  
		Last Modified: Wed, 10 Jun 2026 23:39:46 GMT  
		Size: 44.2 MB (44208065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14356188705148a948907491c78974967557826c6ca92209148b3bc14f0f659`  
		Last Modified: Thu, 11 Jun 2026 01:23:38 GMT  
		Size: 21.9 MB (21949873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f917f7c68aa5629a37a99de2287c5dada27c5ba0cd553e5b4f28471c0e6c213`  
		Last Modified: Thu, 11 Jun 2026 02:43:46 GMT  
		Size: 59.7 MB (59661587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1f9d453566f9492c5a02115b3e3090fef81d6957bace4fbb3b7015cbf4942b`  
		Last Modified: Thu, 11 Jun 2026 05:07:07 GMT  
		Size: 66.3 MB (66338954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6017a74f67fe3bf0e9dc5d0c334ab5929b4a454a86c2f391ecc6e1d3f6697e53`  
		Last Modified: Mon, 08 Jun 2026 22:48:21 GMT  
		Size: 97.7 MB (97735035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c03ffeec343870facbc0dda637965fc90bf03bcd0a1805a77b2bbf83c83b5d5`  
		Last Modified: Thu, 11 Jun 2026 05:07:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260606-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:c72f591c838f0a593c5a3beab9ad81ae7025c4c6b1fd659986e0493eb07d2a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62abc8a7f5c8c879780c0ed5473016b8a448d59e55e8ac01fc8e790c4f52e05f`

```dockerfile
```

-	Layers:
	-	`sha256:a25fdd871a3e3200d57662fa011b1cccebbd10f9f7b79ef77dc375513a83ff1d`  
		Last Modified: Thu, 11 Jun 2026 05:07:05 GMT  
		Size: 10.3 MB (10303769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9994eec82ccccd4f0e39d932dda3327448db860688930129a4ce294136f6cdbb`  
		Last Modified: Thu, 11 Jun 2026 05:07:04 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260606-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:e7a63f65d9fc8ee858e1739e1a9c21c66945a32c27926e089edbc197ae7593fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.5 MB (319514451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b035a6210fee7990d60f2744e370ef886a17866cebac420e3212df6cd14b34e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 04:18:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 04:20:31 GMT
ENV GOTOOLCHAIN=local
# Thu, 11 Jun 2026 04:20:31 GMT
ENV GOPATH=/go
# Thu, 11 Jun 2026 04:20:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 04:20:31 GMT
COPY /target/ / # buildkit
# Thu, 11 Jun 2026 04:20:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 11 Jun 2026 04:20:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f511b4c80a6e453785fbcd573c1bf1cb986c4e8d43ed4500ad1ac9a4719762b`  
		Last Modified: Thu, 11 Jun 2026 00:43:56 GMT  
		Size: 23.6 MB (23613296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b715a6712db064e97302c819acd7a39c0c72f8a315ff83c6ad1c27bfa1b275e`  
		Last Modified: Thu, 11 Jun 2026 02:25:01 GMT  
		Size: 64.5 MB (64487878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8ff6d00e6043c0eb328904a409e1791288c1ae9bbfd3fe29f81ed0fcb478d4`  
		Last Modified: Thu, 11 Jun 2026 04:21:00 GMT  
		Size: 86.6 MB (86554685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2308f1cb629a8c8fe52b3b591bdcfb51ba3716d584492ccac8858ffd19fbe4d4`  
		Last Modified: Mon, 08 Jun 2026 22:46:27 GMT  
		Size: 96.5 MB (96469417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7dcab01a60263764b8d6666c6ca97ca725a8476a43e27af5893d065dc21c744`  
		Last Modified: Thu, 11 Jun 2026 04:20:58 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260606-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:59ece2678161742e533c49cd203fb98b77e1da0a768b5fb23b185c80ffe4d920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7a24c5949aec7b5575256bb75691ce48e68300419f98099f16fc3bc0b85c8fe`

```dockerfile
```

-	Layers:
	-	`sha256:32854b1f2257c9464ff8c34c43bcbc389c374473c24ff4cbc7aa77b08ca3527b`  
		Last Modified: Thu, 11 Jun 2026 04:20:58 GMT  
		Size: 10.5 MB (10524897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:970e64a2be5c8676483fdab58ca929e3a2124ff295e705cb0ec692fb27cdc192`  
		Last Modified: Thu, 11 Jun 2026 04:20:57 GMT  
		Size: 28.5 KB (28521 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260606-bookworm` - linux; 386

```console
$ docker pull golang@sha256:c53a88087aa7cac73aa82d2e5b37de566121539ac5eb13be325a69cf5501de7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.3 MB (330296875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a042037a754874f09aa00bc3434bbc0bf3fc80bb195494756bfa428137aa35b0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:44:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 02:24:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 04:14:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 04:17:09 GMT
ENV GOTOOLCHAIN=local
# Thu, 11 Jun 2026 04:17:09 GMT
ENV GOPATH=/go
# Thu, 11 Jun 2026 04:17:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 04:17:09 GMT
COPY /target/ / # buildkit
# Thu, 11 Jun 2026 04:17:11 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 11 Jun 2026 04:17:11 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:08773a2e9b0fe592ef47b4e93c883d32a351ff89ea9cd33f1ad47abd4081b4ca`  
		Last Modified: Wed, 10 Jun 2026 23:39:44 GMT  
		Size: 49.5 MB (49491206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1abb617cf69e81d401bea3de65ddcc50a1ac250e94890ec9ab61cb42a18679`  
		Last Modified: Thu, 11 Jun 2026 00:44:59 GMT  
		Size: 24.9 MB (24879714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cc4b12d03ab32e6c96be6bc5f6e0fc347b431b1f7686aa5f92f4cd1a5cccbc`  
		Last Modified: Thu, 11 Jun 2026 02:24:53 GMT  
		Size: 66.2 MB (66244000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a167d72aa8306eecab6e762ebe6b498d4cb4fb0484b5e093c1523b1df3dadca`  
		Last Modified: Thu, 11 Jun 2026 04:17:38 GMT  
		Size: 89.9 MB (89903788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c856874e83d87ce8611744942560effd5d1e879f3a49a6259f9e0f789a54f9b`  
		Last Modified: Mon, 08 Jun 2026 22:47:42 GMT  
		Size: 99.8 MB (99778009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0743c005b2e3b6f0f78ce2d62b59be98b420617f1d37a0c282797f74d6899d`  
		Last Modified: Thu, 11 Jun 2026 04:17:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260606-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:2f9e2015be964571bdeb16a74e0129ef06d940987f3e0a2bee31a2640104cb55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10505006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253ac9507e2f5f1b9bd54f9df4f471a68329568ad8f52547866cf804c857ed1f`

```dockerfile
```

-	Layers:
	-	`sha256:f376374e8ff4ab24801d7e8d4f3b1d9dd3cc7f866aaf8deb44791315ecfbdc4a`  
		Last Modified: Thu, 11 Jun 2026 04:17:36 GMT  
		Size: 10.5 MB (10476653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26d169f152685836539c9083ed25da9905ee849fd2159a8c291f074051cb2947`  
		Last Modified: Thu, 11 Jun 2026 04:17:36 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260606-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:ea9d993bf7a5d44bb2f592e60814e2a2364271b637ae7b2ccfe7c9599e803695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.2 MB (301237555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a47cf17832096fbe1adfedac5b35d53e1eb3bab8d919224473bbb02ea14bc4fc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 10:04:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 15:11:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 16:19:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jun 2026 00:49:01 GMT
ENV GOTOOLCHAIN=local
# Tue, 09 Jun 2026 00:49:01 GMT
ENV GOPATH=/go
# Tue, 09 Jun 2026 00:49:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2026 00:49:01 GMT
COPY /target/ / # buildkit
# Tue, 09 Jun 2026 00:49:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 09 Jun 2026 00:49:21 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:813eaff938e8991b3dd16851af2c46dd2ffc5bb600e30ff866dd5a60502fbffa`  
		Last Modified: Tue, 19 May 2026 22:35:13 GMT  
		Size: 48.8 MB (48786239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2853b2ecd2cc91271c3528597da43fc45c41515894834d1de212a390afbf0ade`  
		Last Modified: Wed, 20 May 2026 10:05:32 GMT  
		Size: 23.6 MB (23621201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bf4bd887b67ee95b1804bd893717310da36bddd5a598cce7e9b621ff52ee05`  
		Last Modified: Wed, 20 May 2026 15:12:43 GMT  
		Size: 63.3 MB (63316337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d8edfd178bcf28b946d64eb3ad538d4ee96dacac854fd44ba3af295e68b368`  
		Last Modified: Wed, 20 May 2026 16:21:18 GMT  
		Size: 70.1 MB (70084514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb92ec573830782d1ca10f30b4f9a01477e80ea6a11033a9eddfae8ecb46681`  
		Last Modified: Tue, 09 Jun 2026 00:52:05 GMT  
		Size: 95.4 MB (95429106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8309b5ad60730b52d1fed4597ca8807ce124ceca387a26feab1d8f3ab4d7b2d0`  
		Last Modified: Tue, 09 Jun 2026 00:51:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260606-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:5e5c51230604e3639b26b49798484c6b1c64409c1faee75c74b575fa496393c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0dd476f5d88d7fd37ad9b7623d6ceb3535bd728f2959869a5c3ce4e47efff4f`

```dockerfile
```

-	Layers:
	-	`sha256:964c6be7b8bfb44589fa18b34c23b8874b28d3ee0a6363b2e926d23fde56082a`  
		Last Modified: Tue, 09 Jun 2026 00:51:52 GMT  
		Size: 27.1 KB (27124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260606-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:f7aafc7587ede928b8c036c3b98c2f0312c527c6dcc922f156845b2f3a532e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.8 MB (336803225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f412d7b3e213cb5198ff7c012c9af331cd8d3b7b3540deb7da05870e20670f3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:13:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 06:50:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 16:42:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 23:06:07 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Jun 2026 23:06:07 GMT
ENV GOPATH=/go
# Mon, 08 Jun 2026 23:06:07 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 23:06:07 GMT
COPY /target/ / # buildkit
# Mon, 08 Jun 2026 23:06:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Jun 2026 23:06:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f46c910cb3dd366a8b080c77b15459d7465da54412b3570454cddcaf0cdf40`  
		Last Modified: Wed, 20 May 2026 01:13:39 GMT  
		Size: 25.7 MB (25686466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67cb71cd5984ee53ab56bef57a29d3b0ef6e8939c352146b1efe66402d4c7ff`  
		Last Modified: Wed, 20 May 2026 06:51:27 GMT  
		Size: 69.9 MB (69853485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0548bbd70587587ebc4a21c63b5f4bd00f3fc220c1a3dc53c1a1b9debf81aa66`  
		Last Modified: Tue, 02 Jun 2026 16:43:17 GMT  
		Size: 90.5 MB (90495650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1d5d0b8da3315c28f7e047d6d8c920d4423531520a738d9dbd717fd24afb93`  
		Last Modified: Mon, 08 Jun 2026 23:07:16 GMT  
		Size: 98.4 MB (98427267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5778b7a3a72f40e37771cf0810028b6f21ab903020915686feec1da23d7faec`  
		Last Modified: Mon, 08 Jun 2026 23:07:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260606-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:72b27b298677b3e8d070e5ab508395e87768c1d1c7bde04449ca2577c50a125a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f517914df79d9313c91a6716842b3ceeb2cec95ccca028583ad2f68b93421e54`

```dockerfile
```

-	Layers:
	-	`sha256:c9737c6316324c6d5e55039bee74701c5f49db0c6d9d2fe05feb5cce630fc6f5`  
		Last Modified: Mon, 08 Jun 2026 23:07:13 GMT  
		Size: 10.5 MB (10469540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68b0a99d34c1eaf2c303687207fa5e7e2de4017296ff8840ee83eb8541b1d66f`  
		Last Modified: Mon, 08 Jun 2026 23:07:12 GMT  
		Size: 28.4 KB (28432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260606-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:50dbd3618d7f5a49db90d0ce0498a16dc5b11e0fae34617bd96942b0021f1e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.3 MB (304272503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429bbf6985f753e87da4eda1741f05a8587d371883a47c6b914b154aac693579`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:17:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:05:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jun 2026 16:42:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Jun 2026 22:52:26 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Jun 2026 22:52:26 GMT
ENV GOPATH=/go
# Mon, 08 Jun 2026 22:52:26 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 22:52:26 GMT
COPY /target/ / # buildkit
# Mon, 08 Jun 2026 22:52:29 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Jun 2026 22:52:29 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e0fc2c7a6bb12f7a9b333cc117b6ea5fa5cf251c5fa4dd298303beee01028f59`  
		Last Modified: Tue, 19 May 2026 22:35:39 GMT  
		Size: 47.2 MB (47155589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79feab17202415ba0b431eca0e903b1c895e662e755c4c9f1b5678ad8eb605f`  
		Last Modified: Wed, 20 May 2026 00:18:12 GMT  
		Size: 24.0 MB (24039201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511ade0407a6db3c4a6853a735563e5fb22577aaaa32942a9458cc0c09942583`  
		Last Modified: Wed, 20 May 2026 02:05:37 GMT  
		Size: 63.5 MB (63498321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f90b46dcc8622719e19e9e04b1bcb5bc39309966d69636e349c233ba832e30`  
		Last Modified: Tue, 02 Jun 2026 16:42:45 GMT  
		Size: 69.1 MB (69088003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56217687aa3cc648280b9c7052cd68f26077339d92dab45c68b721ed5388981`  
		Last Modified: Mon, 08 Jun 2026 22:53:02 GMT  
		Size: 100.5 MB (100491232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd08ea32efd9c11828b1255d55ab235bb8c1c583bee295d934ea31598fce050`  
		Last Modified: Mon, 08 Jun 2026 22:53:02 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260606-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:273e5a43e244d5924bbdc4767314a4dff32a3f6bb88de9685c20ebfd2507919c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a7cdbbb57abc0c03c2ccf94f6a45f999fb3481d1f5963277d86ec05ad508af`

```dockerfile
```

-	Layers:
	-	`sha256:698115f10be521fd06223098e65a12e9b483f4b1c345620b3eda36b15a4b92fc`  
		Last Modified: Mon, 08 Jun 2026 22:53:02 GMT  
		Size: 10.3 MB (10329561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:716a0f057098121180cb9a966d1cce91bda9e050aa2170f742ccf0e93cb697cf`  
		Last Modified: Mon, 08 Jun 2026 22:53:02 GMT  
		Size: 28.4 KB (28390 bytes)  
		MIME: application/vnd.in-toto+json
