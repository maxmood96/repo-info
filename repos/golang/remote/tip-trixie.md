## `golang:tip-trixie`

```console
$ docker pull golang@sha256:8f2d65a63558e0dbeefc472b18ec29afeea48aca6a121a16868a634ba2f1643e
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `golang:tip-trixie` - linux; amd64

```console
$ docker pull golang@sha256:fcd59df25d0a8b56d4d5e6d745541924266e0aa2d9cabf737a91098d8bee0f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.9 MB (339876219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:146e53ff6ab73d25149651c83f2762d41b538b064ed174a5d1bfa56cd57f81ec`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:10:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:54:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 05:27:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 05:29:11 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Jan 2026 05:29:11 GMT
ENV GOPATH=/go
# Tue, 13 Jan 2026 05:29:11 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:29:11 GMT
COPY /target/ / # buildkit
# Tue, 13 Jan 2026 05:29:14 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Jan 2026 05:29:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2ca1bfae7ba8b9e2a56c1c19a2d14036cae96bf868ca154ca88bc078eaf7c376`  
		Last Modified: Tue, 13 Jan 2026 00:42:40 GMT  
		Size: 49.3 MB (49285621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e18c5e1c15ff34b31f1443e9327b69daaa0c1bd65a23846328fc3738c7f8f1`  
		Last Modified: Tue, 13 Jan 2026 02:11:21 GMT  
		Size: 25.6 MB (25613410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be442a7e0d6f290b909f8da51840566e06ab51bfbea277c70fbda26c44c8259d`  
		Last Modified: Tue, 13 Jan 2026 03:54:48 GMT  
		Size: 67.8 MB (67786776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0424c58d341088bc798ea7f2af5695ba0872af2c75cdf5dd89948be25d2c41`  
		Last Modified: Tue, 13 Jan 2026 05:29:52 GMT  
		Size: 102.1 MB (102138405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e09070cc4c8c6b4577469e540a043174ece319f2134af5f8b6f76f4d7806aa`  
		Last Modified: Mon, 12 Jan 2026 20:05:02 GMT  
		Size: 95.1 MB (95051851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d284a2bce2d42d03bb64d089ce5280bd3d56b842873185d143630cff9b072cd`  
		Last Modified: Tue, 13 Jan 2026 05:29:46 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:2d3c13ea382037a351ac31256779a251472f33a1d34795806a96e7ba226a4cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10814552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af380c5050d0d1c5c27579bf51090fce1396e60e98c74b106eefe8a5107a5a9d`

```dockerfile
```

-	Layers:
	-	`sha256:0f60a1b45d43c54346e9cb5592b3b2e7ebaf5efd961a153f7a0743226be41009`  
		Last Modified: Tue, 13 Jan 2026 06:27:24 GMT  
		Size: 10.8 MB (10785583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3467b471eeef85fd4443f7790c03dddafd7d8abd6088293e4184f7b9fee9bfc9`  
		Last Modified: Tue, 13 Jan 2026 06:27:25 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:06b14085bb509a67fcd8cdafaab86b64626b7a813d72a1de335214718d0040ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.9 MB (301931540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a587ae301af3f23eddb16617d400ec2861b8ffaf61c7aff22941dcec6f94b0e2`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 00:35:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 02:07:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 12 Jan 2026 20:01:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:03:54 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 Jan 2026 20:03:54 GMT
ENV GOPATH=/go
# Mon, 12 Jan 2026 20:03:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:03:54 GMT
COPY /target/ / # buildkit
# Mon, 12 Jan 2026 20:03:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 Jan 2026 20:03:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d20050ceedb84a03f8a4208462819500ff366fe1a69cdbba74b118aa8a38a87a`  
		Last Modified: Mon, 29 Dec 2025 22:28:10 GMT  
		Size: 45.7 MB (45718317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1468c2ee0f43e81d6e097b24054de66ae95db50d77cef08d1eabe51a5dab43cd`  
		Last Modified: Tue, 30 Dec 2025 00:36:02 GMT  
		Size: 23.6 MB (23619911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fa494d16bf7a563003db4c95fa508ca504a77c791075afbc16c7f5a1be17761`  
		Last Modified: Tue, 30 Dec 2025 02:07:44 GMT  
		Size: 62.7 MB (62713662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0ab50dea02f2e70ae39c2606120ff29f94e069200d7d9051ef228a928f84a3`  
		Last Modified: Mon, 12 Jan 2026 20:04:42 GMT  
		Size: 78.7 MB (78745098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb06c5933c094de46d52df9ed5d5962ecacceb10cdc72056e1307b0ee8c18640`  
		Last Modified: Mon, 12 Jan 2026 20:04:47 GMT  
		Size: 91.1 MB (91134394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663db82b186a7e01f52595886098984ce6987a4f476e38e45335e8463e923d1a`  
		Last Modified: Mon, 12 Jan 2026 20:04:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:631fd8bae098a4908ea91ba9144c80e7b69a07bc2c552ec53c2a4e94eaaa99b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10609577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa7be8e3b2214099c5461d6aaa0f95eb7b6ff92d093b0894ae104344a0e9a6b`

```dockerfile
```

-	Layers:
	-	`sha256:bde2297635764f3513473e79309a16ef1c36f5a1860e21133866243eeaf9b068`  
		Last Modified: Mon, 12 Jan 2026 21:24:05 GMT  
		Size: 10.6 MB (10580485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d408eb322859eeb8d6db5b41dd41af61265ad6c0ad6358a31f8dc0f0dedfe310`  
		Last Modified: Mon, 12 Jan 2026 21:24:06 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:3a8a83c1159a59addc0d4419a0d35d002d6a5ca87bcda556098089e73b6b3de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.7 MB (330682982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12af2ece773665689381b2a6122c50c2800617acbc1a5e5b6292bf989cacd305`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:15:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:58:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 05:24:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 05:25:54 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Jan 2026 05:25:54 GMT
ENV GOPATH=/go
# Tue, 13 Jan 2026 05:25:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:25:54 GMT
COPY /target/ / # buildkit
# Tue, 13 Jan 2026 05:25:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Jan 2026 05:25:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:51 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d5b6b6766fd729045e2e7d0396d1f61fe41c612d4aef6bb3bf5ea7db12ae2`  
		Last Modified: Tue, 13 Jan 2026 02:15:57 GMT  
		Size: 25.0 MB (25022636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b629762372f548de0ebccf01b8e80ae5ce251dfd36aef6fc3ae8d963493edf`  
		Last Modified: Tue, 13 Jan 2026 03:58:49 GMT  
		Size: 67.6 MB (67591513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c05cb667e5c85585ed8fd31312103a7a47684b321ef8a0b9f2bf29d377f1303`  
		Last Modified: Tue, 13 Jan 2026 05:26:34 GMT  
		Size: 98.3 MB (98283283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cab7771dc3fd9d6c93b2e8fcd20d3b05cdc987b52c3e09c78b1417acc8931f2`  
		Last Modified: Mon, 12 Jan 2026 20:04:26 GMT  
		Size: 90.1 MB (90137309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ea66fdf05e198af944d6070597e0af2d8dd94fd1c07f1291309fd2fc1384e7`  
		Last Modified: Tue, 13 Jan 2026 05:26:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:9258bcd40f114c573519efa46edaaa8078539437260acb50ccf15875de45bfca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10935162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92d6277bd778e3ddad178fd2d926836ebdc23091a01035d96ded67e0127b2c6e`

```dockerfile
```

-	Layers:
	-	`sha256:e285d10b1bebdb840dc851b58a0b6f44745b6621e25344c918192f5869262f24`  
		Last Modified: Tue, 13 Jan 2026 06:27:42 GMT  
		Size: 10.9 MB (10906038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ea6a8ce2155b25b79bcefecb2793ec66e85c4bb8149f4b073126fc146998a7c`  
		Last Modified: Tue, 13 Jan 2026 06:27:43 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; 386

```console
$ docker pull golang@sha256:630ba0837ff737764cf8da41028d0f2121afbcb73ec72209b5b7a2de754af73b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.9 MB (340908528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f800cf767ba1c2aa376891b6623c42bcc01f79d7879d7031a90ec405e48c1a29`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:03:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 03:04:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 13 Jan 2026 04:25:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 04:27:52 GMT
ENV GOTOOLCHAIN=local
# Tue, 13 Jan 2026 04:27:52 GMT
ENV GOPATH=/go
# Tue, 13 Jan 2026 04:27:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 04:27:52 GMT
COPY /target/ / # buildkit
# Tue, 13 Jan 2026 04:27:54 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 13 Jan 2026 04:27:54 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1f0b243ad587d8f60f107748ba9fe54e338921c7b90e6a5d26e1d50d32f7481b`  
		Last Modified: Tue, 13 Jan 2026 00:43:36 GMT  
		Size: 50.8 MB (50798876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef949cdbd6ae265d5239bd005e65c3d578de54ebe10474ccd2feb9708b6e1843`  
		Last Modified: Tue, 13 Jan 2026 02:03:47 GMT  
		Size: 26.8 MB (26778274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ad78e3f6c783e58b723e0e1c78c005c2b612d1657c3a40830f5d7d97f9d85c`  
		Last Modified: Tue, 13 Jan 2026 03:04:58 GMT  
		Size: 69.8 MB (69803208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5813700a25c469a50c2eddeed956afd8b9daebda8e69149354cd156216538327`  
		Last Modified: Tue, 13 Jan 2026 04:28:34 GMT  
		Size: 100.6 MB (100582458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42b2997976651e9da981a359adb745663b505ba580ded35d1fcd67a84ec5f37`  
		Last Modified: Mon, 12 Jan 2026 20:05:45 GMT  
		Size: 92.9 MB (92945554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090d623ae5461901899bea23034956e65dd57a838b7f3e8c67657d4e451cccf4`  
		Last Modified: Tue, 13 Jan 2026 04:28:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:7d84548e6d62c8906514dea4ff8d1f56f1e9f952ed823c3912a5ba89595fbfc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10785772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeb94be942be288e287f6da0821b25e569262851d1ca8f4e961f345dcc33cc2e`

```dockerfile
```

-	Layers:
	-	`sha256:41d9aae574d2d8710c4cd62ba29485b5b82594f9d0b33def81c7d9fd0c06f352`  
		Last Modified: Tue, 13 Jan 2026 06:27:52 GMT  
		Size: 10.8 MB (10756846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bd93ed353c8c7dbf71b8cff8829042e698fdf2fdd06adb596beb12933a9cabe`  
		Last Modified: Tue, 13 Jan 2026 06:27:53 GMT  
		Size: 28.9 KB (28926 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:53e16fa9f65a500d4e191ddb2c03357362d1f7f571f97b07faaded0eafcfe0a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.6 MB (337635891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed963895040c469cec5d161a811bf8f284fa6bf98e01876e09d9a77adf208252`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 03:18:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 08:22:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 10:23:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:05:00 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 Jan 2026 20:05:00 GMT
ENV GOPATH=/go
# Mon, 12 Jan 2026 20:05:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:05:00 GMT
COPY /target/ / # buildkit
# Mon, 12 Jan 2026 20:05:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 Jan 2026 20:05:09 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d586c84fb9377f9b3f4030e2c3e1e9ff7b1a23a68b8abc2c48a43163a3589257`  
		Last Modified: Tue, 30 Dec 2025 01:51:01 GMT  
		Size: 53.1 MB (53108485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd44afe623a2af1e017b0756e314b5b0882afdc551ddbb8ab4a0e0d718eb8f20`  
		Last Modified: Tue, 30 Dec 2025 03:19:14 GMT  
		Size: 27.0 MB (26996817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1464b5ef37e07d88bfdddc49e0cb0b76c46c151a0ee23e6a2bd75bd6783f9790`  
		Last Modified: Tue, 30 Dec 2025 08:23:35 GMT  
		Size: 73.0 MB (73031008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c305b2563d5a320b2f5d542cb42b58b482a07941244656f1dd066b0fb90900`  
		Last Modified: Tue, 30 Dec 2025 10:25:02 GMT  
		Size: 92.8 MB (92815505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c1f34a163f68379a85adaf1396976b01cd79b6100ad42ff3e6581c97310f7b`  
		Last Modified: Mon, 12 Jan 2026 20:06:42 GMT  
		Size: 91.7 MB (91683920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba7819a636ad71abed7becc2cfb517aaa851c7f08a6fa01a34bf7568fad5926`  
		Last Modified: Mon, 12 Jan 2026 20:05:40 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:a2874812b2d89e0e5fc8e00727acd3718e196c19ed4c006a69b98e942fe2cc78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10809141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006838b4d2b9ff1b3be5b27d32b1e3c46f985ac738564fcc35325b96c04a7621`

```dockerfile
```

-	Layers:
	-	`sha256:e78a217707cd6e0a10ca5d8e4241f70180fd21621edf7feb7f66c538940364fb`  
		Last Modified: Mon, 12 Jan 2026 21:24:51 GMT  
		Size: 10.8 MB (10780294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04bca97a85cbd6f05005616bf21a8b836cdb016242cb751068c0c76598514a4d`  
		Last Modified: Mon, 12 Jan 2026 21:24:53 GMT  
		Size: 28.8 KB (28847 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:4227b64b234ea11f6fc98f6266e3fb5a8f989cf916c05dfdbdd38183b10f77fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.3 MB (363293476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c104e5c5e1534220ae2ab104e6d994efc7941de17712943a63fc1090b5cd4918`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Wed, 31 Dec 2025 10:16:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 01 Jan 2026 12:43:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 02 Jan 2026 20:23:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 06 Jan 2026 01:07:38 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 Jan 2026 01:07:38 GMT
ENV GOPATH=/go
# Tue, 06 Jan 2026 01:07:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 Jan 2026 01:07:38 GMT
COPY /target/ / # buildkit
# Tue, 06 Jan 2026 01:07:55 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 Jan 2026 01:07:55 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:aaf3ef12aa0c431a6203a456b21b1e30e26cb56dfc257b8bca2efe1ba7c531de`  
		Last Modified: Tue, 30 Dec 2025 00:51:33 GMT  
		Size: 47.8 MB (47771153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3f7933c6ef71f06a1f0f33145f157cbfe6df70a0a3efc496c514e6bf0f3c52`  
		Last Modified: Wed, 31 Dec 2025 10:17:43 GMT  
		Size: 25.0 MB (24953863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e727fba04feac92f30181733d92a9aab095f91af402efca58918b26fc389037e`  
		Last Modified: Thu, 01 Jan 2026 12:46:54 GMT  
		Size: 66.7 MB (66660576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b560385f3861ed5a056fb65f6efa479b98fb4edb93cd21d11160f19961a6e0`  
		Last Modified: Fri, 02 Jan 2026 20:32:15 GMT  
		Size: 131.6 MB (131594843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c89a20e33326bd3dc067a98c23f95a9f71a46db050c57b5d95bf4165852889`  
		Last Modified: Tue, 06 Jan 2026 01:15:07 GMT  
		Size: 92.3 MB (92312883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a854a0e7ecb9ef44b4aa62f32b01bf67fd4beb6d7776cb78b502c99f40235383`  
		Last Modified: Tue, 06 Jan 2026 01:14:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:82940c3600f37b2b532932f72d57cd3c099955dd153506477a2ff52555ad4686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10883154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845399ab2348e5670bef91a3be11398e46548c4d1812aa5e35d6334024744123`

```dockerfile
```

-	Layers:
	-	`sha256:33d146c0d9911e481f3fb6176fe62f919ed36b93944794e58b8a3e0cabe21fc0`  
		Last Modified: Tue, 06 Jan 2026 03:24:05 GMT  
		Size: 10.9 MB (10854127 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a823c4dc98b1ef77e153dc72ea02fc1734c629a85254b4c97fc4f4510311ece`  
		Last Modified: Tue, 06 Jan 2026 03:24:06 GMT  
		Size: 29.0 KB (29027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; s390x

```console
$ docker pull golang@sha256:75f0adeecc946ae76261c7c8f794710333dc1349004b49ffdb05d33fa66fb333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.9 MB (314912401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3af474550431b0b1a281869159325f4f0be7569910d1d9b99b16b1bbc6a219f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 04:14:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 06:03:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 05 Jan 2026 20:14:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 12 Jan 2026 20:19:14 GMT
ENV GOTOOLCHAIN=local
# Mon, 12 Jan 2026 20:19:14 GMT
ENV GOPATH=/go
# Mon, 12 Jan 2026 20:19:14 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 12 Jan 2026 20:19:14 GMT
COPY /target/ / # buildkit
# Mon, 12 Jan 2026 20:19:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 12 Jan 2026 20:19:22 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:85bc4a4d1f4e52a33d42907057e0ab87c5eb2560b332d94f6e9d7da79c0c76b8`  
		Last Modified: Tue, 30 Dec 2025 03:26:29 GMT  
		Size: 49.3 MB (49345959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ac6efd7cfec1d611dcf0011d64b56f69fe5f6fe47195e090cb8c04e2584e93`  
		Last Modified: Tue, 30 Dec 2025 04:14:36 GMT  
		Size: 26.8 MB (26786464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978ec2f50f1462efd64a546370da30e382c7f6044ad53993a4af33689f25341a`  
		Last Modified: Tue, 30 Dec 2025 06:04:24 GMT  
		Size: 68.6 MB (68630336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6456995ae6524fffc7b4ebe4332c1913baad4a63bb1876c47a776c976b1b6d2`  
		Last Modified: Mon, 05 Jan 2026 20:14:50 GMT  
		Size: 75.9 MB (75919580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560c721b150b3efd4976a8fc9ccaf826512a0d88981fdddc7ad84ff81c3bfa69`  
		Last Modified: Mon, 12 Jan 2026 20:21:03 GMT  
		Size: 94.2 MB (94229904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aca14230f5c93257ab286dc9043afbbdfa5041a681294abfe0030a7f19bec68`  
		Last Modified: Mon, 12 Jan 2026 20:21:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:692053d3ec2739bafb1b46742525faa640537071284285551d7cb1adbfd4577d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10623871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a16ee13488937d09d7694082e164a7a88eb99a20fd99046806f3497620a5238`

```dockerfile
```

-	Layers:
	-	`sha256:4caec4f68984bd17f69d9b2322480f6db7f2265441df44c043f0fd668d80cf91`  
		Last Modified: Mon, 12 Jan 2026 21:25:02 GMT  
		Size: 10.6 MB (10594908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0af274580c11d85ab27a3e706b99017b62658fbd9cefd8fedc8cc49cc899d547`  
		Last Modified: Mon, 12 Jan 2026 21:25:04 GMT  
		Size: 29.0 KB (28963 bytes)  
		MIME: application/vnd.in-toto+json
