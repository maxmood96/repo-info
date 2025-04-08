## `golang:bullseye`

```console
$ docker pull golang@sha256:663c61bf69e9f78c6710e41a641326dadd1a85502878c7854c5de318c4a5b466
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

### `golang:bullseye` - linux; amd64

```console
$ docker pull golang@sha256:4004bd72c4be1d0f54edd901382d0430fc0e34bab7c7f2f23ae1b89858e4f8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289210330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec3a52fb42afd9c3281f85b7a91c0a590c1f6d3a86d7243817d6b094ba21133`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a7819131060d3c79e48555fb5b04fa584b86d2fb80e3ede0864c7e6bba7d87`  
		Last Modified: Tue, 08 Apr 2025 01:24:24 GMT  
		Size: 15.8 MB (15763510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0f843b455b9b7bececb5cfeb4ba5839d4aa47845ded1258734c375304df3d0`  
		Last Modified: Tue, 08 Apr 2025 02:13:52 GMT  
		Size: 54.8 MB (54755152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c278869e67bd29bc2b7ea425f1e1cb108a94e8c3773916f617c6379f9714e50`  
		Last Modified: Tue, 08 Apr 2025 03:16:27 GMT  
		Size: 86.0 MB (86000763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d296901bdc593d88a0813bb00eef0974b68222cba6add046b831c086a1c68c`  
		Last Modified: Tue, 01 Apr 2025 17:07:26 GMT  
		Size: 78.9 MB (78942217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6de0c6a090010958dcf78ff31774fad23fcc4b7e15d5116fb924eb8111cc3f3`  
		Last Modified: Tue, 08 Apr 2025 03:16:26 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:7ee3ce6955bf3ea7786fa867d3c54f1767f7d7e7758b0b2a67b7f5e0e1fd2f60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10291890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b852a55dae039e710864ce42e55e0627a9c046902a79c06f10a399362e552c3`

```dockerfile
```

-	Layers:
	-	`sha256:2706546c163586c03c08b6d0c47892845cebbc85238bcd03734da5a08db5af5f`  
		Last Modified: Tue, 08 Apr 2025 03:16:26 GMT  
		Size: 10.3 MB (10265423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9af5f5900972881b73aaef4755d80e29ec03eb2f741e6c179599883368a5b4c8`  
		Last Modified: Tue, 08 Apr 2025 03:16:26 GMT  
		Size: 26.5 KB (26467 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:7830b73ba96b5704621ba7998a795cf880bae36b3a46c81006663e5fd05b4c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.4 MB (256365055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:740cc8b9b4f9f30b3a6152529df72f1e1011eea63c1ab32a2600b78aaf450fcd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1742169600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:c0fd1793bf8bc1764ff6503ad6f86ae0f1151de2bd8b7285b28dc6f5cc6001c3`  
		Last Modified: Mon, 17 Mar 2025 22:19:04 GMT  
		Size: 49.0 MB (49026561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fd5d78189f9a0219a8d445519fe59067dcfa82b8799cf047c0b783ffa33a78`  
		Last Modified: Tue, 18 Mar 2025 07:26:06 GMT  
		Size: 14.7 MB (14674012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31183489ce2b77443c42eee08badb4a4fcf8ad4cef9299e71603f2239cb4064`  
		Last Modified: Tue, 18 Mar 2025 15:29:13 GMT  
		Size: 50.6 MB (50640225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0192ce451b4bc1458959a86a1dd55f46cf5148c4d3e016589a215f847b4e66ae`  
		Last Modified: Tue, 18 Mar 2025 16:49:06 GMT  
		Size: 64.9 MB (64922890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9003e8a4d55742a1a2128c3dabddda68ec2c585f52d2aac5eaee8bd68089640`  
		Last Modified: Tue, 01 Apr 2025 17:07:37 GMT  
		Size: 77.1 MB (77101211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a808b38cff5495c1b3614a6c03b2fa95da3624cb272af6ffe48f832fe121793a`  
		Last Modified: Tue, 01 Apr 2025 17:08:29 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:df4ce0baa46a83aaead67c55cea39b34e8dc511c06eb33de7a376b9c2cc08a1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10096439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21cf391077d817a5ed580faa5434d944bdef84543b7ecdb82f9c73d20775e310`

```dockerfile
```

-	Layers:
	-	`sha256:dcb4659b39c023c74571decf849e77ca3ef5464fd9f859e0cdbe134d92ff2b25`  
		Last Modified: Tue, 01 Apr 2025 17:08:30 GMT  
		Size: 10.1 MB (10069869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:664e1b7dfc65d513f61bc451e7723188b38102ddd4ac0c79fe2a292dec8f7b56`  
		Last Modified: Tue, 01 Apr 2025 17:08:29 GMT  
		Size: 26.6 KB (26570 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:762ff38a7cc50f345d00d5acea02dc737e636f8fadaedbc4ab64d6b52b332274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.5 MB (279467457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae37a33f506c577dd8abd80d8d2a5a72400377eeabf882eb8adaa2a99468d65`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9322dad1d7c942b6794e486e4e0b838c10dfb06247f1794d20cc703ddfee969f`  
		Last Modified: Tue, 08 Apr 2025 06:03:40 GMT  
		Size: 15.7 MB (15749086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebaef8f9f6ff21c71a0e336a0e9a00fbb65d469480593ef8d1ef507941e6f6d`  
		Last Modified: Tue, 08 Apr 2025 12:18:43 GMT  
		Size: 54.9 MB (54850009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27ffa7089c7997362d7d2d391d3249f29fc8431e52166ced49625eb7e5ff974`  
		Last Modified: Tue, 08 Apr 2025 16:00:04 GMT  
		Size: 81.4 MB (81413774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a002eda2038f0953467f843586445333b2af3e827e57b15849040931f2903fb4`  
		Last Modified: Tue, 01 Apr 2025 17:07:27 GMT  
		Size: 75.2 MB (75200208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf55ebb982db6ff9bd27c424b9aeefb8b4741ffcfc61ce94956edbf901720a3`  
		Last Modified: Tue, 08 Apr 2025 16:00:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:bb3b96dc726bc3b5259180c3b8ce975e559d25f663727af47fa6297ccf950518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10293621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168222c09dc2d147fbcefcce80f9da9e17f043e5ba4f6a421d3a43069b3e897a`

```dockerfile
```

-	Layers:
	-	`sha256:434359bc7842a191b79c9f0c8089bd1a64dfc12ddc3f2e3729e532183b225f19`  
		Last Modified: Tue, 08 Apr 2025 16:00:02 GMT  
		Size: 10.3 MB (10267019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac59fb37bb08b110b0c25929b754d361a9f9674aa1fb9d24aadc3630646bea74`  
		Last Modified: Tue, 08 Apr 2025 16:00:02 GMT  
		Size: 26.6 KB (26602 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:bullseye` - linux; 386

```console
$ docker pull golang@sha256:ba697b95b1e857eec72945dd33aa3fdeaf9dcba48001200e6325a79a35b5d39f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.3 MB (291298798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e9a02af52647f98fc2f3780fb36b03abfde618ed233ed987258e036f87f7b9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:0606c6e417e3f273e94fb33ac515dc5e3bacfec2558aa1e3ab7b9413dd31655c`  
		Last Modified: Tue, 08 Apr 2025 00:23:00 GMT  
		Size: 54.7 MB (54684465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ffef4e17cbc252fc170472ff3910647beec8b91ac9abe188d6595b2087a0dc`  
		Last Modified: Tue, 08 Apr 2025 01:24:12 GMT  
		Size: 16.3 MB (16267037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684d7ac3a47d27aefe42d135394e4d8b703fb530ab3bd2ad6ef78b8c9beaf885`  
		Last Modified: Tue, 08 Apr 2025 02:13:59 GMT  
		Size: 56.0 MB (56047217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef496c80d4833c19f81234f2f53b96b6f7a5b54c3c3fa8b2d22db75e88109c35`  
		Last Modified: Tue, 08 Apr 2025 03:16:48 GMT  
		Size: 87.4 MB (87426507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb556227a38cd463b29410ff393a23b771d304e2f2f265b6c233fe487c9ca9ff`  
		Last Modified: Tue, 01 Apr 2025 17:07:28 GMT  
		Size: 76.9 MB (76873414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad285d9f309f7f2e0f4390f7a5f629cb267f98d563385886db71449a1ade988`  
		Last Modified: Tue, 08 Apr 2025 03:16:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:d54a5e8d7a5f40d928ca93e15b2d02bbf8123f52abb43d455c03e21d0c8274be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10281640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b372fbb8706229714e429a043575c4f01471fe36629ec7bc5d8e1cb76a8e4d4c`

```dockerfile
```

-	Layers:
	-	`sha256:74018a58d4f410fe178ea6e6ceb901d619f4493e0a3e325f334fcaed1d150b65`  
		Last Modified: Tue, 08 Apr 2025 03:16:44 GMT  
		Size: 10.3 MB (10255208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce864839b6a7106af06d3947f8c56ac733990a070dbf2c7460490d21c4529823`  
		Last Modified: Tue, 08 Apr 2025 03:16:43 GMT  
		Size: 26.4 KB (26432 bytes)  
		MIME: application/vnd.in-toto+json
