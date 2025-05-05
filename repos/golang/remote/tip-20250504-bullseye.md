## `golang:tip-20250504-bullseye`

```console
$ docker pull golang@sha256:e2a4dfa3557d5877fe8506f52d8f7c17d50fed39bb365f1b7d767aea905eef56
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

### `golang:tip-20250504-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:78ceb37149ba9c15a8b9626c9aadf7a41e79a76187765847a30e461ee98a61df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.7 MB (342720560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2c019a69726fbea9266af41ec7378d13920e4d998b096e29474d3cc0ffbde32`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 May 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 05 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 05 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee1ef79bfdcd8777f441528bcffb7a16f7a3d0852661baef04456810160e792`  
		Last Modified: Mon, 28 Apr 2025 21:55:44 GMT  
		Size: 15.8 MB (15763544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68201ec6e5815a0906ce41187e7e52419a2d2c28d73d199e7612f268f81bbc35`  
		Last Modified: Mon, 28 Apr 2025 22:15:30 GMT  
		Size: 54.8 MB (54756006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47e2812dc7daed54fb83b4b63ef1e805f4f93a8d68290f63c3c40db7bb4f8d6`  
		Last Modified: Mon, 05 May 2025 17:33:16 GMT  
		Size: 91.7 MB (91713022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f43c76dc6ee2ca1c3cdba208e84ccb4e1c5c0677efaf8a998b57c3e624b57e3`  
		Last Modified: Mon, 05 May 2025 17:32:51 GMT  
		Size: 126.7 MB (126740090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf07f23354512529fdf033cba241829dd0609f12b49090e26d91ccdbb16482ad`  
		Last Modified: Mon, 05 May 2025 17:33:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250504-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:cee3bd06fe133224881addc57420c6796e60a0999b46133791664827b3d3b93f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10294731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cffa5d2ad0771d742987907ccfc9387d282b9c2b26e2e7e057f0bc8f72b835cb`

```dockerfile
```

-	Layers:
	-	`sha256:18cc86e33f30fcd29248d4a87d086028a91a69d16e003e5592db71b783db7d0e`  
		Last Modified: Mon, 05 May 2025 17:33:14 GMT  
		Size: 10.3 MB (10267670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed4e3820fa061af9c09fc0733b59c4a0decb655af823d5758192dde6e9a9aa63`  
		Last Modified: Mon, 05 May 2025 17:33:13 GMT  
		Size: 27.1 KB (27061 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250504-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:3529add1e97d781018a57e721fab0c7e9b22b72642fbffa7f900687eca255285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.2 MB (301232359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f791f28ed89f6b2c443289699ce48cacfd7637e9683fda5455b7ec00543d65`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 May 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 05 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 05 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:72fa46f1d669ee2de1ffbc36b654bfe8dd0aad49156f4143a5d9edd3a5c3d559`  
		Last Modified: Mon, 28 Apr 2025 21:16:06 GMT  
		Size: 49.0 MB (49040048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de64850f276e76efd1e91be51cb4b2577218e49bf52707b1bf6de3be76028cd8`  
		Last Modified: Tue, 29 Apr 2025 03:37:44 GMT  
		Size: 14.9 MB (14879026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc4cecedb434598f97e33a3320b6af6e1676388e6c13b31f0aab4b7c9372012`  
		Last Modified: Tue, 29 Apr 2025 13:23:50 GMT  
		Size: 50.6 MB (50625161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dc7e83fbdf292bf0238a22da7ed8a7b954d4a791ff1772973394bf28d278ed`  
		Last Modified: Tue, 29 Apr 2025 17:00:23 GMT  
		Size: 64.9 MB (64922699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185f617f5384afe02adfbf4600ef1c02d06ba922d332b58b68dacf2c75505cb9`  
		Last Modified: Mon, 05 May 2025 17:58:33 GMT  
		Size: 121.8 MB (121765268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43196f48089665eebab8c7be5e9ead230275031d9ae303ca760877307b8f8b77`  
		Last Modified: Mon, 05 May 2025 18:02:42 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250504-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:43f865c2e124c8771b6a8c85210a710b660e965dbfd20e4722076a68aae43c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10099937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:390ee596330fce88f2be65cc4932e6def8b06486b250c10354099622d261d5f6`

```dockerfile
```

-	Layers:
	-	`sha256:48e80bc552489c7d49b20195a0ba14feb647a032a66f198d05d758dcce7dc274`  
		Last Modified: Mon, 05 May 2025 18:02:43 GMT  
		Size: 10.1 MB (10072769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ce13ae54c1b46a29c9c986741f0e2e21f7fd4f31206b9c5e1e39c7660f5871`  
		Last Modified: Mon, 05 May 2025 18:02:42 GMT  
		Size: 27.2 KB (27168 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250504-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:dde42bb12a19b04b939c5043e9a949f9103fc35bc0401df5d9511e5a85133bdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.8 MB (323752833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7de637b488edeae60eec6e74875d90900e887a3b523ac1610c529be46de6df`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 May 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 05 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 05 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4b10bbe754ef0579f7ae8162881d71484a39910114f01fdcee0bc53987fec1`  
		Last Modified: Tue, 29 Apr 2025 01:47:13 GMT  
		Size: 15.7 MB (15749108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b30b3b7ef57604d52a4f287f3a1202fa7094c2c34ba89e66f13f2ef75a47ae`  
		Last Modified: Tue, 29 Apr 2025 18:37:49 GMT  
		Size: 54.9 MB (54850001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8c6322f6933d3c7c501627d667e914654793c3d67e2daa5122b6519e08d8af`  
		Last Modified: Wed, 30 Apr 2025 02:35:23 GMT  
		Size: 81.4 MB (81414127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef5eba61a9fd66fab686113f68ca3d5af338e13d6c7abcb7f6724a255553e9d`  
		Last Modified: Mon, 05 May 2025 21:09:20 GMT  
		Size: 119.5 MB (119493460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7396831c8294bc0ccf7ed1363583bcee39bb25b0fb5715e8c8cbbb533a293c`  
		Last Modified: Mon, 05 May 2025 21:11:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250504-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:376838716791da58f50b8165c2b6bb43a0cbafc5df1989b713a09f811e31812a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10295198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5267e5c205daeb2b02cad182bb8ba59500001f97c08071ab72eccbbfc9f3aca1`

```dockerfile
```

-	Layers:
	-	`sha256:c135f5ddf07c03577f4c07fdf58842fde2500e1f6e8c95cf9d8407bf5c1d6a7f`  
		Last Modified: Mon, 05 May 2025 21:11:37 GMT  
		Size: 10.3 MB (10268001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8d0944e18ee29a893b7b49ff0280918771a1192af9d1e225a86d3802e4d3d93`  
		Last Modified: Mon, 05 May 2025 21:11:36 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250504-bullseye` - linux; 386

```console
$ docker pull golang@sha256:eaebf75710f248d71070768b1583049fc8b73ecf56607d814ce2125ca6c4e893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.8 MB (344848821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df31e65e4b6f49abad9a8253f5b46711503fad457cccc9d69c677756d13c8b52`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 May 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 05 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 05 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 05 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 05 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 05 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 05 May 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4ef50a397f2c0106a3e44d1d1bae16cf52fb5e7e855c588f4098e281321c3e7b`  
		Last Modified: Mon, 28 Apr 2025 21:08:10 GMT  
		Size: 54.7 MB (54683102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbb48ef4c334135b55fe5dd328911059bfd41eec15edf03ff0ab96ca44fb6a1`  
		Last Modified: Mon, 28 Apr 2025 21:53:52 GMT  
		Size: 16.3 MB (16267399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229f9ff435d5a831802e386be1d29f22419a5d3951a76711fcdfc9f9bad0e6e3`  
		Last Modified: Mon, 28 Apr 2025 22:14:52 GMT  
		Size: 56.0 MB (56047280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b94d1f03ccd9def322116e17b6dc536c25764dbdb985db70d77113d763d0f9f`  
		Last Modified: Mon, 05 May 2025 17:33:35 GMT  
		Size: 92.7 MB (92710945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0adf2ac7302cf0e124e19835cb5b85e5efb297232f12a426c19cbe865f7f8c6`  
		Last Modified: Mon, 05 May 2025 17:33:28 GMT  
		Size: 125.1 MB (125139936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd4a235619852db086b59becc85bff78fe57721e6e687533e142881a52ca1d8`  
		Last Modified: Mon, 05 May 2025 17:33:32 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250504-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:cd0993d960dabf158c5a0ea50aec036994e44250a5fbe97359f3aef7db39dcfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10284489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d731ef2dc640c24c5c0b29d137796a21b58630786495142d9bd61730f44000b`

```dockerfile
```

-	Layers:
	-	`sha256:ff79a2c36604da6cf6aa738da56657b0c044a97f8f5a43e3d8007c10bd442eae`  
		Last Modified: Mon, 05 May 2025 17:33:32 GMT  
		Size: 10.3 MB (10257461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82b8265e945b19aeb1d3f9658043d3bf8e2529c2979b6ba1a9f40449ebfa6a29`  
		Last Modified: Mon, 05 May 2025 17:33:32 GMT  
		Size: 27.0 KB (27028 bytes)  
		MIME: application/vnd.in-toto+json
