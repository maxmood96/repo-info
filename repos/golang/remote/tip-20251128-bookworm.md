## `golang:tip-20251128-bookworm`

```console
$ docker pull golang@sha256:5fb4e7ba4b0c6ae667a8a0e71266a6b4c699304feae419bf1417fb4ce936fa24
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

### `golang:tip-20251128-bookworm` - linux; amd64

```console
$ docker pull golang@sha256:9d6b5a6838157748cc85ab160770c3de694754b5f7d2dae349dd8ba91a924fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.4 MB (323430272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17fd5b52c25def3494c9d0e431c2db81dd4f3a81333ea2a32834ea45f49fb539`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 06:38:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Dec 2025 23:55:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Dec 2025 23:57:08 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Dec 2025 23:57:08 GMT
ENV GOPATH=/go
# Mon, 01 Dec 2025 23:57:08 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Dec 2025 23:57:08 GMT
COPY /target/ / # buildkit
# Mon, 01 Dec 2025 23:57:10 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Dec 2025 23:57:10 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:708274aafe49b02dddc66f97a5c45bb0b8fcf481ce6b43785b11f287fd4e4e1b`  
		Last Modified: Tue, 18 Nov 2025 02:26:32 GMT  
		Size: 48.5 MB (48480761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdff261ed5cee6fd4e729e68c2831a0abc6c7c017569ab45dfd2240bcc3712d`  
		Last Modified: Tue, 18 Nov 2025 05:09:33 GMT  
		Size: 24.0 MB (24029348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078b2eece9b24f617524f986db4dd04f977e3e7d6fe15a9088a584147bc6ba05`  
		Last Modified: Tue, 18 Nov 2025 06:38:36 GMT  
		Size: 64.4 MB (64396262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5deeae8ddcd000a56af182e4b45be0d0af4fa3a555285369af4a3701c318f0`  
		Last Modified: Mon, 01 Dec 2025 23:57:52 GMT  
		Size: 92.4 MB (92410511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da39c78191c9be13a8adf6d46ca789532fb58292a09979c1057608fd7cf7b31`  
		Last Modified: Mon, 01 Dec 2025 23:57:34 GMT  
		Size: 94.1 MB (94113232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbedc3a8df4a16bed00e837624d61249114c6442dda6e6234edd5cac383e115`  
		Last Modified: Mon, 01 Dec 2025 23:57:31 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251128-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:8cc0048773e8ee3b5459c2ef51d6afee5622aec4f9ca8af2df50411f3d462bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10524776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68e03ff10eda7d89d741b1dede47d6d6e79750fe0e6dab4d6b4cd676b9bd4f9`

```dockerfile
```

-	Layers:
	-	`sha256:fe82a9ca4e3e034c491bace2af32fac5d87a49f25131a91b7997917fb9b29824`  
		Last Modified: Tue, 02 Dec 2025 00:24:17 GMT  
		Size: 10.5 MB (10496390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e49b98a75c54ec3c2c50ddccdf96f4fa05e3db1961c8043cf0ed736c0f5db34`  
		Last Modified: Tue, 02 Dec 2025 00:24:18 GMT  
		Size: 28.4 KB (28386 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251128-bookworm` - linux; arm variant v7

```console
$ docker pull golang@sha256:3f27004bdbce10c62f97721c551b11b26217a3de101135a51737084f19698258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.3 MB (282257924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f75d5efeb79f2294c98777fc751c52093b8439d1501f2062f352c0bdac9693`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:57:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:27:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Dec 2025 23:58:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 00:01:02 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 00:01:02 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 00:01:02 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:01:02 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 00:01:08 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 00:01:08 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0158bd5d23c60bb6a03530bd01d88f6a45760dc4a0fabd84d18325160d4b02c9`  
		Last Modified: Tue, 18 Nov 2025 01:13:52 GMT  
		Size: 44.2 MB (44196124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b067c08defb5dc0221b7289b52ff90ebfcb1222dbf4e40ab567aa11a08488b79`  
		Last Modified: Tue, 18 Nov 2025 03:57:49 GMT  
		Size: 21.9 MB (21934687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b6eb0fb27a6d99b6b7a2a32ab126d30b16ebd113a3a3e174d37a032cde9bd1`  
		Last Modified: Tue, 18 Nov 2025 05:28:17 GMT  
		Size: 59.7 MB (59652137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84172fbd1cac40ced23a7a9e2ec5559d3cfcecbea0f484d23e714074f2e7b9e0`  
		Last Modified: Tue, 02 Dec 2025 00:01:47 GMT  
		Size: 66.3 MB (66276474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb1234642b8e59fff163165b022247bc43b3cbce7229072851dbefb3454b51c`  
		Last Modified: Mon, 01 Dec 2025 23:59:32 GMT  
		Size: 90.2 MB (90198345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f718f66ca8fcba794d9615880d81df690fa13dd3d8c1288cb72c9bc876f26d`  
		Last Modified: Tue, 02 Dec 2025 00:01:38 GMT  
		Size: 125.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251128-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:94a5f08320e93d25aaa24d82e1ddda1d915e47c7edf478987c8a914144a7192f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10331584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed10a69f8224bf24916cd2bd0319cc2407f1020cd8077fa86a7d9bfd5d2efe90`

```dockerfile
```

-	Layers:
	-	`sha256:3ec48a1956526016269097b887be30c18f2e8233e33bf700a72ef356f07c5d32`  
		Last Modified: Tue, 02 Dec 2025 00:24:37 GMT  
		Size: 10.3 MB (10303086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db26e108255c19db51f519a6e849b2ed0715e1f5aa2f22ff78cd5542e293875e`  
		Last Modified: Tue, 02 Dec 2025 00:24:38 GMT  
		Size: 28.5 KB (28498 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251128-bookworm` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:997f87d507f49f0f9de23c3e6efe6df90b1c917a52d9f6425b75a3bc051ca598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.0 MB (312031393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3fe0af7052f3a626ab88b76da50b4125276e7130add9ac077af70bb8992840`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 03:22:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:38:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Dec 2025 23:57:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
ENV GOTOOLCHAIN=local
# Mon, 01 Dec 2025 23:56:47 GMT
ENV GOPATH=/go
# Mon, 01 Dec 2025 23:56:47 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Dec 2025 23:56:47 GMT
COPY /target/ / # buildkit
# Mon, 01 Dec 2025 23:59:26 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Mon, 01 Dec 2025 23:59:26 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:feee3ddb262f9d1c832461cb752127e86e2073fdb517f793f53d91bd737b7983`  
		Last Modified: Tue, 18 Nov 2025 01:12:43 GMT  
		Size: 48.4 MB (48359138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193223eb7a0b7291c1c5cd557aa1bd6fc52f0319e92b514dcf57a6476b6ac98d`  
		Last Modified: Tue, 18 Nov 2025 03:22:37 GMT  
		Size: 23.6 MB (23598320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25d805ffe4d6247a3ab7494e663f6ae84d04e36c5270a200f1d1d34db32a26c`  
		Last Modified: Tue, 18 Nov 2025 05:38:35 GMT  
		Size: 64.4 MB (64371414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd778373a4855ba7be345bf5d5e6b1d1f9326a83215dafcbf9c739d82ba13008`  
		Last Modified: Tue, 02 Dec 2025 00:00:18 GMT  
		Size: 86.5 MB (86490955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5ad4011b8323fe08610380aae994bb765f6965dfc1e0886815c89502e86415`  
		Last Modified: Mon, 01 Dec 2025 23:57:41 GMT  
		Size: 89.2 MB (89211407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687ae42560e220cf6ddf2d9454dbf740ebe69258934010d17185afe2dbb06b25`  
		Last Modified: Mon, 01 Dec 2025 23:59:57 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251128-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:ae23b84621c039a0a3b4700d171ba86d7a8041845e825c41fbadcbe2cecb3241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.6 MB (10552736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd4a2ec0e96ab3346317cf174fab3bff742339e071f3522bec67f9fd5b38608`

```dockerfile
```

-	Layers:
	-	`sha256:c6e95e7fcf38b756cd4786b38912053d67247e4f03210577014d924765aed6d9`  
		Last Modified: Tue, 02 Dec 2025 00:24:47 GMT  
		Size: 10.5 MB (10524214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89607c42c74225fe515b6f44fcb32731d26b54d9a3f2ab3fe3233c47bb9a0679`  
		Last Modified: Tue, 02 Dec 2025 00:24:49 GMT  
		Size: 28.5 KB (28522 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:tip-20251128-bookworm` - linux; 386

```console
$ docker pull golang@sha256:9f594f07bc86ba7c20dafd15fa492159bd9a224561d415249c60bcc573ac2758
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322433624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac24d8cb5570c7bfebee05ec683887608470e0dd317cb1022c59d7ad7931778`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 02:56:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 04:08:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Dec 2025 23:58:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		g++ 		gcc 		libc6-dev 		make 		pkg-config 	; 	dpkgArch="$(dpkg --print-architecture)"; 	if [ "$dpkgArch" = 'arm64' ]; then 		apt-get install -y --no-install-recommends binutils-gold; 	fi; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Dec 2025 00:00:10 GMT
ENV GOTOOLCHAIN=local
# Tue, 02 Dec 2025 00:00:10 GMT
ENV GOPATH=/go
# Tue, 02 Dec 2025 00:00:10 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Dec 2025 00:00:10 GMT
COPY /target/ / # buildkit
# Tue, 02 Dec 2025 00:00:12 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 02 Dec 2025 00:00:12 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:0c53f2648d459c8aba7ef684ca52b0fa14af1ef11e0bff818a5e40a62573ca73`  
		Last Modified: Tue, 18 Nov 2025 01:13:02 GMT  
		Size: 49.5 MB (49466866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1ac37f50532a7306717e1be2f4760a581740981b55bfee41fb74edf971bbbb`  
		Last Modified: Tue, 18 Nov 2025 02:56:28 GMT  
		Size: 24.9 MB (24864418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931488dec4785216610c9f2c064b20b308e9839859b58a6fb0171606dd6f0514`  
		Last Modified: Tue, 18 Nov 2025 04:08:56 GMT  
		Size: 66.2 MB (66233867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18370f8dbc6bd2470a85a6bdacb5fdc9847eaf6593d777369f0c29f519b5a265`  
		Last Modified: Tue, 02 Dec 2025 00:00:52 GMT  
		Size: 89.8 MB (89839910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64bdcb75a4ff23e4aa0af6e0121aa066fd65b3acbe84f5a324aa319fab9e281`  
		Last Modified: Tue, 02 Dec 2025 00:00:09 GMT  
		Size: 92.0 MB (92028405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6cfa0516dc1d03b3998e991f2b446965702fef466e15be946c1e06ac6dfaf1`  
		Last Modified: Tue, 02 Dec 2025 00:00:42 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:tip-20251128-bookworm` - unknown; unknown

```console
$ docker pull golang@sha256:17735918446ffac931afa55488fedcb23019eec14cde24985b959a8a4868ac39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10504322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:175f69b424f5ad9817f3afaa49a3cd2a1a596a0a283244b711fbf28745fafaa6`

```dockerfile
```

-	Layers:
	-	`sha256:2f137391b0a0d51c9f9644fdd1ae7a363fc05099acfe3d3ffeeaf1aeaac8956c`  
		Last Modified: Tue, 02 Dec 2025 00:24:58 GMT  
		Size: 10.5 MB (10475971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3dfeb3ac46907b5094033b03c57238b01b0a4831039dd62cacb8bcd49086e76e`  
		Last Modified: Tue, 02 Dec 2025 00:24:59 GMT  
		Size: 28.4 KB (28351 bytes)  
		MIME: application/vnd.in-toto+json
