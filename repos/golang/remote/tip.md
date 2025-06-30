## `golang:tip`

```console
$ docker pull golang@sha256:860e664cacb00fcdf3d2915adbed2a8fb5db950ab222379c915525cf1a3f934d
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
$ docker pull golang@sha256:98d031bbd558b7c14ac3ff40aef6b425f6b055f5d16f59d68327d43a84137165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.3 MB (312349953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ef14b0fe29a961185f7f800b1bac7bcee873464d95258105b7a1c6ae790fe5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 30 Jun 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1eb73e993990490aa137c00e60ff4ca9d1715bafb8e888dbb0986275edb13f`  
		Last Modified: Wed, 11 Jun 2025 00:01:09 GMT  
		Size: 24.0 MB (24015708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b8a0660a31403a35d70b276c3c86b1200b8683e83cd77a92ec98744017684a`  
		Last Modified: Wed, 11 Jun 2025 00:02:18 GMT  
		Size: 64.4 MB (64399794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadd39e1969c3fbea8ef3eadcb67ad3ea50606f13f4ca8d697a624b256a0742b`  
		Last Modified: Mon, 30 Jun 2025 17:31:07 GMT  
		Size: 92.4 MB (92354966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d8f8c49f445d30fa7cd4c028a18d5365e5bdfe97436ef61eb7709425c99cad`  
		Last Modified: Mon, 30 Jun 2025 17:30:36 GMT  
		Size: 83.1 MB (83085055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040b71e16e6da809c4a165379d01caaa4d9ad2c05e963d9c70f46d3eab41d74e`  
		Last Modified: Mon, 30 Jun 2025 17:30:54 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:9203eab042976f9a4f7695c0fb65c1952987656eeb6f78ceba4cbd1de2ab3de1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10515047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06e825ca6ab3421a0a2a6e8e6ae63ddbae5a5a9dbe8c0db3509f4da58707dbbe`

```dockerfile
```

-	Layers:
	-	`sha256:415563599e2be4ce4c364610380d7d9bf981b091404b8df867c4579a31c76c5d`  
		Last Modified: Mon, 30 Jun 2025 20:23:56 GMT  
		Size: 10.5 MB (10487389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c02cab769afa82bf3afb429d84f78b7cbe701c9098dd5e1f6cc4a799b7487a`  
		Last Modified: Mon, 30 Jun 2025 20:23:57 GMT  
		Size: 27.7 KB (27658 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm variant v7

```console
$ docker pull golang@sha256:05b197c810639636e83d94bad85c75b3821b263201c004661cdd18817f0d2b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272161678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10952d6e2b3deb6b04214a922eb1ac7c710638fee92d6e8daa1ba5ef4105aa03`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 30 Jun 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:df7fd9070ca37866fcc3543148432e42d1e1723497b9b47c1e35615a2ca676ec`  
		Last Modified: Tue, 10 Jun 2025 22:46:46 GMT  
		Size: 44.2 MB (44208210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7ffa2f9b76643f2e264873b25d4450552d1d018f96ebfda08d41449ffa7dad`  
		Last Modified: Wed, 11 Jun 2025 06:07:15 GMT  
		Size: 21.9 MB (21924642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe8855ed7a68d9f8fe7d302fae88c166a75915bfbd2d109d79128b51764e3ec`  
		Last Modified: Wed, 11 Jun 2025 13:11:47 GMT  
		Size: 59.7 MB (59656919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b0a248bc7fbf888bccbf6729078aec3b1f376d1d95c8ee77854eaa13fe0986`  
		Last Modified: Wed, 11 Jun 2025 18:27:12 GMT  
		Size: 66.2 MB (66208380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6586f6a3b72edca5355ba2231baded357cf799f55b8944edc8ae75b0c7b67acf`  
		Last Modified: Mon, 30 Jun 2025 17:31:46 GMT  
		Size: 80.2 MB (80163369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338ac6df1d23b684cda5d56ae4db81602f850a271ef7637e49ffc0c19b8764f9`  
		Last Modified: Mon, 30 Jun 2025 17:31:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:67ad50b13fc71d798faa1b7d9c03d4cb24385b2d43d070f5dae744c89cc66513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10321886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f259e7bbf4f3e48097884acb056c2ebb0bd27907c9abb43b05a096fb20bf0c0`

```dockerfile
```

-	Layers:
	-	`sha256:50ffcca7b570220c58734a0cf57fa001d110f6f6c97f9ff02a06e94904d55009`  
		Last Modified: Mon, 30 Jun 2025 20:24:06 GMT  
		Size: 10.3 MB (10294103 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ef21ee5ddf7dad8aa470fbff7deed36fcca59da8d14aa4438c8f2660aa8e0f4`  
		Last Modified: Mon, 30 Jun 2025 20:24:07 GMT  
		Size: 27.8 KB (27783 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:913eb64f1ad3974fcd90dd8a0eb7ac16dd6bc46928fd0ab4b6f5631af8a72117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.7 MB (301736543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a76bc805b37b95a2c038105fb38700faf9c4bda10e2f18363d56bcc2b05d147`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 30 Jun 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e137b9ec173f900a44376f31987bb15c0f5bb562aa6f8ad5db5a090ec88b2e`  
		Last Modified: Wed, 11 Jun 2025 02:56:23 GMT  
		Size: 23.6 MB (23551557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f5719d6358cc525f45e16c04ce36e5245978df9021dec8d0619729d9de8537`  
		Last Modified: Wed, 11 Jun 2025 10:32:40 GMT  
		Size: 64.4 MB (64362852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399a17febfc3c309501dc6427821a98f0a207b994da4369bc17d53bfee0ec1e7`  
		Last Modified: Wed, 11 Jun 2025 23:08:08 GMT  
		Size: 86.4 MB (86425354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f0e5c856fb20135c901f955406b40129ab946b3615cd5e0d5839e969930423`  
		Last Modified: Mon, 30 Jun 2025 17:34:31 GMT  
		Size: 79.1 MB (79057770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa7ae73b1571a3c9e89d3c8f013d261e1a8e4bd4b7d6e54062017e2f991bab0`  
		Last Modified: Mon, 30 Jun 2025 17:34:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:0acbf1afd18a5ffcc426db8e7a3102845757c0472a94a8808359179c6c7c36ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10543054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d1dc4b36ae7e870449a70c18d5110ee1cf7e48e0030f40f80a5397cbfd158a`

```dockerfile
```

-	Layers:
	-	`sha256:d95cf68c3de8cd1580dce87b0ff3069a95b731f1b286dfe0a114e644777a695e`  
		Last Modified: Mon, 30 Jun 2025 20:24:14 GMT  
		Size: 10.5 MB (10515237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b8de2816276074e6e117b46bcc225fde34442f2f114668607d751480894cb90`  
		Last Modified: Mon, 30 Jun 2025 20:24:15 GMT  
		Size: 27.8 KB (27817 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; 386

```console
$ docker pull golang@sha256:3b937881d1909603ec5bcd48ea4c48d117a903351fe84f4d83b1057cd15cb534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312143332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c4477661064fdd315e965b5b31c515de229dfe3e10ce0902d4f3ae6a085737`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 30 Jun 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:50aa93171dc54d5887d119d6829bb0958ed27d02f138b34d7976c569b66f68b7`  
		Last Modified: Tue, 10 Jun 2025 23:24:01 GMT  
		Size: 49.5 MB (49477474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7731d58cf259468f5a31e00d6a586bde147720039c92e6c1ff4cb48a5dd996ae`  
		Last Modified: Wed, 11 Jun 2025 00:00:38 GMT  
		Size: 24.9 MB (24855706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce073e7b00b22009464483e266ff8ba48a8c0db86f16c877aa302337bbed6e9`  
		Last Modified: Wed, 11 Jun 2025 01:13:32 GMT  
		Size: 66.2 MB (66225240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928706b226cfe60760568848844fe360f9d933eeaff076d8ef6e4e47c314b853`  
		Last Modified: Mon, 30 Jun 2025 17:31:19 GMT  
		Size: 89.8 MB (89774613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb2781a7c01ceed520d1e8478386c7e0683cbeab9ca6a32207c24229a367897`  
		Last Modified: Mon, 30 Jun 2025 17:31:11 GMT  
		Size: 81.8 MB (81810142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca0375fe01e8183983db8a00867f8915740472f3adedd5f6f3e1d34d55771360`  
		Last Modified: Mon, 30 Jun 2025 17:31:12 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:96e02c83850aa6748d53a367ab0c3c2b3c49ff224ef9e587d7dba2b3564ed50e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10494583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a78ec6e71e25d690477ae36478d1eca45a29a90b0b6b42bf053d2d3facf21ddf`

```dockerfile
```

-	Layers:
	-	`sha256:befab0796f508029970a4b6c762feb77d579f6fd23c0d7457822823334bcb3de`  
		Last Modified: Mon, 30 Jun 2025 20:24:23 GMT  
		Size: 10.5 MB (10466967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5174e209c3e4a0cb1250d6cac039ab4f7661deb1371ff3c52463d7852e686661`  
		Last Modified: Mon, 30 Jun 2025 20:24:24 GMT  
		Size: 27.6 KB (27616 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; mips64le

```console
$ docker pull golang@sha256:443a8904b2e3e3531c585b02d2d4c77be78160c1760565c3bb7e95b91383a347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283441108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc2111ce3dece0c18ab7fb704b938060d0aea88f22fc6a17220779544d2cc1f1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 30 Jun 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:348f1ed415b5b1e1f9982a78ffeb15637cbc5b41f93b83724c5938c2c226a58a`  
		Last Modified: Tue, 10 Jun 2025 22:47:59 GMT  
		Size: 48.8 MB (48775597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ad14aceadbd8dec6fff454480e4e098f48c504f528663aa483f102aed68047`  
		Last Modified: Wed, 11 Jun 2025 13:00:39 GMT  
		Size: 23.6 MB (23598558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1117c8734bd4897d340d37aa929ac7b2c46b5a9f691f51a958aabc871f6639b1`  
		Last Modified: Wed, 11 Jun 2025 21:03:24 GMT  
		Size: 63.3 MB (63308749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8492b77d6bf957cded76e087bd45cb2dc99a21e61d8bf5a9dc72814542a2ff45`  
		Last Modified: Thu, 12 Jun 2025 08:23:42 GMT  
		Size: 69.9 MB (69945632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d93da9c44ad0cf5204fa695dbbb19af7842d91e70bc8e38610b3cca4f51ff75`  
		Last Modified: Mon, 30 Jun 2025 17:56:24 GMT  
		Size: 77.8 MB (77812415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1507d7eb57d50b3e84d7d8d884b473f49ed7a1cb2c1f0dadcca21295ffb2e8c9`  
		Last Modified: Mon, 30 Jun 2025 17:56:15 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:9506d612f2d1e4ffb1627fd23437a04a4ea593582a4e2a07b06e8c401a39b87a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c417adeecf8d2d15c76e924baf64f173658fc1357ece72df87eeaa00b86c76a`

```dockerfile
```

-	Layers:
	-	`sha256:22188f1d9cc63dc8901ce67f40b066dcab18a52dc09b8d7fb61d2be3cf9c50d4`  
		Last Modified: Mon, 30 Jun 2025 20:24:30 GMT  
		Size: 27.5 KB (27531 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; ppc64le

```console
$ docker pull golang@sha256:b1db25e151e9a9b478703c939da46b5a8f107ed9d34f3fe3eb8fd8ab6c382850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.6 MB (318554846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7432d66ab8d3779d9e1979c050d311044a28a6b1a675ee820dc68edab1c0e02`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 30 Jun 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:65d348c3abfb8493d4b77022d58f0afc8e2daa19b2af853f803aef5c836212f9`  
		Last Modified: Tue, 10 Jun 2025 23:28:11 GMT  
		Size: 52.3 MB (52337357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bcd3217ebdd78ee7f5f6a67c7b4b49ee252ec2305007272d04d562f9e83004`  
		Last Modified: Wed, 11 Jun 2025 17:40:53 GMT  
		Size: 25.7 MB (25657425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f5e3e648b0af066a27f67ff1ab192ecc1e665ef5dd174521d0a856b9bff018`  
		Last Modified: Wed, 11 Jun 2025 22:39:56 GMT  
		Size: 69.8 MB (69839696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef04a97584b773cb2e3f5ef36cf5fd266e7a5329383a4acadeef6edef21349bf`  
		Last Modified: Wed, 11 Jun 2025 23:31:25 GMT  
		Size: 90.4 MB (90369172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90415633da1367f6a55f0b20986162d53698245a02ffb8afb2ac26988cca44e`  
		Last Modified: Mon, 30 Jun 2025 17:31:50 GMT  
		Size: 80.4 MB (80351038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db53a85ee12f80b15b0be43515ddd328030c56eec08d3a8edc27419c785c319f`  
		Last Modified: Mon, 30 Jun 2025 17:31:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:a19e1e440da571d1df33f1c2399555a3bea8812b6858fcdb93479d1f8f22c32a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10487589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bddf85be01be04754e32cb43e18c674f43a71e087185f9d627ce45d8a7a44b54`

```dockerfile
```

-	Layers:
	-	`sha256:99d02b92a9d9845e747aa835af16f981edd8250937136aedbbd11641e1131e84`  
		Last Modified: Mon, 30 Jun 2025 20:24:35 GMT  
		Size: 10.5 MB (10459872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f141d16ea946a9ccac4293c8bf3bf48602c3192568a490d96555a1f20ebf1eb1`  
		Last Modified: Mon, 30 Jun 2025 20:24:36 GMT  
		Size: 27.7 KB (27717 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip` - linux; s390x

```console
$ docker pull golang@sha256:432e616d209cdacf6e02a4dfbc0e05dbbb1557f7eff16a1f4cb85d7c69d27b41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285215584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af38cf2fee97669e80ab0f52028a8c8df71c30c3d662802c8d326b9a547b52eb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Jun 2025 05:23:23 GMT
ENV GOPATH=/go
# Mon, 30 Jun 2025 05:23:23 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Jun 2025 05:23:23 GMT
COPY /target/ / # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Jun 2025 05:23:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:92d876c60c42d9677caf30587cba2266fe6860ddc50efdd0a6fcec154e589f76`  
		Last Modified: Tue, 10 Jun 2025 22:48:13 GMT  
		Size: 47.1 MB (47149408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83030d8a694f635685bec1602230ad1d5fec4773d5158ddbd025887cae3655fe`  
		Last Modified: Wed, 11 Jun 2025 10:15:26 GMT  
		Size: 24.0 MB (24015002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c056714c54676358218cd75dc0c5d3298e3c0e7e53c127fdefd363c4380d95`  
		Last Modified: Wed, 11 Jun 2025 12:03:11 GMT  
		Size: 63.5 MB (63498247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d972cf1551f655df3a01c76dc6db428d58e500c24a29c3c7b92136f0ee2d23d`  
		Last Modified: Wed, 11 Jun 2025 11:13:11 GMT  
		Size: 69.0 MB (68957331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc1d310562389511c34710f540a5f40a96841fcdf844e9a2742b152e861d58d`  
		Last Modified: Mon, 30 Jun 2025 17:32:00 GMT  
		Size: 81.6 MB (81595438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d78178103459a0b9e28049e6b2986f5e2764e474168d99930410d585b7444c`  
		Last Modified: Mon, 30 Jun 2025 17:31:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip` - unknown; unknown

```console
$ docker pull golang@sha256:b458108124e8c8907b02973f88e2ed00283c8b020c5a4601ac7b37d21d2092fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10346806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25959b79aadd6acf90ee90c13cff2635a56b668ef40ef4a176fbe17cbf338a48`

```dockerfile
```

-	Layers:
	-	`sha256:a5fe7e3beac845f33dab58743c8b6d4b7cc16b808e423f5f3d22239e0697b21c`  
		Last Modified: Mon, 30 Jun 2025 20:24:43 GMT  
		Size: 10.3 MB (10319147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ad0a9b3355b636ef3774f363cfd8676dd53ac5c49ddbd7489c1672317212e39`  
		Last Modified: Mon, 30 Jun 2025 20:24:44 GMT  
		Size: 27.7 KB (27659 bytes)  
		MIME: application/vnd.in-toto+json
