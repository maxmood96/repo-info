## `golang:tip-20250906-trixie`

```console
$ docker pull golang@sha256:30c02db7ece1dd34f34e3b7e57c6202d6bc23e89758aebf46dffe40ade476b3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `golang:tip-20250906-trixie` - linux; amd64

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

### `golang:tip-20250906-trixie` - unknown; unknown

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

### `golang:tip-20250906-trixie` - linux; 386

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
		Last Modified: Mon, 08 Sep 2025 22:43:23 GMT  
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

### `golang:tip-20250906-trixie` - unknown; unknown

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
