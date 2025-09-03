## `golang:1-trixie`

```console
$ docker pull golang@sha256:56d8e182842c1db6b9082cc6e03ff5ce485d6ecacd2bcafe58437d8d4870fe66
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

### `golang:1-trixie` - linux; amd64

```console
$ docker pull golang@sha256:dd84ad5b4781ff4d910eff44647426b525991249d3420b18d761ec9b40bd0ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.8 MB (304769612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07f39aa67e93ef338b152c113a5f9c646ddf092ed75fa5f7cf6d68bb90ca97a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOPATH=/go
# Wed, 03 Sep 2025 18:13:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Sep 2025 18:13:04 GMT
COPY /target/ / # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e4db86de6eba33869491caa7946b80dd71c255f1940e96a9f755cc2b1f3829`  
		Last Modified: Tue, 12 Aug 2025 22:14:12 GMT  
		Size: 25.6 MB (25612940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea45766c6449310ca2fc621a7e00bedb4b9b803a7fbfe2607efce6d2e07e435`  
		Last Modified: Tue, 12 Aug 2025 22:15:03 GMT  
		Size: 67.8 MB (67777316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f11ba9dc54fb3093c52b298810f7893d5da705f07707c6fd3bd3f962305fa9`  
		Last Modified: Wed, 03 Sep 2025 19:04:18 GMT  
		Size: 102.1 MB (102055309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330457f0054be4c07fbaeac90483ac4f534113ccd944fe16beb9e079a3ab3a36`  
		Last Modified: Wed, 03 Sep 2025 18:49:05 GMT  
		Size: 60.0 MB (60045609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994678d1c2a93bf605782bddb80bc3a0c17db79ca705f3c2205cc880671e0dc7`  
		Last Modified: Wed, 03 Sep 2025 18:55:30 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:b6fa7a8f2c55dcc87db6bdefb66281b9004bb8fe76acf49a97c2a308c3d7f3e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10808698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0458b50bbf17babdf68355fe94386717b250f5ea782eda45cce33416540d320a`

```dockerfile
```

-	Layers:
	-	`sha256:6123e4d18f2197ff587a02c0d8048035728f51fb1fac8ec8f23150b637dc106a`  
		Last Modified: Wed, 03 Sep 2025 19:04:45 GMT  
		Size: 10.8 MB (10779702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a07f7cfc7af2922ca6d6e0a125a61f392768a736856722160bd44fa700649a6`  
		Last Modified: Wed, 03 Sep 2025 19:04:46 GMT  
		Size: 29.0 KB (28996 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:5dc7f9c13f56c1e39f9b482a9f43e035dc247ea48ecac1f51ca3953b4b0edf3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.7 MB (263721594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9295fdbb3b4bd45d2500f6743a5ec7bab45825db3a7af21b6169c82754ae626f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOPATH=/go
# Wed, 03 Sep 2025 18:13:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Sep 2025 18:13:04 GMT
COPY /target/ / # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:58382c67f397ebdc005890f56dc436f7798aeeee2e0d603ba02e89d6243c138b`  
		Last Modified: Tue, 12 Aug 2025 20:51:59 GMT  
		Size: 45.7 MB (45712631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce72873bc1bfa1e9338237d9573d1640f6647f61a1636bbd71d8128d16503087`  
		Last Modified: Wed, 13 Aug 2025 00:16:54 GMT  
		Size: 23.6 MB (23613045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe0a58e6c2887b271354fa2e1067ff7e829f063163f76c4a3d4f1da179eb22e`  
		Last Modified: Wed, 13 Aug 2025 06:50:21 GMT  
		Size: 62.7 MB (62718501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983e43eed239a19cf297a7ce2beb2041dbb4789440168f810815da1dfa6cf3c8`  
		Last Modified: Fri, 22 Aug 2025 17:33:19 GMT  
		Size: 72.7 MB (72699083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec999c8e928607a0bc4da54080226a6c247c744815a64f6c10bf38b015958ebf`  
		Last Modified: Wed, 03 Sep 2025 19:08:36 GMT  
		Size: 59.0 MB (58978176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c00e91ff50d758d873399ecf3d096c2df608ea0f9b11561b699af1676e2cf8`  
		Last Modified: Wed, 03 Sep 2025 18:56:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:f4c53f7d29f49a92b449cd639d48989b664f013d08df0c1ffd0a943895667b53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10604748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a77ff60300bf43b4844bbe993cf0c23f93c39e39b4c5e0e43b464685b9920f95`

```dockerfile
```

-	Layers:
	-	`sha256:90770feb1310ab630335a0c7173b2223ce84e0839874acf39ed1ac2de9309c2e`  
		Last Modified: Wed, 03 Sep 2025 19:04:55 GMT  
		Size: 10.6 MB (10575623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54854d0c35d2bac970bc6829b2e1457986a325227d0013f16e06bb05eebe0890`  
		Last Modified: Wed, 03 Sep 2025 19:04:56 GMT  
		Size: 29.1 KB (29125 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:ca32d0ba792a39f0056e99b46cb44370cad1597f5357f2c2bed080f64a4ab94d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.0 MB (298005662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e6c5c0060c3eef564278ad1589fd24c5ae1ad903ad35e2d6573094abe8cc978`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOPATH=/go
# Wed, 03 Sep 2025 18:13:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Sep 2025 18:13:04 GMT
COPY /target/ / # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9923852056eb09462c3344515191318e7aa33ff28057c946bc41a414ee57df0b`  
		Last Modified: Wed, 13 Aug 2025 07:30:07 GMT  
		Size: 25.0 MB (25014610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bcc8bff74cbeacbac9c6869b6a9def273b93cc67de196b347688de2a9185de0`  
		Last Modified: Wed, 13 Aug 2025 15:31:50 GMT  
		Size: 67.6 MB (67593628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1ac401574f911479ede74ac51bf6b97a3e9068a260cb14b2cb133e3cf3eb58`  
		Last Modified: Tue, 02 Sep 2025 17:24:12 GMT  
		Size: 98.2 MB (98200183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4681030a890db37290ab2fddf45adb75dbd1fbf983ba1b16efefb7221b97b1ec`  
		Last Modified: Wed, 03 Sep 2025 18:48:35 GMT  
		Size: 57.6 MB (57555480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c243ddef96e454514954a8c9d9198ead969fbc75461927be95aa14678940cfbf`  
		Last Modified: Wed, 03 Sep 2025 18:48:27 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:f041b583c4bce1be3929e0cda012ac6cc40289f0ce5eb99b7d9ec3444930bf94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10929377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d52ccfb4ed13e122eadd1935bd549df5322a963d0df331d0c46bdf4a541c79`

```dockerfile
```

-	Layers:
	-	`sha256:7e7d66d44f4930fdf2b8fa7320f4f70bd7a219a88501ec17bed66b5c18671ef5`  
		Last Modified: Wed, 03 Sep 2025 19:05:08 GMT  
		Size: 10.9 MB (10900205 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eac001761d7c73b83001eac49f3cff79d3be414ed2da182d828165d82a31853`  
		Last Modified: Wed, 03 Sep 2025 19:05:08 GMT  
		Size: 29.2 KB (29172 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; 386

```console
$ docker pull golang@sha256:d1f456edb20fc8f14ed70879c05f12e08f3cf4b531857224bb20cb8076046c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.6 MB (306624257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7499906468a80841b11e3231586917e9994de85f38c19f146d82428186df5f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOPATH=/go
# Wed, 03 Sep 2025 18:13:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Sep 2025 18:13:04 GMT
COPY /target/ / # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3d9f8c7ff550056ffe2cca57d7110ae0306e74220a891574e97ddc10ba49823d`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 50.8 MB (50794258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde29e7bc69fcf496b5e5df92d7d82da6ff9f4877784085c4dcba73f6ee6a1ea`  
		Last Modified: Tue, 12 Aug 2025 21:20:38 GMT  
		Size: 26.8 MB (26772559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd9904337df106e0852d247e06047929e66d5097f2d2c13861e2e31ecc63f4b`  
		Last Modified: Tue, 12 Aug 2025 22:15:57 GMT  
		Size: 69.8 MB (69794753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989d8f3d26cf9cee91ce8ddc9173d63ed3ca1d5501272b703084b01e49a46dbf`  
		Last Modified: Wed, 03 Sep 2025 18:49:35 GMT  
		Size: 100.5 MB (100498481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8134730600d4cfc74c5293aacb74478de1de4810632b08ac46dafe23f69bbce`  
		Last Modified: Wed, 03 Sep 2025 19:04:05 GMT  
		Size: 58.8 MB (58764049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0f4aece25c6f91eb4311c08c7c3751cf751e03ea46f6a5eab8580addf1eec2`  
		Last Modified: Wed, 03 Sep 2025 18:49:22 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:8a3b851f8edae11a64ec88a3d99b97749fbde41d49917755f1a7d42bf9971994
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10779888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b183c28c1266ee61be44368b08a9406c98c526088e55c0ad81dd93b62a705c42`

```dockerfile
```

-	Layers:
	-	`sha256:b4f55adc076b31deb0728c710463a7ba961a8605e161aaef673ffbd2458bb1fb`  
		Last Modified: Wed, 03 Sep 2025 19:05:18 GMT  
		Size: 10.8 MB (10750948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbf8332cc6f3c930dac75f594d98e1ad6082c73369b36f5deea3f6f1b5d22d43`  
		Last Modified: Wed, 03 Sep 2025 19:05:19 GMT  
		Size: 28.9 KB (28940 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:04117a3832a626a1b04516767ec419bb31e6482459d26f3b778b0276d936bd94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.9 MB (303912717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b21e9a862699dba89a3c4da4076952febb88fe4e47f1485eeea73b72c4c113`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOTOOLCHAIN=local
# Wed, 03 Sep 2025 18:13:04 GMT
ENV GOPATH=/go
# Wed, 03 Sep 2025 18:13:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Sep 2025 18:13:04 GMT
COPY /target/ / # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 03 Sep 2025 18:13:04 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a327675583423e2c44eae4c02a88be15dbeac36073deb88700ba487e0c0e35`  
		Last Modified: Wed, 13 Aug 2025 15:15:16 GMT  
		Size: 27.0 MB (26992868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf20d9e1e5f16d7552d637dd4a12484b22e52928311f81dd13c82b6838c2ae7`  
		Last Modified: Wed, 13 Aug 2025 21:23:59 GMT  
		Size: 73.0 MB (73018659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c109f1eaaa6062f2aff79b79857ba42623f33aab83075f001a97de36d13c1403`  
		Last Modified: Tue, 02 Sep 2025 17:28:09 GMT  
		Size: 92.8 MB (92761484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9295eaa21ceb778d7859c40f41ccdf7cdeffaaa99a56ac388f747e3eb72308f3`  
		Last Modified: Wed, 03 Sep 2025 18:50:02 GMT  
		Size: 58.0 MB (58036165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3682b6985247a3ed55b89a36950b213d50741dfc19f202d0106b90b8cd3da9`  
		Last Modified: Wed, 03 Sep 2025 19:08:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:1bd02eb176e2ea752cc61d6a77669c6dce720845d8fa4246bf7ba71301c9cbda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10804574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4508616b02eb0e9cc997d2204de607cd6b151c3e6fa1a7d8ba4dbafebdc3b0ef`

```dockerfile
```

-	Layers:
	-	`sha256:800619d40628a401588beec3e0698b28ed410f11c9e821361ef909bcdabbf57c`  
		Last Modified: Wed, 03 Sep 2025 19:05:29 GMT  
		Size: 10.8 MB (10775510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f06f2722d0b80fec595157c3a8d1e0f0dc5b7960a4e764f97fb00bc758313754`  
		Last Modified: Wed, 03 Sep 2025 19:05:30 GMT  
		Size: 29.1 KB (29064 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:0469643cc51e045664a38a7c52c911f994b248946d47cb468e433914d85f4a83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.5 MB (329485334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f69182d7e073994c46e36ac705394d1ca482d3c7a53f4e7836bb79bd02df7fa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOLANG_VERSION=1.25.0
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOTOOLCHAIN=local
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOPATH=/go
# Thu, 21 Aug 2025 20:07:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Aug 2025 20:07:19 GMT
COPY /target/ / # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:59f3e0adb655cb03f7d489f3cc57e302e249916bbb076c78008f9329238bfb20`  
		Last Modified: Wed, 13 Aug 2025 01:13:55 GMT  
		Size: 47.8 MB (47764303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751e41821bc74a26f64d4f81be6785aac1d7f09df07149a206784ae23523e36a`  
		Last Modified: Thu, 14 Aug 2025 14:47:51 GMT  
		Size: 25.0 MB (24950584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcb0b64daccd6b787f78c1a1622c08097763f53e2dee005bedbf3141bbaa8af2`  
		Last Modified: Sun, 17 Aug 2025 07:49:06 GMT  
		Size: 66.7 MB (66658307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633618253f092f4a4acbf99fa7a220a8363959887159df8b8feac3518e23d810`  
		Last Modified: Mon, 25 Aug 2025 01:07:47 GMT  
		Size: 131.5 MB (131541938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8818a250444a855ca5b23afc25325ec1add801f7bb83153c967335fb20cce8c`  
		Last Modified: Sun, 17 Aug 2025 10:47:36 GMT  
		Size: 58.6 MB (58570045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb26f7d1c5e9568ec7148d2fae44ac2bbd1d07c9415eb5050648e13bb1c1b81f`  
		Last Modified: Mon, 25 Aug 2025 00:08:59 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:689405cf77af1f9e8f7e219eb7f5b217c22c1b27206dae16882c4197ad3abc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10878410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fba55ddf546f1d940c76919292735e01427a4a55de68efde4115663b7390d65`

```dockerfile
```

-	Layers:
	-	`sha256:0df1241845c7e31cf6a3f69e67bf55cab7057b4e697ccb9a7eea3a3dffdd6810`  
		Last Modified: Mon, 25 Aug 2025 02:23:03 GMT  
		Size: 10.8 MB (10849343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:185e0617b03d4279795a6e7ccb469894edbb7f0dbe2e6c387c32266145ff4023`  
		Last Modified: Mon, 25 Aug 2025 02:23:04 GMT  
		Size: 29.1 KB (29067 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-trixie` - linux; s390x

```console
$ docker pull golang@sha256:5aa9673d0f18d1f3b18bd2ce33290f7f8733e31202b39d60bbe1b49fc68914b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 MB (279989088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c34a19de47efdcd2f357afce71f34ee0b9029be311251899a3106f6eac43074f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOLANG_VERSION=1.25.0
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOTOOLCHAIN=local
# Thu, 21 Aug 2025 20:07:19 GMT
ENV GOPATH=/go
# Thu, 21 Aug 2025 20:07:19 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Aug 2025 20:07:19 GMT
COPY /target/ / # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 21 Aug 2025 20:07:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c3b791adea90b39bc59919a9959b7f44f65aa3364a03dd0271a5ff658488877f`  
		Last Modified: Tue, 12 Aug 2025 20:59:03 GMT  
		Size: 49.3 MB (49345161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47181ddd75754adfc74e4f58b4a898ec33ad906976b71219b567efd19470677`  
		Last Modified: Wed, 13 Aug 2025 03:27:04 GMT  
		Size: 26.8 MB (26779580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415f63d435cf750f4bda1af6afa07ce9f812fa19c74e6f9f050da85f47eb36e7`  
		Last Modified: Wed, 13 Aug 2025 17:21:16 GMT  
		Size: 68.6 MB (68619998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d954366204dd198f5f29a2ea512acfb1c64ff1a9eab53a5c7474b137bbaab1`  
		Last Modified: Fri, 22 Aug 2025 17:36:11 GMT  
		Size: 75.9 MB (75868390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9485872b5fffc22e2aefdcb4ea3e4e402d1d172e8c40a2f24d72bf50eaca3d7d`  
		Last Modified: Wed, 13 Aug 2025 22:23:58 GMT  
		Size: 59.4 MB (59375801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54653c832ccda7a9dd284c9f77fe718e3c3e934b80ceea2f2553b394423c5eb`  
		Last Modified: Fri, 22 Aug 2025 17:36:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:56a53c703d4a1833929039f2800c2bc7ef116b8a445f55a206dfcb30397a0b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10619094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd152cf7ff610cd956658c27111bbe05129373ea17f54638d9f10956faac115`

```dockerfile
```

-	Layers:
	-	`sha256:498ae6a7786a649af75ae1d32fc299b43f715dc030d97b71dcf5a057890f84e2`  
		Last Modified: Fri, 22 Aug 2025 20:23:43 GMT  
		Size: 10.6 MB (10590102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94b6e8af0000013d68fecb7058c8f976170093448eb62e17f20c205778443f78`  
		Last Modified: Fri, 22 Aug 2025 20:23:44 GMT  
		Size: 29.0 KB (28992 bytes)  
		MIME: application/vnd.in-toto+json
