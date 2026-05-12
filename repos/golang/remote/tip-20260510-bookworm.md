## `golang:tip-20260510-bookworm`

```console
$ docker pull golang@sha256:ab10ea505dfa4b90a7725a88b6792476e8c00faaee87a948bdf514847523913f
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

### `golang:tip-20260510-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:a0ee686389efbf16af0257d2f0075103371ff29615c9358c300edd308c777bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.8 MB (326824616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af11a9c5d09a3706ed699eb31c143c79ec1b46a38370d4184286f960c4b71e22`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:40:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:21:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:23:39 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 May 2026 23:23:39 GMT
ENV GOPATH=/go
# Mon, 11 May 2026 23:23:39 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:23:39 GMT
COPY /target/ / # buildkit
# Mon, 11 May 2026 23:23:41 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 May 2026 23:23:41 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d055cea50c88c57fc27fcd44845ebabfe5b830ea8a0a621b89d38a2b650b7ff3`  
		Last Modified: Fri, 08 May 2026 19:40:29 GMT  
		Size: 24.0 MB (24042180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0869e5c4dac5849d3555a38db741288a16528478145da8dcb95b8dba2464d55d`  
		Last Modified: Fri, 08 May 2026 20:26:25 GMT  
		Size: 64.4 MB (64397036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9357d5c14dd28f2537bd69a9efd5ffd360d6f2b9e24a5a07cad99709cc0ab8f3`  
		Last Modified: Mon, 11 May 2026 23:24:10 GMT  
		Size: 92.5 MB (92480163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970dd4e15afd4dda5f0073081cf90c52ecab4076d0f8b775deea9b5b1305744d`  
		Last Modified: Mon, 11 May 2026 23:24:11 GMT  
		Size: 97.4 MB (97416403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7243d4afa8ac19d8ebc95e8191961a3ae626b5f79113027fa14877c0dc8b95`  
		Last Modified: Mon, 11 May 2026 23:24:06 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260510-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:8826c5b8f9a78a2088c460643fd7e449fb3baf39312a96721908c6eed5a1e093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10525419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458b5700f41dedde9997a97edacbb5be128712f3887c20706159e1a2111ecabf`

```dockerfile
```

-	Layers:
	-	`sha256:4e7e2cd9f5e92c3e7e0a2b5db1b6956205e69e34c6b60725bd73e0ccc6509b9c`  
		Last Modified: Mon, 11 May 2026 23:24:07 GMT  
		Size: 10.5 MB (10497033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89d28b06a5653a28bb317a15cce41fceabae17a3cb5e33f1304cc83200390eb9`  
		Last Modified: Mon, 11 May 2026 23:24:06 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260510-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:760c9492e15cc6f3744376ae91a880fa4bd8fda3bf238487ca6e50e50f969704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.4 MB (285404399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643c38dff3a6bafd66a88cf301916135f2b6d38296c1ff4f707bc71bf62997d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 21:34:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:31:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:34:25 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 May 2026 23:34:25 GMT
ENV GOPATH=/go
# Mon, 11 May 2026 23:34:25 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:34:25 GMT
COPY /target/ / # buildkit
# Mon, 11 May 2026 23:34:28 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 May 2026 23:34:28 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:752ba895535a5b96e621b623e0a11ff696fe28fb2110ab16de49e150423d0a89`  
		Last Modified: Fri, 08 May 2026 18:36:54 GMT  
		Size: 44.2 MB (44207696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0504388ca2bf72a5fec3556b58015e5dce736337a948976b22cd4cce283cb0`  
		Last Modified: Fri, 08 May 2026 19:44:39 GMT  
		Size: 21.9 MB (21946392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbef2e4eed112ac2d8730e2603fe97cab1d0ce708d52061992fd2f72e1db7e12`  
		Last Modified: Fri, 08 May 2026 21:35:07 GMT  
		Size: 59.7 MB (59653543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efecda96b981c61380798bb881e153fcf740233ed2ea177ee818ad6b4d0aac00`  
		Last Modified: Mon, 11 May 2026 23:34:53 GMT  
		Size: 66.3 MB (66341388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa5a325591cc56f1ee0a299253454b588317de6e43dc9dde0447e3b98aa2508`  
		Last Modified: Mon, 11 May 2026 23:34:36 GMT  
		Size: 93.3 MB (93255222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3969baadf4d8994909c4cd6991bbe60bcc8a5d7a3dbacf736d1053939a9a3fa`  
		Last Modified: Mon, 11 May 2026 23:34:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260510-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:027700486ef0401c522208cb9b2964c1fded65672e0353f665c303ef28d36181
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10332227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0923e47d5126fd5525486358230342bc8646ebb08149dd045ec7678342b53d3`

```dockerfile
```

-	Layers:
	-	`sha256:94aca4045fff9e2a2ebc07d6e324c2731bcc2edfeb38c5f02d38e6db503728f9`  
		Last Modified: Mon, 11 May 2026 23:34:51 GMT  
		Size: 10.3 MB (10303729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8e8a6b51f38642619883a8708ec3ab5f18620da8c55ddf24ba3addf4645088b`  
		Last Modified: Mon, 11 May 2026 23:34:51 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260510-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:2aec35525173a19a25b08ac2c38abde1d5fbf2a956fa82b8a0f25205b1ac93bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.1 MB (315140487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33882dbc4acca9520b8026b2d11ed3695eda0837c5338cf382e5e291e5d73fa1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:42:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:31:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:22:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:24:02 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 May 2026 23:24:02 GMT
ENV GOPATH=/go
# Mon, 11 May 2026 23:24:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:24:02 GMT
COPY /target/ / # buildkit
# Mon, 11 May 2026 23:24:05 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 May 2026 23:24:05 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f56578c9577bd69a05b2319baacd770a986ae61a8568047ddd91db1a1893b4`  
		Last Modified: Fri, 08 May 2026 19:42:30 GMT  
		Size: 23.6 MB (23609357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd5c3bf1fab727b805a2f735f33789c10938680bdeb2f8922a44aa2738df91f`  
		Last Modified: Fri, 08 May 2026 20:32:11 GMT  
		Size: 64.5 MB (64479741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a0b6ee6e84764ad9718c249615061ec2ef244f6a44d912130ff353b8e0135f`  
		Last Modified: Mon, 11 May 2026 23:24:33 GMT  
		Size: 86.6 MB (86554854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff2fbc71fe7b87fac66a8dadd85dade8191c7b4ae8add0914f8708f3a3fd259`  
		Last Modified: Mon, 11 May 2026 23:24:28 GMT  
		Size: 92.1 MB (92123227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ca942c200aa1f0b9dbdc6b2796b3568009b56de5721ed6d05c20bc031a5ab1`  
		Last Modified: Mon, 11 May 2026 23:24:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260510-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:8538ed258c111b04d4173d8100f118c5731c7b5fde877b1b9b1a34c6fc5f873f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10553379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f547464d6070b742665af9364744d825be27e5010169059eaf7bd772a0e69c`

```dockerfile
```

-	Layers:
	-	`sha256:850ddf57b5ac78c686f80da52a7563981ffc5bede3d2f9c7ce4ce289ff09a84d`  
		Last Modified: Mon, 11 May 2026 23:24:29 GMT  
		Size: 10.5 MB (10524857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7576a35999e98b6931c083fceab1435f155e68ee8c084461cca3a6fefa55031`  
		Last Modified: Mon, 11 May 2026 23:24:28 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260510-bookworm` - linux; 386

```console
$ docker pull golang@sha256:b07b2a5dc4521cf7ec7cc7053bdb1ed6a665be70207a28ab2eab72388fbb47cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.7 MB (325664735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1082d594edc3e7056e306ea8b2661bab5ddd4030576b58bddd6a15a7780e49fc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 19:43:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 23:04:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:27:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:29:40 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 May 2026 23:29:40 GMT
ENV GOPATH=/go
# Mon, 11 May 2026 23:29:40 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:29:40 GMT
COPY /target/ / # buildkit
# Mon, 11 May 2026 23:29:43 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 May 2026 23:29:43 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:e8fda93cd5bc3b53d403a41ac2e9a09760cd4b6b193c50e68ab6c1d07685411e`  
		Last Modified: Fri, 08 May 2026 18:30:42 GMT  
		Size: 49.5 MB (49477798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c4c78b842a600b86f5f6446efc3bd0e383975b503d9d424b2fa6514ef50eb2`  
		Last Modified: Fri, 08 May 2026 19:43:16 GMT  
		Size: 24.9 MB (24875736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ccd29fc1efdeca894dc5760aafe435a0b88e33948dc45f4dbd0a3c9db72c550`  
		Last Modified: Fri, 08 May 2026 23:05:03 GMT  
		Size: 66.2 MB (66235145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:221761c1f48e05315d93578ba8e86edf26bf9d5dfd77221e9eba71493d7796a4`  
		Last Modified: Mon, 11 May 2026 23:30:10 GMT  
		Size: 89.9 MB (89901030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5caf08a2b699c1c99de16bf0901d8891e91bf0fcf2a4afdcaef52c57556a2e35`  
		Last Modified: Mon, 11 May 2026 23:29:39 GMT  
		Size: 95.2 MB (95174868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e9202453d944defeac2ad9f249f2d1e1b275b01ddd56eba42f0a03f96009d2`  
		Last Modified: Mon, 11 May 2026 23:30:07 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260510-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:1cfa03f32ed387a3f54d2af181df75b0d0fbf6a70fd6317195424bf4022a21bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23046d34d6048613abe04d64064d796c6aa7d0baf799ad4999fc52d8e87c4864`

```dockerfile
```

-	Layers:
	-	`sha256:1086f2f885d8eb520714eb07b612495ab7fd1012f37b1048d9b5e21f8759cc18`  
		Last Modified: Mon, 11 May 2026 23:30:08 GMT  
		Size: 10.5 MB (10476613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c81cbfbc840ebf579d7ef04758a6828fef6c25ba0411977cf4d80bfe58a0df71`  
		Last Modified: Mon, 11 May 2026 23:30:07 GMT  
		Size: 28.4 KB (28353 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260510-bookworm` - linux; mips64le

```console
$ docker pull golang@sha256:d6de87320cb34d2f06049f8a67079ebe2feb43896c17529d7b95665203b9ea6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.8 MB (296848599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48cd2c6a1664758c40db1fe1d1a4d2c864e3642117a31445841f906a879fb689`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 06:28:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 11:38:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 12:25:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:45:34 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 May 2026 23:45:34 GMT
ENV GOPATH=/go
# Mon, 11 May 2026 23:45:34 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:45:34 GMT
COPY /target/ / # buildkit
# Mon, 11 May 2026 23:45:50 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 May 2026 23:45:51 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:08baa8fe1f531703c14c631b772a987ffc44ae832951ae77c2cf756cd9309b97`  
		Last Modified: Fri, 08 May 2026 18:19:35 GMT  
		Size: 48.8 MB (48782513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef35895719420bc7ff8be1345d21e6969bcbf53abcec5b59c476a0fa55636de`  
		Last Modified: Sat, 09 May 2026 06:28:59 GMT  
		Size: 23.6 MB (23615685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6733e62261bdef4b105b9d3a88929418fe62b78559d54a4e8e5768eaa929d6`  
		Last Modified: Sat, 09 May 2026 11:39:51 GMT  
		Size: 63.3 MB (63309897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0597812d9d9ff7a1f06052e0ac78d38dc20231c03c4d4c2602a450e3436a8b`  
		Last Modified: Sat, 09 May 2026 12:27:10 GMT  
		Size: 70.1 MB (70085449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09dbd3ccf97a104937e9a208109956f053429fe21efdf8bc09e219d0ee4fd5d3`  
		Last Modified: Mon, 11 May 2026 23:47:46 GMT  
		Size: 91.1 MB (91054898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd15a396fd7b53dbe2257984f7768ca841744881d83403a75a8b848fb0b9d724`  
		Last Modified: Mon, 11 May 2026 23:47:36 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260510-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:a7990c593beb0dc734f14e79f67c2ac11d0d79a7b3d072829ca8b1af396fd93b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 KB (28240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c687cb8d6540242647a4f51d1d10f3727e61a62c0a149096616eff41eb06553`

```dockerfile
```

-	Layers:
	-	`sha256:19ba6b1ff1f8e06f71aa9d9bd5662707b273aa67e9d6f7c948e1f0304c17442f`  
		Last Modified: Mon, 11 May 2026 23:47:36 GMT  
		Size: 28.2 KB (28240 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260510-bookworm` - linux; ppc64le

```console
$ docker pull golang@sha256:47554d30c9e0738eaa84966812c85f68061c97124e6558e0f2091f0ed4a69272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332331439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afbce8b1257fd915c541cdd67adafdf840cf41c5d8c47ef953760637ea4fe67c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 22:30:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 03:26:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 06:12:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 May 2026 00:42:13 GMT
ENV GOTOOLCHAIN=local
# Tue, 12 May 2026 00:42:13 GMT
ENV GOPATH=/go
# Tue, 12 May 2026 00:42:13 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 00:42:13 GMT
COPY /target/ / # buildkit
# Tue, 12 May 2026 00:42:19 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 12 May 2026 00:42:19 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:30ef9f53c997c6c1f1ab8f4cc559b32d9206d169c54ad5a0f0363076708fffef`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 52.3 MB (52336787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76bedc371abd17d2a145cc444214f9d4db5b827f6b018dfa08217a285aa62a4`  
		Last Modified: Fri, 08 May 2026 22:30:50 GMT  
		Size: 25.7 MB (25679486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12437260b341898b5eafdacd454cf094e6357253f008361a2200d2d98887726`  
		Last Modified: Sat, 09 May 2026 03:27:08 GMT  
		Size: 69.8 MB (69846587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ec4dbf644bcf257e161f5313a10dd6252193021f042ed6183f14c9719379df`  
		Last Modified: Sat, 09 May 2026 06:13:40 GMT  
		Size: 90.5 MB (90489146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c0dd6efbd44f19e1e0d6c48f823bb7238da1300bf904818347619de09b8359`  
		Last Modified: Tue, 12 May 2026 00:43:15 GMT  
		Size: 94.0 MB (93979275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fea8cb9937689fb509fcb3ca048a2edeb041d5e9145f172a4c222ddeec92bcd`  
		Last Modified: Tue, 12 May 2026 00:43:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260510-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:9fae7dc9c0e30d54d2b9265c7ed30eed09a8bbb7f5728e8e2479dec74d7c775c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10497950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab43fa17c205274d29b519da78aa0cdfa6a79e62e631820826d11da45a098da`

```dockerfile
```

-	Layers:
	-	`sha256:7cf653e2b3bf8ca9c24bb32887a964a0d8092cb54431c398f5eaa8645cb26dc0`  
		Last Modified: Tue, 12 May 2026 00:43:13 GMT  
		Size: 10.5 MB (10469518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2084bd1a31c3c514a55f1b087940017b0151dc400ecdea7c36edbbd1dc887ce1`  
		Last Modified: Tue, 12 May 2026 00:43:12 GMT  
		Size: 28.4 KB (28432 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20260510-bookworm` - linux; s390x

```console
$ docker pull golang@sha256:ff0486d272026c928d726dde955852edd1d1ef6b740a5ac1a567e332692a3a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.7 MB (299713865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7336dd99aad325cae6ee12e4c751d55ee00595668a25e059a430c30127d243b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:52:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 22:33:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 00:16:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 May 2026 23:26:01 GMT
ENV GOTOOLCHAIN=local
# Mon, 11 May 2026 23:26:01 GMT
ENV GOPATH=/go
# Mon, 11 May 2026 23:26:01 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 11 May 2026 23:26:01 GMT
COPY /target/ / # buildkit
# Mon, 11 May 2026 23:26:03 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 11 May 2026 23:26:03 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:124dbe049873037f973f01d877ec004bf4cd3ce5723d0b8f2067c58ad98137d6`  
		Last Modified: Fri, 08 May 2026 18:27:29 GMT  
		Size: 47.1 MB (47148023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ff8edb12d0e4a9c32ee4c3e2a16590b1236e70a297fedfff3debbb7297bb6e`  
		Last Modified: Fri, 08 May 2026 20:52:47 GMT  
		Size: 24.0 MB (24036421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8415cd4e27961a67eff09b7f658209a310ebce2d9bf3e1cf2773aa7e405d5e`  
		Last Modified: Fri, 08 May 2026 22:33:37 GMT  
		Size: 63.5 MB (63500120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ed1d14819ad17ebadc592338770e92592ab67cfa52d2e43878b8b4b1626a1a`  
		Last Modified: Sat, 09 May 2026 00:17:01 GMT  
		Size: 69.1 MB (69080942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccba99e1a42acaee11681a55a3c5791d533460e7e22dee60816a7d3a0553d4c0`  
		Last Modified: Mon, 11 May 2026 23:26:26 GMT  
		Size: 95.9 MB (95948201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa65f0829bb4f182876dd090e9075726dd257cf995011f53608e023dd59cc56`  
		Last Modified: Mon, 11 May 2026 23:26:33 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20260510-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:3e1d9f401e0eb1c12e1ce5c0a58dc52ac9fac323c3c94bfa55069f3e932f3afe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.4 MB (10357925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d84ae063fc7a14252134511ec23f501ccad4d90bdb24009d33ed4ede07b574a`

```dockerfile
```

-	Layers:
	-	`sha256:8255fad772acb4b8e17ebcf5a8ef607b13a8825d733ca27c3e9f43a655ed5096`  
		Last Modified: Mon, 11 May 2026 23:26:33 GMT  
		Size: 10.3 MB (10329539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e23c6413ca3601df1e10d1fe34d9a5396023287c2f3265bc789b5f0f9c8b541`  
		Last Modified: Mon, 11 May 2026 23:26:33 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json
