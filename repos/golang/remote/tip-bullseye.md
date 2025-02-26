## `golang:tip-bullseye`

```console
$ docker pull golang@sha256:b46b921519726a4e2da528b40fa75b4a45d7aa3cf42ba24af9d1806e01a2e3ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `golang:tip-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:5f019cba43ad0dbec1bf32dc2594a0e00401c8e2cb05406f639b44372f7965a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.6 MB (339556016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2fc9e88358a8e4940e7a29b87efbdf9f721760690468fb34f81cf73e10366d`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOPATH=/go
# Tue, 18 Feb 2025 12:02:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 12:02:31 GMT
COPY /target/ / # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4ff5a3a54264ee833e4a09583363bbe779e881f15449fe4f4a6a662885dd37fb`  
		Last Modified: Tue, 25 Feb 2025 01:29:47 GMT  
		Size: 53.7 MB (53741401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6bcbc2151ce4be9aa40b26468719dafd6528d7d11d6f6cb60e3a58a3447305`  
		Last Modified: Tue, 25 Feb 2025 02:12:52 GMT  
		Size: 15.6 MB (15558424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e36295709cc3855d0f98f8a6b939053cc43efcf3092756703c1fc518d73fe77`  
		Last Modified: Tue, 25 Feb 2025 03:13:48 GMT  
		Size: 54.8 MB (54752085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00dc29f93ae4a3e4b56a6b3e324ac4a50b328ec374686d1432617f3488c69a5f`  
		Last Modified: Tue, 25 Feb 2025 05:13:49 GMT  
		Size: 86.0 MB (85971517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7cc5764bfa5625e90d4c9d1c4bb7361ceb8d3451c8f3534f5e3a80e9f8aa6e4`  
		Last Modified: Wed, 19 Feb 2025 00:31:23 GMT  
		Size: 129.5 MB (129532433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c4a505fcb168e1abd1151fc8765bc2bc79e1d29ee69de3a0f9a8756dce7c35`  
		Last Modified: Tue, 25 Feb 2025 05:13:48 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:0c5c83093e661214f2bf7da8e176f0b95d5fec5be87397a422cc5ecf64753d15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10294147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67b29ca5cfef6323be8694540d9e9fb0073992bb1a0de3f3f2c2cb6330527f82`

```dockerfile
```

-	Layers:
	-	`sha256:3c6cee0f54c8c102d64095a88650cc1f01c6d6a81033c5ac7dd7aeb7396e6628`  
		Last Modified: Tue, 25 Feb 2025 05:13:48 GMT  
		Size: 10.3 MB (10267086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7a4d3de8b2cabde5fd8e0a05df56f699cab7b7089e7f3d810a07c4090d8fdf7`  
		Last Modified: Tue, 25 Feb 2025 05:13:48 GMT  
		Size: 27.1 KB (27061 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:5f6fb34677c28738c6b5df95952264366baf5cec46367d7e6fc4cb61eff56a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (302032174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e4333794a727dd37dbc4682fa6e847bf8d7eea65037ea026c2a5e682f2a0eb4`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOPATH=/go
# Tue, 18 Feb 2025 12:02:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 12:02:31 GMT
COPY /target/ / # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b371c05b17ddc4521fa62e27633ef500c9e18d0922c933dc30ad692d163a6adb`  
		Last Modified: Tue, 25 Feb 2025 01:31:01 GMT  
		Size: 49.0 MB (49026733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce7f37fed942ce7eb6947b63b02cebac1a836c49ae19b59c3dfd4d0dafde5e9`  
		Last Modified: Tue, 25 Feb 2025 07:17:13 GMT  
		Size: 14.7 MB (14673973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3908d2a88cdaeb59d430f53cffe54008e1006a05c4aa7a391f2dce9c9b9aff8`  
		Last Modified: Tue, 25 Feb 2025 14:18:51 GMT  
		Size: 50.6 MB (50640099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0260b683984b5458b67512624176ac3f678832da5b7aa4c808cea1226ddb01`  
		Last Modified: Tue, 25 Feb 2025 17:02:06 GMT  
		Size: 64.9 MB (64892946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbce18d551f744b2f9a445aaedbcd8c5e283783570d9da4735469555773098f`  
		Last Modified: Wed, 19 Feb 2025 01:09:24 GMT  
		Size: 122.8 MB (122798265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae98f092082c90f0ad1d335d9d7d16d575e847e0acc0459161d0f55fd65adb1`  
		Last Modified: Tue, 25 Feb 2025 21:12:25 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:b3cf468f283334ef2d0aa9d3ab049846beca777eecf2483aeea001bacb7f1bfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10100595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56762df8348cdc595dd7f8d210aece2685f3e8cac5ee686114a98b503eb7e5c8`

```dockerfile
```

-	Layers:
	-	`sha256:34391d1de9112677b46ffddabfd7c5f745b3864803e7d2837df9a89fac04ecc3`  
		Last Modified: Tue, 25 Feb 2025 21:12:26 GMT  
		Size: 10.1 MB (10073426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:345e29b28956cc076e1c528ff8dbc05a61e31da3e8dc50106639278aef0cb6c4`  
		Last Modified: Tue, 25 Feb 2025 21:12:25 GMT  
		Size: 27.2 KB (27169 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:3f5d42564b8f9fc108c90441f69e0d45f52978e0948d19bd4219090af74a8135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.4 MB (326384267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04bf3c8c9a90ecf756a233f75bf80defa949f5d4f570960009e8ae64abbb8929`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOPATH=/go
# Tue, 18 Feb 2025 12:02:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 12:02:31 GMT
COPY /target/ / # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7e1cabb756c27ddad3e1de86c2aaf2bca04f012bff531cd99d37f98896026ca4`  
		Last Modified: Tue, 25 Feb 2025 01:31:16 GMT  
		Size: 52.2 MB (52248644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7364a649b3acc0e2c47a31825e92a687c9eae217b5c8c062f3efaabe7bec06f7`  
		Last Modified: Tue, 25 Feb 2025 05:42:11 GMT  
		Size: 15.5 MB (15544146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8a227b92685cb13561fe06ec9cfa79231e26157c7e163ab5b9af993e63bd10`  
		Last Modified: Tue, 25 Feb 2025 11:54:42 GMT  
		Size: 54.9 MB (54855421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2614c2a3e3d51531f3e6054729bc451d46f9dc5a940312857ed35b9f27a5d5aa`  
		Last Modified: Tue, 25 Feb 2025 15:29:12 GMT  
		Size: 81.4 MB (81382606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5298385c49d911d309658b69d6f0a6876dfdb4d5bed9f2c1fff825ca2fb2fcdb`  
		Last Modified: Wed, 19 Feb 2025 00:40:43 GMT  
		Size: 122.4 MB (122353292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8319be907a866e61c7625cbe30eb5f40b2e687dfe1b55db40be9107059c9410b`  
		Last Modified: Tue, 25 Feb 2025 19:17:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:be1dc85b40f972c9c048656022f9063c6adc18070426834ac7899478464900ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10295855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f12e567b1a822e74251a3551566f5810f58c573a99b3366dbeeba1143c60548`

```dockerfile
```

-	Layers:
	-	`sha256:a0e2e92bef5d0a6a4574cdeae0d443aba87aaa755dfaad2f1e1ad2eb97a30321`  
		Last Modified: Tue, 25 Feb 2025 19:17:12 GMT  
		Size: 10.3 MB (10268658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2297864eb63a1ac1e00f6bcc2130a109b4d9113d74fc5b43acaf2b2baad8a80f`  
		Last Modified: Tue, 25 Feb 2025 19:17:12 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; 386

```console
$ docker pull golang@sha256:1e5fca4543af3c0aee73dcf5d0f4a53fa11831884e77ff4ae7915e54306969fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.3 MB (340336146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a298fc23f24eb2ddc4bdc9f00d0a1c07419ef974f832e2b72297974509e6f9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOTOOLCHAIN=local
# Tue, 18 Feb 2025 12:02:31 GMT
ENV GOPATH=/go
# Tue, 18 Feb 2025 12:02:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Feb 2025 12:02:31 GMT
COPY /target/ / # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 18 Feb 2025 12:02:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7d167bff82d228d113e8b77cccc9449d0007cd097723599b66c8772979708da8`  
		Last Modified: Tue, 25 Feb 2025 01:29:52 GMT  
		Size: 54.7 MB (54678863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e1763bdfcd7e692c8f35c71602a5206ff9e4716856edf6ae712febb4cc579d3`  
		Last Modified: Tue, 25 Feb 2025 02:24:11 GMT  
		Size: 16.1 MB (16062177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820de11811e966e41fc39b6790cf28a33ce0645127033d9f041fa3707235430e`  
		Last Modified: Tue, 25 Feb 2025 03:13:43 GMT  
		Size: 56.0 MB (56030023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee9af4ec198fc9298147d65e6f399f6f943d41330f1c58e2faaf968b360bd5e`  
		Last Modified: Tue, 25 Feb 2025 06:14:46 GMT  
		Size: 87.4 MB (87397986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c865367c21802db35d933085cc324482ddcbb8bd28bfbcd89b6ea5d6a248d00d`  
		Last Modified: Wed, 19 Feb 2025 00:31:35 GMT  
		Size: 126.2 MB (126166939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc23d3755cd37e37e9559025e523c5b7a6057f1d8a20c81aed7834e3aabf7aef`  
		Last Modified: Tue, 25 Feb 2025 06:14:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:ad67486e2d2fa6e240f85f5e1179c53682f4b66f122a91b7c824ef9a9033d8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10283905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97eeaf7c7e8f48eb0d1cd19a61fc11a74fbd37ea2811e6404173c0c4add8bee8`

```dockerfile
```

-	Layers:
	-	`sha256:23779a568b10f4324f26d3808323982f4291e1742c40a196485d4ad6ad019e45`  
		Last Modified: Tue, 25 Feb 2025 06:14:44 GMT  
		Size: 10.3 MB (10256877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2636d69ece919d3254df29f48e97ced2019dd7778fb28adf432cf8efb994d8d8`  
		Last Modified: Tue, 25 Feb 2025 06:14:43 GMT  
		Size: 27.0 KB (27028 bytes)  
		MIME: application/vnd.in-toto+json
