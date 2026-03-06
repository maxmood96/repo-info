## `golang:tip-trixie`

```console
$ docker pull golang@sha256:27d1e7ed330252ccc9e3d85bcb98e96fccadac35a7b80e75893e104af3980b6c
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

### `golang:tip-trixie` - linux; amd64

```console
$ docker pull golang@sha256:f9a37b2fe0691dbb7a6eb6487453b98edf5d3f786c8c902fc1393db880e4e824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.5 MB (338456528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd334a739c439d0f180332f4ef7e79e241824f25d703988329187328561cc717`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:04:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 06 Mar 2026 01:59:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 02:01:21 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 02:01:21 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 02:01:21 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 02:01:21 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 02:01:23 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 02:01:23 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed881fbf1b07b42dd470cd5b56a8feb684d60879c6f8028a9e7a8715e0e72361`  
		Last Modified: Tue, 24 Feb 2026 19:20:17 GMT  
		Size: 25.6 MB (25614562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da421ddeb655bdfb3960e490b39373b0d1351e3eaba61d01978107920638392`  
		Last Modified: Tue, 24 Feb 2026 20:04:27 GMT  
		Size: 67.8 MB (67778971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87218d05e2573402f1bd91c0819fe54a26ad6f6cf8bdfec316d901956ebef5a6`  
		Last Modified: Fri, 06 Mar 2026 02:01:49 GMT  
		Size: 102.2 MB (102166366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689a8c664b692c42c224e696026ec9ec2afa2556b09a298fb5881d3823f0c6dd`  
		Last Modified: Mon, 02 Mar 2026 22:02:43 GMT  
		Size: 93.6 MB (93603346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce1d2a9ea688db57e207cb77d868932db9aef9a43bb07e9724d72dfaae1ce78`  
		Last Modified: Fri, 06 Mar 2026 02:01:46 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:26b00c3e4161555d132b891c58b06130d55c98c1b3243d0285536eeae298267e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10814552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85af7288e98ac84e874d9e016ca2f4fed5e75ebd55d4cabcf88fd831e8af8c52`

```dockerfile
```

-	Layers:
	-	`sha256:463da7af79e9f46d6f49b46da47b40f9e30d7b0541ea45cfd7f279a629a08f0d`  
		Last Modified: Fri, 06 Mar 2026 02:01:46 GMT  
		Size: 10.8 MB (10785583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d003326daabd898137f44a1586fbda432b95111fc19975f276431e257177056c`  
		Last Modified: Fri, 06 Mar 2026 02:01:46 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:1315e2c33da87c39417f5b69b579edaae191bed3d1a55953a84a5788c62d6fd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.6 MB (294572758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62892fd2075b371128892aef297b092025387a7362c985cbdcb83ac9ae8f66e7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:04:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 21:34:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 06 Mar 2026 02:00:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 02:03:09 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 02:03:09 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 02:03:09 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 02:03:09 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 02:03:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 02:03:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e7e4c87ce6959403c140ef3f01bab08f94d7dd517c0acf6ae810804957e70b9d`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 45.7 MB (45725086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77120a84626d4a7f2d6bdca75bb942d16ac419ff1bc25fc6e9d95035fe35f65e`  
		Last Modified: Tue, 24 Feb 2026 20:04:48 GMT  
		Size: 23.6 MB (23633662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c27016c2923c40df4d7f8b1909d8aac2050fedaaac6d29c1a4942dcab0ae038b`  
		Last Modified: Tue, 24 Feb 2026 21:35:13 GMT  
		Size: 62.7 MB (62713584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b28800361a69e4350c04714553d9cf20267914dd0c2b9b6ee07b7a38c58fb5`  
		Last Modified: Fri, 06 Mar 2026 02:03:36 GMT  
		Size: 72.8 MB (72803605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d47f42e49b5b1824f0c700b4d521593aedaa7278226bf8d2c8c937a0110183`  
		Last Modified: Mon, 02 Mar 2026 22:04:34 GMT  
		Size: 89.7 MB (89696663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2329fcbc5be6e13557982e46473260c8dfcf3a224fa783edf1eef6d1c41f5bdb`  
		Last Modified: Fri, 06 Mar 2026 02:03:34 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:1925a212df807f2e4eb748cc5850cce5d85f7e92baf4c80e6974b1637a749201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10610562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a3271cb7da9ed4079e2e6dbbffdc9c1f4ca30c971d8b429f94f541e030f461`

```dockerfile
```

-	Layers:
	-	`sha256:74011ae22f36eba43e48564ec8babcc95835f515e78977bb8eaf84c6f330875d`  
		Last Modified: Fri, 06 Mar 2026 02:03:35 GMT  
		Size: 10.6 MB (10581470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:449abc07fd09cc64da56be4ad9f03ca0d390f3e6e6c4e6334eed92e695d76abe`  
		Last Modified: Fri, 06 Mar 2026 02:03:34 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:5da770ea85bf7cdb9e3f0c551df87e67e322bdd9ae7ac211130bf599c82eb125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.4 MB (329356877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9e91c23cd543f66fe9a26cdba8f48ccd1e4064f7d890bd7237ff1672ecf2080`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:24:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 20:14:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 06 Mar 2026 01:59:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 02:01:13 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 02:01:13 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 02:01:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 02:01:13 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 02:01:16 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 02:01:16 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95da832d1713c4ed161275cd40c4161680fbdd97c6faf23e71654d26bb2e58d6`  
		Last Modified: Tue, 24 Feb 2026 19:25:09 GMT  
		Size: 25.0 MB (25023493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c46eec5989abc098640d80ee9b97658d4487864f3268219dadc63c0a047866`  
		Last Modified: Tue, 24 Feb 2026 20:15:09 GMT  
		Size: 67.6 MB (67585551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604649270cba5190b7ce4e165ec3e2559e023d972135abf7b737666f583611f2`  
		Last Modified: Fri, 06 Mar 2026 02:01:42 GMT  
		Size: 98.3 MB (98310677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e982fdcb72c3ad1cca7a139b473ea3951042395bd4cf7fbdb4f775c24a9b551`  
		Last Modified: Mon, 02 Mar 2026 22:03:07 GMT  
		Size: 88.8 MB (88784830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bda102bcf0d21270f1a81184670a9fe179f4111e66a5f492be827923df49204`  
		Last Modified: Fri, 06 Mar 2026 02:01:40 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:4056fc1301596fd78916b62977d4011db18e7d0c9750d9d8f53855d64c1ee7a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10935162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ce4e4949d0c875ab0ec8cdd8ebe8fa0b8e32a3153daa282d4f52b4a8d86d52`

```dockerfile
```

-	Layers:
	-	`sha256:5858d47780f026288598a98cec58dfa763614b74d10435484bff7afc85845a7a`  
		Last Modified: Fri, 06 Mar 2026 02:01:40 GMT  
		Size: 10.9 MB (10906038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:226da378237685a7dbb6a76f3ba354b68490bd321f23a0a0c33f4d8642058f8d`  
		Last Modified: Fri, 06 Mar 2026 02:01:40 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; 386

```console
$ docker pull golang@sha256:9336ca766b59396bec969e614ab5b18acedd5ae15dd4ee493ee29ac949246e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.4 MB (339436603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3993d6a7f05ee8a887f14c59fa94e7fa4ddc843ef32a4601df2ba3bd54a2925`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:24:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:57:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 06 Mar 2026 02:00:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 02:02:38 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 02:02:38 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 02:02:38 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 02:02:38 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 02:02:40 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 02:02:40 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:cdaf5c618b8ff25cb29f813a6c008ca0cb7de6fe5f93f3ba4939cc9fc10fc6cc`  
		Last Modified: Tue, 24 Feb 2026 18:42:38 GMT  
		Size: 50.8 MB (50805272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c637225671ff7a033f6873454fdf6a539c15748206b024d30b37d32f91f3c21`  
		Last Modified: Tue, 24 Feb 2026 19:25:06 GMT  
		Size: 26.8 MB (26779652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c73fe9d5e539e615e830926d2ddb692fd4ffb36bb2ea42d3131dcab6528d49`  
		Last Modified: Tue, 24 Feb 2026 19:57:28 GMT  
		Size: 69.8 MB (69794855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa77c404011b3c78822b919d2a5b7792bc533943fe55723a10ac9e47b2820f9b`  
		Last Modified: Fri, 06 Mar 2026 02:03:06 GMT  
		Size: 100.6 MB (100607745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:862b2140e9f06d205b6b5af3fcc14f26b13013365f22129c2ff99cb48ee34776`  
		Last Modified: Mon, 02 Mar 2026 22:04:44 GMT  
		Size: 91.4 MB (91448922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:875a1458a51c7bdcbffd053503a462bd6922b7043b1dc0493176081e5496e009`  
		Last Modified: Fri, 06 Mar 2026 02:03:04 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:c4d56139810c79afbc43d77354026ea615eb86bfb042c4872a3e5a0af0505f8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10785772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938070bdc89728de964934c4417b7e25fdd01d52b333004cf5bbd805a2f2fedb`

```dockerfile
```

-	Layers:
	-	`sha256:f4c4cfb2b7aeb23f371027b480706ba953f98f1afa973647fa6c8c16f18c206c`  
		Last Modified: Fri, 06 Mar 2026 02:03:04 GMT  
		Size: 10.8 MB (10756846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b6122c1e7e335e708a73a7e87bf4d21187aac8f2502836a53e3975c45e0da3a`  
		Last Modified: Fri, 06 Mar 2026 02:03:04 GMT  
		Size: 28.9 KB (28926 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:cd5ff969c7c88e0efee5bfae7c2f6bbd040ffeeace8b8da2622d9dd06219d1fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.3 MB (336322943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f02962642eca174220f90594f2a3493bf9246f69e23f0fd23749863411184bf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 21:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 25 Feb 2026 02:58:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 06 Mar 2026 01:10:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 02:02:04 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 02:02:04 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 02:02:04 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 02:02:04 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 02:02:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 02:02:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b88c878e5079331d2b0e1bf13313604e6e446232728ee7b159499795ff9def2`  
		Last Modified: Tue, 24 Feb 2026 21:23:39 GMT  
		Size: 27.0 MB (27004375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8078b8ed13f55a8d2e3bc098e87fe680e2a4289c11315d3e460db7bcd51cc93f`  
		Last Modified: Wed, 25 Feb 2026 02:59:03 GMT  
		Size: 73.0 MB (73022125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784245641f5583c22125d8b1795377396b0329cd3dddb9ca69cbe55bdfecb75d`  
		Last Modified: Fri, 06 Mar 2026 01:12:06 GMT  
		Size: 92.9 MB (92868135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcc3a57b0d1a4c549275152be846eeab1e4bfda9d363982944775991fe15219`  
		Last Modified: Mon, 02 Mar 2026 22:05:31 GMT  
		Size: 90.3 MB (90315888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8e13cee2e6d623c3bc102a2c6265bcaa57f0780480865fcb57823cf3aa1911`  
		Last Modified: Fri, 06 Mar 2026 02:02:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:8283c14858fc8a6d5730e0e7665d381f0028dcc54c49a85b19471d47a9e2c626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5ed7abe814814f7f6190b1f8b4f27406351873379ffaa8c0e78cacf16cdd3a2`

```dockerfile
```

-	Layers:
	-	`sha256:6295cd9537a7fef29dfa8221e5d9bcbb3467881e7339930950a1eabad0e2d66a`  
		Last Modified: Fri, 06 Mar 2026 02:02:57 GMT  
		Size: 10.8 MB (10781371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b7c39a36cf7d8ce24613d906df479c064e826b1a6052d98c1e08b0e7a4d7424`  
		Last Modified: Fri, 06 Mar 2026 02:02:57 GMT  
		Size: 29.0 KB (29022 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:dec5dd4706c968593588bdd904e7f6f19aeedcb9ac9d37411969cebd9e800844
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.8 MB (361831160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b28701823fd69cfce0a974aad97423d872dc50ee927f5ec3b4d1f7de4487419`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Thu, 26 Feb 2026 21:43:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Sat, 28 Feb 2026 19:58:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 03 Mar 2026 01:38:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Mar 2026 09:03:40 GMT
ENV GOTOOLCHAIN=local
# Tue, 03 Mar 2026 09:03:40 GMT
ENV GOPATH=/go
# Tue, 03 Mar 2026 09:03:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Mar 2026 09:03:40 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 02:37:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 02:37:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:3be247472b67578a1d05739722d8adeca41098796e5d6210800176db58046fa7`  
		Last Modified: Tue, 24 Feb 2026 18:57:42 GMT  
		Size: 47.8 MB (47776936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:115c3a1cec8ab5f3346656c92bb6a04391222dacf945336ca2f360cb9afa1d32`  
		Last Modified: Thu, 26 Feb 2026 21:45:21 GMT  
		Size: 25.0 MB (24951819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be1aad3c88d849328eee587bd71226c07edf0e2f5081fc7ec8dc66c3ee7e1d0c`  
		Last Modified: Sat, 28 Feb 2026 20:02:17 GMT  
		Size: 66.7 MB (66662373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37ae9709038f63e30e164a548c422deaa7a5733b337f89853b60db2fe5818b5`  
		Last Modified: Tue, 03 Mar 2026 01:47:15 GMT  
		Size: 131.7 MB (131650592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7550964df09cbec6e16da50f25098e25826ade610bf4557ad9371e12e9ced3d4`  
		Last Modified: Tue, 03 Mar 2026 09:10:27 GMT  
		Size: 90.8 MB (90789282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2db863f9b88196d1b415760aeac3c290e5494f690a634938d043317b0bf8bc4`  
		Last Modified: Fri, 06 Mar 2026 02:41:59 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:c6820ab9ac978b13ae9dbb70acdcaaeba4b94d8d50d35e7cddf32dd0cd4966b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10884231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae21d1da4bd852e389a1f2e797f29f72c387ca2856c2dd01b9b0fc649af531d`

```dockerfile
```

-	Layers:
	-	`sha256:f0fa01deb547a8bd57f4934ee4ca9d881553d6cb3695b3cbcd33a032c1419d29`  
		Last Modified: Fri, 06 Mar 2026 02:42:01 GMT  
		Size: 10.9 MB (10855204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8befe4e1f107bc884d5a6812a05e6a66397e1fb4d51a793492c13779b8aead1`  
		Last Modified: Fri, 06 Mar 2026 02:41:59 GMT  
		Size: 29.0 KB (29027 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; s390x

```console
$ docker pull golang@sha256:7f5fbbad568ddc7105b77eec9c69585a094f51be6223064ad0c27e6dfb453e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.6 MB (313563026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543e27dc545059f0664cc5b72765b8a8601b34e693f61ea996e8552e56d4232e`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 20:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 23:53:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Fri, 06 Mar 2026 01:10:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 06 Mar 2026 02:01:51 GMT
ENV GOTOOLCHAIN=local
# Fri, 06 Mar 2026 02:01:51 GMT
ENV GOPATH=/go
# Fri, 06 Mar 2026 02:01:51 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Mar 2026 02:01:51 GMT
COPY /target/ / # buildkit
# Fri, 06 Mar 2026 02:01:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 06 Mar 2026 02:01:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:aba9aa950add2749194487d5c63a3069af6daf9dfe54d80cfbe32bfa7a5faa07`  
		Last Modified: Tue, 24 Feb 2026 18:43:53 GMT  
		Size: 49.4 MB (49354534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b9712b896509afe6ce616cc91aa36b272afd379950384122674a69ff7d6929`  
		Last Modified: Tue, 24 Feb 2026 20:59:42 GMT  
		Size: 26.8 MB (26801071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d62d9ba5f66f052b2790c9aa6ddd7ff161b24db86972e603be616bc922281de`  
		Last Modified: Tue, 24 Feb 2026 23:54:27 GMT  
		Size: 68.6 MB (68624526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9684e467c80be7a48b834eccb7a527228d490fb7acd8db34ebc728ce3079a9e`  
		Last Modified: Fri, 06 Mar 2026 01:11:18 GMT  
		Size: 76.0 MB (75980176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb2d3098d11b942b930d9b88ef8d2b13e42c10d7ccd12c5e317467f410cfa58`  
		Last Modified: Mon, 02 Mar 2026 22:04:29 GMT  
		Size: 92.8 MB (92802560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56538e5ff79691f8731a8cc867abaa5fe4bd9f2e3960d42e3f551e894d3367a0`  
		Last Modified: Fri, 06 Mar 2026 02:02:21 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:77a4df34ffa8e1fd25d8c700e8227424d820c6c018c379f3104e853045d045da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10624947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6959ac1403e6c551151affe9ee9a45b0bc68653fbc782059e6a5ad6a8377b1c2`

```dockerfile
```

-	Layers:
	-	`sha256:bafb24a9ef6e056af024711079ffb99a67971ca6d8a7c570940262ce2b65baab`  
		Last Modified: Fri, 06 Mar 2026 02:02:21 GMT  
		Size: 10.6 MB (10595983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8dfae9d1f90a18aededc1935f2368374c7f8b69e5c264f16352a7f7dd79321a`  
		Last Modified: Fri, 06 Mar 2026 02:02:21 GMT  
		Size: 29.0 KB (28964 bytes)  
		MIME: application/vnd.in-toto+json
