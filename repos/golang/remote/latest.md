## `golang:latest`

```console
$ docker pull golang@sha256:1a13867f40c6ba8c3e7c07ab5fa921cb58cf8402bcbe452f4d41cd614655e700
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	windows version 10.0.26100.6899; amd64
	-	windows version 10.0.20348.4294; amd64

### `golang:latest` - linux; amd64

```console
$ docker pull golang@sha256:930f4d70383bcd71fb100b119638550ebdebdc7e5de3694c330823e92a242634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.9 MB (304923426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316cc6cbbe4313c184f1505a5fc2a57057dcc0bda6acc119c0a6765380864567`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOLANG_VERSION=1.25.3
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 21:30:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 21:30:34 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd090f42c4b7844c5846f9b4c719994f496fac3befe1d30f0ff20794e742370a`  
		Last Modified: Tue, 30 Sep 2025 03:17:21 GMT  
		Size: 25.6 MB (25614810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c9d6d993ac93f222ba87ca01097d40f632be9b48f6b5e399f2c5da1b3133d1`  
		Last Modified: Tue, 30 Sep 2025 03:18:12 GMT  
		Size: 67.8 MB (67784949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32509455572920c79ad1dc7d570d63f8614422bce1ff5b59a4030b7efaca0337`  
		Last Modified: Mon, 13 Oct 2025 22:32:31 GMT  
		Size: 102.1 MB (102088532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91631faa732ae651543f888b70295cbfe29a433d3c8da02b9966f67f238d3603`  
		Last Modified: Mon, 13 Oct 2025 22:32:32 GMT  
		Size: 60.2 MB (60150352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705714eb49cf742adf358e4deb85ea46651a082c56dc7a50b99a93df48a4a92c`  
		Last Modified: Mon, 13 Oct 2025 22:32:21 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:b45ee21ef5a7413001c3078e5eb8877106908421980ed0b9d956fb6edfa92f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10813322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f3f475bee0f4657c470fed1847d28baad92e13b994f676e90eb7d0b1e99eb2`

```dockerfile
```

-	Layers:
	-	`sha256:41a1a85d9b49b75954e8801e9e43e9c34c1ddbea41764a43c2d8c9d574d581bb`  
		Last Modified: Mon, 13 Oct 2025 23:22:45 GMT  
		Size: 10.8 MB (10784326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5fd5bb360f4e9f1c393443f6432646e341f310052a3edf54873008506e2306e`  
		Last Modified: Mon, 13 Oct 2025 23:22:46 GMT  
		Size: 29.0 KB (28996 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; arm variant v7

```console
$ docker pull golang@sha256:05b51d909e6854c349d683286e166869264dd596f27c51eac881b7ae49638c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263853373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab1deb182eefe5c86c9e0cf5464e7d8eec762246cef86cf0822eff87dcf6d04c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOLANG_VERSION=1.25.3
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 21:30:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 21:30:34 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:25723cf5ae8b10c461d8c699bc5f9e41058f8fd5113212d106848ebe89fc0ffc`  
		Last Modified: Tue, 21 Oct 2025 00:20:56 GMT  
		Size: 45.7 MB (45716494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452a743b80bee0c18e49576c93efcfb6c736c07dbdda0e38658362cec14c6415`  
		Last Modified: Tue, 21 Oct 2025 02:45:21 GMT  
		Size: 23.6 MB (23616662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfad6891ec6a8c0bc6bb36a13c5e7bc91999a0a3e69d53912de98fc37f3aa42`  
		Last Modified: Tue, 21 Oct 2025 04:11:23 GMT  
		Size: 62.7 MB (62713404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2980cee2e23d26ccf9098baf202141f33b3a05722868ca329f4612e3730088f7`  
		Last Modified: Tue, 21 Oct 2025 05:19:41 GMT  
		Size: 72.7 MB (72733704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af0985c887920d8ad25f36932e706271ae84032a3ae370b1f5325188b8578bd`  
		Last Modified: Mon, 13 Oct 2025 22:33:14 GMT  
		Size: 59.1 MB (59072951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42bb8ae654695135cc469bbf92028349e320675a60bed3ff51fc4cbd51dbacc0`  
		Last Modified: Tue, 21 Oct 2025 05:19:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:e5adac4d7cc4f49e5353f1521dc63fe30b3c52b7654f26ffc185b5a0795d0c4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10609431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc1170f41ffcb2c13d8d97d31697461644eae2ac51837a7aee1fc960d15af0d`

```dockerfile
```

-	Layers:
	-	`sha256:b87d97bdb0929c2436271aa52ddf4d4f18f3c6c57ebf81d733a592cb0111fed7`  
		Last Modified: Tue, 21 Oct 2025 08:22:30 GMT  
		Size: 10.6 MB (10580301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54876418e31431df4dc465bccfb784851a0ec436102f17caaa0c5cf6b543cd3d`  
		Last Modified: Tue, 21 Oct 2025 08:22:30 GMT  
		Size: 29.1 KB (29130 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:36cc36b5b5a0045a44006f424e18e24c886470fa5ae2ff5bb4d641d5515b1db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.1 MB (298135136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fbc43c30d51196df9f605843fea7d98d36933cd8c4ca2749a90d918bc8bea27`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOLANG_VERSION=1.25.3
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 21:30:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 21:30:34 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2a101b2fcb53d61db540cb76da094137d4f0291a93fa41357ab70c3debf4d3c3`  
		Last Modified: Tue, 21 Oct 2025 00:22:57 GMT  
		Size: 49.6 MB (49649743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f510ac7d6fe76c0362c0162daee6964c5b93b20f5ddf65021b0bf3bcce16f306`  
		Last Modified: Tue, 21 Oct 2025 01:47:21 GMT  
		Size: 25.0 MB (25017463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721433549fef8bfa398445abce4a12b5c7e64775b3de57bfc3ff37c8ed6fc0e4`  
		Last Modified: Tue, 21 Oct 2025 02:35:46 GMT  
		Size: 67.6 MB (67583109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef09c14ebeabdf7d08e722b3d986ea437e784a0bba756e414a5921c563664f9a`  
		Last Modified: Tue, 21 Oct 2025 03:17:58 GMT  
		Size: 98.2 MB (98234501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dab1238d3d9c3bd1753609badeac4c19b7239aef9927c6dc13db4335a66b568`  
		Last Modified: Mon, 13 Oct 2025 22:33:13 GMT  
		Size: 57.7 MB (57650163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f0c1c4638d72c6ba08a7bb33482907faf1f373a763855bd415db1ee2f1bd49`  
		Last Modified: Tue, 21 Oct 2025 03:17:51 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:d32192d0e7e9f6f9b084d9f8b5a453b91841aba0b7bf97c5352b33755a4d5e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10934057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:262517b293adfb7bbf030494bdc60f0edee3be60caebcd7e198e3c66b48f0c29`

```dockerfile
```

-	Layers:
	-	`sha256:1222299cad0a3e2ada72baf5f38d5714ca3bba500d4cee3676639dc6be4080d9`  
		Last Modified: Tue, 21 Oct 2025 08:22:39 GMT  
		Size: 10.9 MB (10904883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42b46172c09b88d0bc18b394d541bf9fc902a8ec1926926121fb668c2ace46cb`  
		Last Modified: Tue, 21 Oct 2025 08:22:40 GMT  
		Size: 29.2 KB (29174 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; 386

```console
$ docker pull golang@sha256:418d465080fce22b16eadcd2690eaa3478d77c12cce179d0b5f347e47467fc4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.8 MB (306773556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:774229b42ae66220479b16e1ecfc2d2db69c1b290f4d3abb66bbb91dc388107b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOLANG_VERSION=1.25.3
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 21:30:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 21:30:34 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f1c1f592b5569b5e2093c3107a48f2929b609f05af6d24c06d41a7ec1ae5e0e1`  
		Last Modified: Mon, 29 Sep 2025 23:35:36 GMT  
		Size: 50.8 MB (50800229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e5d861644e3a43dbea9917a86fd0d6ccf184bc7514ee58118ffa521ac4bc61`  
		Last Modified: Tue, 30 Sep 2025 00:21:14 GMT  
		Size: 26.8 MB (26774670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acddf1ffebf58f05179a0e8a785ab62df40c7d1c75ee543282d404ca07d3ffec`  
		Last Modified: Tue, 30 Sep 2025 01:21:21 GMT  
		Size: 69.8 MB (69794474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2048517c90fd5b621f6afd96c15dfbb43f3df8eb05ccda86d17f28a76a2ddc5b`  
		Last Modified: Mon, 13 Oct 2025 22:32:53 GMT  
		Size: 100.5 MB (100533124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f95a97777f39c24f1a92cb9717c8fb60aaa699bf624bf9ea8e2cf61d0d8d4abe`  
		Last Modified: Mon, 13 Oct 2025 22:32:51 GMT  
		Size: 58.9 MB (58870901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1b6ea646edf870c25a2472325d64977ff34207399759a8ecf37a49f07fef8b`  
		Last Modified: Mon, 13 Oct 2025 22:32:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:e05ce100a20632de045700c03fd5e6380747937e24f960206bab66529b62982b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10784512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b733d6c9516b98c7c89d5adaf1d6194d28af776d4b7435df285031dd7a8cf4f7`

```dockerfile
```

-	Layers:
	-	`sha256:636eec7b5391f9b290474ae2ae0b0efd7afcc9836049ee29e45db9067155ae38`  
		Last Modified: Mon, 13 Oct 2025 23:23:12 GMT  
		Size: 10.8 MB (10755572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b436e881514948d76d9a058faecae99626f3f9d92ce62020fed22715fc04ab7`  
		Last Modified: Mon, 13 Oct 2025 23:23:13 GMT  
		Size: 28.9 KB (28940 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; ppc64le

```console
$ docker pull golang@sha256:483e57b4d71e0bae17b8c82ae5a787659e5ebcedca4dc1972a38d40aa40cc272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304068839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b8171c2fcb45b768dddce194d18cf1b110fa53dfaa5095f43df9f403f1acf3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOLANG_VERSION=1.25.3
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 21:30:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 21:30:34 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:71fbf24a239310917388930bb043e64907cb532b9ac8f265e44e032dc3bf4409`  
		Last Modified: Mon, 29 Sep 2025 23:41:05 GMT  
		Size: 53.1 MB (53109217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97a0b9869d194af98b70e095598cab3ab85032828ead695d63f75204d7418fc`  
		Last Modified: Tue, 30 Sep 2025 09:24:30 GMT  
		Size: 27.0 MB (26995278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed492992022fa9e4a253b427574c9ab21d82072f73e353ad6f09e1555a92cc4`  
		Last Modified: Wed, 01 Oct 2025 11:14:56 GMT  
		Size: 73.0 MB (73034854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39ff1a0b943456854e6b1ed7d946a7e67cf44c76fe8ec18f870bf569ea577a6`  
		Last Modified: Mon, 13 Oct 2025 18:24:18 GMT  
		Size: 92.8 MB (92794871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd79e032fd555b767c904ba3576a69bc211a15c564010ebf1a3788cd00df21d`  
		Last Modified: Mon, 13 Oct 2025 22:32:24 GMT  
		Size: 58.1 MB (58134461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfa2e42a785c8b3671f46c6bc69169c666f9220c55e7bcdcb5625f6b7272a50`  
		Last Modified: Mon, 13 Oct 2025 22:32:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:e231b7f4b69003a24399b194a335cb84868542e27d663cbafb2b27972fbf00ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10809198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f047dd11c65ce69196824f760b494ab5ae3a4a812cbe4e51e081d9c5c4327f7`

```dockerfile
```

-	Layers:
	-	`sha256:0d536d1cba8a4aaa477f4afc9dae55f7e69ddacb42c59f333320c3ce46a9cb30`  
		Last Modified: Mon, 13 Oct 2025 23:23:20 GMT  
		Size: 10.8 MB (10780134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1360b79d13b7215497df4d9eb5aeebba0f395e05ae873855f4f0733e24ae511a`  
		Last Modified: Mon, 13 Oct 2025 23:23:21 GMT  
		Size: 29.1 KB (29064 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; riscv64

```console
$ docker pull golang@sha256:0cd86f3af75ac394317034371c5a89fceb0d00fd515a7a1a3ff7542cf4ec0ffb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.6 MB (329630600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ceb0163c5571b385bfa7bf060035050873de9d7c97f5ddde3dd49e368ea9f42`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOLANG_VERSION=1.25.3
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 21:30:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 21:30:34 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:913254a25f5e448a50a1e74fa50f037e22f85cfe4d6a3c626f4b7405299b7c1b`  
		Last Modified: Tue, 30 Sep 2025 01:03:38 GMT  
		Size: 47.8 MB (47770009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8533144b875d90b1f9c5a4ecb4c26177d9b646c254cea7d68fd43c77c27f975`  
		Last Modified: Wed, 01 Oct 2025 10:56:05 GMT  
		Size: 25.0 MB (24952783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c645409e32b37950d400f06f75fff87e9a716322f248e5d01d290689226a51f`  
		Last Modified: Sat, 04 Oct 2025 03:44:05 GMT  
		Size: 66.7 MB (66659977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146033d470e9e45a40f2f8858ac379252d8b815c5b3ca04f3f509638a2ed95db`  
		Last Modified: Sat, 04 Oct 2025 11:31:35 GMT  
		Size: 131.6 MB (131577430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7738f55d50b335f992c80eaabcdddcb36c67eae2749a3858d5261b9c2e4d583a`  
		Last Modified: Wed, 15 Oct 2025 07:20:46 GMT  
		Size: 58.7 MB (58670244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b45b07b8d243a8de1febb1203543c0add14c2ac9afff94c307827285969269f`  
		Last Modified: Wed, 15 Oct 2025 07:20:43 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:6e1ef6b729f0e78390201d7bed4139ab0d22caba8bab45dc2fcd1273dedc1b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10883035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b48426f6b4d6b709df490d227e26319716b622ba050bd9027a6373960712226`

```dockerfile
```

-	Layers:
	-	`sha256:155f82712364b0da20287c26efeb98a624a41e67d6876a4991cc07caafc62bd3`  
		Last Modified: Wed, 15 Oct 2025 08:22:58 GMT  
		Size: 10.9 MB (10853967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50a291a35ae65b9fa49f0d30814164ef7adf48e7c997fa1805eb9c8031ff74c3`  
		Last Modified: Wed, 15 Oct 2025 08:22:59 GMT  
		Size: 29.1 KB (29068 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; s390x

```console
$ docker pull golang@sha256:091a0626f86e683542ac2d08cf08660b4aa9258d090e70c18c573d1c53016355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280155872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b9c436ad59f39fb2474d1bcb0d4d060f61b41bc77e398dcccf0b088f992c4f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOLANG_VERSION=1.25.3
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOTOOLCHAIN=local
# Mon, 13 Oct 2025 21:30:34 GMT
ENV GOPATH=/go
# Mon, 13 Oct 2025 21:30:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Oct 2025 21:30:34 GMT
COPY /target/ / # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 13 Oct 2025 21:30:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:024d6c344f0b9dbb2baf07e95dfd2abbfadc5c8262ca381f39f6489670cbaff5`  
		Last Modified: Mon, 29 Sep 2025 23:41:06 GMT  
		Size: 49.4 MB (49351442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae40148dca91a7d747a8331f403c812cb96e16b0e939c3f7e22eaed6bd4173a3`  
		Last Modified: Tue, 30 Sep 2025 09:36:14 GMT  
		Size: 26.8 MB (26782227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2360823d72f62f7ab99d1125b961476d915cd531da8e87d42d3767dfd3b86d6`  
		Last Modified: Tue, 30 Sep 2025 15:54:22 GMT  
		Size: 68.6 MB (68637856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a77bd0f38ef8a06aa5c038a198543d87d293c0d046b35c3e41c08fb8c27b73`  
		Last Modified: Tue, 30 Sep 2025 23:49:14 GMT  
		Size: 75.9 MB (75901079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0cce485d826b4034b25b00ba2ffd0ae02402af07840c83aa561b76bede0f4bb`  
		Last Modified: Mon, 13 Oct 2025 23:28:51 GMT  
		Size: 59.5 MB (59483110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042df149e1bb156d95f67cb26148ba540e9fdddc77df1f301a55ab6590852f2c`  
		Last Modified: Mon, 13 Oct 2025 23:11:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:38cce48d1da8e0149c1003303d5e37eb7bbcedc61ab69129328c51a14a51d6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10623717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd8eae67bd27d8b48961dca404f6e20793246c6d428a475310383cf0e4b1b13`

```dockerfile
```

-	Layers:
	-	`sha256:7fa924303a19dc8ec79ae4963f29f5ba5b6c5d6e991655a4e043359dcaee54a6`  
		Last Modified: Mon, 13 Oct 2025 23:23:35 GMT  
		Size: 10.6 MB (10594726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:787dc75056a30cff678ec5abd63c3ce03f306da4034aa35afe3c9033cae242b4`  
		Last Modified: Mon, 13 Oct 2025 23:23:36 GMT  
		Size: 29.0 KB (28991 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - windows version 10.0.26100.6899; amd64

```console
$ docker pull golang@sha256:2cc70ddf34ed2361d546e51c2cd1a667733b0158b92468f6b91759817502cdb9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3334616550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a4325f9378dfd37ef819c354e1df7043dbf0a60840ec650c42b8aa6a22f7d7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 14 Oct 2025 20:43:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:52:04 GMT
ENV GIT_VERSION=2.48.1
# Tue, 14 Oct 2025 20:52:04 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 14 Oct 2025 20:52:05 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 14 Oct 2025 20:52:06 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 14 Oct 2025 20:52:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 14 Oct 2025 20:52:22 GMT
ENV GOPATH=C:\go
# Tue, 14 Oct 2025 20:52:27 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Oct 2025 20:52:27 GMT
ENV GOLANG_VERSION=1.25.3
# Tue, 14 Oct 2025 20:53:40 GMT
RUN $url = 'https://dl.google.com/go/go1.25.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bc249a599c6fe9d0d4093c363856f6c6320dbbe05e5d5d8818b711fb4a14fc23'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 14 Oct 2025 20:53:41 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b31ef2acd9573fa311450133976eaea07e0ccfd74f3de24d672c7bf465eba24`  
		Last Modified: Tue, 14 Oct 2025 20:51:54 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54fdfe8df00e8f65fe05a8dcec1a9c9bcf157c585b485a2340afa46effb3085b`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac8a0f1afc6455ae3e0664ae53a39e9bd14cb6a5c24f30dac042aadaba2c68e`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641c16ab7c76d00518e5cc280a143ac590175746d5286f778f18384e14808fd4`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb7dc60695c767c62fcb8c95fe9f65ab74aa094069e1022f44b558d9087d1fe`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448bbef62076939cd63e6f8d49609b8fb2adc5beb02d651aba41b27b5702f96a`  
		Last Modified: Tue, 14 Oct 2025 20:54:12 GMT  
		Size: 51.2 MB (51215295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5381a3a340e7179938beb724daee446199efa60f6e2cfc31e2d0e932f20778d`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde940859bdd8f52eb029aaf1674f8befbf5a6e712052af1f487c267fe2cf267`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 343.8 KB (343824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ee53223a19ebc6db910b4cf71152ac4afb2dc0c40dec04a2a4ea6163d91e57`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d18c4ba82afefefaa36e2c54c74d9af40f5daffa1b867c5db38409718e2062`  
		Last Modified: Tue, 14 Oct 2025 20:54:13 GMT  
		Size: 62.6 MB (62566357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d1daea032d064b1593edc0e230f0d136629eb5b98e4814a5cf121e139cb48d`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - windows version 10.0.20348.4294; amd64

```console
$ docker pull golang@sha256:c8a1345a2888b020bef1985264ae178b833b3cc0541e697b5e5856f9e4a58de1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1603101506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a10eaf26230615f494b283abaf5efeb0d0ad98b13fb8abb2f7d5e94a7eb3699`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:40:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:48:05 GMT
ENV GIT_VERSION=2.48.1
# Tue, 14 Oct 2025 20:48:06 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 14 Oct 2025 20:48:06 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 14 Oct 2025 20:48:07 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 14 Oct 2025 20:48:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 14 Oct 2025 20:48:20 GMT
ENV GOPATH=C:\go
# Tue, 14 Oct 2025 20:48:25 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Oct 2025 20:48:26 GMT
ENV GOLANG_VERSION=1.25.3
# Tue, 14 Oct 2025 20:49:47 GMT
RUN $url = 'https://dl.google.com/go/go1.25.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bc249a599c6fe9d0d4093c363856f6c6320dbbe05e5d5d8818b711fb4a14fc23'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 14 Oct 2025 20:49:48 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fbaa2338b5f21199cd9a50079b2aa9af297c6a713f9ac529a66776518157d9`  
		Last Modified: Tue, 14 Oct 2025 20:45:23 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c3b813dc7ba82664e25602bf23eca0555e39fd4c8db3e4b5cea8dd5cb63684`  
		Last Modified: Tue, 14 Oct 2025 20:50:13 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbc0cbd485010589123d3c954333b3e31de258d93ceb4881aa8254eb854795a`  
		Last Modified: Tue, 14 Oct 2025 20:50:12 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8bbab51a4ef7da8fb4ce71160e000a619b7ff90526f7a1d15f24ac344affc3`  
		Last Modified: Tue, 14 Oct 2025 20:50:12 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96655a8476594fc962861d6373df47e44d988e8bb522e8ec4cfb3f0b5264234`  
		Last Modified: Tue, 14 Oct 2025 20:50:12 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cfcbd44bf5ee262eeba744d74262df094cb049f6cc12f68708d3e2febaf7fb`  
		Last Modified: Tue, 14 Oct 2025 20:50:17 GMT  
		Size: 51.2 MB (51192440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34eab3d542ab2f4d152e28c7fcb5ec9cc478120ba60f960883c914847fb10965`  
		Last Modified: Tue, 14 Oct 2025 20:50:12 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f8de3e5df8cc9929810718498835877b0a3cf52904e99f36b7f6fe7ecc909b`  
		Last Modified: Tue, 14 Oct 2025 20:50:13 GMT  
		Size: 328.2 KB (328166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1813806449f9be4848aa3bafe546d146d08dd7f1e604207dc85254b7ce6b8ef6`  
		Last Modified: Tue, 14 Oct 2025 20:50:12 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:defc5d1813487d83f5589871c1d6e9c87957a21e22cc5ea4a82f85aef1d3fedc`  
		Last Modified: Tue, 14 Oct 2025 20:50:19 GMT  
		Size: 62.6 MB (62551140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2196c0c5d4509a124a9b49a564537a41cd612720376961a53277865c4e420c4`  
		Last Modified: Tue, 14 Oct 2025 20:50:13 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
