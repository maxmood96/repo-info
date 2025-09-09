## `golang:tip-trixie`

```console
$ docker pull golang@sha256:8c5a596c946d713bbf198ba0ca8730cfa7fc9905630cfab5720c0e197793a269
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
$ docker pull golang@sha256:6cfcb7400c83f08b50ef29d968fabe8b310c967e02eff75a61db145992fcba07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328368558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c56a0dc7b1e781b04e7141839b5b296c9a5332beb2b4929393dfa63e19199df`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 08 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:15b1d8a5ff03aeb0f14c8d39a60a73ef22f656550bfa1bb90d1850f25a0ac0fa`  
		Last Modified: Mon, 08 Sep 2025 21:12:52 GMT  
		Size: 49.3 MB (49279531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22718812f617084a0c5e539e02723b75bf79ea2a589430f820efcbb07f45b91b`  
		Last Modified: Mon, 08 Sep 2025 21:55:17 GMT  
		Size: 25.6 MB (25613635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401a98f7495bee3e8e6943da9f52f0ab1043c43eb1d107a3817fc2a4b916be97`  
		Last Modified: Mon, 08 Sep 2025 22:13:47 GMT  
		Size: 67.8 MB (67776756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bfeb328681e8eb50506c32236a8cd3783e34e57d64b7ccfeed0ba5d21fbfb4e`  
		Last Modified: Mon, 08 Sep 2025 23:28:35 GMT  
		Size: 102.1 MB (102071837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:981ded06cd7fc4272134c8fd8dd6fe01e98f582c7adaa60ab9166ea8bfd71723`  
		Last Modified: Mon, 08 Sep 2025 22:39:32 GMT  
		Size: 83.6 MB (83626642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e2c24e95175353f3f1daa4ad75a393ffb11cce50cd5707bcf7bc82f511de56`  
		Last Modified: Mon, 08 Sep 2025 23:28:41 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:7d08cb1104d400c85985461d16b7404d7670c4fbde5a7ea2ef4a51c3f83213cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10811946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02df4e075ece3c54785c9b9d8296c99c30c7bbccef0a07f05c6f7b4da290703c`

```dockerfile
```

-	Layers:
	-	`sha256:6e3e347d87859d93306c9bb73e26c600a05bbee131170a764144c1668eb596e5`  
		Last Modified: Mon, 08 Sep 2025 23:24:16 GMT  
		Size: 10.8 MB (10782934 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e8d33b3cdce602e34a68fb86e2fb0b5809ff6949d67506255562a4ba96a5693`  
		Last Modified: Mon, 08 Sep 2025 23:24:17 GMT  
		Size: 29.0 KB (29012 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm variant v7

```console
$ docker pull golang@sha256:f2f374b17ead9383ab3ce63890fc04dc4b55bb24e9d5783518a43ef40f935c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.3 MB (285255706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ff4a7e4bc2ea2d17662b48385b74b6d21e79a22a20d1abc63057231fc43a82c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
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
	-	`sha256:c8183d7d02c47a9b085b3d0bc6d67309b7fa4b7ef97cac1694dc0b5ea8b6ce9c`  
		Last Modified: Tue, 02 Sep 2025 17:26:14 GMT  
		Size: 80.5 MB (80512289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb66d9008f9a76950a9ccfbe90f3fb0d7ce9b75d3b9cb197dd869f061e91f2d`  
		Last Modified: Tue, 02 Sep 2025 17:26:09 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:8bf83abbd57f16eb7a904d37ef0ae2236a46d4a6f6d26f9684a2e2a4e331058f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10603330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:809696bb43e3f6ed446eae18f864a9ccf662afb7b70646d2aea65a0f050dc48a`

```dockerfile
```

-	Layers:
	-	`sha256:5848bb76be10fde344f690290e649f1eb2a8f8ae576a6f1679d23636ab437b95`  
		Last Modified: Wed, 03 Sep 2025 20:23:53 GMT  
		Size: 10.6 MB (10574199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ea0feee2408b987ba4db9f35399830fb7a1dabbfe1494648fbc619c89d6a9b4`  
		Last Modified: Wed, 03 Sep 2025 20:23:54 GMT  
		Size: 29.1 KB (29131 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:55433ebadc6fe79e2633310fb865180e49613d2810ff1746787c4b612241cb60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.9 MB (319913644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475af52a5a7e74fbde0fce18578c9270d8b971ac8105833dda8c76b1c11d35c0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
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
	-	`sha256:948ccd09d5c498d3bdd3015babafec64e8e01106fe6a739f268b131403fa7cbb`  
		Last Modified: Tue, 02 Sep 2025 17:24:20 GMT  
		Size: 79.5 MB (79463464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79007f8d2ad39915608c909cf5ee90fd0d4ac82557885aa4608653d9e1183acb`  
		Last Modified: Tue, 02 Sep 2025 17:24:05 GMT  
		Size: 124.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:226aee4674588688bbd0f869afffab8dc92a4e66794147d300792eda7746ce84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10927932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c220316cb762fbffa60957e41b877622ce7cd6cfc1c88af444a2318b4f83af57`

```dockerfile
```

-	Layers:
	-	`sha256:6be4756ad95c3770499caf0d6cfced2dff88937efff6e0af43cfa0fd45a3df7b`  
		Last Modified: Wed, 03 Sep 2025 19:08:45 GMT  
		Size: 10.9 MB (10898765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc4eb9f5e3680172250689a7524cc5f1acb2e8ac4eced519cbc82ebd0c701d8e`  
		Last Modified: Wed, 03 Sep 2025 19:08:47 GMT  
		Size: 29.2 KB (29167 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; 386

```console
$ docker pull golang@sha256:6b921ce5fae1f05bf319aa33b133a805075be7d4720411a1cf09c7f9bddaa83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.2 MB (330170173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43bcce50c3a5f3cf0acb5abcc61d4a1fb70476f34d5526388607694a3546dee`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 08 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 08 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 08 Sep 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c9dedb413b4079d00183873186dd00dae4338c64e4152f334d39473e37deb8c5`  
		Last Modified: Mon, 08 Sep 2025 21:12:41 GMT  
		Size: 50.8 MB (50794950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95e6ff4859ead75e29b179b0636a999dd68cde264f9c74ad8882d9d5dcfc9c7`  
		Last Modified: Mon, 08 Sep 2025 21:55:26 GMT  
		Size: 26.8 MB (26773510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4adf19bf3e6f542f3c00d3fc4bb83f2ec48ccc9675502c518d9eb368d0232a`  
		Last Modified: Mon, 08 Sep 2025 22:13:48 GMT  
		Size: 69.8 MB (69794254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0460ad7b36efddf6462702f1ca83a389309044a7e024a949d014b3b74f8cac03`  
		Last Modified: Tue, 09 Sep 2025 01:27:23 GMT  
		Size: 100.5 MB (100516758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518dceeeab292a9ac96f797a930543374e02f8a442c539c30c018a2f30d27fff`  
		Last Modified: Mon, 08 Sep 2025 22:30:33 GMT  
		Size: 82.3 MB (82290543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04dd84d330bdecdb3c2668c2100d7cdc7d07cc641db49f7e1a6725512ff4ea48`  
		Last Modified: Mon, 08 Sep 2025 23:17:09 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:482cb751be8876790bc8d9f012f7e29cc628319d56dbdc8f11e511102ae030c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10783168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f45306e73a0d478d91c191415b446d559b6f8c611ac02832a4f0d94efb4b593`

```dockerfile
```

-	Layers:
	-	`sha256:938e7b96cf8e88ac6bd3a3c53a1918bbe542f553924462247d6009632be5e6b5`  
		Last Modified: Mon, 08 Sep 2025 23:24:27 GMT  
		Size: 10.8 MB (10754200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f74b7b58bbaca96a2e6a76071c79a6ccc6db8531c1beb26012d01c990a3a96e`  
		Last Modified: Mon, 08 Sep 2025 23:24:28 GMT  
		Size: 29.0 KB (28968 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; ppc64le

```console
$ docker pull golang@sha256:a42a3355309e30b71d4070c64566b55ab8f3f3168bea66c54d43a9171f857756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.7 MB (326692471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9201ecd9dc3728d9d2ccba9a213a06fc669af7888044b7005d869229631f1cc0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
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
	-	`sha256:65adef97a585f4d6f34375efc6b453ef50bc737c051ef6eb9403cedd2e831eb9`  
		Last Modified: Tue, 02 Sep 2025 17:28:09 GMT  
		Size: 80.8 MB (80815917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4f938eb650cdd055cb3206ba4313b09ffb5169fa8d8b6747c466578679e443`  
		Last Modified: Tue, 02 Sep 2025 17:28:01 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:e02e53c007bb1aad719501944a506ede228573566e636066c11d95fbb817ca5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.8 MB (10803158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaad57b4b194c283a274d9255226c5f04b74843d6915613ef37c588aefbf7374`

```dockerfile
```

-	Layers:
	-	`sha256:ba40c99991c2aa5fa947ee5877aba30f00dbf707dc00dfe084064db222a418df`  
		Last Modified: Wed, 03 Sep 2025 20:24:19 GMT  
		Size: 10.8 MB (10774094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f328e7a8722f40e47aed7b3c0a50983f54e766ac8715bdf563118050205a0e1`  
		Last Modified: Wed, 03 Sep 2025 20:24:19 GMT  
		Size: 29.1 KB (29064 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; riscv64

```console
$ docker pull golang@sha256:4ea11b5fe699cb5fd148f11e6c687d59f1718368fef00df6bdb363cf6116d7b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.8 MB (351806425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c7169822cd522d76403008e9c1eee45e885ec9b15d4baf49b818ac2dd3e50d3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
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
	-	`sha256:293eb689539c18522b5644ece27c44567aa0a4ab5ae7b74edd76c1cea9f0f71c`  
		Last Modified: Wed, 03 Sep 2025 05:13:46 GMT  
		Size: 80.9 MB (80891135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fe1353d17ab68f294e17de00736dfed8838e5854d8e23bf806821af406411f`  
		Last Modified: Wed, 03 Sep 2025 05:13:41 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:762df54fc334ea9e1a213c0cd7d4bfc398e08bf25f8c83712bd5d2e3c31f6c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.9 MB (10876997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e52a9ee6e0d0e6648a61e85a80d56788665333f1e0f56ca58800877cd7d0f89`

```dockerfile
```

-	Layers:
	-	`sha256:b0288d4c61a3d658fb6c3358ac72589a79da31e073d2656d5caa2c0c6aea5469`  
		Last Modified: Mon, 08 Sep 2025 08:23:45 GMT  
		Size: 10.8 MB (10847927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dee56feb939a056b7dd1811ce4dd8fbfe3416e44b5b54d18a3fd321dde222649`  
		Last Modified: Mon, 08 Sep 2025 08:23:46 GMT  
		Size: 29.1 KB (29070 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-trixie` - linux; s390x

```console
$ docker pull golang@sha256:956dd0b727257342b7fe9137afb0fd8ecb1779fc893149046c986a85ab0d83ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.6 MB (302645115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36fcd75baeab128fcf4dabaf3d7df0070aa5703518c762ce751142b569f3e7a2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Sep 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 01 Sep 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Sep 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Sep 2025 05:23:20 GMT
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
	-	`sha256:c97116a214b647f741495fbb3bc9e147a964980fd8a45718f9a7cbf059b8ee0a`  
		Last Modified: Wed, 03 Sep 2025 20:23:10 GMT  
		Size: 75.9 MB (75869165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d5b2317c0e6d0b707d21864c7e46b8277ee225d4365f7839ca2960a88e985a`  
		Last Modified: Thu, 04 Sep 2025 01:06:05 GMT  
		Size: 82.0 MB (82031053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b67a92a60630b98164746d1c10c9fc2159f8b4f192df7b15d1631967e1cd30c`  
		Last Modified: Wed, 03 Sep 2025 21:17:18 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-trixie` - unknown; unknown

```console
$ docker pull golang@sha256:eb53b337e93ca9dc32229fd486640dce6431769d5eb0356783e4e7de9a1f3dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10617717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10fc574ff2a7b64d8a217d07bb1c4aea797289745cb14f4c069bd46d00ac81ce`

```dockerfile
```

-	Layers:
	-	`sha256:b2c374e738cf17a9c10437ee253e29dda44633ff8f136744e24fcc03498acd42`  
		Last Modified: Wed, 03 Sep 2025 23:24:50 GMT  
		Size: 10.6 MB (10588710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b153d02d6bf525fdbfdd7c91eedb2e4d20e88855ca1a140692bd2b2825067e11`  
		Last Modified: Wed, 03 Sep 2025 23:24:51 GMT  
		Size: 29.0 KB (29007 bytes)  
		MIME: application/vnd.in-toto+json
