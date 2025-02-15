## `spiped:alpine`

```console
$ docker pull spiped@sha256:a679ffdc3ad120ae7de7668604ed652020594f65147c395d0a948bd1f5ab0e15
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

### `spiped:alpine` - linux; amd64

```console
$ docker pull spiped@sha256:7ac6025838d2bc44ef0e0fafaf5982e0fc4373b688d82fd8fcf05d8b97ca538b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3759143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38502c733d8809263c7b9aef9befc5daac0d3a04ff701311a9df754f155a16b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cbb4d14e8e59f505be1081c094889a892e335b697f6d0c4944a24ea721d7a2`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb14bfd2d59e15880cb805303a18fd6fc6bc7e980d9ea46c8fddaf5072a577e7`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 7.9 KB (7910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f93bc17b0afa3407e99dd41fd4909fb96e359b2cb4612c46ded356003ed053`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 107.6 KB (107606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d9fa481a10b5130c48f48db6dbbe9a30b114bf719e8fe78001449bca914634`  
		Last Modified: Fri, 14 Feb 2025 19:24:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585408ce1d63439f4bd520d967524dbc4d7e05e0d452c10c0dc69c4709d28e50`  
		Last Modified: Fri, 14 Feb 2025 19:24:09 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:91bf4effc5a6d6617632764adb1237e80919976921e5e3964f445b458cdffe5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157e2618e51acb8116b41dc6c3e43f214685385070706f8e531392d2a2b5a32f`

```dockerfile
```

-	Layers:
	-	`sha256:2744be77085e9a3321af7adcd6b3545cf6bfe6ed121b65fb85ada625330919e6`  
		Last Modified: Fri, 14 Feb 2025 23:04:36 GMT  
		Size: 79.8 KB (79822 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54db7fc3515a2461325d4de9fc957a390badfaab3a19d15be7868d671af57e54`  
		Last Modified: Fri, 14 Feb 2025 23:04:36 GMT  
		Size: 14.3 KB (14301 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:df12325bd4f67527eef210da2e785cccf9fee709f5839bb817095148b372e4f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3463168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef2998ff82432e374d083b5b629bb256e09097ef1a9f83eea7d0ab00e5516ec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066b47e1325b9f6db29d2d135e8ce6b8fcbf90a8f37138d1f3356a294928613b`  
		Last Modified: Fri, 14 Feb 2025 23:04:54 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014f6178dbec0d9fa86b0b438929f32378f60d88338518b7952956c6aa1b5cb7`  
		Last Modified: Fri, 14 Feb 2025 23:04:54 GMT  
		Size: 7.9 KB (7917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6bb96c10a3bddea4cf5fb950ac49b22112a43dc906ac1a150c2651b21621161`  
		Last Modified: Fri, 14 Feb 2025 23:04:54 GMT  
		Size: 89.1 KB (89139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7b5d6ff490ba5ca8f35cbb9b0d65060b194abf98610c588e99805f81d8e35d`  
		Last Modified: Fri, 14 Feb 2025 23:04:54 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ce1526e7b45007e682aa0fd80fbd9c1aa1537c854c4ee7ec3a9ad9037b0b67`  
		Last Modified: Fri, 14 Feb 2025 22:32:56 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:45bcf73666108868c8355e70fce85a00349f2a252225bb8117406a06cb74e674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f115d9a33ace52d319c520b7bfc5952bc13d2e791d27cd9170c8ee19fbeefa12`

```dockerfile
```

-	Layers:
	-	`sha256:787453bd83dce9d473689f5e983cfc99224f335f52dda1d16a0e5b0302d0f106`  
		Last Modified: Fri, 14 Feb 2025 23:04:37 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:12817cd6117bed3cdf9e7e4b52de247dd1a87d2876d8dc7434e5115f0fc9a549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3188067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1cba0ff108ef4a8e8108d49bf7ccd596afac4a82110a7c14e80a001be5fa5bd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ae962cfc489c298278551ba32bca1e0ed1f67cd05192848331b7c3ee926a77`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1114d274ac423361940bdd6b0c7904acc23cb9903e6f1a2904b32a6b89f331c4`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 7.9 KB (7915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51637362b800c4f96d7abb05ca7529a770947ee4b1e9623b35af4b936195f4a9`  
		Last Modified: Tue, 28 Jan 2025 01:37:32 GMT  
		Size: 81.6 KB (81648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b15074482593cb5d5f416eda5eadebe75a10ba5005975523c4c34e81f46e618`  
		Last Modified: Tue, 28 Jan 2025 01:37:33 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db71199d0efb2f82ed5530667b5595dd7a34230b43f8dd94dbe9c99654b1b9ae`  
		Last Modified: Tue, 28 Jan 2025 01:37:33 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b5a94554ddb9da6514578c1b09075a2b4ab9c4410f3e3e231bae96919d45f4b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2f515b3bed3192db05a2ad5b870421a369f4a33d6b7164dac00142ecf5bc150`

```dockerfile
```

-	Layers:
	-	`sha256:49f4a9e142d4f0bbdb2b6f12f002efa4735f8926b13589ba3a9a5a9ce1a027ef`  
		Last Modified: Fri, 14 Feb 2025 23:04:39 GMT  
		Size: 79.9 KB (79852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c72de5bccb3b20f12aaba84aa22f33c24e0ef214459867af7cbe28470672cb2`  
		Last Modified: Fri, 14 Feb 2025 23:04:39 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:47f6dfb20be478dce9979b1e2494b93143aa488741abf7dc66ba6f515e197d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4102884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f508cb0494d2702e3a13db5d6fc2fd1ca41256c5959e0c4652e04994a249388a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e9ace35db34c3304a810302430fb8aef69b65f583bd5e243d327da73e37c2a`  
		Last Modified: Fri, 14 Feb 2025 22:23:47 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a714b728344222c6dfa8f49bd713be1cc1d83e747cab7f88cfaac3caef9ebe58`  
		Last Modified: Fri, 14 Feb 2025 22:23:47 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a90c58f039279dd810920bc66f47f0c176890374bc494740bfa97ecbfa53767`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 100.6 KB (100551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898ec4dd7aa4832397a2e91d629904b2a48c8298de7db9365c04d33ebbf1bedc`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26adf19273ff38a41503b067a8d1c5a35d4048e2291780e1ffa91def36425f6a`  
		Last Modified: Fri, 14 Feb 2025 22:23:48 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b00591e00a263982885b0bee54a5d7c27ebcf5249fdaa334c51fc223467aabf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90bf2a0d811c39c7759e43d4257b01711ffdf36fa3dceffc397887cc7f8fa9d0`

```dockerfile
```

-	Layers:
	-	`sha256:c19f26a228bd4be6de3aa9d8196866405d54f8bc38d014c8f26254efe16ae04e`  
		Last Modified: Fri, 14 Feb 2025 23:04:40 GMT  
		Size: 79.9 KB (79878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5a1704deb4400e22af6abe356817cdee187689b0cba34988ce227508adfd78f`  
		Last Modified: Fri, 14 Feb 2025 23:04:40 GMT  
		Size: 14.4 KB (14433 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:61b83f6f4da433231db95db1a13fe86dbe85aaecde12dcb9a669f0b0ed0b6e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3593051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68ea95baf750c2a2749ec794c8238c510e5792dc8857ed4a3645d071f394823`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89de02b79b34b2bc491f8c7e8607233cc124ed19295cf456e64382e5afc72fbd`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff1d235c70003f61e0de885229553d72517e82d7f45df6d561b480b2cd9c5fc`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68a0453a1d3c0248fee96f306a8ede9aa3d7f2dd02652a8dbdff1b0d8c9438b`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 120.1 KB (120130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e021c9b7ed20e7390deef74c89a7a5540f6309865137308f9a80ac607be260f`  
		Last Modified: Fri, 14 Feb 2025 19:11:58 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2872beb154170ecfc36e7b32d8019cfc1e29a60d26d251929d28131277a7fd0c`  
		Last Modified: Fri, 14 Feb 2025 19:11:59 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:4c3f4670bd80d3c0136a64e6f27ff285948a413faee904ef1c460b8f51d4e516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c5f2d723a731a066cf77f9a59824e65134fef732e62678056b932016e17282`

```dockerfile
```

-	Layers:
	-	`sha256:b1e174fd16318b9fb1190150ba833822f30825a45606ea9af9ec1723ce03867c`  
		Last Modified: Fri, 14 Feb 2025 23:04:42 GMT  
		Size: 79.8 KB (79797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86e4a7deb35e498340a41c762c8316785005a9ab4e93a2ab0a677fc623e721fd`  
		Last Modified: Fri, 14 Feb 2025 23:04:42 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:0763e833f3d2e767ad7c1ab64d3a1778d9543cffbe2731d7f8c40bee27d44a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3696292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1cde70893ef4a0b94f4624b6bd8ea6a51522d65faf50b2646cac866d386dafe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22ff6ba800883c9495b3d17b7735935035a83bdb153e380d5f5f6c80c3573c5`  
		Last Modified: Fri, 14 Feb 2025 21:51:56 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77eb59aefcf51d96da7771cb0671fa43ebe8e636326ce4db947ff446ea9b4eaa`  
		Last Modified: Fri, 14 Feb 2025 21:51:56 GMT  
		Size: 7.9 KB (7917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b657e1255fd2cfb228ed06e75846652368ff0d80307f8b278c3db5e5558f4f64`  
		Last Modified: Fri, 14 Feb 2025 21:51:56 GMT  
		Size: 112.6 KB (112646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1de73da0d337b9f7fd4e60cf9b67d3592f9e6f6f539421800b167a2735f1bdb`  
		Last Modified: Fri, 14 Feb 2025 21:51:56 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ad280a5133fac353984bead0c9962cf3a9c94714d7806a61832de902c8e929`  
		Last Modified: Fri, 14 Feb 2025 21:51:57 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:522f73a6a1f1e955300602615eb9a993897959108be79c09d235f1db5e488940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 KB (92255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f95185cb2bad6bef09c576b8e4d9d0bf6563783c294a92e69f28b758029f2ac0`

```dockerfile
```

-	Layers:
	-	`sha256:eb306f89b50101c069df46fb92b19620767f2503887c596aedfc415f347a4246`  
		Last Modified: Fri, 14 Feb 2025 23:04:43 GMT  
		Size: 77.9 KB (77905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c821af9afc609e7780dcfb284627dd581cbede4a66c24cc04b41f590c6244531`  
		Last Modified: Fri, 14 Feb 2025 23:04:43 GMT  
		Size: 14.3 KB (14350 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:756e00d72198e903bfd6356e80496c2936c64fa26149b3662c09c044393ac715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3458360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3b076b4ea8c2964765a22bf8c5d8b2fb8141f171e1f335b628572524c3ab7a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Tue, 14 Jan 2025 20:35:37 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410676c340782e10ad961429d12c4fc7bc22fe42e602f44af8fe4564583fa790`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb03e5e951a5c0dc5098e3f3712ba683716c2830cd781627b8c589f37e35d49e`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 7.9 KB (7900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d4da436692d4ab0fd5035ee54eac03b05bf24df9aa3304a4cbb3e6bb7fb7de`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 98.8 KB (98808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b11f3813ff058c0963785dcdc5c5f860f00840874673c02d724b273f844d53c`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d897b6a73cbb856ebfd058f311b8f0e39512fdede0d33460f38db93bb89b6c`  
		Last Modified: Tue, 28 Jan 2025 02:22:45 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:877a9cd3fe26f402674032844c26b7149200267a47a431963b72e3b4563d519c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b37c1a9028694f866e7acc219fbf431ce5b97965a6f5489a14f064c84a12b1`

```dockerfile
```

-	Layers:
	-	`sha256:40546cca6e89cde845ebe9184ed940f3b4f38ba1e18049e3b36b047821e42722`  
		Last Modified: Fri, 14 Feb 2025 23:04:44 GMT  
		Size: 77.9 KB (77895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12a0377ea7376b0115517894b6c6f3d26482dcf699f270a21454fd463c994114`  
		Last Modified: Fri, 14 Feb 2025 23:04:45 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:de25b12e766fe57e24177257227c53d5a27fc1a3ca4abe48e8bc60e0351bdaef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3573783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62cb095475057abb702522c9d705013168c8522d986f39b9047739ee6efe16b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Sun, 26 Jan 2025 16:57:02 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["/bin/sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENV SPIPED_VERSION=1.6.3 SPIPED_DOWNLOAD_SHA256=70c53070dbbb10d1442754aeafb01b08ec829203d41023647dbf1a1435ee4a65
# Sun, 26 Jan 2025 16:57:02 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
VOLUME [/spiped]
# Sun, 26 Jan 2025 16:57:02 GMT
WORKDIR /spiped
# Sun, 26 Jan 2025 16:57:02 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 26 Jan 2025 16:57:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 26 Jan 2025 16:57:02 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a28161d111a002ad388fefdd709f7bb67cb61071bfdfa7960202816d14c2e2`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30984a12769648824acad7e1386b7ba7193bf81929e37f44ce5f3c04f82acc6`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 7.9 KB (7915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b5b85eee8dde04ba3dbc50eb3b644d79d18255b1eb4dfa5c888403b0ad97cc`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 96.9 KB (96918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8860fa829f189bb5e960d5036162d15a1aac72e9ce8bed6c40b68549752c2199`  
		Last Modified: Fri, 14 Feb 2025 22:26:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb23aa9487acbddced4252bb38b3510de48d049a3a347fcfb6b24f40c9ff730`  
		Last Modified: Fri, 14 Feb 2025 22:26:11 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:2065dca98493b203898ab91ad7de40fb703351116ab3bfc12c9a52026ce6c13e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f932f07832d03eeec80862781aec2cb3efb7c48fadec873786bd1c8af939e6f5`

```dockerfile
```

-	Layers:
	-	`sha256:8b919ae512d1430c2c7488ea884c9bc49e2ae21b5170043f2a370c90e9af6c60`  
		Last Modified: Fri, 14 Feb 2025 23:04:46 GMT  
		Size: 77.9 KB (77871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddf9c418603cd0c1fdf650dfd352e9ae11c6eec907de4024a31a994019249053`  
		Last Modified: Fri, 14 Feb 2025 23:04:46 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json
