## `golang:1-bookworm`

```console
$ docker pull golang@sha256:42d8e9dea06f23d0bfc908826455213ee7f3ed48c43e287a422064220c501be9
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

### `golang:1-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:b305f4915fa2152ad8ca281d741a1772947515c48d97ddf80c3ea7e93ce8ffcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.5 MB (289455146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9694c84b5819f05226d65e3fe2f47f0653be3c742d9f9ff0b1d37df93e948ae4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOLANG_VERSION=1.25.2
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOPATH=/go
# Tue, 07 Oct 2025 19:07:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 19:07:03 GMT
COPY /target/ / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c6b11972fd12973831818babf60f1ffc1c4047507943d132dffc612884022858`  
		Last Modified: Mon, 29 Sep 2025 23:34:14 GMT  
		Size: 48.5 MB (48480557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3dba6026a3c551d6b8e98308c073fff4fd569fd2fc61f21384cb996da82c9e`  
		Last Modified: Tue, 30 Sep 2025 01:43:53 GMT  
		Size: 24.0 MB (24025876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb1b35a6fc14463ada297f3f0605409cbfe29368b38fd5d1e41f7dcf29bb6fb`  
		Last Modified: Tue, 30 Sep 2025 03:17:35 GMT  
		Size: 64.4 MB (64397411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f39239b877e74b17bfccc17f3349a25a665d9591cb9def6f1ee94fe6ad298ad`  
		Last Modified: Tue, 07 Oct 2025 20:47:47 GMT  
		Size: 92.4 MB (92401967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2aec7ef170b5f02e240ef6c8aac64fb96a14688ea0750c962c145c141f3830`  
		Last Modified: Tue, 07 Oct 2025 20:47:28 GMT  
		Size: 60.1 MB (60149177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85708ca427454aee2c76c67e745746bd9bd7438e274740ef419f925d8ae115a7`  
		Last Modified: Tue, 07 Oct 2025 20:47:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:4190eec4ff31cbed60f524e38d2f8aaf7e1134a08f9ebe77e729397bb7987a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10523580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4199de508ac1d0df11dcf4344b51b6251a82c3e87a7f84499cf72e0983b2a59`

```dockerfile
```

-	Layers:
	-	`sha256:30c38d52df867fdff7c065a04dccdd3316fa282fa987761067c4cb8d65d39ca1`  
		Last Modified: Tue, 07 Oct 2025 21:18:22 GMT  
		Size: 10.5 MB (10495740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59cae562bf899f85bc66bf358d5688a19ff0bf0fb2bbbd169c57742433be1bae`  
		Last Modified: Tue, 07 Oct 2025 21:18:23 GMT  
		Size: 27.8 KB (27840 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:350daea46336487d3c869837448a84cffdc2f158e872f55eef589dc8ea4e5f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.1 MB (251108466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71b2caf4ba7fd5a738dd555f0180b70ace8a9ea18e57a7c986b4091b69d63e80`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOLANG_VERSION=1.25.2
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOPATH=/go
# Tue, 07 Oct 2025 19:07:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 19:07:03 GMT
COPY /target/ / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:03e514ef7fa283c62434ceaa5569a1dfd7eb8f0bc5744761a741cccd05a62353`  
		Last Modified: Mon, 29 Sep 2025 23:34:15 GMT  
		Size: 44.2 MB (44195923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de0c6a4c275fbc1127f1e13a9f6de6ca4fdc975838d76828750e675f4b1fd24`  
		Last Modified: Tue, 30 Sep 2025 01:05:07 GMT  
		Size: 21.9 MB (21930710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c9e67a849318ef85c3217c9988076f862a279a4fa96c042c09b84353bac8b7`  
		Last Modified: Tue, 30 Sep 2025 02:39:14 GMT  
		Size: 59.7 MB (59652531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7aecb2d26d0b90f5cd7f76e1337f3424ffe430b896a394b0bb28e70b022303`  
		Last Modified: Tue, 07 Oct 2025 19:34:15 GMT  
		Size: 66.3 MB (66255061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28977543608eb3d47060855462d9576fb750f3b4671b32d32fcc7f41fe2a4f4`  
		Last Modified: Tue, 07 Oct 2025 19:34:15 GMT  
		Size: 59.1 MB (59074083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab94e3f8c81043c743ffb28a891ceef928a4fcc94914a1b0be901a4fa62c0f66`  
		Last Modified: Tue, 07 Oct 2025 19:34:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:39e4875ac74aef9897445d5900b1166a65e0f047b0e15e5d3b5343c7e6209cdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10330400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e85ca7d6a625c862113df22108243c043d63eec5c84d2c56d34c1bdeedcc899f`

```dockerfile
```

-	Layers:
	-	`sha256:371c2f15f4a7211a4ce553cca512e8f52a13ae9899d64eeee1e26c1d5e3cf3ad`  
		Last Modified: Tue, 07 Oct 2025 20:24:06 GMT  
		Size: 10.3 MB (10302454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24e5292ea16bd8935fe9762a8d58a4c4376211a1cd0bfbd0c7f18e2aded81777`  
		Last Modified: Tue, 07 Oct 2025 20:24:07 GMT  
		Size: 27.9 KB (27946 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:7e77ce38e8f44c4a7105ebab727641972a12d8aeb549e36bab0bfacbc78d5d0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.4 MB (280444987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ba4264857425d8888b093e7c28c359bc8ff3ed890a2372d10f93ccca37945b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOLANG_VERSION=1.25.2
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOPATH=/go
# Tue, 07 Oct 2025 19:07:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 19:07:03 GMT
COPY /target/ / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:f7b43f0d0a8b99591b27457b368e70a582002600d32503fd07798c1bee7cd134`  
		Last Modified: Mon, 29 Sep 2025 23:34:16 GMT  
		Size: 48.4 MB (48358915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b261306f7eb1436ff95e3b9d948f5373b0dcf6ca1223aaa4c2fb303b03e744c`  
		Last Modified: Tue, 30 Sep 2025 00:56:21 GMT  
		Size: 23.6 MB (23594734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a2f93f2f0e198bff671333b38213c36ed741b7f552b83c033cf63f52b58c0e`  
		Last Modified: Tue, 30 Sep 2025 01:19:31 GMT  
		Size: 64.4 MB (64371209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0064dfb4dc3009e8efe9f652644591857954aca41e27e0a5a71e2bfc2ac40cab`  
		Last Modified: Tue, 07 Oct 2025 19:34:33 GMT  
		Size: 86.5 MB (86472152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66626199bcfab248906ccbdd0d977cc77ec2231a37f1710a42892109d86b2544`  
		Last Modified: Tue, 07 Oct 2025 19:34:30 GMT  
		Size: 57.6 MB (57647819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88a9fa7b3acc01daf898918d03c0827636f9d52d4ec45360ff1b2ebd7fef6a1`  
		Last Modified: Tue, 07 Oct 2025 19:34:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:6ccb5bfb99a414ecdb7164baf4ed55b1225a6011bbf2eb5ae2a2a985e9d269eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10551562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b4d8a23e5569cd3b45ee2bf7c5c14da084f94df89c6a04ea6dd03dcf075619`

```dockerfile
```

-	Layers:
	-	`sha256:d18504412f32269ec09ba8de29a15804ec8631b4cceef13a71ad6b5ac3b297b9`  
		Last Modified: Tue, 07 Oct 2025 20:24:16 GMT  
		Size: 10.5 MB (10523588 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18f41af1e6052d9ba2e496c3a9c55c8d749e2a6df15a230c68b009c99a05f6b2`  
		Last Modified: Tue, 07 Oct 2025 20:24:17 GMT  
		Size: 28.0 KB (27974 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; 386

```console
$ docker pull golang@sha256:ed18b24f8bc6ad759cb86ffc2c5bc9d5e105b474e36ed310839094ac51577f3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289254029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2df5669eb08cca920486989f970fd20c20e4e047bdf8383886bd1b40cd9fe752`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOLANG_VERSION=1.25.2
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOPATH=/go
# Tue, 07 Oct 2025 19:07:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 19:07:03 GMT
COPY /target/ / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:2212ccc79525753c3f36994bd936e194dcec09d69b21786be4caa60f697693d8`  
		Last Modified: Mon, 29 Sep 2025 23:34:26 GMT  
		Size: 49.5 MB (49466651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304a8a7ec291d92cb9effbdbbb7bb5864ca1d87b5e149ee45db584ed39cfc4eb`  
		Last Modified: Tue, 30 Sep 2025 00:20:19 GMT  
		Size: 24.9 MB (24860635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:963263603b7fae742ca79dc45230eee7f46d0be670e6738f50212dea9f77470b`  
		Last Modified: Tue, 30 Sep 2025 01:18:20 GMT  
		Size: 66.2 MB (66233435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682289fa7580e252ac66f6b7b6de016ca93a6606235d7be305043efeaf82ad87`  
		Last Modified: Tue, 07 Oct 2025 19:34:34 GMT  
		Size: 89.8 MB (89823288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1303a4fd3683897bef6c94e29bf9e3651f1c90c65f26cacc89697c837708724c`  
		Last Modified: Tue, 07 Oct 2025 19:34:26 GMT  
		Size: 58.9 MB (58869862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa21ee7f670fa76975def6d17e743770c04a785592596ee5c1c8e31586344575`  
		Last Modified: Tue, 07 Oct 2025 19:34:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:c2e5966b25665f11a2af138e371567c98b58c581399242c4435a26576cea7e11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10503117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4172a7b86b7ab71785f98ef012007b4886a80737066766458636f2ab50a2dc`

```dockerfile
```

-	Layers:
	-	`sha256:68bbe06300cbdf8bb36f5264fd52b78a14ce5cc2d9bd9a1f8ad99b38af38aabf`  
		Last Modified: Tue, 07 Oct 2025 20:24:25 GMT  
		Size: 10.5 MB (10475313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:179e03782db1060b3605a991a9dd1b1aece96cb60f1051765ec1a152a8d8cb97`  
		Last Modified: Tue, 07 Oct 2025 20:24:27 GMT  
		Size: 27.8 KB (27804 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:756fe7a2eb4b5dc52bd2e25060ef9ee5d970ebde3fc66c34b743f9a1c98b87ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262250693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b6f07e2b4673eb6c96fb4a0af328368206c720f2f93f127211c4ebf9fc8132`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOLANG_VERSION=1.25.2
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOPATH=/go
# Tue, 07 Oct 2025 19:07:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 19:07:03 GMT
COPY /target/ / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7eacf7da1d9ca68e46013f3f56395614b995d68904a39e73d4a5bad90579014f`  
		Last Modified: Mon, 29 Sep 2025 23:33:18 GMT  
		Size: 48.8 MB (48760734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300a1eca9595b83f733381d5f5c6ca135b5d5a79fcdb8204a00ace454f493a78`  
		Last Modified: Tue, 30 Sep 2025 16:39:43 GMT  
		Size: 23.6 MB (23611218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4ad543e1bb93773e8c6b716a20da76b363bb9d042051784870a3254e450de6`  
		Last Modified: Tue, 30 Sep 2025 20:27:52 GMT  
		Size: 63.3 MB (63309463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b39be94b43c7b8fee0fdcf795208f91323ad52fb7cc0e21f16aaaac555d61b8`  
		Last Modified: Tue, 30 Sep 2025 22:53:31 GMT  
		Size: 70.0 MB (69997146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f890e15b402b837e157faa2cb0832dbab9e79a8fa0b1c8b79f942dbb1ac7ce`  
		Last Modified: Tue, 07 Oct 2025 19:35:23 GMT  
		Size: 56.6 MB (56571974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab94e3f8c81043c743ffb28a891ceef928a4fcc94914a1b0be901a4fa62c0f66`  
		Last Modified: Tue, 07 Oct 2025 19:34:04 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:c6069a30953ebee699b0df7d214146093006a0d41b1a229041b67d4135f2aa94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 KB (27697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04faf39ef59887d4345221c66f6e1c87c0448d01bdfc19353514d7edc7e24e38`

```dockerfile
```

-	Layers:
	-	`sha256:e1acaf96227e3235e072e7eb04509029076bbba3c5f1b7eeb3261321a4a2d74e`  
		Last Modified: Tue, 07 Oct 2025 20:24:33 GMT  
		Size: 27.7 KB (27697 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:9331bc0d7ae2edb967fabe8635d4c330833d3d19c272534f316f269b3a0e546a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.4 MB (296392893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a56c7f8d069cf86f7d4d98ce956bb918199776c25c8ce0584fabb2eda7277ac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOLANG_VERSION=1.25.2
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOPATH=/go
# Tue, 07 Oct 2025 19:07:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 19:07:03 GMT
COPY /target/ / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:812b25f785969d275d8c3962568c03f83ccc4df31b95f01c0646d79d6d5069f3`  
		Last Modified: Mon, 29 Sep 2025 23:33:30 GMT  
		Size: 52.3 MB (52326764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f96d9492071bbcb8f94f1c41ed34bb1a985729d6a6ad6f8a6d10f9bd6e3f16`  
		Last Modified: Tue, 30 Sep 2025 02:24:29 GMT  
		Size: 25.7 MB (25668919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8559f87b306ba2a8705f64aa230b6840e422b552a6363650f02e37cde768fc14`  
		Last Modified: Tue, 30 Sep 2025 09:20:33 GMT  
		Size: 69.8 MB (69845543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b9b052a32cc9593256d5096437790565c79483c5e1e301697d510145037fed`  
		Last Modified: Tue, 30 Sep 2025 19:48:33 GMT  
		Size: 90.4 MB (90417716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbab16c006e3e87a0bd86bfecf5ca21f23b4930a744517459433c08bfbfc59e0`  
		Last Modified: Tue, 07 Oct 2025 19:34:11 GMT  
		Size: 58.1 MB (58133794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc7fa57303267464c481c6ce6ca543a6c45675b93b5cd042dc36341a694db9f7`  
		Last Modified: Tue, 07 Oct 2025 19:35:18 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:f6e114f83cf600c14765424157bf80009c2aae91d7f31a53d397357d0254745a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10496121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504eccb29b23103328fbff87d8b5c38511db639145f09e3ea0b68485c5ebec20`

```dockerfile
```

-	Layers:
	-	`sha256:834720f10e07ace93576008afa7d430a5c51096d225906208c3519d9353be991`  
		Last Modified: Tue, 07 Oct 2025 20:24:44 GMT  
		Size: 10.5 MB (10468233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e09d59cf86058298fd90ac5ffe91d1d7fad03f01e49dd00a7d5544874f195ba6`  
		Last Modified: Tue, 07 Oct 2025 20:24:45 GMT  
		Size: 27.9 KB (27888 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:a6dba1556a28d248a82aa5c708eb44dbeebf112ee81be78a2108e30f29d0c030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.1 MB (263147795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19bf2b0a0028e06a83f2354b4caa0f74f1d2791265f716c8591511e4227752f2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOLANG_VERSION=1.25.2
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOTOOLCHAIN=local
# Tue, 07 Oct 2025 19:07:03 GMT
ENV GOPATH=/go
# Tue, 07 Oct 2025 19:07:03 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Oct 2025 19:07:03 GMT
COPY /target/ / # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 07 Oct 2025 19:07:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:87d1bec83b35277b636c6e05b9418301b2f025752d7539cecae442f0b94d8fbe`  
		Last Modified: Mon, 29 Sep 2025 23:33:26 GMT  
		Size: 47.1 MB (47137446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2365377a8d4ecfdf70b8afc073fddfe487283a41bc28927b47a4757047f66c`  
		Last Modified: Tue, 30 Sep 2025 03:09:03 GMT  
		Size: 24.0 MB (24023716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc9730cf662a91a14b192c512ec1973efc8f7eabd745b63f8c6c877f23bf0d0`  
		Last Modified: Tue, 30 Sep 2025 09:32:19 GMT  
		Size: 63.5 MB (63501350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08a4dbf2eab022c30a4f1ad0d69bb0be8e9a7b59d1d848c5eb4bcf43acac22ef`  
		Last Modified: Tue, 30 Sep 2025 23:54:17 GMT  
		Size: 69.0 MB (69006320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6429ba33a49b3f3080422ca98d26430f3e1c1ba8f8f41bc6d8af4cff9843f4da`  
		Last Modified: Tue, 07 Oct 2025 19:36:10 GMT  
		Size: 59.5 MB (59478805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04965c7b24bd096507ade2726211e4b0153c631f202aca7dec0a1efe1b21550a`  
		Last Modified: Tue, 07 Oct 2025 20:31:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:1c479e26fe2c2c9640b667787c6fcae1311cfa320bce9741b94ea65aeac08e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10355338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd71fe4171714f8754a01fd33a576b6faff691a86ff5427338617b8afef7366`

```dockerfile
```

-	Layers:
	-	`sha256:8e85ae711d44fbb9f7273d0ab331b6bf1ce3b88d724d51048797cfe4593ef705`  
		Last Modified: Tue, 07 Oct 2025 20:24:52 GMT  
		Size: 10.3 MB (10327498 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c47220b613f9b38f60fa36bbb5bfa4a379d1c7c71d397d83cb9c78fa02a6b3ac`  
		Last Modified: Tue, 07 Oct 2025 20:24:53 GMT  
		Size: 27.8 KB (27840 bytes)  
		MIME: application/vnd.in-toto+json
