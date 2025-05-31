## `golang:1-alpine`

```console
$ docker pull golang@sha256:b158e66c797e8939c17eab2fdc3783eb9558845217d76c29c2632a2d7d2bd349
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `golang:1-alpine` - linux; amd64

```console
$ docker pull golang@sha256:26e5827d0bcee61db5b976014a99018c1ff8f8e6248de8f3ee85bf12229c4b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83073483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee6ed942a4adbd5fff6accec75d55baab0125eb21f31c26144ba0e8d3da49914`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 20:49:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 30 May 2025 20:49:27 GMT
ENV GOLANG_VERSION=1.24.3
# Fri, 30 May 2025 20:49:27 GMT
ENV GOTOOLCHAIN=local
# Fri, 30 May 2025 20:49:27 GMT
ENV GOPATH=/go
# Fri, 30 May 2025 20:49:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 20:49:27 GMT
COPY /target/ / # buildkit
# Fri, 30 May 2025 20:49:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 30 May 2025 20:49:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Fri, 30 May 2025 18:04:24 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965f7aff83c4fc694f4ad4c3166a22df4df5eb2caf149cfdbe8a2bb6af7ebdb5`  
		Last Modified: Sat, 31 May 2025 00:05:13 GMT  
		Size: 294.9 KB (294905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b00dc8dfbaa6cd7e39d09d4f1c726259b4d9a29c697192955da032f472d642`  
		Last Modified: Tue, 06 May 2025 19:25:20 GMT  
		Size: 79.0 MB (78981573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ee4818046b39b38d9211e2793dfd046836a88da1dcbf0df5855493ba4c368a`  
		Last Modified: Sat, 31 May 2025 00:05:13 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:e51a6dfa9305cf03313caee0c0b2867bf012bd25b76ce72f865eece72da5b52a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 KB (239917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f47e4ef4e0d9c1d9f536379dd9d9ec5914ad8bc41e291954bf1b98392cf8b1ea`

```dockerfile
```

-	Layers:
	-	`sha256:e12d90bc2f86ac5bba051245b53a70bada6c42edeea1902dd9a63b5742514eff`  
		Last Modified: Sat, 31 May 2025 00:05:13 GMT  
		Size: 213.8 KB (213847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12383393b6275a25498526ba3041e6b92159714223c5f481cfc03777285474e3`  
		Last Modified: Sat, 31 May 2025 00:05:13 GMT  
		Size: 26.1 KB (26070 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; arm variant v6

```console
$ docker pull golang@sha256:362c0d476fa31d0cfee39aaa1015761b702fd189200144139a0c0325a060a6b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.9 MB (80941883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a116606f1351d6775d0742da9f8bf52420caca1e99e64d0018ac186d43fa2a9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 20:49:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 30 May 2025 20:49:27 GMT
ENV GOLANG_VERSION=1.24.3
# Fri, 30 May 2025 20:49:27 GMT
ENV GOTOOLCHAIN=local
# Fri, 30 May 2025 20:49:27 GMT
ENV GOPATH=/go
# Fri, 30 May 2025 20:49:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 20:49:27 GMT
COPY /target/ / # buildkit
# Fri, 30 May 2025 20:49:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 30 May 2025 20:49:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Fri, 30 May 2025 18:04:31 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade1a66512d0d840a56a8c3fcd61678c4f71bc9949c18f7ee679feb7494b20e0`  
		Last Modified: Sat, 31 May 2025 00:11:16 GMT  
		Size: 296.3 KB (296292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e897536fb13ccfca87cac1110a2b716225d73570f890064e1f163d9b5875cd3a`  
		Last Modified: Tue, 06 May 2025 19:25:09 GMT  
		Size: 77.1 MB (77144504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f98c558f4395907f5145a02e200a6bcb6b27304169e896bf74fd0156c4e4d92`  
		Last Modified: Sat, 31 May 2025 00:11:16 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:9e349414cbfc896b3b3da9a2a6251958ad3ad193845fe3bfd766627abcf787f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (25988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d9e6ad0179205e29aa7acda3c5df536ba59ca9ace898b98e401575595fa4a4`

```dockerfile
```

-	Layers:
	-	`sha256:4ed2806a76c3f9fde7e73fedd679ce87d66d62c26c4a82542b7b1838d345b0cb`  
		Last Modified: Sat, 31 May 2025 00:11:16 GMT  
		Size: 26.0 KB (25988 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; arm variant v7

```console
$ docker pull golang@sha256:2de8bf47149280ad3f622f558e0de10d61632299e3ea02f22159af6780307f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.5 MB (80537920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93e59e4ba1636ad3fc55005e01088f978efe02858a16581059e0c8642f007394`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 06 May 2025 18:58:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 May 2025 18:58:00 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 18:58:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 May 2025 18:58:00 GMT
ENV GOPATH=/go
# Tue, 06 May 2025 18:58:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 18:58:00 GMT
COPY /target/ / # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 May 2025 18:58:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77833ee7d3adeaa883db3f960686c769232a931d3442cfcc8bb6a4790098520`  
		Last Modified: Fri, 14 Feb 2025 21:47:46 GMT  
		Size: 295.2 KB (295199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f32012e82345c04270d988b1e520857596a775a43ec4b22744ab73bea39d15b`  
		Last Modified: Tue, 06 May 2025 19:25:39 GMT  
		Size: 77.1 MB (77144440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c23a49fcd1db2181cfd2a2ea5f43879dc7c393ddaf883fdbeca06dced4512fb`  
		Last Modified: Tue, 06 May 2025 19:27:05 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:0a50d0472623a4834237cbbf0ef3114aed0a702664507831a32c89b1ac6c7fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 KB (237713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:530ed125ca0fb5607d8cc0587202c3f01f177892d11ca2184623a72949c14246`

```dockerfile
```

-	Layers:
	-	`sha256:d91b8a8a4e9fbb08e3d542a709f0b2cb3f5383992ba310ce59353d46ca56e86f`  
		Last Modified: Tue, 06 May 2025 19:27:05 GMT  
		Size: 211.5 KB (211509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af7366a3157db1a92e08bdd09aa8c7540bda2ad21d1ff85aa7aa5b89e2b3e5df`  
		Last Modified: Tue, 06 May 2025 19:27:05 GMT  
		Size: 26.2 KB (26204 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; arm64 variant v8

```console
$ docker pull golang@sha256:fc5d0e129a17eb8c40c872b3337f548ed003ae93e658b647761562e17ff3058d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79521615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8767db7742a203b950bed890fe630eeda2e41b716cd841866bb7ce821fff8fa0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 06 May 2025 18:58:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 May 2025 18:58:00 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 18:58:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 May 2025 18:58:00 GMT
ENV GOPATH=/go
# Tue, 06 May 2025 18:58:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 18:58:00 GMT
COPY /target/ / # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 May 2025 18:58:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a2f34450ab6893f9de21e818c13da20ab31676614598eac0352797a074049df`  
		Last Modified: Mon, 05 May 2025 21:13:39 GMT  
		Size: 297.9 KB (297874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae64884db43f30f8dbc9ec3362124d99c8bad23b957254ac52fb30413bd14a7`  
		Last Modified: Tue, 06 May 2025 19:25:16 GMT  
		Size: 75.2 MB (75230554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bdee32b0d6cb9863bfa2b0996b359506fd0a938301ae9bfdef13cb97a59b1e8`  
		Last Modified: Tue, 06 May 2025 19:26:19 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:48697ee9baa1ca09156b96e0422e735d1aad96237f2117bc6e559ee8d7167aba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.8 KB (237833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20fcc6393775ad9ac4d279f33191af7ce562efb2a45c04670d34c502cdc3b6e4`

```dockerfile
```

-	Layers:
	-	`sha256:bb3b0cfac622b860d5d6f582358d7bb86177df726153ca31f4c21ba6e1e7d987`  
		Last Modified: Tue, 06 May 2025 19:26:19 GMT  
		Size: 211.6 KB (211581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f829cb88d81b2ee3bc35cc91a2f7448e78a35c77dfbd82f1b3cb7f4e034dc26`  
		Last Modified: Tue, 06 May 2025 19:26:19 GMT  
		Size: 26.3 KB (26252 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; 386

```console
$ docker pull golang@sha256:bebe32d43d3e2296976f14d0f1504d954c5dfef32e921b79afeb2cb0b02c4f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.8 MB (80811681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ae29c1cc5f88b2435d74982dca2ae9aa805dfb806f2b46562fafffab162974a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 20:49:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 30 May 2025 20:49:27 GMT
ENV GOLANG_VERSION=1.24.3
# Fri, 30 May 2025 20:49:27 GMT
ENV GOTOOLCHAIN=local
# Fri, 30 May 2025 20:49:27 GMT
ENV GOPATH=/go
# Fri, 30 May 2025 20:49:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 20:49:27 GMT
COPY /target/ / # buildkit
# Fri, 30 May 2025 20:49:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 30 May 2025 20:49:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Fri, 30 May 2025 18:04:26 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77266b52f087863e4db36cbc21961211045b93b75e09c4620d9241c76f9c8214`  
		Last Modified: Sat, 31 May 2025 00:05:03 GMT  
		Size: 295.6 KB (295615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db714197af43811f01d03462392675e848884e82b9483811c21c83a08d3e7834`  
		Last Modified: Tue, 06 May 2025 19:25:35 GMT  
		Size: 76.9 MB (76899879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a4956705ca371b40f082195060a46eee6a7043cf5c2e0a1c8ad5c5aaf52d75`  
		Last Modified: Sat, 31 May 2025 00:05:03 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:d0e1fa470f6820355afa1d7396ad9842fdccdc292f9f0c9c69c3bfe53ef32b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.8 KB (239780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824ab379ce6eb5ffb3e3dadc9d2c69f4c4a916c87d04d5d0c2c809ff9ab3bebc`

```dockerfile
```

-	Layers:
	-	`sha256:36b47b580849ba7bfb4f91aae77d62468d14661ddad8b16dc12f4d6782a7c203`  
		Last Modified: Sat, 31 May 2025 00:05:03 GMT  
		Size: 213.8 KB (213766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5710f964d84b7f393e534c8ce7bfc8ccbfb699bf58af721d8e782d49d1b4b7af`  
		Last Modified: Sat, 31 May 2025 00:05:03 GMT  
		Size: 26.0 KB (26014 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; ppc64le

```console
$ docker pull golang@sha256:939dc6763ec3903cd6780e0845b8397f884c375aa120b442d76a7f9df35858fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.6 MB (79573158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f68de6cb9520e5efe955d45e639919d03bdf7e9566a63ad5e2340829344a5f1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 20:49:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 30 May 2025 20:49:27 GMT
ENV GOLANG_VERSION=1.24.3
# Fri, 30 May 2025 20:49:27 GMT
ENV GOTOOLCHAIN=local
# Fri, 30 May 2025 20:49:27 GMT
ENV GOPATH=/go
# Fri, 30 May 2025 20:49:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 20:49:27 GMT
COPY /target/ / # buildkit
# Fri, 30 May 2025 20:49:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 30 May 2025 20:49:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Fri, 30 May 2025 18:14:22 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a187c79905be9977c8b81d03082bbff0333d20fe9ac9a7740864c66f7e0e5c7a`  
		Last Modified: Sat, 31 May 2025 00:09:46 GMT  
		Size: 298.3 KB (298320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f44821f8171df650a338e8fdd3b017af075382eee8cc2d34256864c2264897`  
		Last Modified: Tue, 06 May 2025 19:26:37 GMT  
		Size: 75.5 MB (75544493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a20b670a8973fed72b0d8abbd15c7fc0ccf2f293ca8e609a29f3ddaa23b7b56`  
		Last Modified: Sat, 31 May 2025 00:09:46 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:a32f5ab9e476a5234e0d5abd941e9849052263ecdc995f74f9c27a84ac653fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.1 KB (238132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0453fdf58579a2588500c76524e57440dd7517f24b9da7660d506985ef0d9cc0`

```dockerfile
```

-	Layers:
	-	`sha256:e22d562605c9ebd416546252e6e9704946628865d200c7e20453310d896d48a8`  
		Last Modified: Sat, 31 May 2025 00:09:46 GMT  
		Size: 212.0 KB (211990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39de5cae760974f5c02bd7f1f1b7644c06a64cec08c639df08804be1031364b9`  
		Last Modified: Sat, 31 May 2025 00:09:45 GMT  
		Size: 26.1 KB (26142 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; riscv64

```console
$ docker pull golang@sha256:bf55136b05c9ddadbf937d94f039123465dda09baebbd89b32333aa3fce68dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (79960818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75fdccd10d437aa7cffa54aeb2cda5f4a9c8e9502546e43fc4eb123b241ef87`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 06 May 2025 18:58:00 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Tue, 06 May 2025 18:58:00 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 18:58:00 GMT
ENV GOTOOLCHAIN=local
# Tue, 06 May 2025 18:58:00 GMT
ENV GOPATH=/go
# Tue, 06 May 2025 18:58:00 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 06 May 2025 18:58:00 GMT
COPY /target/ / # buildkit
# Tue, 06 May 2025 18:58:00 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Tue, 06 May 2025 18:58:00 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd81befb40433dc7da0b53543acafce5d4aa75d9a2bc5815536bad6b9db1682b`  
		Last Modified: Sun, 16 Feb 2025 05:52:00 GMT  
		Size: 295.3 KB (295346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4ce4a757d65543eb38e825fd00a5434bd6efef264c5b31052eab1a8e5fa09b`  
		Last Modified: Tue, 06 May 2025 19:30:07 GMT  
		Size: 76.3 MB (76313875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555e229a2d28126c4330a6abe25a2a95ad318d2cecd47079fa9c53484f9e6608`  
		Last Modified: Tue, 06 May 2025 19:29:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:6be925253cb7d9a960dd4cd0ae3eb3cc2098405227a50c285a93ea1dee57bc95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 KB (235758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:018bed7d26e327055ec3ba5c013d5669c6e6d815172155a2a17b973aca7bc075`

```dockerfile
```

-	Layers:
	-	`sha256:3369149973e2a592e0486c7a319de2bcf68f315c1093d0b9946734c8b8743c09`  
		Last Modified: Tue, 06 May 2025 19:29:56 GMT  
		Size: 209.6 KB (209616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77ed2e8ce2596be6b3a52a610ac74f1ccc62bd42fa7642661efdebd6fbb0b06f`  
		Last Modified: Tue, 06 May 2025 19:29:56 GMT  
		Size: 26.1 KB (26142 bytes)  
		MIME: application/vnd.in-toto+json

### `golang:1-alpine` - linux; s390x

```console
$ docker pull golang@sha256:d6deb051858dca9a8f29161b7dfe730d419e5918f1ab0d320190f4cfaaeb0c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81731797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80855ea78f206998f3a84b1bd2dd250a77a6c385a2bf511d3808bac7206ba170`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 20:49:27 GMT
RUN apk add --no-cache ca-certificates # buildkit
# Fri, 30 May 2025 20:49:27 GMT
ENV GOLANG_VERSION=1.24.3
# Fri, 30 May 2025 20:49:27 GMT
ENV GOTOOLCHAIN=local
# Fri, 30 May 2025 20:49:27 GMT
ENV GOPATH=/go
# Fri, 30 May 2025 20:49:27 GMT
ENV PATH=/go/bin:/usr/local/go/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 20:49:27 GMT
COPY /target/ / # buildkit
# Fri, 30 May 2025 20:49:27 GMT
RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 1777 "$GOPATH" # buildkit
# Fri, 30 May 2025 20:49:27 GMT
WORKDIR /go
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Fri, 30 May 2025 18:13:14 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c02725f6addf0718099c43b5965203aa513fc71aa710978afc18cf384dfb4798`  
		Last Modified: Sat, 31 May 2025 00:11:27 GMT  
		Size: 296.2 KB (296215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553e83890111f2cfa590a0023450ca3f44d60d123d688835ec1c4ba557b336f8`  
		Last Modified: Tue, 06 May 2025 19:25:37 GMT  
		Size: 77.8 MB (77787898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c818aeeba86e6909543a7c30446c8af7ad1c77d11d7f7614fcaee1a72afe1741`  
		Last Modified: Sat, 31 May 2025 00:11:27 GMT  
		Size: 123.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `golang:1-alpine` - unknown; unknown

```console
$ docker pull golang@sha256:4c350cdb71c1bb4ec75886a5174c99cf5e4a8e1d83aacf2e0985c1e283ae6e54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.0 KB (237966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ccbca0ef6375957dee2a5be921dc0306ddeaafaa31da628bb8fe99bd864f04`

```dockerfile
```

-	Layers:
	-	`sha256:c73e25584340854acf4f9af2139d99a9322f9fdaea4dbfa98d9974448f4d1d9d`  
		Last Modified: Sat, 31 May 2025 00:11:27 GMT  
		Size: 211.9 KB (211896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:347f67b5f03c92226d69ac6e2410c7b3aab5068cb3ad041fbd235f6d7f713ed5`  
		Last Modified: Sat, 31 May 2025 00:11:27 GMT  
		Size: 26.1 KB (26070 bytes)  
		MIME: application/vnd.in-toto+json
