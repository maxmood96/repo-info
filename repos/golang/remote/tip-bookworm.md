## `golang:tip-bookworm`

```console
$ docker pull golang@sha256:a0ef525a067640f8da30f733e8c00dca52d21eaab086214f4331801e3839a98b
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

### `golang:tip-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:297652a8a123de2c908cd65d72c8c19de008b29e33d9c73c316993bad6f25619
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.3 MB (331303301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e0e488fe9c8467b766acc1f1322afa56d20880345e2e33551d5b73c7e8b7e85`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 May 2026 00:20:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 May 2026 00:22:31 GMT
ENV GOTOOLCHAIN=local
# Wed, 27 May 2026 00:22:31 GMT
ENV GOPATH=/go
# Wed, 27 May 2026 00:22:31 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:22:31 GMT
COPY /target/ / # buildkit
# Wed, 27 May 2026 00:22:34 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 27 May 2026 00:22:34 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a234579dfb0d2a4c7e869bc6c39c06f306aa019f90ec3e79f682671badaeb4f3`  
		Last Modified: Wed, 20 May 2026 00:26:20 GMT  
		Size: 64.4 MB (64404451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9f1984cdc40de2fb469b78811b0bd43d661ec906c72954c9d5b27c53c5e5c3`  
		Last Modified: Wed, 27 May 2026 00:23:01 GMT  
		Size: 92.5 MB (92480468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77da848857ba8d560346623b29060265d568e3fd544a353c4d3226bc71f30e13`  
		Last Modified: Wed, 27 May 2026 00:22:37 GMT  
		Size: 101.9 MB (101879418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f0eac8cc50ba5beee3cc5223c4595c6949c2ebfadd430989fd33566a282566`  
		Last Modified: Wed, 27 May 2026 00:22:58 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:3c38914741be2cac3e3187b87232dc0bf1758407ababf5fdb90606ddf3d92477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e169fccc9b6ff277afb4bcf0a588e0159523ad96a1802de393b334a1e06fee9d`

```dockerfile
```

-	Layers:
	-	`sha256:6ce43bc147faad7fe901506d981af175f86f47376131af6cd98f79a2b68c29e2`  
		Last Modified: Wed, 27 May 2026 00:22:59 GMT  
		Size: 10.5 MB (10497055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca9bf34163253c19432c6287657b664703e25cdf278fe39663ffeeb411a9961c`  
		Last Modified: Wed, 27 May 2026 00:22:58 GMT  
		Size: 28.4 KB (28390 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:f113ef378f539866b58de9d9fc09935c4deb32518e6e9b5378e4d3c7431ebe41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289735736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:290ac17fdc50e49ce5ff85a6293be5d905e3768f05997536acb1282668085ce5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:02:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 May 2026 00:18:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 May 2026 00:21:24 GMT
ENV GOTOOLCHAIN=local
# Wed, 27 May 2026 00:21:24 GMT
ENV GOPATH=/go
# Wed, 27 May 2026 00:21:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:21:24 GMT
COPY /target/ / # buildkit
# Wed, 27 May 2026 00:21:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 27 May 2026 00:21:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1af0b8b84389f4347663cc563bc1f6d59fe6d6f21081f428bafa1a09f6a276ce`  
		Last Modified: Tue, 19 May 2026 22:35:59 GMT  
		Size: 44.2 MB (44209154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61246c0a5a0fe9fe8cdc1bfde0fdfa49ffafcc94cba31f4aecc0c34bc346064`  
		Last Modified: Wed, 20 May 2026 00:02:11 GMT  
		Size: 22.0 MB (21950133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56a54e4354794da97ac9fe5173f689d775d13afa792e8b390e49425c3caa6b5`  
		Last Modified: Wed, 20 May 2026 01:34:11 GMT  
		Size: 59.7 MB (59661818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c931a2682b0f37983f2159c0c52fc9d29cd2a05d5274f2c7fb880a609165ac`  
		Last Modified: Wed, 27 May 2026 00:21:52 GMT  
		Size: 66.3 MB (66339668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10970b698e6007676a0ddc85a9b7bd9dc803ec199aba70539ca19e2e26b490dc`  
		Last Modified: Wed, 27 May 2026 00:21:38 GMT  
		Size: 97.6 MB (97574805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b82ecbf6026e570821f9155558cc8b5f786b8c0756ec55f37c8c6de58c8e870`  
		Last Modified: Wed, 27 May 2026 00:21:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:e8f9aab0ed53e0ca199b0ee0c350a09e639c1628c56e6f4578ef7ca51694ade5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da8ee23b77a57df5fd708a73aae8811d1be9e6c11450337e923efb343f8b2b8`

```dockerfile
```

-	Layers:
	-	`sha256:ccf1709b6e28b376e9c8a52ddcffd1cdddc18c2282d3700374fcbae29c6f269a`  
		Last Modified: Wed, 27 May 2026 00:21:51 GMT  
		Size: 10.3 MB (10303751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd0d321af40f262196ef367cc16e0c878090ccdb5fe92174e4487849ebe0e9d9`  
		Last Modified: Wed, 27 May 2026 00:21:50 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:4f1304e915085d70ef19aa8261320e5aed1162b29cd76eae201faba0d9692ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.3 MB (319348970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f84036bce33823e6e17ac33f2856c16f97d75feed40ad56aba59f9ac7b5846a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 May 2026 00:19:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 May 2026 00:21:25 GMT
ENV GOTOOLCHAIN=local
# Wed, 27 May 2026 00:21:25 GMT
ENV GOPATH=/go
# Wed, 27 May 2026 00:21:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:21:25 GMT
COPY /target/ / # buildkit
# Wed, 27 May 2026 00:21:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 27 May 2026 00:21:28 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daebbc198bd7b84bdd72840d7f4ded251896f03b9a9f880894e95e926bc543`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 23.6 MB (23613394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c669ec0346d48159cb837d6257098593cd53e61de677d9c0426474d36e1c5e`  
		Last Modified: Wed, 20 May 2026 00:27:16 GMT  
		Size: 64.5 MB (64487655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b6de3adfd4d391377e655d37a6e5a925943cbb42536a6df24f79eca3334ad2`  
		Last Modified: Wed, 27 May 2026 00:21:53 GMT  
		Size: 86.6 MB (86553766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb11297bd411607a8b57c42b1e75c7973dc6c61df122e261576bba30bd7fe3ac`  
		Last Modified: Wed, 27 May 2026 00:21:40 GMT  
		Size: 96.3 MB (96314565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fecfbe17845846de683446af061d43073bdd58dba2ef4be3bb014c887e0d4086`  
		Last Modified: Wed, 27 May 2026 00:21:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:d652be245457fafd843473210c4a7679d8a6a711cdeb8e04d709fe0547b0c879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46b589cad9cb3fdcb04ed3ee874b34a692e7dab597b1746998bf9fbb6fd9ae4f`

```dockerfile
```

-	Layers:
	-	`sha256:b3bbde42f90a66134059a168a934a31666eccce27694df1dab5f5f096b88bacc`  
		Last Modified: Wed, 27 May 2026 00:21:51 GMT  
		Size: 10.5 MB (10524879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf41af0e59de7746e3801d52342fbe6ff3cb8116c68ab34a510ca15a76e7810e`  
		Last Modified: Wed, 27 May 2026 00:21:51 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; 386

```console
$ docker pull golang@sha256:247a8883910f40beec3ded2c1077bec448a3f4ff13466b12118825e0102325d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.1 MB (330113964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada15788bcfd51f0920f1060c65dfb9ed97fa212c00cad53d6577bee8185cb34`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:24:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:44:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 May 2026 00:24:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 May 2026 00:23:12 GMT
ENV GOTOOLCHAIN=local
# Wed, 27 May 2026 00:23:12 GMT
ENV GOPATH=/go
# Wed, 27 May 2026 00:23:12 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:23:12 GMT
COPY /target/ / # buildkit
# Wed, 27 May 2026 00:26:32 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 27 May 2026 00:26:33 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8bf11fb6e89cfb8d682f511fb7d1b795e747af9c12a192f45f6e50ae7ca54f50`  
		Last Modified: Tue, 19 May 2026 22:36:20 GMT  
		Size: 49.5 MB (49483120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db105b3a1c2456422c428304ae93436fac4214751cb65053af119fa6d81d85dd`  
		Last Modified: Tue, 19 May 2026 23:24:59 GMT  
		Size: 24.9 MB (24879482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e2a05321daf588afd8b06b380f7ea0a3d7c0de2097ec6f355a74453e7ec6af`  
		Last Modified: Wed, 20 May 2026 02:45:13 GMT  
		Size: 66.2 MB (66243865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ef2dbae9572e55252f550bb2d79de8738ea472691ac055ca4f33c0cca62345`  
		Last Modified: Wed, 27 May 2026 00:26:58 GMT  
		Size: 89.9 MB (89903261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849d403214e905076ef37eb9bf9b81fdb084f9e69d1847d3cf7505e9a15c9cfa`  
		Last Modified: Wed, 27 May 2026 00:23:45 GMT  
		Size: 99.6 MB (99604078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800bef6ec7152e32eebd5ed1a4efa425d4f251e8d52ac7791dea0d52f8eed85e`  
		Last Modified: Wed, 27 May 2026 00:26:55 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:3ebd5d6d74a0a0335ddb246cb91c5621d5f110d1bba979528be772c0f2d879ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a1f804048aa58903415c1e184342f0ac34c5a7d358ce8c37df3283043cd5c5`

```dockerfile
```

-	Layers:
	-	`sha256:b78c0290c639ea5adbbaa64b325543c58c0a7f1ba213eba91900e42dbc379e4d`  
		Last Modified: Wed, 27 May 2026 00:26:56 GMT  
		Size: 10.5 MB (10476635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f465c9cd0cc889468f1bbfb36182ad91e535633325c507648791b47161623a9f`  
		Last Modified: Wed, 27 May 2026 00:26:55 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:6d9b06757c30520f30250c2bf65e9c8084bca38e1c42459e4dcc10a0fb1cfac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.1 MB (301077345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:705556e83342cbedeab265ee3e5da6c9ac0b31c10f1d782af9138cc4bf2aafb6`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 10:04:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 15:11:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 16:19:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 May 2026 00:43:20 GMT
ENV GOTOOLCHAIN=local
# Wed, 27 May 2026 00:43:20 GMT
ENV GOPATH=/go
# Wed, 27 May 2026 00:43:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:43:20 GMT
COPY /target/ / # buildkit
# Wed, 27 May 2026 00:43:37 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 27 May 2026 00:43:38 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:813eaff938e8991b3dd16851af2c46dd2ffc5bb600e30ff866dd5a60502fbffa`  
		Last Modified: Tue, 19 May 2026 22:35:13 GMT  
		Size: 48.8 MB (48786239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2853b2ecd2cc91271c3528597da43fc45c41515894834d1de212a390afbf0ade`  
		Last Modified: Wed, 20 May 2026 10:05:32 GMT  
		Size: 23.6 MB (23621201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71bf4bd887b67ee95b1804bd893717310da36bddd5a598cce7e9b621ff52ee05`  
		Last Modified: Wed, 20 May 2026 15:12:43 GMT  
		Size: 63.3 MB (63316337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d8edfd178bcf28b946d64eb3ad538d4ee96dacac854fd44ba3af295e68b368`  
		Last Modified: Wed, 20 May 2026 16:21:18 GMT  
		Size: 70.1 MB (70084514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7cee96e764c402d0ab7ef57746ebdba9de153d8787ebb6701ac8df7bdd4fd8`  
		Last Modified: Wed, 27 May 2026 00:45:40 GMT  
		Size: 95.3 MB (95268896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4181a8d6dbeedd4e92eaaf2bf9fe02cd5be97f107c8f8a775072bd11724569a0`  
		Last Modified: Wed, 27 May 2026 00:45:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:0a5b0a182a9992160ca1ca5a2809f3bec587f7b6d2c8078c2a98e282ee5f2bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 KB (28240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3643e7c835d4d8679fe29bff3cbacb0422c100806444d2362c9f3b889b0ddd`

```dockerfile
```

-	Layers:
	-	`sha256:34b2f1e41cc093f5be6cbd67e0138656556e60fa12390d5fea9d74c7e0539530`  
		Last Modified: Wed, 27 May 2026 00:45:31 GMT  
		Size: 28.2 KB (28240 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:c850fe37433167078174d1402993b55ead570559a9f99a8a755c38353323e583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.6 MB (336619495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd83b1cb9a7adf5ef0825078203d36d2aff52a235f2bfdd51b7d0bfac42222c9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:13:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 06:50:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 09:12:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 May 2026 00:33:54 GMT
ENV GOTOOLCHAIN=local
# Wed, 27 May 2026 00:33:54 GMT
ENV GOPATH=/go
# Wed, 27 May 2026 00:33:54 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:33:54 GMT
COPY /target/ / # buildkit
# Wed, 27 May 2026 00:33:59 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 27 May 2026 00:34:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f46c910cb3dd366a8b080c77b15459d7465da54412b3570454cddcaf0cdf40`  
		Last Modified: Wed, 20 May 2026 01:13:39 GMT  
		Size: 25.7 MB (25686466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67cb71cd5984ee53ab56bef57a29d3b0ef6e8939c352146b1efe66402d4c7ff`  
		Last Modified: Wed, 20 May 2026 06:51:27 GMT  
		Size: 69.9 MB (69853485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bae1f9f6144fca8edf5d9d7cc5bb0fe155a272843049769232560831cade6a9`  
		Last Modified: Wed, 20 May 2026 09:13:22 GMT  
		Size: 90.5 MB (90495115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5d83b0a2acae5776f1d36a1951e6d604ad7e905260707ce03d30294ae6c508`  
		Last Modified: Wed, 27 May 2026 00:34:56 GMT  
		Size: 98.2 MB (98244071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed399457ffacb972e9b13c8577c87822007be9eed2b467388e8a2a757b03173`  
		Last Modified: Wed, 27 May 2026 00:34:53 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:f94c7c72fc8e540c474490305cdbe30bc20be15c15a1895cd31ae58ef561cf6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee85baae8fe23211d65bd0469b40d039fa422ccdf6e62230420f35ea18b208d`

```dockerfile
```

-	Layers:
	-	`sha256:975615db76bd6fc281f456ce7e6a32387e3844da08d1492e2acd9abb8c28f159`  
		Last Modified: Wed, 27 May 2026 00:34:54 GMT  
		Size: 10.5 MB (10469540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bda1be5f3e7ad312bc4ca3041fa25ee2c7d53190c1d377465ceefe41839e7b82`  
		Last Modified: Wed, 27 May 2026 00:34:53 GMT  
		Size: 28.4 KB (28432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:78206f48ab74f089a271a055142f08aab7328f0c198e6c4a33dedf8edc996ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304074179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:864fe85272729f646dfacda251f577ff51b06eb476bfcc7766700609677f4856`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:17:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:05:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:46:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 May 2026 00:27:22 GMT
ENV GOTOOLCHAIN=local
# Wed, 27 May 2026 00:27:22 GMT
ENV GOPATH=/go
# Wed, 27 May 2026 00:27:22 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 May 2026 00:27:22 GMT
COPY /target/ / # buildkit
# Wed, 27 May 2026 00:27:30 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Wed, 27 May 2026 00:27:31 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e0fc2c7a6bb12f7a9b333cc117b6ea5fa5cf251c5fa4dd298303beee01028f59`  
		Last Modified: Tue, 19 May 2026 22:35:39 GMT  
		Size: 47.2 MB (47155589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79feab17202415ba0b431eca0e903b1c895e662e755c4c9f1b5678ad8eb605f`  
		Last Modified: Wed, 20 May 2026 00:18:12 GMT  
		Size: 24.0 MB (24039201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511ade0407a6db3c4a6853a735563e5fb22577aaaa32942a9458cc0c09942583`  
		Last Modified: Wed, 20 May 2026 02:05:37 GMT  
		Size: 63.5 MB (63498321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d6ff3d818fd97aacd81ce6295e3d8da60684c2af3275bbdd42cc1809ea7991`  
		Last Modified: Wed, 20 May 2026 02:46:53 GMT  
		Size: 69.1 MB (69087355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def8ca56de94c50983811539154fa57356ce10e9aa7caf4558fbf0aca8e494c9`  
		Last Modified: Wed, 27 May 2026 00:28:25 GMT  
		Size: 100.3 MB (100293557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91adcf5b602225959ebc0d88e8b313b49caa41d298d6e5053172c2ed6b6343c6`  
		Last Modified: Wed, 27 May 2026 00:28:31 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:f626cd851961ece89b43e41582adfbcaffdc11a8255e47abdb1828e626fe5ce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881482bd27a5ec8dbe80e9696f411e00dd89468e9af29528ff065286252ef7bb`

```dockerfile
```

-	Layers:
	-	`sha256:b550aaac0ea3dcfd0a8b5da0c3bde28baeb9b5ac3f38164a4a77aa4536079630`  
		Last Modified: Wed, 27 May 2026 00:28:32 GMT  
		Size: 10.3 MB (10329561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29f513b30bd42833b0d203a02f4a585bd46d0d76c76fa2e0e83c2a63790e75fa`  
		Last Modified: Wed, 27 May 2026 00:28:31 GMT  
		Size: 28.4 KB (28390 bytes)  
		MIME: application/vnd.in-toto+json
