## `golang:tip-bullseye`

```console
$ docker pull golang@sha256:f1e61df7bc87b278b98ba0472aac7d8040b62b9f59ec5f9a7b9a8e404cb8ed5f
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
$ docker pull golang@sha256:62dcac6d70fd58dcf14803c3cb50fa66675fa630e8d180b30b71757012607a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.9 MB (339891724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60759757b46e93764a6461bf52e7fc2ea9ee6fda4b4054179a202f4a682b9951`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
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
	-	`sha256:6d44c2a3aadd581d3ba33981fbf40d89bc93f7f56b7b4f0b7f9f36756e074333`  
		Last Modified: Tue, 04 Mar 2025 21:59:58 GMT  
		Size: 86.0 MB (86000883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b704ebeab23a12c1391628665925189d800995f90d6bab09fc653f615d683c07`  
		Last Modified: Tue, 04 Mar 2025 00:32:19 GMT  
		Size: 129.8 MB (129838774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0deb6359486f9aeadae095056f0cd9deaf1f001e2eb897398e42a6eef196653`  
		Last Modified: Tue, 04 Mar 2025 21:59:57 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:4fd56450e99edcb0c8b206d9346ce4df0df08a21aa1d6e68b280c672761bd293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10291345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6b14208ed32284604d9967d921c86129cd4e5c2b134ca91b6f48dd7d6cfb57`

```dockerfile
```

-	Layers:
	-	`sha256:cc1fd163b16f0853b2665dc97349995a283da74a3889e6b96c3614fd55123ece`  
		Last Modified: Tue, 04 Mar 2025 21:59:57 GMT  
		Size: 10.3 MB (10264285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6ded37c5c98599190e6d355c5960ae04be289c30392fef26f3ffe2117709bb3`  
		Last Modified: Tue, 04 Mar 2025 21:59:56 GMT  
		Size: 27.1 KB (27060 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:a837900a5d01c9547b57977ea1a02bf58b80e7511f11f4f8595c93e627175084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.3 MB (302321460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177e21b309adfd8889d84e4032513dffe79d27b718f105981f993bb5b4f31a1c`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
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
	-	`sha256:c66a4732c96edfeab450050a70f02b158342482c6f2a5dcf7aeba30aac7fcc17`  
		Last Modified: Tue, 04 Mar 2025 00:33:46 GMT  
		Size: 123.1 MB (123087551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae22e48255c2f697b9fca095191c64ef9ed4dbb370fe1ee1e80e85c90a5274d2`  
		Last Modified: Tue, 04 Mar 2025 00:37:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:25af0f0c1196cd8ad32d78feb1c9fa62f9819ab3a1daefbc1b2e005f7415b816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10097793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4963da3acef477f39691ee4f80c26fd79d4c730a43035bbe22d2c589d0d163fc`

```dockerfile
```

-	Layers:
	-	`sha256:707121e3da254088f7e27a8a442185b19fa81e3b0f6f9a2034f6a865cfe8e5fa`  
		Last Modified: Tue, 04 Mar 2025 22:15:04 GMT  
		Size: 10.1 MB (10070625 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d21325f6a0da5de13e757a3d24baf279c62a8c807fb691aee48a906f6f2ea60`  
		Last Modified: Tue, 04 Mar 2025 22:15:03 GMT  
		Size: 27.2 KB (27168 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:e9da58c31852e94c9d6b192024d06896897f027441c926eb70fa4dabe93d1775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.7 MB (326682733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa2f0ba3e67dbb5bf8eb1eb1ddc3744d82e82d55f96b45e07f33998ae843585`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
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
	-	`sha256:79c63332dc2fc1cf0757c0675d81bf024aa3d2b601d0c397704255d7fd384be6`  
		Last Modified: Tue, 04 Mar 2025 00:42:12 GMT  
		Size: 81.4 MB (81413797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2fb2f15af0e54e78387b98706e083a5882e5cd46c9ae24a07d9c9a7de13391d`  
		Last Modified: Tue, 04 Mar 2025 00:39:29 GMT  
		Size: 122.6 MB (122620567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b74e6d376969b3acea37d06a45e7f19217aef54404da6c16397c1abc7641bdb`  
		Last Modified: Tue, 04 Mar 2025 00:42:10 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:451f28dfd57647c211f072df5bcf49aa1c7fc25244bd07e0b8ed5e36cc9c83d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10293054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98efb21f10df10b51c350b6727cc500d1d19f65b05bc6452d241139d1fc4af15`

```dockerfile
```

-	Layers:
	-	`sha256:7d4a5c1e45a18fec7adfb277a307acb61ab383ec5081da380d2d93e5c252c87f`  
		Last Modified: Tue, 04 Mar 2025 22:20:37 GMT  
		Size: 10.3 MB (10265857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad119960eb2d0449d19288fcb159c141e98569eb9a5399f7196c5c5d7b0e7e6d`  
		Last Modified: Tue, 04 Mar 2025 22:20:36 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bullseye` - linux; 386

```console
$ docker pull golang@sha256:14a81ceb13fc174873ff5c395855425659fee0eb0b439d1524e37cdbfb658564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340656022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f9483359d29a5c0f11f5452e4547cb3437c15f40b9efa8cc8a0bb8a97f7108`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOTOOLCHAIN=local
# Mon, 03 Mar 2025 00:23:21 GMT
ENV GOPATH=/go
# Mon, 03 Mar 2025 00:23:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 03 Mar 2025 00:23:21 GMT
COPY /target/ / # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 03 Mar 2025 00:23:21 GMT
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
	-	`sha256:099e714f411a07c15d57b3291da56d563f413f354f5a9a169b3f04559c50214a`  
		Last Modified: Tue, 04 Mar 2025 22:00:29 GMT  
		Size: 87.4 MB (87426571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc05ee2fc954345b4dc36b55c348df7ba176cd1d037dcc0fd8ba6eedfb02eea9`  
		Last Modified: Tue, 04 Mar 2025 00:32:40 GMT  
		Size: 126.5 MB (126458230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdfb8dad7a2ca58369213b68e78a8918222d70b5007d71a284c56deff914743`  
		Last Modified: Tue, 04 Mar 2025 22:00:26 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:9d356a7a5610e38fc11c48ad588f37f8d5245ae01bf555e85e8310d2cc6e19f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10281104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119c6d1a122719c68ae6e8f9dfdf6d46e3b947d8cb1d797f87400939f8c6a5e4`

```dockerfile
```

-	Layers:
	-	`sha256:1e85627f1007a87bddba176e6eba977720698f76ea28f7322ab8d93f60479fa9`  
		Last Modified: Tue, 04 Mar 2025 22:00:27 GMT  
		Size: 10.3 MB (10254076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1d2ed2804e0506bac981f4ce8cf371fdc5d1c252f37c334126dc54e4c390b3b`  
		Last Modified: Tue, 04 Mar 2025 22:00:26 GMT  
		Size: 27.0 KB (27028 bytes)  
		MIME: application/vnd.in-toto+json
