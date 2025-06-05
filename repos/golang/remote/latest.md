## `golang:latest`

```console
$ docker pull golang@sha256:db5d0afbfb4ab648af2393b92e87eaae9ad5e01132803d80caef91b5752d289c
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64

### `golang:latest` - linux; amd64

```console
$ docker pull golang@sha256:2ba8aa7693241f09f3b6e5526a00234f59ee950e22f0a6b39f8b5cd467895f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.2 MB (308240926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb837ec5cdf87efbbb7a12922b7a25798eefba9c5aec82cd1f3913837d5725d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOPATH=/go
# Thu, 05 Jun 2025 18:53:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 18:53:13 GMT
COPY /target/ / # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37927ed901b1b2608b72796c6881bf645480268eca4ac9a37b9219e050bb4d84`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 24.0 MB (24015635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b2f47ad4443652b9b5cc81a95ede249fd976310efdbee159f29638783778c0`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 64.4 MB (64399858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e554ae2ef7dd7520cfb45dc7aa0f66036d4f127f965b16a3e11f06ab3842827b`  
		Last Modified: Thu, 05 Jun 2025 19:27:53 GMT  
		Size: 92.4 MB (92355220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f67fead7e33763b5fa924cb2e4644bbf5332ed056eb32ba0bcd3bdb68eea3b`  
		Last Modified: Thu, 05 Jun 2025 19:27:55 GMT  
		Size: 79.0 MB (78981811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56df01461c4335d211d049a65ae27676cd31d459a63b98ba0b3797e767cb1b1`  
		Last Modified: Thu, 05 Jun 2025 19:27:45 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:18a5a31bc558c4f5d2767baeebc3b921b58d918463474aa1dd1efb091e0c8a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10340391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b377ea50a355099c795a582f458d24fd4da4c2cae15ce3a5692a28be49764ab`

```dockerfile
```

-	Layers:
	-	`sha256:ffa1aa01c837be67f249c10218a6f618b0a6c7b873ee62b29a6366392229d944`  
		Last Modified: Thu, 05 Jun 2025 20:22:45 GMT  
		Size: 10.3 MB (10312745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79940778aa50b431891bea890e4f43f41f8847d815b819acddfcb65c173a8232`  
		Last Modified: Thu, 05 Jun 2025 20:22:46 GMT  
		Size: 27.6 KB (27646 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; arm variant v7

```console
$ docker pull golang@sha256:bc4305e8f1d713edc1e194c74cae30fcf7d5af10654248ccc17329cbe6f43c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.1 MB (269138656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:437d6115d708bc2fe3dde386713163c09e6108bc2b23765501d5a39f9a3480fc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOPATH=/go
# Thu, 05 Jun 2025 18:53:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 18:53:13 GMT
COPY /target/ / # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3a781f536825e084b88c231841be4d1c7df016a4aa2ebdd27d7431b5f1ab3419`  
		Last Modified: Tue, 03 Jun 2025 13:35:03 GMT  
		Size: 44.2 MB (44202771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b02150b4002b569f2f9be5055a06c94a228e07937f6f39fd4d84b52042b2f01`  
		Last Modified: Tue, 03 Jun 2025 13:46:06 GMT  
		Size: 21.9 MB (21924635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c061a668a2586bc3366d21d8a069b30ac6fdff27bb5140a653d59b71241213`  
		Last Modified: Tue, 03 Jun 2025 13:46:06 GMT  
		Size: 59.7 MB (59656286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6769ccbcbb302e58183ef7d1b1458e5ec9e4e0e712cf266d56ddefb34341bfd`  
		Last Modified: Tue, 03 Jun 2025 14:36:19 GMT  
		Size: 66.2 MB (66210504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ca4d2f2221547bbb6d011d5b305d7607f58d76e99b3112e811b1627f40e830`  
		Last Modified: Thu, 05 Jun 2025 19:28:26 GMT  
		Size: 77.1 MB (77144302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6094ad649b487a228298716ff4d34086af5bdf0b8a27620254e902000494e983`  
		Last Modified: Thu, 05 Jun 2025 19:28:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:2d3d9e6fb8070c98b75035e646cbedb9324a364343c272e4a07530afd4940e76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10147246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280da97f617b8c989f7ca43245c73a786fa3bd7df26e584644fe2fdcea25ae03`

```dockerfile
```

-	Layers:
	-	`sha256:20f6558ab306335c28d6a9f3f79b6087374d87dbd53386214aad6c4e6146d5cd`  
		Last Modified: Thu, 05 Jun 2025 20:22:55 GMT  
		Size: 10.1 MB (10119466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ae6b4a43a628f54a31c5066478fa8c597ea6810d6c9ca3d888f4c5f3e3857f5`  
		Last Modified: Thu, 05 Jun 2025 20:22:56 GMT  
		Size: 27.8 KB (27780 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:f692138c53fd540f6d19fe65e259d0d1b681776d15187c50ab566297acf28227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.9 MB (297881391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd4095bdf35388c48f7b567b9a331abc514c2791a8beb35cd1558fb10d91285`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOPATH=/go
# Thu, 05 Jun 2025 18:53:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 18:53:13 GMT
COPY /target/ / # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280bbe393e788ced1dcb033580604b24de083601624337be66b3ec31781dae40`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 23.6 MB (23551398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4f297e4f699ae0f384d5cc1ea42065f58a115aa0a634d427cbb186f91cb4d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 64.4 MB (64361989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e45158653cee17fd0433bb95f654076603c1dace770784457d1f08ffc1f1bd`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 86.4 MB (86409121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f244882bda0eb70b1153262e9054d1f8801651888a3a6fc5a828db420391040e`  
		Last Modified: Thu, 05 Jun 2025 19:28:02 GMT  
		Size: 75.2 MB (75231544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08d494a376b9ba066591a0d5e15795ecaa4ca7b89566facd3b70f93b58f9cfa`  
		Last Modified: Thu, 05 Jun 2025 19:27:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:55ebfd7c5cfe5b1e436bfbe647cfb660c94238c0088bc260f216e6ea0a9d4661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10368467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe622c3fe8a4a8f4ee297ed1daa12f2f328b6606263f36542d39c801e35961d`

```dockerfile
```

-	Layers:
	-	`sha256:571354225ad4793303fc998bc1df4940a5a703c057b78e16590aca004afe3696`  
		Last Modified: Thu, 05 Jun 2025 20:23:04 GMT  
		Size: 10.3 MB (10340640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f35ccc13b671c8163764df2439f71d22c044a6c6ab258262ec5baaa9bd68f7f8`  
		Last Modified: Thu, 05 Jun 2025 20:23:05 GMT  
		Size: 27.8 KB (27827 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; 386

```console
$ docker pull golang@sha256:9c8284d96c19716e9308ecafa23bda5baf455017748c79b5ef8026c8be918828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.2 MB (307226552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f859e7f94fdafda7641a4e8a454441d809edb5877d566dd95a2ad74314054e3c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOPATH=/go
# Thu, 05 Jun 2025 18:53:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 18:53:13 GMT
COPY /target/ / # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7bdd0d6ce898fe017a461e5f67ccf41a15f147063ffe1c496fb7e5f75037adfb`  
		Last Modified: Tue, 03 Jun 2025 13:36:49 GMT  
		Size: 49.5 MB (49471562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296134322e370a0aab10509f2b47d9ce416e7da5a792e7f8badd9284ecbabeb0`  
		Last Modified: Tue, 03 Jun 2025 14:02:05 GMT  
		Size: 24.9 MB (24855668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc8c7f8292580c2c70e8cb47ec957249f0882ee6ee3737bf3250e44650a38db`  
		Last Modified: Tue, 03 Jun 2025 14:02:15 GMT  
		Size: 66.2 MB (66224115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b24403347b1a7b362b8af82990bb7d98dc50fa5b5fe2e07fecd23367657858`  
		Last Modified: Thu, 05 Jun 2025 19:28:09 GMT  
		Size: 89.8 MB (89774470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae592fba0490bc253690fa17e5004b2923bab9e7f9c8d6e116245da17997d7d0`  
		Last Modified: Thu, 05 Jun 2025 19:28:06 GMT  
		Size: 76.9 MB (76900579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e1a568aa41953a73ef9d02f21b462ba35e784b398203f1d025189b67b49333`  
		Last Modified: Thu, 05 Jun 2025 19:27:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:3094332490e81494d429d13dfc8b17b4f40929f0b0f98a63f8d20ad378177d93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10319873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3225fbce8e523425ac10a72557c53b5a82230326d82958482a261c8ac75e6b2d`

```dockerfile
```

-	Layers:
	-	`sha256:88c1d857658742a286bf5e4742c40ce4c566aefc04631a4d8112c25e177e04d2`  
		Last Modified: Thu, 05 Jun 2025 20:23:13 GMT  
		Size: 10.3 MB (10292283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:222eeaff881ee86bfe5bf68bb78e46af5ee753e096752c996670a3f9dfc6dfb3`  
		Last Modified: Thu, 05 Jun 2025 20:23:14 GMT  
		Size: 27.6 KB (27590 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; mips64le

```console
$ docker pull golang@sha256:265204de3fefdccef464f3c6a1dd1feafab1459a67d2b1f4930f072a6bdc8abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278560750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0195e4bf5895952606b783407d3ddeda000ae78469c7dadf268903f47e0d6efb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOPATH=/go
# Thu, 05 Jun 2025 18:53:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 18:53:13 GMT
COPY /target/ / # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:d480a40975e955224ed64be37e82f220f731f0379d20a7b8c36be0e47e31d8df`  
		Last Modified: Tue, 03 Jun 2025 14:36:18 GMT  
		Size: 48.8 MB (48769753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7dc05e2d1c7537a7663041b66446ee4a24f98e673290839931cdaf3c0b93f56`  
		Last Modified: Tue, 03 Jun 2025 14:36:17 GMT  
		Size: 23.6 MB (23598613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6fef5bce771d4c7090ec3bddacaa83a3ac07da89649b62764c8f0bb14e3e0ed`  
		Last Modified: Tue, 03 Jun 2025 14:36:20 GMT  
		Size: 63.3 MB (63308472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa4ece845a4d4a4ec28b24cc19384f49afd8d3bee80380c09f3a36d476d34fc`  
		Last Modified: Tue, 03 Jun 2025 14:36:21 GMT  
		Size: 70.0 MB (69950183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e8449b0f1eec02691482cf8a405aeed88398feceed91dd2882173d43b2ff08`  
		Last Modified: Thu, 05 Jun 2025 19:30:59 GMT  
		Size: 72.9 MB (72933571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5aabfafde5cefb387e977850f7f6549819305e1ef13db8ef65b7fecfae86b41`  
		Last Modified: Thu, 05 Jun 2025 19:30:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:158336816f99a7e12d5e90231406891397cbe0ce8876dda23635cff12d2efc6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1c0d38d195b15364930060e9f4860957811998cb25f2ba71dcd81358b6a318`

```dockerfile
```

-	Layers:
	-	`sha256:fd3ad77dfeaa8ed6a363459d917a99e39923eda77c2746706ca02fcdfe970be1`  
		Last Modified: Thu, 05 Jun 2025 20:23:22 GMT  
		Size: 27.5 KB (27539 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; ppc64le

```console
$ docker pull golang@sha256:cdbb0fc52497eb50a170fa38add6c92d349d5fdb8d9cd2b4560130c4a31a0c17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.7 MB (313731061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3569d5f9c55fda89710fd876e1280c2b5d5a1499aae27e8f34cd40f64517fb0e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOPATH=/go
# Thu, 05 Jun 2025 18:53:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 18:53:13 GMT
COPY /target/ / # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Tue, 03 Jun 2025 13:33:40 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d82206e3ae1269ed70d5c84db92f6478d2de4719db96fab0f36254db269f0fa`  
		Last Modified: Tue, 03 Jun 2025 13:36:57 GMT  
		Size: 25.7 MB (25657297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c498d213a2aac9e38fe414de433d75bc8ba03faa40c2b4f0690897cf17174f58`  
		Last Modified: Tue, 03 Jun 2025 13:36:59 GMT  
		Size: 69.8 MB (69839678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc3651009f91cf27e970ae7dc7349e20fba94b97f4d2143617e748afd3d930d`  
		Last Modified: Tue, 03 Jun 2025 13:43:23 GMT  
		Size: 90.4 MB (90354720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1857e797654b7f586891362befa86842c081cc043ee887ea9708f0fb0ac7c27f`  
		Last Modified: Thu, 05 Jun 2025 19:28:59 GMT  
		Size: 75.5 MB (75547589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241901a30a5b57fe338f45c995fd59502cb331350716985edd2427dc41b7a4ce`  
		Last Modified: Thu, 05 Jun 2025 19:28:44 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:6a19c7307168c17bb52a323044ae991f74635963a86fd766acebb178dcd4eee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10312986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d79abbea9c69112ba0f9be0735d62a89d2244595c6aa5787a97a75d892f9a9`

```dockerfile
```

-	Layers:
	-	`sha256:87bf0e11b3639aefce7fcbd8fae44c94b21171ddf2cbf5e809d31ebe9986fa55`  
		Last Modified: Thu, 05 Jun 2025 20:23:26 GMT  
		Size: 10.3 MB (10285269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a186b5ea31e1ea29f6b7ae1c238648780433441fad9a00b4152567f7c7f5d01`  
		Last Modified: Thu, 05 Jun 2025 20:23:27 GMT  
		Size: 27.7 KB (27717 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - linux; s390x

```console
$ docker pull golang@sha256:d7e41b7f27cf3a1db2643971bdccf309f0f5d5dfb675e1efe894b6efbb0825d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.4 MB (281389145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ec2aa251320d234139f5c88e409461d7be3f939a96cdefb90883c8384583b5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOTOOLCHAIN=local
# Thu, 05 Jun 2025 18:53:13 GMT
ENV GOPATH=/go
# Thu, 05 Jun 2025 18:53:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Jun 2025 18:53:13 GMT
COPY /target/ / # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Thu, 05 Jun 2025 18:53:13 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Tue, 03 Jun 2025 13:33:39 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86a43d043466908a6aee9cc569c707c9cb9b87fe3e55b5a27e7fe7f7f27d73c`  
		Last Modified: Tue, 03 Jun 2025 13:37:08 GMT  
		Size: 24.0 MB (24014856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bf0b00f04b5784c02aa34bd5edd104e26e960d8480606e6f206c6a22330235`  
		Last Modified: Tue, 03 Jun 2025 13:37:11 GMT  
		Size: 63.5 MB (63498527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd113c317127acbfc86d7af2a1be3cb7e330fa8c58847cef98b51c46d4e19c94`  
		Last Modified: Tue, 03 Jun 2025 13:43:29 GMT  
		Size: 68.9 MB (68943692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14182d78ce72a37aa9fbd4fe4a033502956e576c76e8aecb7ce69961caf57f90`  
		Last Modified: Thu, 05 Jun 2025 19:28:45 GMT  
		Size: 77.8 MB (77788070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35e08809023e067ed21d9c73579812701663aa785070bc9ca8afd96c5edc9b7`  
		Last Modified: Thu, 05 Jun 2025 19:28:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:latest` - unknown; unknown

```console
$ docker pull golang@sha256:4ecddac6d5267e014615f5fb6218781fa96b3ecc4393835c6667427795e31b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10175041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ef854a13580a721dbecf104d3b200f0d6f9b1cd87bd20fbb3194abf0bc9f2c5`

```dockerfile
```

-	Layers:
	-	`sha256:eedc69155d75dec59459fe2f21ae0616e288f4b3645698534388f1944094912f`  
		Last Modified: Thu, 05 Jun 2025 20:23:36 GMT  
		Size: 10.1 MB (10147396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91d7123113ea32a0f71e49c5043728095415032c0c0b3fa20038baa79bdd3faa`  
		Last Modified: Thu, 05 Jun 2025 20:23:37 GMT  
		Size: 27.6 KB (27645 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:latest` - windows version 10.0.26100.4061; amd64

```console
$ docker pull golang@sha256:117b24d86c9a12c2e228f32450a11fabc09cd61a224142e0574713e27b91b9eb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3564902709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1edf1e06f38e6de7d060219e487cf8c30c3ad49506fa7d9c2ee69f33a268de1f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Thu, 05 Jun 2025 19:32:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Jun 2025 19:32:15 GMT
ENV GIT_VERSION=2.48.1
# Thu, 05 Jun 2025 19:32:16 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Thu, 05 Jun 2025 19:32:18 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Thu, 05 Jun 2025 19:32:19 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Thu, 05 Jun 2025 19:32:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 19:32:36 GMT
ENV GOPATH=C:\go
# Thu, 05 Jun 2025 19:32:43 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 05 Jun 2025 19:32:44 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 19:34:14 GMT
RUN $url = 'https://dl.google.com/go/go1.24.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'b751a1136cb9d8a2e7ebb22c538c4f02c09b98138c7c8bfb78a54a4566c013b1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 19:34:15 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Thu, 15 May 2025 19:25:03 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a3e66d4220d7f9f5a6411899aac3915c770eda10088cd634f6a052cb5a2b5d`  
		Last Modified: Thu, 05 Jun 2025 19:37:45 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc19017373380e9b0b9edf43846b6be8c7dad65f5a508448b0ee09f160f8e132`  
		Last Modified: Thu, 05 Jun 2025 19:37:46 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d185da177b316110f11a8a3c16f1f828ef3a3eeaaa0870d979adfc149ebfd3`  
		Last Modified: Thu, 05 Jun 2025 19:37:46 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1b21ac541d3e07c8779af620cd9e3fab32483297b5e09d8772496b12f60495`  
		Last Modified: Thu, 05 Jun 2025 19:37:47 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3349a08aceebf31d5ae799a8b507ec56bed3a7e208c9542fb7a1d0785f11e21`  
		Last Modified: Thu, 05 Jun 2025 19:37:47 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbab237a913014f164af5990ce988f8061865e78da27bc48bc1e9cc90a35059`  
		Last Modified: Thu, 05 Jun 2025 19:37:52 GMT  
		Size: 51.3 MB (51251143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac191e966ff8d7e70c93e7fe51ade3e5a5b4bae5915faca1e44237a7e1edb92`  
		Last Modified: Thu, 05 Jun 2025 19:37:48 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1992a769adb2f858ea7d6fa40088db7544af925a01135aeaf5496c7539b2e86a`  
		Last Modified: Thu, 05 Jun 2025 19:37:48 GMT  
		Size: 373.1 KB (373118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54167ab553bbda59b7f8bb4d87954ea7c4fb63be4d3798a7fa87bcb259e53de`  
		Last Modified: Thu, 05 Jun 2025 19:37:48 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2956456b63fdf5f4665bb8eb7ec18eafdba410a8bf547d60a25bcb627437b62f`  
		Last Modified: Thu, 05 Jun 2025 19:37:55 GMT  
		Size: 82.5 MB (82502117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a426a9df1e5965ee924710f8182501db217396568f2fee36e8d4e5aa663f200`  
		Last Modified: Thu, 05 Jun 2025 19:37:52 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:latest` - windows version 10.0.20348.3692; amd64

```console
$ docker pull golang@sha256:d63418b9cf7627fc8e93b0db588ac268a66363d1a6d6be59dc884fcdbd8fa5be
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2407426836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9eeb655d8ce27a0b7b924353e44876312efc432ad8a57f1dcd256cce2e30acd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Thu, 05 Jun 2025 19:27:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Jun 2025 19:27:01 GMT
ENV GIT_VERSION=2.48.1
# Thu, 05 Jun 2025 19:27:02 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Thu, 05 Jun 2025 19:27:03 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Thu, 05 Jun 2025 19:27:04 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Thu, 05 Jun 2025 19:28:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 19:28:32 GMT
ENV GOPATH=C:\go
# Thu, 05 Jun 2025 19:28:39 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 05 Jun 2025 19:28:40 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 19:30:57 GMT
RUN $url = 'https://dl.google.com/go/go1.24.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'b751a1136cb9d8a2e7ebb22c538c4f02c09b98138c7c8bfb78a54a4566c013b1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 19:30:58 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f4aadbb8b02245006768330af5ea5b31ea0852a8ad30f1a19d88e3a92f5c64`  
		Last Modified: Thu, 05 Jun 2025 19:31:42 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a28e7282133be00a06c24b4362b9fe3204ad1afc7f9e04d958fc63887164fee`  
		Last Modified: Thu, 05 Jun 2025 19:31:44 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677253b09f334f1855066ca4928950c32fecd2040910ea8ac1cfeeb9ef888033`  
		Last Modified: Thu, 05 Jun 2025 19:31:44 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bcb461d88cbedd160bbc5a00cdabd05399a3674e938fc4fb43ed3a450ac6f9`  
		Last Modified: Thu, 05 Jun 2025 19:31:44 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aeebf9fb7661b6e87b595e8c8060f0e765a9c210cb1e3ea58e04414bd36f40e`  
		Last Modified: Thu, 05 Jun 2025 19:31:49 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14c62b064a5ceb4630a030c3a6feaa7ab3e3e7155a0a6de6797bafcb097242f`  
		Last Modified: Thu, 05 Jun 2025 19:32:14 GMT  
		Size: 51.2 MB (51215597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec7fb67192f40da3304349c4bfa52a0296ab85c5ae9ec01c1e620cbccb2deef`  
		Last Modified: Thu, 05 Jun 2025 19:31:51 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4075bf8480cf36e01ecd44235179e1e98b02cbb888964878948f5299ca503ae`  
		Last Modified: Thu, 05 Jun 2025 19:31:51 GMT  
		Size: 314.4 KB (314374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bbc0f653f5598792e249d3fcd6c5ee0899dbeadb882033ac73f22d60323114`  
		Last Modified: Thu, 05 Jun 2025 19:31:52 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c382c912e8acd86f63da560ccef77570ecd60f4d5a8cbf1c37ff4113a9c8049`  
		Last Modified: Thu, 05 Jun 2025 20:00:41 GMT  
		Size: 82.3 MB (82258319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137f56501bc2ff0db6dd54b894d78751f8c8e21083ad5862964e08b4e4107b77`  
		Last Modified: Thu, 05 Jun 2025 19:31:52 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
