## `golang:tip-20250413-bullseye`

```console
$ docker pull golang@sha256:c3236e6910ee36fb2e211c9fc228873ab2d8a2f3ffa285372860967e5c4795bd
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

### `golang:tip-20250413-bullseye` - linux; amd64

```console
$ docker pull golang@sha256:0f7234f3fac2156afb70de194d6b52796321ac71cc80543746422bf2614fa488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.3 MB (336345186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14beb25355c41e4a022f4b2e274adacee3e0a24506990450276064fd27dafddd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 14 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
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
	-	`sha256:9edd975f44cbaf32f44507d954566e4e914b573eb99b755fb3b967ec3d780343`  
		Last Modified: Mon, 14 Apr 2025 21:51:40 GMT  
		Size: 86.0 MB (86000759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013504ab5187d636f1901fcb4a6eeb2b2ad7ca1cea03792606973678944bf0e4`  
		Last Modified: Mon, 14 Apr 2025 21:51:15 GMT  
		Size: 126.1 MB (126077078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d9e3a7f7990500950cc2e28ce7db61cfadbbc1739bdf959cdba3fb7409d5e7`  
		Last Modified: Mon, 14 Apr 2025 21:51:38 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250413-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:dc769f6ce170cadc076d75a84a0d834722f40db15c9fec5a727dbf877457a6b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10293404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e37979f9b018ea90a4210bcb99dd7611a7b445bbc0d4d36f787cfb2c2a9df45f`

```dockerfile
```

-	Layers:
	-	`sha256:946298b8fd968cf5051aac8b8479f98d689091ac4d96b8119a1e30f0703b590a`  
		Last Modified: Mon, 14 Apr 2025 21:51:38 GMT  
		Size: 10.3 MB (10266343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c644dc207dff178cdf6731859458962ed417bfc2e8ade38ca05d0f9990c81d57`  
		Last Modified: Mon, 14 Apr 2025 21:51:38 GMT  
		Size: 27.1 KB (27061 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250413-bullseye` - linux; arm variant v7

```console
$ docker pull golang@sha256:7d6f0eca5f947e6dc2144bc449d7d408414d21eb46abcaf10953187880a34dda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.6 MB (300565472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d09049ac3f8e377b1adfaf131b00517dc92d2001d304d09d9a9f5a70145bbc38`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 14 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:8c2fc9e6d23f3debfa68416a2b96331b92d563b20272933315ecfbbada38e955`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 49.0 MB (49031449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525b68fed12d763a57f1b020aa1579673112de80a5b780b5ffaa045109c81f23`  
		Last Modified: Tue, 08 Apr 2025 07:38:26 GMT  
		Size: 14.9 MB (14878713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909681b45fdfcbd0bfebc28d96cd1bdab32fd85e3af6788b49d9cb80e8ff865a`  
		Last Modified: Tue, 08 Apr 2025 17:30:33 GMT  
		Size: 50.6 MB (50624452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cc995e80cedd9d30db7ba6d1ae52e5693d2c40c74ff9101649c68046e8319c`  
		Last Modified: Tue, 08 Apr 2025 20:43:27 GMT  
		Size: 64.9 MB (64922622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e131e20eff5d97e9796f801f5335249fcb3b27557a67cdb1b0533cbc32974fff`  
		Last Modified: Mon, 14 Apr 2025 21:52:15 GMT  
		Size: 121.1 MB (121108078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05cc21f7ca140e81ea70a6fc004b82e56e22b678c1cd9e9fa81be4238da0b24b`  
		Last Modified: Mon, 14 Apr 2025 21:56:15 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250413-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:f4d8c3baf1f1934fc256b27865d6dd1b64135e583b08695606b5ca257ff90435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.1 MB (10099852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62eac8fe9602e4fc5f779f04f01fd9108b10aa0e62caed9ac1a5b00ad0401c8f`

```dockerfile
```

-	Layers:
	-	`sha256:fed6dbf16985c769bd56382f72d2c2020dfbd9c85dc5abd1f885ad5113bea25c`  
		Last Modified: Mon, 14 Apr 2025 21:56:16 GMT  
		Size: 10.1 MB (10072683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b073399f59ca7aa78cf9630b4560c81bcbeec76b135e99957072ffcc55d8564`  
		Last Modified: Mon, 14 Apr 2025 21:56:15 GMT  
		Size: 27.2 KB (27169 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250413-bullseye` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:9b26aa55c44c34b8c9ec4b172946840ac8058072499e9bdee32b6aec38eaaaab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.0 MB (323037370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9abac7ad9de4ea2b1d70760ea8534013da1f2e06676362fa922af7030c0c0d4e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 14 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
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
	-	`sha256:b066ec7b453f1f7a4cbf31adea4a73d091a7499693ce31c56205980d8778c9c9`  
		Last Modified: Mon, 14 Apr 2025 21:52:34 GMT  
		Size: 81.4 MB (81414208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b206f4f1851ae209ce8b8172ce5c71a21bf857b5a5fc8341f94dabec27aaed`  
		Last Modified: Mon, 14 Apr 2025 21:49:56 GMT  
		Size: 118.8 MB (118769688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb025503c61a09267fc777ba8b58d467bcc6994f0ab84eadbb8f869bfdc7f40`  
		Last Modified: Mon, 14 Apr 2025 21:52:31 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250413-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:82cdca6a15923ebfd6d883fe5e0fd9300d01d921770d540d90777785e95d5920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10295112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46dd6cc944b3be1b100626ad925dc3b7a4f10a34b07cc80bc70978d701c06e67`

```dockerfile
```

-	Layers:
	-	`sha256:055126a06c93a32696465ec96f351da029ec55ceacc13ad4c1ffa5750de93cf4`  
		Last Modified: Mon, 14 Apr 2025 21:52:32 GMT  
		Size: 10.3 MB (10267915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38e28779e57591033ffe49d95edd328465339bbece331c7e1246e3d34683a0ec`  
		Last Modified: Mon, 14 Apr 2025 21:52:31 GMT  
		Size: 27.2 KB (27197 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20250413-bullseye` - linux; 386

```console
$ docker pull golang@sha256:426c72b444e9441901698a126511d7dd4a34870207d7c489772a38a0ec89258c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.7 MB (338675414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e66182b5dd71c2a78be8d3e19a817c448ba45f24c4890afacbe6e125af74566e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOTOOLCHAIN=local
# Mon, 14 Apr 2025 05:23:20 GMT
ENV GOPATH=/go
# Mon, 14 Apr 2025 05:23:20 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Apr 2025 05:23:20 GMT
COPY /target/ / # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 14 Apr 2025 05:23:20 GMT
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
	-	`sha256:cd3639ed7f0d8b0ff999199fb0d7dbb5db588e9f3259d4ba063b45d5259e6df2`  
		Last Modified: Mon, 14 Apr 2025 21:52:07 GMT  
		Size: 87.4 MB (87426534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a1236535bef233193363d469e87ef11dfa5b282a53e3685fad2f41147bdd6d`  
		Last Modified: Mon, 14 Apr 2025 21:51:51 GMT  
		Size: 124.3 MB (124250003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34247ef38b9882b2b93ddad85af1faf5aa5e05b661b389d8c1240d1a08845abb`  
		Last Modified: Mon, 14 Apr 2025 21:52:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20250413-bullseye` - unknown; unknown

```console
$ docker pull golang@sha256:8775bf297078b1d67595fdaf931d6d454fa631f439b04522fc0618f782101707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10283162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce4082abcceb6ecff77c8df11d774c57bcf79ebfb9cf2f87e06c92c5c198bf8d`

```dockerfile
```

-	Layers:
	-	`sha256:735ff593503144e1666ee81d66d57a1b3057482c5c913c4131a97c15f4a4f190`  
		Last Modified: Mon, 14 Apr 2025 21:52:05 GMT  
		Size: 10.3 MB (10256134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31cf086ab17f38c11ef541803bd71fa24ec8e2d2fc1be9fe56c8e44dbb69f8df`  
		Last Modified: Mon, 14 Apr 2025 21:52:05 GMT  
		Size: 27.0 KB (27028 bytes)  
		MIME: application/vnd.in-toto+json
