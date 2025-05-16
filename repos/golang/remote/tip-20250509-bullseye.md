## `golang:tip-20250509-bullseye`

```console
$ docker pull golang@sha256:50144a21ae5cce4d3fa34e7b7393f0d28e60812b8a7cf5533d973dbfab71eb4e
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

### `golang:tip-20250509-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:5a0e67f76db9213bd4068bc40ddd1ac235b09090cde008fa2dbac960158d25d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.5 MB (343499696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add2ed03ae9f0454520682b69daa914caae87eb24bceb392bc860c1c5848ba8c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 May 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 12 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 12 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 May 2025 05:23:20 GMT
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
	-	`sha256:a73e8fd31eca2fb5a74e8f18a918f47f1a29b889cbaf9c4a2e2c420858cf8a7f`  
		Last Modified: Tue, 13 May 2025 19:19:04 GMT  
		Size: 91.7 MB (91712999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a030b6acdb6db93394700b17a9f3cc951920ccdced1afb5118ff9ea25b238acd`  
		Last Modified: Tue, 13 May 2025 19:17:15 GMT  
		Size: 127.5 MB (127519249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248c86feda1cc610a2d8d5e11756dcf296675a6b52bf6a1eaab3297680a1978d`  
		Last Modified: Tue, 13 May 2025 19:18:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250509-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:461480bdd92c1635794cb0111c9f9bab069491ac84e1c4d786e6d118722c0153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10294731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76fad5dc082ca8891ebdf8ccb67096fa82829109a90b0bf42b4b66b1433b84d3`

```dockerfile
```

-	Layers:
	-	`sha256:6f89ca0e479416e024600eaa79fead54c28b4dae465a4336fc8f204d7d9bf684`  
		Last Modified: Mon, 12 May 2025 19:16:08 GMT  
		Size: 10.3 MB (10267670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb1bf644caa980ad9827d4a6e9770a3ef5c28d27b2b4a30bf0f4adbc9d7a1cf2`  
		Last Modified: Mon, 12 May 2025 19:16:08 GMT  
		Size: 27.1 KB (27061 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250509-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:ba584b1599cfb4e25fc57ac09e23b11e3318162a3d5fa50845c3fd5861846a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (301955748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc59a4e7bd9f741cf3818dc258e2019feb7f761fce664b7f2f32e16c526804bf`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 May 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 12 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 12 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 May 2025 05:23:20 GMT
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
	-	`sha256:8433d2a5af6a5a0cd9e0774121856fe6f3adabe483560b233f2a94fde92edb03`  
		Last Modified: Mon, 12 May 2025 19:24:40 GMT  
		Size: 122.5 MB (122488656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b616e2e083f3725fb32fd33e43136cf94b24e759b8ce2e27fa3c9cdc72032da2`  
		Last Modified: Mon, 12 May 2025 19:29:53 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250509-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:4ac5f8e2569e3ec36a267a98a8ef5039cf8867451d092729f5cf6f795df095ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10099938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13df6f30bb4ffa21f64db3478d9826a5e14901707789ca0fa30fc04f159896b1`

```dockerfile
```

-	Layers:
	-	`sha256:8613e1d8eb4c4298c6c88af458cee271ed94133279fc94193edec3c1d046f324`  
		Last Modified: Mon, 12 May 2025 19:29:54 GMT  
		Size: 10.1 MB (10072769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f42b015803a7478037c5eb0e7f2f34e31cf79182ccf984f0c4fff624b5f19d4`  
		Last Modified: Mon, 12 May 2025 19:29:53 GMT  
		Size: 27.2 KB (27169 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250509-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:51d6f91ba3a34dded7f01decc186a6e5b4f119626da1579e87250d01d014ae1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.4 MB (324411089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eba23661a09eb403658591c553a623503d86c2297f7bfca153163301456ff87`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 May 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 12 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 12 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 May 2025 05:23:20 GMT
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
	-	`sha256:c5330a97dbc92942ba37ce2bac7d5253897166c49acf8935c0dc87f91eec5803`  
		Last Modified: Fri, 16 May 2025 13:26:20 GMT  
		Size: 120.2 MB (120151716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44dba921c70201ef6cdacfcdacdce388d8887b5fae98ab67bf87611cefdbc626`  
		Last Modified: Fri, 16 May 2025 13:26:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250509-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:fe92cc21a736c1d6e01a629cd5e391010b6bf7fa7b5ce331c855051c040aad6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10295197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014c94a13be04e8391896d13b00acbab48ffcfebd43658f1ea5a084fea1fbef5`

```dockerfile
```

-	Layers:
	-	`sha256:162d06aaccac2bd832191b7729f2680523e25866c89418bebe1338c08cbe30c6`  
		Last Modified: Mon, 12 May 2025 19:16:21 GMT  
		Size: 10.3 MB (10268001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa81ec0eee97cc61d91f99f90eb2373bc3873053ff649786d106619fb715e494`  
		Last Modified: Mon, 12 May 2025 19:16:20 GMT  
		Size: 27.2 KB (27196 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250509-bullseye` - linux; 386

```console
$ docker pull golang@sha256:a7209714bdadd1c1decf8ed5bb428cf23c0c925256b37990ab391ab781588522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.4 MB (345360800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00d4cf504417d2956baa90e59569d9572958a3dde7f08eba7a6a17c2a5b997e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 May 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 May 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 May 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 12 May 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 May 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 12 May 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 May 2025 05:23:20 GMT
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
	-	`sha256:766cf9f231a3ea0cd32772b53ad352b88331a25483b728200717c2a2e88df861`  
		Last Modified: Mon, 12 May 2025 19:16:11 GMT  
		Size: 92.7 MB (92711128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d7e22db058c2c925ae80e0e254d251aaeb04c6161e3b31757924fb81096b47`  
		Last Modified: Mon, 12 May 2025 19:15:56 GMT  
		Size: 125.7 MB (125651733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34021e2329f3a76e3cf0082a43203e022019e01f79e444b6563abd4508f76032`  
		Last Modified: Mon, 12 May 2025 19:16:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250509-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:2d71ed2977434e9667389968f663d6dbf0d434d68ab22aaa8e7cebbb17e5f093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10284489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f06cdefeb0d7443648ab9f090a08d63b9c8291339b9bb9ee6174dc3602f0caa6`

```dockerfile
```

-	Layers:
	-	`sha256:c1a7c7bcfbecc136ed93d04a3bdcd6d922efed6492bc160e25c49ab37c666b79`  
		Last Modified: Mon, 12 May 2025 19:16:08 GMT  
		Size: 10.3 MB (10257461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c17ab9de301b84949a29c839d8a549e627297d3b0905d4c8a8e39cbc3a0e4550`  
		Last Modified: Mon, 12 May 2025 19:16:08 GMT  
		Size: 27.0 KB (27028 bytes)  
		MIME: application/vnd.in-toto+json
