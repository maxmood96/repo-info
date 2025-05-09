## `golang:tip`

```console
$ docker pull golang@sha256:7514ce191caca835d4ffabb36c1663bb207d0d9765bc45c063dec2b0da811eeb
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

### `golang:tip` - linux; amd64

```console
$ docker pull golang@sha256:93b4a5f0f42b9e1f981656075713ea1396eddd88ac19d45eef8757db55d7d129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.0 MB (355986786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ece0099f8934af77bb571e0b8730bba6fe075316c66452e0fecbfeaefc86ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Mon, 28 Apr 2025 21:55:02 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca513cad200b13ead2c745498459eed58a6db3480e3ba6117f854da097262526`  
		Last Modified: Mon, 28 Apr 2025 22:15:10 GMT  
		Size: 64.4 MB (64394427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd547bf1cc2b0f794244d2e3a18a68cc3b1ca4bbb00f0c919bf8fc456239d80e`  
		Last Modified: Tue, 06 May 2025 20:11:19 GMT  
		Size: 92.3 MB (92349731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f43c76dc6ee2ca1c3cdba208e84ccb4e1c5c0677efaf8a998b57c3e624b57e3`  
		Last Modified: Mon, 05 May 2025 17:32:51 GMT  
		Size: 126.7 MB (126740090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1adf35db1a2016afb7d67813fbcccb656f8cbaf5ee58bdf2daf5372c8026e12a`  
		Last Modified: Tue, 06 May 2025 20:11:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:484f137d04e220b2937ca02c27e6b6a4b1adc5ca8a15c615fd35c87a1618c1ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10299563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd92876a66e8ca86139fd1197a8b2025562d6ce89ab43d05e1894e5316aefa7c`

```dockerfile
```

-	Layers:
	-	`sha256:6b6ea21d2c50150670f6a23e376de929f2e1d45ba894dcd9ed57a771c54b9f47`  
		Last Modified: Tue, 06 May 2025 20:11:16 GMT  
		Size: 10.3 MB (10271900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f0e22e01da98e9d0d86a1343f127e2dda40a92fcb981ad9fd3f82f3ef05ea13`  
		Last Modified: Tue, 06 May 2025 20:11:16 GMT  
		Size: 27.7 KB (27663 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm variant v7

```console
$ docker pull golang@sha256:7b2256e6e0a904096eff0f4488bd6462936b2d990a7db19062361fcfc4ffadbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.7 MB (313743566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8080f19b234cd92ddddbadf4605b4f2a64abf14f58be8b6f28c46f041a008fb9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:a735d4b4a53e8e11448d15bc50ce4670d54dff52e426cf0510c9b713d3a7ad09`  
		Last Modified: Mon, 28 Apr 2025 21:15:27 GMT  
		Size: 44.2 MB (44197079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b01e6436acd06b177253a4ba25e5179715088c2f493e89c91bbf6fdc41a2034`  
		Last Modified: Tue, 29 Apr 2025 03:37:10 GMT  
		Size: 21.9 MB (21918380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3553b1499305feec4f182c1e2562e06daaecb3dc337d83b89b8c909f46c0a1`  
		Last Modified: Tue, 29 Apr 2025 13:22:56 GMT  
		Size: 59.6 MB (59640211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6442f47db55887d087c4346d5fccc35d5cd8441653b35deaf402943d7978ae1`  
		Last Modified: Tue, 29 Apr 2025 16:59:19 GMT  
		Size: 66.2 MB (66222470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185f617f5384afe02adfbf4600ef1c02d06ba922d332b58b68dacf2c75505cb9`  
		Last Modified: Mon, 05 May 2025 17:58:33 GMT  
		Size: 121.8 MB (121765268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06e886256250c55cee0d4474107e57fd83f2d05ddf42ea52113d566c0f44d08`  
		Last Modified: Mon, 05 May 2025 17:58:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:fd70930f1ac832bcd4aece4dc801967b0d8eb3dbed1c9523b8d05b7881ac4286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10108009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d0a6534bb6ed4063ad6092aa3b2b1c7d93b4772af9306efc200089308898e8d`

```dockerfile
```

-	Layers:
	-	`sha256:dbf6ae5c10b2c1a10a6ac511a2f706af30d61cfdee8d40ee4f3bb23a3a51dc8d`  
		Last Modified: Tue, 06 May 2025 20:10:12 GMT  
		Size: 10.1 MB (10080222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07543472f9f610b1c45a589c292be635a07396ad84945e141b2b0b720ca72f3e`  
		Last Modified: Tue, 06 May 2025 20:10:11 GMT  
		Size: 27.8 KB (27787 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:902398e3c3afea45f91cca12c593bfcbee68771bda03aec40979ec641c74704a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.1 MB (342136611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7283e5591079a54d8d2f5372452c6ce61f3ef73f44c8dc19468fa131f46d3c15`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:de07ba6f486e0ce29760ab32d4381edabbc660a04c493e95eb9a8056925d8955`  
		Last Modified: Mon, 28 Apr 2025 21:20:23 GMT  
		Size: 48.3 MB (48327644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649bff67ea459549b6f371f7045d9968d6ebf370b815c922a625f3ab065724`  
		Last Modified: Tue, 29 Apr 2025 01:46:47 GMT  
		Size: 23.5 MB (23544262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a2a14f59a002f5ef50911a0687d30beadf65bbe35bde8bd3823c3496cbd465`  
		Last Modified: Tue, 29 Apr 2025 18:37:11 GMT  
		Size: 64.4 MB (64355683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919170863bb5513bdfe1ce20b4f372538ef99b950b570408aa6aec57bfd91916`  
		Last Modified: Wed, 30 Apr 2025 02:34:40 GMT  
		Size: 86.4 MB (86415404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef5eba61a9fd66fab686113f68ca3d5af338e13d6c7abcb7f6724a255553e9d`  
		Last Modified: Mon, 05 May 2025 21:09:20 GMT  
		Size: 119.5 MB (119493460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b790936db2407cf4fae118a1647adae8628a4c90d31535ec8dd9b8b8f22aa60`  
		Last Modified: Mon, 05 May 2025 21:09:17 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:a51225dc7407b28d6f8358da35c1b420e295e5923d365aec4a1105c44ad2f3d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10327570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f70c01c155cc8985ed18cbf0296560d2edf08f4e0b87c813797c5ba4782d833`

```dockerfile
```

-	Layers:
	-	`sha256:1c78d7fde1dbc7f2c548df6592f6301cede56f1ca7a065607f48a66fc8537017`  
		Last Modified: Tue, 06 May 2025 20:09:07 GMT  
		Size: 10.3 MB (10299747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fda81c45d9051e3065742a52354f5baaf40e70eaba8f11ed0291d22b8055199`  
		Last Modified: Tue, 06 May 2025 20:09:06 GMT  
		Size: 27.8 KB (27823 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; 386

```console
$ docker pull golang@sha256:3a000434e53fa5d825685298ace7d4a650252fa5edc01b58303ecbaab517f66b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **355.5 MB (355472038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df0e708249123521e359742fba77177f575f52906a5909d9a0f8f297f0ca61fb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:d6426ff7fee55f1c5da8050672c1463528bb15df73bf93e3ac0a5200042f6c3f`  
		Last Modified: Mon, 28 Apr 2025 21:08:03 GMT  
		Size: 49.5 MB (49478572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8121c387e441201e2e932ee9747762becb1f76490293a373bd9505310d1fe4e`  
		Last Modified: Mon, 28 Apr 2025 21:53:42 GMT  
		Size: 24.8 MB (24847147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce8929d56fab56325a8eea211cb4cd1021bc6ffc1e7a794d505ddbe638b23cd`  
		Last Modified: Mon, 28 Apr 2025 22:15:00 GMT  
		Size: 66.2 MB (66228922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e7837d96f535639d068e11521e556e8ae65f13166e649b54b9853b696ff3de`  
		Last Modified: Tue, 06 May 2025 20:11:50 GMT  
		Size: 89.8 MB (89777303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0adf2ac7302cf0e124e19835cb5b85e5efb297232f12a426c19cbe865f7f8c6`  
		Last Modified: Mon, 05 May 2025 17:33:28 GMT  
		Size: 125.1 MB (125139936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2154c6042332668da056608b780d352ccb7ac880be607040e0f12e0a20223f10`  
		Last Modified: Tue, 06 May 2025 20:11:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:f13ca482416759396cea7681e5970b86c37f41f8bce7d9672884f2325494fffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10279594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780783ee560287614e500a18eb7662811d31370379a1109883c4b0f5849009c8`

```dockerfile
```

-	Layers:
	-	`sha256:f971f8312f7e71f6a81c780b3c75df907a4c74ef03886e927cac8407ddc48442`  
		Last Modified: Tue, 06 May 2025 20:11:49 GMT  
		Size: 10.3 MB (10251974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7448a654e2d546fea9fa7ced6d8cf9cbb998c593743caaa7b535aee53e45935`  
		Last Modified: Tue, 06 May 2025 20:11:47 GMT  
		Size: 27.6 KB (27620 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; mips64le

```console
$ docker pull golang@sha256:b65eda36fcf3c389a08669fbf499a6996f2f127105117490713de7fde09d7d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.0 MB (322955588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a937ee72823ce243a21967ce93a1972fa6bf1be3058161df18a0b77ce0586b10`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:fa5acbf36757d3126014bc0e0a159fb5593a1d68ddba5992ef7ac9aa3e7db8dc`  
		Last Modified: Mon, 28 Apr 2025 21:10:59 GMT  
		Size: 48.8 MB (48775438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d3e6811de68483322bf4607ec4cf0620d9d7f95dc19ce670b2ee81bd283341`  
		Last Modified: Tue, 29 Apr 2025 12:43:07 GMT  
		Size: 23.6 MB (23595734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1d30b00e6e88ef455123e625951481f519a50849cb9e967c590e851c17b408`  
		Last Modified: Tue, 29 Apr 2025 21:16:09 GMT  
		Size: 63.3 MB (63308148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c420f992cbaa8d211ae04be243041a640a38dda712f3d832718a146e390dd6fb`  
		Last Modified: Wed, 30 Apr 2025 03:40:22 GMT  
		Size: 69.9 MB (69942341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5a08ed28aec63dfbdc9d44ad55c4f0f52c4bf291857699358f5a81c02a7290`  
		Last Modified: Mon, 05 May 2025 18:01:38 GMT  
		Size: 117.3 MB (117333770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11291286cd8058e3d2029a6302b2d54b094ee1660ce1f04c6b7faf1e7713f8e6`  
		Last Modified: Mon, 05 May 2025 18:01:27 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:63835a29460c26dcb7ee106a44a762eb2561d3e6e577fbf424b1b5965113b8cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62b9fad1c037102476f5925dcb37859c6caa53b7d3faeda672ef353f776b611d`

```dockerfile
```

-	Layers:
	-	`sha256:1f3d986c24eb0ac01878cc754a73cc681b5aaafda1e7311e3468591c8a0488c8`  
		Last Modified: Tue, 06 May 2025 20:28:33 GMT  
		Size: 27.5 KB (27535 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; ppc64le

```console
$ docker pull golang@sha256:6359f8017693d363a6ac093607643c9727b559ea9d24960bf2f770e38c304262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.8 MB (359805558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a9b09ff1bf65e9658cf785d2aa446ef2a18fe8a790d0e4ca17fcdcd09743703`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:33862e890d6c23fba01df0303b503e727dad5c72574fdf8af76d76dc3140d561`  
		Last Modified: Mon, 28 Apr 2025 21:21:34 GMT  
		Size: 52.3 MB (52332129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4617415431bf61f96c81d815cfb6cf010eef7bd0d8a8de24b02c1a7fe8407026`  
		Last Modified: Tue, 29 Apr 2025 07:46:58 GMT  
		Size: 25.7 MB (25650113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae70f40efc6df1466aa415707fbf58268a1633e6ab2dde78f23ec024d7c1e42`  
		Last Modified: Tue, 29 Apr 2025 08:29:00 GMT  
		Size: 69.8 MB (69840424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d38985afc96fb14b472c445470120222b7866d3e3e26c3337d073be6739a829`  
		Last Modified: Mon, 05 May 2025 18:58:04 GMT  
		Size: 90.4 MB (90350389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31ed22752475c6f8926b1f87264c9b47f4ccaebd9fffea12e01e7f160cb5e70`  
		Last Modified: Mon, 05 May 2025 18:58:04 GMT  
		Size: 121.6 MB (121632345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a3f9dc509462b73e9c4d60a72cf3ab10f4c21d11361e81a7f590124e94bfec`  
		Last Modified: Mon, 05 May 2025 18:58:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:7505a83f0d3d713538a6a0fb77848a438c3d9a0836ab1de107842cdbd944c285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10272314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f094397e1ccc7cad24d82e41265f46a975a1a1aae05ef80c673a05c3450a03ee`

```dockerfile
```

-	Layers:
	-	`sha256:c17d8db5d63921606b6e9cc93c9df4856e6d7917075cf62fb57a8406130bea8c`  
		Last Modified: Tue, 06 May 2025 20:10:37 GMT  
		Size: 10.2 MB (10244593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db01da032bfd4c5ba033b8d3a324c315ddb2a7915ee1388af16d422ce61a6e4a`  
		Last Modified: Tue, 06 May 2025 20:10:36 GMT  
		Size: 27.7 KB (27721 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; s390x

```console
$ docker pull golang@sha256:9b71516682d3ddcfdcafd91d8e198bd74572b34712ea69698ce90764d2d93a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.7 MB (327731041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53415c4ecf1d6a9aa6a60dd8de7d4364038c42bd2d42001ee0070ef24fa4b111`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:a5e7ec27bb28a531688c62bada8c4b448d8e280327ecabb8be798bc43be30c38`  
		Last Modified: Mon, 28 Apr 2025 21:07:54 GMT  
		Size: 47.2 MB (47151332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05c607354a47eba0ce7493f4dc26e0f40aaeea360944111a83eeeeb61083045`  
		Last Modified: Tue, 29 Apr 2025 00:01:21 GMT  
		Size: 24.0 MB (24008311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15250b46b7f7ffe8ad5ce0f3a2d64d0437e4fdf3d36b87579551846c0b2dd2bc`  
		Last Modified: Tue, 29 Apr 2025 02:58:48 GMT  
		Size: 63.5 MB (63496877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09d77a76fd2957750185d2378dd52b653f61b03e2e717f3f19442ac80e377a3`  
		Last Modified: Mon, 05 May 2025 17:53:08 GMT  
		Size: 68.9 MB (68938149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4145acb431091c4f38f8aa86656f1534dd86342d379c6569a1f1b1af46cd2b6e`  
		Last Modified: Mon, 05 May 2025 17:53:10 GMT  
		Size: 124.1 MB (124136214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04dafefbdc0dc7854e8853c7520f9de4efa9fd9be01685f40bf3c6eb05ddfb4`  
		Last Modified: Mon, 05 May 2025 17:53:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:ec921dea8740ecd9beb4f5d58c77fb81c672d8d48ab7f8574564e16a70bbc687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10135543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a2e1d96eabef932cba05dc4aa0d77e278ef48b8c49d525c4f9dc2bb61f4d98`

```dockerfile
```

-	Layers:
	-	`sha256:38135a0c0015de029f28e411ef74372c8c227ab57a66d4604f1ea37199c7aaa4`  
		Last Modified: Tue, 06 May 2025 20:10:39 GMT  
		Size: 10.1 MB (10107880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dfa7940dc29d3533e39726a85d50b1c7dcbc881c007d14a390fa15deacf87dd`  
		Last Modified: Tue, 06 May 2025 20:10:38 GMT  
		Size: 27.7 KB (27663 bytes)  
		MIME: application/vnd.in-toto+json
