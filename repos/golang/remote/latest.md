## `golang:latest`

```console
$ docker pull golang@sha256:227d106dca555769db9977f33e5d3d27422c5e75af1afc080b92f390c326de80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 17
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
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7136; amd64

### `golang:latest` - linux; amd64

```console
$ docker pull golang@sha256:86d1854c5e3d0539ccc5eb052ebb60c8d40abf34e3a17833ccb2167931527d22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308173697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec829c45babe26254b2b8aa569b45d60af9f2a8c3cc8d94f3240a4ca34ecfeac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOPATH=/go
# Tue, 01 Apr 2025 16:30:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 16:30:57 GMT
COPY /target/ / # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d1b5af933d2dfc3d0dd509d6e20534825e4a537f7b006a6cb5b8e5a1f20905`  
		Last Modified: Tue, 08 Apr 2025 01:24:20 GMT  
		Size: 24.0 MB (24011090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb98adba0eb44a2e4facf9ca3626a4a66feedd0dd56d159cca90a35205744e7`  
		Last Modified: Tue, 08 Apr 2025 02:13:59 GMT  
		Size: 64.4 MB (64396468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb08228d7a5ec326856f57d2a6db89dd7a3ee8773f9adc904269c2f16e4eade`  
		Last Modified: Tue, 08 Apr 2025 03:16:31 GMT  
		Size: 92.3 MB (92333222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d296901bdc593d88a0813bb00eef0974b68222cba6add046b831c086a1c68c`  
		Last Modified: Tue, 01 Apr 2025 17:07:26 GMT  
		Size: 78.9 MB (78942217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc508665364bf890145a9b00cb0af7704946c2051213fcb9f3be3df777619bc0`  
		Last Modified: Tue, 08 Apr 2025 03:16:29 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:b90c7139c16db8d50f97344ca53be7c193d9c73af85cf16c9814e41502c076d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10299170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d1a305eda502392dd94995cd462efc5d34b5cddf30131500e6ddc3b020bcf4c`

```dockerfile
```

-	Layers:
	-	`sha256:0eccc1874f63da3ee73fee8170f7c8a013cbf240cf34835ab519f1149076dbcb`  
		Last Modified: Tue, 08 Apr 2025 03:16:30 GMT  
		Size: 10.3 MB (10271524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ace4262010f477b6b2db4aafad61af35a4111bd57e70129c76525e7fecbcbe7a`  
		Last Modified: Tue, 08 Apr 2025 03:16:29 GMT  
		Size: 27.6 KB (27646 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; arm variant v7

```console
$ docker pull golang@sha256:361fda01f0ae7140f45fe7fceb9d287ac62c12789d2a5e78f02f007936d9eb71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269053288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:430ce225bc899f47512ca3240ae4c1172136bb08a116552ce81375199e6424c9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOPATH=/go
# Tue, 01 Apr 2025 16:30:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 16:30:57 GMT
COPY /target/ / # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e40f48a2e6d38c2746e98a645887fe65e2b335f766dc7c61af172a1356726d5d`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 44.2 MB (44196771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d083faafd756a71980d33b1aeb908b0db85cdc7a159e3d49107170305f1bf41c`  
		Last Modified: Tue, 08 Apr 2025 07:37:54 GMT  
		Size: 21.9 MB (21918243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5414268749270f000845caf5689fb7740534b9fe922712301ba571a6afca96`  
		Last Modified: Tue, 08 Apr 2025 17:29:39 GMT  
		Size: 59.6 MB (59639425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d9a9e8df2c13231c1e0a205f7e3ac9fa85454d09e0c0e5c18afbd185b211ea`  
		Last Modified: Tue, 08 Apr 2025 20:42:26 GMT  
		Size: 66.2 MB (66197481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9003e8a4d55742a1a2128c3dabddda68ec2c585f52d2aac5eaee8bd68089640`  
		Last Modified: Tue, 01 Apr 2025 17:07:37 GMT  
		Size: 77.1 MB (77101211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cabdd5ce0dc6c2cc2a5be4c94210b968f639888441acda83036485d8f742560`  
		Last Modified: Tue, 08 Apr 2025 20:42:24 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:c119634881d06ed74441f7a69f3e371014b957fe3b17e299c655951392c81973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10107662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b855eb6651c89a3f5aa96de034b1ca25546a452c9c8d9548dc1b4bc7a37e09a9`

```dockerfile
```

-	Layers:
	-	`sha256:017911a3c155dd54e319b2a5e191c9fea9c69480ca1a3780057eda0aa648cde6`  
		Last Modified: Tue, 08 Apr 2025 20:42:25 GMT  
		Size: 10.1 MB (10079882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b60da6bdf0988cc4dafc5e1578ee91ba54de266261fb5e544733f36aba741e1`  
		Last Modified: Tue, 08 Apr 2025 20:42:24 GMT  
		Size: 27.8 KB (27780 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:ac74596dd7c9a7afb1b9060358c2a48fb738f7047ff8464214e3ff90c6fe4194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.8 MB (297825457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f95322a4cbef0e1516d9010e45c7e31378ba66ccd6b7c0e6c9839c0df0075ed`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOPATH=/go
# Tue, 01 Apr 2025 16:30:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 16:30:57 GMT
COPY /target/ / # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d81c64672754c46e5d99e385c8f3283bec2060a79ad7dacdb2f5ce904caa401`  
		Last Modified: Tue, 08 Apr 2025 06:03:14 GMT  
		Size: 23.5 MB (23544339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf144460616b42eb1462fd80a5e1909e578b1e1f7285b185e468ba2b01308b9`  
		Last Modified: Tue, 08 Apr 2025 12:18:06 GMT  
		Size: 64.4 MB (64355780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9726b91366b288f3bf9f1b85d5cf8b7e50e8f51867ff670418d5b03a1f259c`  
		Last Modified: Tue, 08 Apr 2025 15:59:21 GMT  
		Size: 86.4 MB (86397502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a002eda2038f0953467f843586445333b2af3e827e57b15849040931f2903fb4`  
		Last Modified: Tue, 01 Apr 2025 17:07:27 GMT  
		Size: 75.2 MB (75200208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56146eb78922cf6f61dd2c8d20c1d5940497be10ce6e425fd9e9044825f6f08`  
		Last Modified: Tue, 08 Apr 2025 15:59:18 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:fd71dc79973d366f476b5c81b83d361c569403cd052037c8e0ddf141d7d4892f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10327246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b67a1db62b3de68766fca76726951dd4d77b5517ed1902081e05c293e6eb0bd8`

```dockerfile
```

-	Layers:
	-	`sha256:92162f0e478c5f9cbf7aa0ea75eec2d30c6025c8616be4e88266a708c91de27d`  
		Last Modified: Tue, 08 Apr 2025 15:59:19 GMT  
		Size: 10.3 MB (10299419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e70685990bfca539d160c1e92b6caa7e93d4a37892f6ff695d2ead96b5c1eba`  
		Last Modified: Tue, 08 Apr 2025 15:59:18 GMT  
		Size: 27.8 KB (27827 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; 386

```console
$ docker pull golang@sha256:977988fb79ac20565065d143e4da85bd85e21945b3e7beb4722326f91998d8df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.2 MB (307188682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314830ecfc14706a530e1c4d8eae1256a6cb76ad5be386dc7b11ee2b568d707b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOPATH=/go
# Tue, 01 Apr 2025 16:30:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 16:30:57 GMT
COPY /target/ / # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:437850497c82f7f6311c6cddf1db9d5ec53b7315e3733ed836cb00852f8fa683`  
		Last Modified: Tue, 08 Apr 2025 00:23:53 GMT  
		Size: 49.5 MB (49478131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fd7cbed080b4cdef804ca7e1b5bf4f3bc870dbef54cd5c74053fef6b147056`  
		Last Modified: Tue, 08 Apr 2025 01:23:54 GMT  
		Size: 24.8 MB (24847203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ffc3e6085548412ccbe96cfa7c6e138ccc7724d5a764a6a99e732fca48b289`  
		Last Modified: Tue, 08 Apr 2025 02:13:56 GMT  
		Size: 66.2 MB (66237424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af70929c043ae68e2ffaa034f91a57b7064f5cc99d166fbc52fbde3cec8262b4`  
		Last Modified: Tue, 08 Apr 2025 03:16:37 GMT  
		Size: 89.8 MB (89752352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb556227a38cd463b29410ff393a23b771d304e2f2f265b6c233fe487c9ca9ff`  
		Last Modified: Tue, 01 Apr 2025 17:07:28 GMT  
		Size: 76.9 MB (76873414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127e83887b8dd56caddfae005da5994c13e9a94120f0e0fa9e572b6ede1115de`  
		Last Modified: Tue, 08 Apr 2025 03:16:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:a14693fa139fec68217109f39fefb19aa0322381405e484ea9d65d436b5a22fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10279171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6b33e771fdb6ad4b35f506abc0da4de92fcf2f92bc1c5898acd0759b0e42710`

```dockerfile
```

-	Layers:
	-	`sha256:f9efbdb73f0f0aa10bf67ae06326aec80895d12157c7abb9355b10199d3f2055`  
		Last Modified: Tue, 08 Apr 2025 03:16:35 GMT  
		Size: 10.3 MB (10251582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af576b14bea6226cb02e1799a47479fce1d2665358fbb35608c56d145f04c63a`  
		Last Modified: Tue, 08 Apr 2025 03:16:35 GMT  
		Size: 27.6 KB (27589 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; mips64le

```console
$ docker pull golang@sha256:f5e84c516a69a7e45cdbaff6594753edd132117939f3f23181b07af5a9af7de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.5 MB (278480948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9c36ee37843ffa7a6a9caa71835ef3fcf4da4fdf0d2f278cf887f5a9da09ac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOPATH=/go
# Tue, 01 Apr 2025 16:30:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 16:30:57 GMT
COPY /target/ / # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:579ff6a9178b7f862c70c40b253d6f0090e7792eed3ce083de0732adfc5f4826`  
		Last Modified: Mon, 17 Mar 2025 22:17:43 GMT  
		Size: 48.8 MB (48756170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc19bfe112f8e8e887df88219c2ac69098bcc8afda18a25b53168674379a8365`  
		Last Modified: Tue, 18 Mar 2025 16:33:21 GMT  
		Size: 23.6 MB (23595590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0a4688093ff24a7c0a47c52d04ce08c1411187824a95dc1fb509b4ab01c8c4`  
		Last Modified: Wed, 19 Mar 2025 05:02:22 GMT  
		Size: 63.3 MB (63308534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2231f6ba5c37aa271ccac7a0771657978751e91d524c076449ab434853b6fbd6`  
		Last Modified: Wed, 19 Mar 2025 09:15:32 GMT  
		Size: 69.9 MB (69916047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a495918ec5dbc0a69aeab6f4eb97f48d3402581aa82d0c68e55768767ae9863`  
		Last Modified: Tue, 01 Apr 2025 17:09:52 GMT  
		Size: 72.9 MB (72904449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13dbecdb408bc13a04bd058e3b723fedad7d4418a690411c38bb9b82b4e1429d`  
		Last Modified: Tue, 01 Apr 2025 17:08:20 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:47f184d35ec19add94aefeef61828d718d8b39811c934d423aec2105b61e3e01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7aaef9ff4cb922244d5b23b7aaf8326809a3de82cdaee669b200257244b1f8f`

```dockerfile
```

-	Layers:
	-	`sha256:9e0a7042a744ca12ead1effc49f3ec89acad3236c483a9de1bd9b93bb853a4ba`  
		Last Modified: Tue, 01 Apr 2025 17:09:45 GMT  
		Size: 27.5 KB (27539 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; ppc64le

```console
$ docker pull golang@sha256:9d148caa22dd99dc72274b716ed2a69821da6038c2c94f9c4074a604b0f13e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.7 MB (313661592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd5ede3652d1021bd70291616c524a03651d86d384d1377444813fa289f3a12f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOPATH=/go
# Tue, 01 Apr 2025 16:30:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 16:30:57 GMT
COPY /target/ / # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:96130533c16d0aeecdcc4c64baab4a3adfb31877715c21a61125a04fe062f893`  
		Last Modified: Tue, 08 Apr 2025 00:23:16 GMT  
		Size: 52.3 MB (52331646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b54c9911bf701a3c84db58a7959c7ebb5f1e34a45bad705a2799f182bc4e0bf`  
		Last Modified: Tue, 08 Apr 2025 04:30:15 GMT  
		Size: 25.7 MB (25650176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02bafec621c70d63b6b8b80ca09a779f1c6500fb5feaa4c53d57a46c6a6ff7`  
		Last Modified: Tue, 08 Apr 2025 08:37:54 GMT  
		Size: 69.8 MB (69843923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ae46de5b9b1bff7a4ad47fdc2c2eaee788abd87244f4992fa97aa13f80c83e`  
		Last Modified: Tue, 08 Apr 2025 15:44:42 GMT  
		Size: 90.3 MB (90334402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee95abad5ecea3c593f42714d65b6f62167cc9a1a7a50eaad85a7db940a3e7f3`  
		Last Modified: Tue, 01 Apr 2025 17:08:51 GMT  
		Size: 75.5 MB (75501286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d0c44e29fc9dae4d9c11649d1f4aa6d03a8c43f9aabfdb39c511095e2b7c2e`  
		Last Modified: Tue, 08 Apr 2025 15:44:40 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:1040ace61d630ff271c51df5051692cf28969a7df7b40d3b878770c90bdd923f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10271955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8ba39a8ac90ac1cdff966ce97d348c1911478e20e74772b736927f09e23e5e`

```dockerfile
```

-	Layers:
	-	`sha256:1592d26d1421822cfc42ad2390bc539fefdfe1adcd4c3216b9b44fb255d800d2`  
		Last Modified: Tue, 08 Apr 2025 15:44:40 GMT  
		Size: 10.2 MB (10244237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e37b216b9754bb0048e0daf04f1b9605956797412bcf079f2b89a0622697824`  
		Last Modified: Tue, 08 Apr 2025 15:44:39 GMT  
		Size: 27.7 KB (27718 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; s390x

```console
$ docker pull golang@sha256:c132f00d6562806e02460c5fbe6f67f98fc3e2e2b297c7cb7b98ba11a51bb92e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.3 MB (281325639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998852d6d255b9dfb86b4006ddda5b7c67ab79d1d50a6624eb6e110030d53e7a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOLANG_VERSION=1.24.2
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOTOOLCHAIN=local
# Tue, 01 Apr 2025 16:30:57 GMT
ENV GOPATH=/go
# Tue, 01 Apr 2025 16:30:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Apr 2025 16:30:57 GMT
COPY /target/ / # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 01 Apr 2025 16:30:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:02fcba40f83e05adf85891b5c708b183d1028fd36fd80528f148e95bf593ab77`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 47.2 MB (47150996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a93e29489c173c9f7bae02e4e3f728f3e5b721748076de87502e6e9fd9108c`  
		Last Modified: Tue, 08 Apr 2025 03:44:19 GMT  
		Size: 24.0 MB (24008336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4fde99ce0eec506f038695c59ba0ff56bd0df358636c0b067f55c60d7d566c`  
		Last Modified: Tue, 08 Apr 2025 06:52:25 GMT  
		Size: 63.5 MB (63498375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6cfd18b484e73fbdf93f4e122dd8460ccf3aeb35fb84d01875ef84dc557fb4c`  
		Last Modified: Tue, 08 Apr 2025 10:11:36 GMT  
		Size: 68.9 MB (68923344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64586fca58b7ef9b98d81252f6468cd1afe274720313716be72d0e12ecde9791`  
		Last Modified: Tue, 01 Apr 2025 17:08:27 GMT  
		Size: 77.7 MB (77744430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ce7a82e6bd3eae4972393110cc187ab1d2511e3b30df9aa6231b79834f59ff`  
		Last Modified: Tue, 08 Apr 2025 10:11:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:881be90a6b304a4d3e504201a9dd07404bfcda702cd9d0de6faa70c5e17e508e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10135150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c702ce8198ddc817fe0e514a805bfe8dde40ba4ae5af1be0d40908c88321e58`

```dockerfile
```

-	Layers:
	-	`sha256:c45695a6b363ce33a214101f8606c7412bb742dd6695d252d29b905e8cc4a5c4`  
		Last Modified: Tue, 08 Apr 2025 10:11:35 GMT  
		Size: 10.1 MB (10107504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01b5c323c3c180f5edfbf12209df41a8338300a7492d2f1c764c48ccffd0db5c`  
		Last Modified: Tue, 08 Apr 2025 10:11:34 GMT  
		Size: 27.6 KB (27646 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - windows version 10.0.26100.3775; amd64

```console
$ docker pull golang@sha256:e29fa934998590e81186bb08c40a15164560e42544d807437c6f89eb5bc9fae2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3528792761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816853d92bdc97451867ed14d5a594511d44b99ac051a03661c3f2e86f17150b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Wed, 09 Apr 2025 00:44:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:44:04 GMT
ENV GIT_VERSION=2.48.1
# Wed, 09 Apr 2025 00:44:05 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 09 Apr 2025 00:44:06 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 09 Apr 2025 00:44:07 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 09 Apr 2025 00:44:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:44:21 GMT
ENV GOPATH=C:\go
# Wed, 09 Apr 2025 00:44:28 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 00:44:28 GMT
ENV GOLANG_VERSION=1.24.2
# Wed, 09 Apr 2025 00:46:03 GMT
RUN $url = 'https://dl.google.com/go/go1.24.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '29c553aabee0743e2ffa3e9fa0cda00ef3b3cc4ff0bc92007f31f80fd69892e1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:46:04 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7672cf33de477ad825cbaa16a956e9d5d339db68a30efa7b3ff24ea6fbd02846`  
		Last Modified: Wed, 09 Apr 2025 00:46:09 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fc7c6dd17b7d72b3a1b65f71da98a86a10e9a2f62f51700a42682ce4268914`  
		Last Modified: Wed, 09 Apr 2025 00:46:09 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e132aab1dd805923e52f664ee264e6f42963c7e99a6037ab371c2d54ca76b32`  
		Last Modified: Wed, 09 Apr 2025 00:46:08 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62eb12eeebab81f5162a35e2db0fc603735dbf320dfdbdc094656656cda055da`  
		Last Modified: Wed, 09 Apr 2025 00:46:08 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e27a60939c03ad6bcc785a1bf280189f4e112281d56c5356ca4876e4c7acd78`  
		Last Modified: Wed, 09 Apr 2025 00:46:08 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a77c9a310a4f142c5098362986c6c9975ca2b1243431d56e12055fef19d49ea`  
		Last Modified: Wed, 09 Apr 2025 00:46:14 GMT  
		Size: 51.3 MB (51253178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0312c7451731be32488e49beb94106a26ff17993a360c0b06498474fa488521c`  
		Last Modified: Wed, 09 Apr 2025 00:46:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8727a8f7c608ffd128685607cf14b845cd5148598a30250657b78a7727fce963`  
		Last Modified: Wed, 09 Apr 2025 00:46:07 GMT  
		Size: 378.0 KB (378041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c156426602a359ef6dae2b64d5ce0a2145b84588c901063d41fd0f1713dd5eca`  
		Last Modified: Wed, 09 Apr 2025 00:46:07 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7906439a638b42ec85dcdd3b2205effee08115f7f42d2dcf9f1a5f2103a07f40`  
		Last Modified: Wed, 09 Apr 2025 00:46:23 GMT  
		Size: 82.5 MB (82471510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e79a665256513d99d621933d5f1489cdfb9bab3495509e0ec43766fe85ced9`  
		Last Modified: Wed, 09 Apr 2025 00:46:07 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - windows version 10.0.20348.3453; amd64

```console
$ docker pull golang@sha256:f50a62a024e851fe1d9684010d18b6dd3db48288cfeeab250726d1e7423e66ad
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2404810921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89491f6a50d6ba7c3221a93691258c9181e343d5d9ef694d4f372a183832f4fe`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Wed, 09 Apr 2025 00:59:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:59:51 GMT
ENV GIT_VERSION=2.48.1
# Wed, 09 Apr 2025 00:59:51 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 09 Apr 2025 00:59:52 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 09 Apr 2025 00:59:53 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 09 Apr 2025 01:00:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 01:00:11 GMT
ENV GOPATH=C:\go
# Wed, 09 Apr 2025 01:00:17 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 01:00:18 GMT
ENV GOLANG_VERSION=1.24.2
# Wed, 09 Apr 2025 01:01:28 GMT
RUN $url = 'https://dl.google.com/go/go1.24.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '29c553aabee0743e2ffa3e9fa0cda00ef3b3cc4ff0bc92007f31f80fd69892e1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 01:01:29 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4345c6a4265223fc889b761aac9cfe0402e9e7ba36ff92c9041a7e01af827238`  
		Last Modified: Wed, 09 Apr 2025 01:01:38 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9c0bc025e49b96a98e158aa3628492681560a9b66371cafa674a13baffb2a0`  
		Last Modified: Wed, 09 Apr 2025 01:01:38 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b147f042085899dbe15fbcbc97b157dadc056218a793c091f8da26fc35b080`  
		Last Modified: Wed, 09 Apr 2025 01:01:37 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88330bb9180b967b8f1ddf3ebb374d770def047428f52d4735e71e7a99e5c150`  
		Last Modified: Wed, 09 Apr 2025 01:01:36 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0414252e9ec98fb3ee28bc6c024d35e323011170f9662b4e95d501f8494e2cb7`  
		Last Modified: Wed, 09 Apr 2025 01:01:36 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ad7c06935374ce4f49b6691c8491cb0a04fbe87314498c7a0eb0fc56be2052`  
		Last Modified: Wed, 09 Apr 2025 01:01:42 GMT  
		Size: 51.2 MB (51209846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bce03b9acb963d134c3f4e69e3472732ebccc067518a62e69db5353b82f613`  
		Last Modified: Wed, 09 Apr 2025 01:01:34 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3181b8f7ca8d16a5332510aa93def630fd3ea6b003489ed120843ba48a1c9bbf`  
		Last Modified: Wed, 09 Apr 2025 01:01:34 GMT  
		Size: 344.1 KB (344106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57de3a3af62347b91455ddc9ebaad5b04aa71cb5c9a01aba9f633e99f023e0cc`  
		Last Modified: Wed, 09 Apr 2025 01:01:34 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:242c423f37cbf4329c08684df4d886ef6f2fe1db3fb69c651eff20ee85a345d8`  
		Last Modified: Wed, 09 Apr 2025 01:01:47 GMT  
		Size: 82.3 MB (82250859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010d64572c273c292cc9d00c8b1835d833c74c4589a70b2fd6536b3220a1c960`  
		Last Modified: Wed, 09 Apr 2025 01:01:34 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - windows version 10.0.17763.7136; amd64

```console
$ docker pull golang@sha256:c110fb0a7415f00e732b5f9860b22ebbd55f43922f9c757dccef79ac84670c1f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2296500885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e256c32d2bf069c4f461bce58676a4e23a841fd285d364090db8b212699bc788`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Wed, 09 Apr 2025 00:54:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:54:21 GMT
ENV GIT_VERSION=2.48.1
# Wed, 09 Apr 2025 00:54:21 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 09 Apr 2025 00:54:22 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 09 Apr 2025 00:54:23 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 09 Apr 2025 00:55:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:55:14 GMT
ENV GOPATH=C:\go
# Wed, 09 Apr 2025 00:55:20 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 00:55:21 GMT
ENV GOLANG_VERSION=1.24.2
# Wed, 09 Apr 2025 00:56:35 GMT
RUN $url = 'https://dl.google.com/go/go1.24.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '29c553aabee0743e2ffa3e9fa0cda00ef3b3cc4ff0bc92007f31f80fd69892e1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:56:37 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02d2e4cd82e1486d8c37ceea51a0f0efaaf886c079dcbf2934f7ece112c6b90`  
		Last Modified: Wed, 09 Apr 2025 00:56:41 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15093f0690bdd7424b0b96331ecc38bdd6301e6a63b3d5e70cf90d7c1ee4b1e0`  
		Last Modified: Wed, 09 Apr 2025 00:56:41 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5c7926e8a15a554949994c42bdfc849f5c59edd204b8b2169a45044a654e0f`  
		Last Modified: Wed, 09 Apr 2025 00:56:41 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22a8386bdc4d78f1288691ecd130bba3666993f6b7e16591cf4bfef191dd364`  
		Last Modified: Wed, 09 Apr 2025 00:56:40 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aea277ef6f3962d14e126a8a4f1af0f399e4677c41003870ca28e2cae932650`  
		Last Modified: Wed, 09 Apr 2025 00:56:40 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518df7556a6bcb9c71a812f8da756e173d093dfb12ce99ee09c73be6414566e9`  
		Last Modified: Wed, 09 Apr 2025 00:56:47 GMT  
		Size: 51.2 MB (51191557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d56ac7b4debc4416f3b91cc7339b2bdb9236407799a9a27006ab2aee4cf22a8`  
		Last Modified: Wed, 09 Apr 2025 00:56:39 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1acd1526edff837e8891600f66513cd21b9a141f65a8fe4c3a8bf56bfe42a464`  
		Last Modified: Wed, 09 Apr 2025 00:56:39 GMT  
		Size: 329.1 KB (329093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63eaaf2a7e9e9c994c6d8055c6e7cdb2137522d943e88b73d1d17a05109bd2d`  
		Last Modified: Wed, 09 Apr 2025 00:56:39 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90f146ef39e2e97f834ec6bbf7dc1d2464835e2f956850e1ae6104f11a84b59`  
		Last Modified: Wed, 09 Apr 2025 00:56:53 GMT  
		Size: 82.2 MB (82243898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0354bf1be150753bb6c24a3032c72b0fd25d4c9c81468650807adcb6fc9f2a1a`  
		Last Modified: Wed, 09 Apr 2025 00:56:39 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
