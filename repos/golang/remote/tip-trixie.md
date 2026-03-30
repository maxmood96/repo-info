## `golang:tip-trixie`

```console
$ docker pull golang@sha256:1d7a251c88e191983fe8029f29af0fdf5e20b4c92ffc40c9f03af0c77a5083e7
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
$ docker pull golang@sha256:dd19f634e975d90039a37aef09199b9ebcdc9dfa71d0c5eae427480b6463fe09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.8 MB (338814503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79220a4c63e4e6a60c579c2cceb4c2c0087c8b0679b645465b2438f46618f5eb`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:38:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:25:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 30 Mar 2026 17:46:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 17:47:50 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Mar 2026 17:47:50 GMT
ENV GOPATH=/go
# Mon, 30 Mar 2026 17:47:50 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 17:47:50 GMT
COPY /target/ / # buildkit
# Mon, 30 Mar 2026 17:47:53 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Mar 2026 17:47:53 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b012eb15dff0bce418c03ec940325aee6aa4300d771c325728855697e620c63a`  
		Last Modified: Mon, 16 Mar 2026 22:38:25 GMT  
		Size: 25.6 MB (25621715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3a0e7d77f0c84203cab438fcf345647c8121bbd80506a3c692f8608a14c4f4`  
		Last Modified: Mon, 16 Mar 2026 23:25:57 GMT  
		Size: 67.8 MB (67780758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7cbbb7aa65444a3770aec61426223f9c39f509dce8ff6be928a41b3511fbd8c`  
		Last Modified: Mon, 30 Mar 2026 17:48:21 GMT  
		Size: 102.2 MB (102169474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc94bcc3a046e419ba11b5fddd09ec7514410ba4c53e7ad8d4f5445debcec8a`  
		Last Modified: Mon, 30 Mar 2026 17:48:21 GMT  
		Size: 93.9 MB (93944870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ec91e1e152aebdb4fa0e821740db2bc56586deac2cc224353ee9d1f0c7cefb`  
		Last Modified: Mon, 30 Mar 2026 17:48:15 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:f512461731b14dd94c56100ff371e235ab84be29859a997955df39867763e59d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10814628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:104ac593d97e7306dcc942b7e675c776df8820cf525bdb25f82535e047417439`

```dockerfile
```

-	Layers:
	-	`sha256:9e07930c57934e82a0bf3beb9941aef202386f7aed3e6418d5aa618fe01ae4e1`  
		Last Modified: Mon, 30 Mar 2026 17:48:16 GMT  
		Size: 10.8 MB (10785659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91256462588fcb1b6f655933649ca3b8a4da079c948b78549923cf81a1d5eb11`  
		Last Modified: Mon, 30 Mar 2026 17:48:15 GMT  
		Size: 29.0 KB (28969 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:56e89e38b42957d4d4646075f5d39a18a9fbb1733d195ad2c8e12b914bad50cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.0 MB (294957657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7e806e0f54f15071d45b36ba9bce1b533343ee52062a9ae437f805ffbe4ffe`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 00:27:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 01:15:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 30 Mar 2026 17:47:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 17:50:33 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Mar 2026 17:50:33 GMT
ENV GOPATH=/go
# Mon, 30 Mar 2026 17:50:33 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 17:50:33 GMT
COPY /target/ / # buildkit
# Mon, 30 Mar 2026 17:50:36 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Mar 2026 17:50:36 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:83d3fd32d825865515469d080b5a8d89e630e2ed8f99a18d7b80d9c437631ab6`  
		Last Modified: Mon, 16 Mar 2026 21:53:25 GMT  
		Size: 45.7 MB (45732648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cceb46da040530c459a3d55c1b9d0ccf68be7e284352029649a82437d5fc663`  
		Last Modified: Tue, 17 Mar 2026 00:27:35 GMT  
		Size: 23.6 MB (23637012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e536a24ef93e50bf0d2984c667c771026334af7e30ed6318f85d146e4ff7a306`  
		Last Modified: Tue, 17 Mar 2026 01:15:28 GMT  
		Size: 62.7 MB (62713901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ea84fa0fdb1477d41dbff18f5a9bb96618f35aa2a3c509ca8e67a585943fd2`  
		Last Modified: Mon, 30 Mar 2026 17:51:02 GMT  
		Size: 72.8 MB (72805131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10a0142adc6609c1699e104cbb6d09e5264e25e4e76c071ff20b820aebd1914`  
		Last Modified: Mon, 30 Mar 2026 17:51:02 GMT  
		Size: 90.1 MB (90068807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7981dd069fd6194dd5174e741337def4b373c0c4e47a655d24a084e4d413f2`  
		Last Modified: Mon, 30 Mar 2026 17:50:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:b79e6ac7f84e68158e1f91b64981c17cafea825f350b21ad1f58557d7f2ef2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10610638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c340221a33b71a6cbef96f1888fe9ccc96081b560d08fe0f1a493ea57ae238f9`

```dockerfile
```

-	Layers:
	-	`sha256:97c32c372126e52c387b997e14193e0d5368c841547c900f4b3485866bca15fa`  
		Last Modified: Mon, 30 Mar 2026 17:51:00 GMT  
		Size: 10.6 MB (10581546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1736de06c05f4666f046e0b24b8397563964434a278d601f69b4809645196892`  
		Last Modified: Mon, 30 Mar 2026 17:50:59 GMT  
		Size: 29.1 KB (29092 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:2c38236421cc825f9c8afc59541ac552d96e6abb916460759a57da5dc1ba9bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.6 MB (329609433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48704c5b2f7b8cc0b2e66b6a791d2da593354bad79381dae199b44f3d2ef7032`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:40:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:30:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 30 Mar 2026 17:47:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 17:49:24 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Mar 2026 17:49:24 GMT
ENV GOPATH=/go
# Mon, 30 Mar 2026 17:49:24 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 17:49:24 GMT
COPY /target/ / # buildkit
# Mon, 30 Mar 2026 17:49:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Mar 2026 17:49:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6778b62bd97b31237948877e89abc29ad2b2c003f3b965027457c8c90d4f44e0`  
		Last Modified: Mon, 16 Mar 2026 22:40:45 GMT  
		Size: 25.0 MB (25023728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d16813bdedcf0a1acbd78336c5bed6fbfaee2674574408140ba7e896cd49cb95`  
		Last Modified: Mon, 16 Mar 2026 23:31:00 GMT  
		Size: 67.6 MB (67584568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3937fa21a857f6d48a12b722dd9831b50a497ced425ac47a414fde0f2eb6ca`  
		Last Modified: Mon, 30 Mar 2026 17:49:54 GMT  
		Size: 98.3 MB (98310060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111f485f6c4b82dc9f58e7d75c491e9181371f2ac26e7bd1ac582e69f4e4bb91`  
		Last Modified: Mon, 30 Mar 2026 17:49:51 GMT  
		Size: 89.0 MB (89025966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8585c25ffc8793a592970b2752490c742adb0007e09b71feaa7da44f828db91c`  
		Last Modified: Mon, 30 Mar 2026 17:49:50 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:6afd386ebc0f0c02b57e943193684f0f9b27e5b8db4842cb896a9603cfef4a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10935238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f9381c013392f4a54c45a6e4417ac197630beca872e0cc9a39fda62c6d9f51`

```dockerfile
```

-	Layers:
	-	`sha256:5d95a98898584f534d58e597438aa05b5e084b276df75bbe35dcf9c00fa467df`  
		Last Modified: Mon, 30 Mar 2026 17:49:51 GMT  
		Size: 10.9 MB (10906114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce5054d6b6a6ef587d4ca213af1cb477473723645bea304fafbae63df525b8df`  
		Last Modified: Mon, 30 Mar 2026 17:49:51 GMT  
		Size: 29.1 KB (29124 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; 386

```console
$ docker pull golang@sha256:406d3ad38c74545c6bf53b7d9b01f39ad59cc0e6d00836a8185d663b2cbcd223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.8 MB (339775763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5c4d71456ee50584f95fe1ef573f9f376ac10f1ad191e19755da85d90161b5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:44:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 23:42:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 30 Mar 2026 17:47:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 17:49:58 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Mar 2026 17:49:58 GMT
ENV GOPATH=/go
# Mon, 30 Mar 2026 17:49:58 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 17:49:58 GMT
COPY /target/ / # buildkit
# Mon, 30 Mar 2026 17:50:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Mar 2026 17:50:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:a59dab062b6e61bf7c8c44e3e14585d36526de4560825ba7d4c8196503c6eb87`  
		Last Modified: Mon, 16 Mar 2026 21:53:40 GMT  
		Size: 50.8 MB (50818792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027db2aaf35fd2a2c9adf573b12a548dde1e9e6733b0a9d987c465038a81dcb2`  
		Last Modified: Mon, 16 Mar 2026 22:44:31 GMT  
		Size: 26.8 MB (26783539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd35fd6ac345d92e539dc7dc49dc31742923ebf394762120d349ae52e655e6ff`  
		Last Modified: Mon, 16 Mar 2026 23:42:21 GMT  
		Size: 69.8 MB (69795316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd03822bd128fbe73b3ac75ff8ffd5f421fcf953d72ddabcd80a7baa502c3777`  
		Last Modified: Mon, 30 Mar 2026 17:50:29 GMT  
		Size: 100.6 MB (100608591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60cd517d6dba9b01cd366f9de5344ce7d7604f0621cccf254c2d056e36d9d4f2`  
		Last Modified: Mon, 30 Mar 2026 17:50:29 GMT  
		Size: 91.8 MB (91769368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:475d5ad2e2c9b0f0623a0d10e5fdad574438862261dddb980886ea7e3b92640a`  
		Last Modified: Mon, 30 Mar 2026 17:50:26 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:465de3bb9cfcf39ad790f88a34cb379fb78d8211a0be7a085a95fd4b983c8a24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10785848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bbca3c5649defa2470dcf7a88574e5f057296eef261d2bc03c3afe8ff0e124`

```dockerfile
```

-	Layers:
	-	`sha256:c474b47f404eb14db13fd373a773a1101142949dfff73e5850e87b2696d976b7`  
		Last Modified: Mon, 30 Mar 2026 17:50:26 GMT  
		Size: 10.8 MB (10756922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01b52a172d76d2209901ac1415896d264df9d6c7bf589c87f6ade1b598826515`  
		Last Modified: Mon, 30 Mar 2026 17:50:25 GMT  
		Size: 28.9 KB (28926 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:cb8ccae6fbafe2bc3d2c61d5dc68d55da20f0837cf5121be4238bde4a66965c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.8 MB (336768485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d0928d0679b326c05c32b0140c8eb560010abe299fdeb4e0acf3cc061a5b852`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 01:50:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 06:05:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 30 Mar 2026 17:50:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 17:49:52 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Mar 2026 17:49:52 GMT
ENV GOPATH=/go
# Mon, 30 Mar 2026 17:49:52 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 17:49:52 GMT
COPY /target/ / # buildkit
# Mon, 30 Mar 2026 17:50:21 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Mar 2026 17:50:22 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:616ed6c40b4f1136ebcda954e46e021bcee567aad248468321da4f4065f4a14d`  
		Last Modified: Mon, 16 Mar 2026 21:55:32 GMT  
		Size: 53.1 MB (53118350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e76fd6649d6d35f910f2df9456726122ef27f29bb48c2f6e7ffbc7d318e0c0f`  
		Last Modified: Tue, 17 Mar 2026 01:51:12 GMT  
		Size: 27.0 MB (27013391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e880a549306a0c27a7c0db6951a348b972ff41cbbc4c467d5d3c95c7797075`  
		Last Modified: Tue, 17 Mar 2026 06:06:09 GMT  
		Size: 73.0 MB (73033284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19b2c0d1e3ca01e04689568b491176564ea4a25d80d79e56f5e79a395c2725b`  
		Last Modified: Mon, 30 Mar 2026 17:51:23 GMT  
		Size: 92.9 MB (92870771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:111969b1f573be958af91f197054c394fc84f73b452627519be6a7f12a1bcd78`  
		Last Modified: Mon, 30 Mar 2026 17:51:17 GMT  
		Size: 90.7 MB (90732531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5455ae05be2bdf5d49c6c0465b8d6bbb502c45169712b360b19937fad15f9bda`  
		Last Modified: Mon, 30 Mar 2026 17:51:14 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:0e8dbfcd913a83eafd1d8112ebb1e21ab4bf58cd687024dff36260d001d10fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10810296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b5b7e5bbbb1aa156b14c15bf97b552ad57196e4cb19696920c5675b81d1942`

```dockerfile
```

-	Layers:
	-	`sha256:11cee9ca26472ad43abf22e064899a68fec6e4d1c23d9e8d6a0b023314659b1a`  
		Last Modified: Mon, 30 Mar 2026 17:51:15 GMT  
		Size: 10.8 MB (10781447 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd944c5d13c02452a16ea90c2d1df354aff58518b6daa950966898d737536526`  
		Last Modified: Mon, 30 Mar 2026 17:51:14 GMT  
		Size: 28.8 KB (28849 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:b0aa841e2ca357d75ebf81f239535a1149d19b56514fabe7cace87bb9b073dc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.2 MB (362159828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d326428a4f7feb2aa62891f1eda40bd5e6803ae1e34babb3a034ecd4ee3a222`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1773619200'
# Wed, 18 Mar 2026 05:11:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 19 Mar 2026 05:31:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 21 Mar 2026 04:55:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 18:23:56 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Mar 2026 18:23:56 GMT
ENV GOPATH=/go
# Mon, 30 Mar 2026 18:23:56 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 18:23:56 GMT
COPY /target/ / # buildkit
# Mon, 30 Mar 2026 18:24:13 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Mar 2026 18:24:14 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:90acba8ac92ad141ae919a99e64549b2f417e5b2ec79f1a99dbc8efba0fea96b`  
		Last Modified: Mon, 16 Mar 2026 22:09:11 GMT  
		Size: 47.8 MB (47792328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d52d7ab982f4bfd5cfc38caa0eefe3bfddcb1b2f76f02a38e1b10725b762ee`  
		Last Modified: Wed, 18 Mar 2026 05:13:23 GMT  
		Size: 25.0 MB (24954925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc9a450c15c86147b6c308f2cb25a618ec75f2ab5a64203aa728b5e309ab137`  
		Last Modified: Thu, 19 Mar 2026 05:35:26 GMT  
		Size: 66.7 MB (66662504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9c3d8cb0eb3839f60f443c07c78a4e233d415f3d669a49057b1e5f1b8cb424`  
		Last Modified: Sat, 21 Mar 2026 05:03:52 GMT  
		Size: 131.7 MB (131650375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6e70b1853c9d42c6bcadfebf9fcf629114d0890e516270d3e090097d9a57f9`  
		Last Modified: Mon, 30 Mar 2026 18:30:56 GMT  
		Size: 91.1 MB (91099540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4959cdbfb7a2089aed29e3e820777655dddc157d9325abb7f203faf1d6b21ffb`  
		Last Modified: Mon, 30 Mar 2026 18:30:40 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:28c3d9c17b26d7eec8e0834ab7d6f9a9f24ff8f84715c9b69a50a9463b413351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10884303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0dd8771f3369dfb3472a9730b8186c08337c943916cbfe6ab628d00c655193d`

```dockerfile
```

-	Layers:
	-	`sha256:1e659411d760c64c158d64798869be5156cec426de937e41214fb044afda50b8`  
		Last Modified: Mon, 30 Mar 2026 18:30:43 GMT  
		Size: 10.9 MB (10855280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8091309a98e98978e9d48ad8e4046f545714313a49ff255994fd6326e8de85d0`  
		Last Modified: Mon, 30 Mar 2026 18:30:40 GMT  
		Size: 29.0 KB (29023 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; s390x

```console
$ docker pull golang@sha256:1df75a4872964eae0ab94f348beef644d30db7195ad6cba8bab16a9f87f0bb33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.9 MB (313902736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b02392d92fab5d42796334ce7a2d9e3c22bb1254ada34efc892d55bfc1be2da`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:45:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 17 Mar 2026 01:34:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 30 Mar 2026 17:53:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 30 Mar 2026 17:52:57 GMT
ENV GOTOOLCHAIN=local
# Mon, 30 Mar 2026 17:52:57 GMT
ENV GOPATH=/go
# Mon, 30 Mar 2026 17:52:57 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 30 Mar 2026 17:52:57 GMT
COPY /target/ / # buildkit
# Mon, 30 Mar 2026 17:53:57 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 30 Mar 2026 17:53:57 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7bc76783a6155f9347e92234e4b5c38bd02638c6de782f4623d0736c769250f0`  
		Last Modified: Mon, 16 Mar 2026 21:52:57 GMT  
		Size: 49.4 MB (49364775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8371259f6819197ae08830e46db090d1aad241011f8c2483f8e3205359263dcd`  
		Last Modified: Mon, 16 Mar 2026 23:45:50 GMT  
		Size: 26.8 MB (26803190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6990bcd0cd48258f05a5e1da913e50e516d08ed7812badfbb9d8451ec894a6a6`  
		Last Modified: Tue, 17 Mar 2026 01:34:59 GMT  
		Size: 68.6 MB (68628445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31d5e3142a4c1073c2b7e8afa1f8be19857d8c721f47ac2591fe74c15a9c4f5`  
		Last Modified: Mon, 30 Mar 2026 17:54:45 GMT  
		Size: 76.0 MB (75982104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d77473e8e347c240104f79da8f95d36830a796c56bf93ad436d6a5a18785036`  
		Last Modified: Mon, 30 Mar 2026 17:53:56 GMT  
		Size: 93.1 MB (93124064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd66918d672b91804815c63259d4ebe805aa9d88601101416729708f7a8bd9b`  
		Last Modified: Mon, 30 Mar 2026 17:54:43 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:4035abdf7f9bbf350a0d6611bf69b019044eb804a2e9c2fb10669fa48f2f4437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10625022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69608c0cb258448a33144bcedf9b070845c614fdd7cb32c90962cb5e9f4478c8`

```dockerfile
```

-	Layers:
	-	`sha256:453dc4b4be07891d15339aa085e2288959785bb22256e50bd1e27baaf65258f1`  
		Last Modified: Mon, 30 Mar 2026 17:54:43 GMT  
		Size: 10.6 MB (10596059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:027a7a64c89d7da88ab2dac960beebd9ae55ab76862cd306fba7cdbaa86552b7`  
		Last Modified: Mon, 30 Mar 2026 17:54:43 GMT  
		Size: 29.0 KB (28963 bytes)  
		MIME: application/vnd.in-toto+json
