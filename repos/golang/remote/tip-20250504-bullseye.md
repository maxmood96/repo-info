## `golang:tip-20250504-bullseye`

```console
$ docker pull golang@sha256:450d9e7285e7a60d52f22c993a804cc615b1558f9b8a423e0b3d48daaaefeeaf
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
$ docker pull golang@sha256:e316f6c237a320d1e11dbeb4e453756f2d35f5d2c9a2b795edd9b46f39733089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.7 MB (342720654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cfcfb2333f31b3db53e32bbd0f156ff0206809e47bdbaab66b6f0e61bb4e105`
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
		Last Modified: Thu, 08 May 2025 17:04:45 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee1ef79bfdcd8777f441528bcffb7a16f7a3d0852661baef04456810160e792`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 15.8 MB (15763544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68201ec6e5815a0906ce41187e7e52419a2d2c28d73d199e7612f268f81bbc35`  
		Last Modified: Thu, 08 May 2025 17:04:55 GMT  
		Size: 54.8 MB (54756006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbe38c158fae60e9b5dc02cb46e567fc32321319ed04c0e7dd5d1d6315190b7`  
		Last Modified: Thu, 08 May 2025 17:06:17 GMT  
		Size: 91.7 MB (91713117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f43c76dc6ee2ca1c3cdba208e84ccb4e1c5c0677efaf8a998b57c3e624b57e3`  
		Last Modified: Thu, 08 May 2025 17:06:26 GMT  
		Size: 126.7 MB (126740090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569401ee1f379d9ac27dc99bae1b8386bdbc4955c9c4de5f99cb8f5127b22daa`  
		Last Modified: Thu, 08 May 2025 17:06:28 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250504-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:0714e3f7f70e8bad61e1cc5f1b1ebd92a7045f215d75dd314fe3ba3e6b16121b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10294731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d9bb9704ffece8967452352a274b16a467ac1068db05ca8c856ee32a8de17e`

```dockerfile
```

-	Layers:
	-	`sha256:7e36e12874a2ebf64cbdd78f0d812229edf52e8f95eb5a80e985a1d633b6da55`  
		Last Modified: Tue, 06 May 2025 20:11:13 GMT  
		Size: 10.3 MB (10267670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eb9165b9d8ee4347d5847e575f67880715cc7f5c3ffafa6e2f90ac6860260f6`  
		Last Modified: Tue, 06 May 2025 20:11:13 GMT  
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
		Last Modified: Thu, 08 May 2025 17:18:11 GMT  
		Size: 49.0 MB (49040048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de64850f276e76efd1e91be51cb4b2577218e49bf52707b1bf6de3be76028cd8`  
		Last Modified: Thu, 08 May 2025 20:08:04 GMT  
		Size: 14.9 MB (14879026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc4cecedb434598f97e33a3320b6af6e1676388e6c13b31f0aab4b7c9372012`  
		Last Modified: Thu, 08 May 2025 20:08:14 GMT  
		Size: 50.6 MB (50625161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dc7e83fbdf292bf0238a22da7ed8a7b954d4a791ff1772973394bf28d278ed`  
		Last Modified: Thu, 08 May 2025 20:08:17 GMT  
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
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250504-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:0e28a658fe2d1818eccf83a73a573803b228e72b0ec33527e4bbd36de26fad69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10099938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310f9e6f641b47c29493cae03a3fba5420e35004aa015e351106c7f37b0e4a29`

```dockerfile
```

-	Layers:
	-	`sha256:6ab05976e0d64f4b3db60a19c9333baa172a50b4b725748b2960b9de85243d77`  
		Last Modified: Tue, 06 May 2025 20:13:17 GMT  
		Size: 10.1 MB (10072769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c99358e0e044176c75eb9927e762eac180af7b3bb39b44f4de42d4228971c418`  
		Last Modified: Tue, 06 May 2025 20:13:17 GMT  
		Size: 27.2 KB (27169 bytes)  
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
		Last Modified: Thu, 08 May 2025 17:08:39 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4b10bbe754ef0579f7ae8162881d71484a39910114f01fdcee0bc53987fec1`  
		Last Modified: Thu, 08 May 2025 17:09:23 GMT  
		Size: 15.7 MB (15749108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b30b3b7ef57604d52a4f287f3a1202fa7094c2c34ba89e66f13f2ef75a47ae`  
		Last Modified: Thu, 08 May 2025 17:09:26 GMT  
		Size: 54.9 MB (54850001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8c6322f6933d3c7c501627d667e914654793c3d67e2daa5122b6519e08d8af`  
		Last Modified: Thu, 08 May 2025 17:09:40 GMT  
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
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250504-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:886bdd7da09fcf7ea3776509c3c4bb8f95a56de4e7c3486314867f4829e1b00c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10295197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac96d0ab79f801366db24171f1c90543df5a06de7f06bc4f4ac48a424f15eef5`

```dockerfile
```

-	Layers:
	-	`sha256:afdb8cf8a0f0ceb7541d64276ac89075709d3d7465e872356760466c7dff996d`  
		Last Modified: Tue, 06 May 2025 20:11:07 GMT  
		Size: 10.3 MB (10268001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91cc4790964b1467c8940a32060465cf3e82871304ca28e2a657c2b71f825cc0`  
		Last Modified: Tue, 06 May 2025 20:11:07 GMT  
		Size: 27.2 KB (27196 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250504-bullseye` - linux; 386

```console
$ docker pull golang@sha256:05c2540adec19244a7d623a5df0ce92c9c22a3d3a60bd64029e4d4ce82050a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.8 MB (344848777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e6751c12962bde4d8d0e7597fd0752f88a04ca7847b7e40df460755abfc01f`
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
		Last Modified: Thu, 08 May 2025 17:55:44 GMT  
		Size: 54.7 MB (54683102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbb48ef4c334135b55fe5dd328911059bfd41eec15edf03ff0ab96ca44fb6a1`  
		Last Modified: Thu, 08 May 2025 20:09:54 GMT  
		Size: 16.3 MB (16267399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229f9ff435d5a831802e386be1d29f22419a5d3951a76711fcdfc9f9bad0e6e3`  
		Last Modified: Thu, 08 May 2025 20:10:01 GMT  
		Size: 56.0 MB (56047280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033de2af4717a63ec14cea6f0515bfb4f409a31191026656ee48122ed5a0c37c`  
		Last Modified: Tue, 06 May 2025 20:11:51 GMT  
		Size: 92.7 MB (92710902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0adf2ac7302cf0e124e19835cb5b85e5efb297232f12a426c19cbe865f7f8c6`  
		Last Modified: Mon, 05 May 2025 17:33:28 GMT  
		Size: 125.1 MB (125139936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a721f144dab7f2fb3f6ee3a016336bb6f3830e1ea9f5840a7a82e19368bf26c5`  
		Last Modified: Tue, 06 May 2025 20:11:48 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250504-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:2b18767c7ab73972d934fcdd07328f45a303be86d2885211ee706b87d482d794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10284488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1070bb8c940c6842b1bb14ce8a314e2ab8a1cb1a3dde20b3d79c92dc9284416`

```dockerfile
```

-	Layers:
	-	`sha256:d7b3fef803db12bc122272903c7ae4bc7fef83546a7c9923e2a2d99be2807618`  
		Last Modified: Tue, 06 May 2025 20:11:49 GMT  
		Size: 10.3 MB (10257461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6c70db0f0a50988f287d02e215e12a821ad4f1dfc0ebdf93048145736e92cf7`  
		Last Modified: Tue, 06 May 2025 20:11:48 GMT  
		Size: 27.0 KB (27027 bytes)  
		MIME: application/vnd.in-toto+json
