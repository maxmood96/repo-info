## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:5c7e4d33c567ce2c052935664bdb5c40a55c846af284c06137e47ec234b2c041
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

### `spiped:1-alpine` - linux; amd64

```console
$ docker pull spiped@sha256:bf4f80de0db396d644d3bd7d284f1a82968f2f5dca2d8cb33ba829c0043fa7e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3748896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1739bfd2f7c6bfc0aec39069cb0902b1e56873b04c7099b83047c17e17df1c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
VOLUME [/spiped]
# Sun, 19 Jan 2025 13:01:46 GMT
WORKDIR /spiped
# Sun, 19 Jan 2025 13:01:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be090fd76d1e36f16806f586b6344fa2de641690144682cd6860b988c3c931d`  
		Last Modified: Tue, 21 Jan 2025 19:28:18 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1155ce8a77b55d5a058c2b75baec72432a1a394f1d53956393a6e547ba0d7f6c`  
		Last Modified: Tue, 21 Jan 2025 19:28:18 GMT  
		Size: 7.9 KB (7909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9276e935161ceb34d567a8fa6cd5945c8199ddaa39aae106a6c0f34b646ff4`  
		Last Modified: Tue, 21 Jan 2025 19:28:18 GMT  
		Size: 97.9 KB (97879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d015ce49382dcd762930d16d6a81450d9b389d35fb79ea80527841a68922f56a`  
		Last Modified: Tue, 21 Jan 2025 19:28:18 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912bdaad70ad3037b03159d81278ab0dad9b2827a758dd7444163a7203f9314c`  
		Last Modified: Tue, 21 Jan 2025 19:28:19 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:379145c25a8027c2a34d73c76346518adda978e2b00e97869e108358e4b33437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28081c4e7942cc3a13ba88170d117e0ff67b48eaa690d6537b01bba98892a90e`

```dockerfile
```

-	Layers:
	-	`sha256:6625a81c2cffef3b41b47962b504e9dc20cff4471d4d6f1e5d96e14770cd2929`  
		Last Modified: Tue, 21 Jan 2025 19:28:18 GMT  
		Size: 79.8 KB (79816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9fee5c0b25d256b52106b1fd933f9f04a617e9e2e3a7d2731ba142a1d8ba0fa`  
		Last Modified: Tue, 21 Jan 2025 19:28:18 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:0c4472e3c5cd36e439567c13f5cd9a379aab66e0a915889d6d42baafbc2500ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3454044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a7cbce52f04ff9256292b0a9817ed2fa7941835bdeebeaa27869591dd7f9eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
VOLUME [/spiped]
# Sun, 19 Jan 2025 13:01:46 GMT
WORKDIR /spiped
# Sun, 19 Jan 2025 13:01:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee72c2b1876a0156b7d396caf2dc29a0f8081b2b7a6733a3ff64d9527f586ea`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1da6fb0facd6416135ae0db69e959ecf3e75cab6ea327aabb4ead163825dfc7`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 7.9 KB (7914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4bfb2112b9ff1da637fda9a1fabd68afd45961279bab992964a8bd6e31408f`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 80.9 KB (80855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074202ffcdbaa57f35bc530fa794482ecb273ad51046c53fe8043f01096270ba`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc4e41cff4eb7a1ada1c481fe378e5268751d48dcbbae7342d3241561661269`  
		Last Modified: Tue, 21 Jan 2025 19:29:41 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:366e5b0763df779aacdfe5468363ac3687088dd4e125b847daef76b5029a5661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a7ede033b2a067297269492b9cc67391a8024877ed9a838acefe18b08c2e7b5`

```dockerfile
```

-	Layers:
	-	`sha256:464626d886af9ffe2ba5aac0067601f31503365fea01536d0142c873f5980371`  
		Last Modified: Tue, 21 Jan 2025 19:29:40 GMT  
		Size: 14.2 KB (14186 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:0ae1d2d6cf54b9aa45265044ba111dd99c549b31e466c67d3afc3abec2fe3ad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3181455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dbc5512e44ca9ebcc11a994bb12f151c14c2878f9ed60b62665f1ef9e2dd061`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
VOLUME [/spiped]
# Sun, 19 Jan 2025 13:01:46 GMT
WORKDIR /spiped
# Sun, 19 Jan 2025 13:01:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
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
	-	`sha256:60770baea6ea5185f492834462f47c3556209ae19718dec68186d538965228ca`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 75.0 KB (75035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0c2868e02a07fed49e900b254ea234eb48f25e37bc10f580198d191565de75`  
		Last Modified: Tue, 21 Jan 2025 19:30:38 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e555c89d083ded756b21c5bd510ca93d93cdc37921edd4764164ed46228bd95b`  
		Last Modified: Tue, 21 Jan 2025 19:30:38 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:2c10a8c0cd22de6c2045282220f18a4879e5e74494a7d1945236baf2eb256760
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c58cb4a63496728162216d59f92073861eee5255f9c2edae3276a72c8777b7fc`

```dockerfile
```

-	Layers:
	-	`sha256:7436f70191232399d4d7c405219fafb240274bd898d8ccd07f712aa394e7a86d`  
		Last Modified: Tue, 21 Jan 2025 19:30:38 GMT  
		Size: 79.9 KB (79852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce64a4a26bf1cd792d2cbba128afa6e7fb692cbf52d2fa21f5297938c26001ee`  
		Last Modified: Tue, 21 Jan 2025 19:30:37 GMT  
		Size: 14.4 KB (14401 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:4f709a7af2244a5ff9f01387d5030ac4aa1c6c573254cd2266bf3100b9a813a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4092686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b82cd26698a5299c656bd15e65f1397979b455479ffdd415881455b92d1991`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
VOLUME [/spiped]
# Sun, 19 Jan 2025 13:01:46 GMT
WORKDIR /spiped
# Sun, 19 Jan 2025 13:01:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987e71ee6cc5ab416ed1f0e49bb9a1696b4b5656b4d3fcc1feca517c7bbe5030`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5faf545dafdf63442f66bf2d829b8ba0c5dd8fe81240a3298cbf9fee767c891`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 7.9 KB (7921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2c84ea327537859da16a3a7c4061d3787af0f266934eb7228b7b3a162359f7`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 91.0 KB (91009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c519261ae45d672eb2ce96c696945b567ef14c566a912cdc782f8a6460f3a5`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c072a47e7cf1bb0073652f81348762878a297e164adca16bd19e1fbed0b7c8a`  
		Last Modified: Tue, 21 Jan 2025 19:50:57 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:b5c38e6ae8441ca778cdfb5a4550cc780f4ef358f0a43882a3235e7eb9042be4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 KB (94305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff3d3634cf407a39a6e662cb942c48f9a3cd5a462a148837480d362d0d3b118`

```dockerfile
```

-	Layers:
	-	`sha256:1a07d546f1499b6116c2af470d73941c09865327e1d8c12e0e00d302b098b024`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 79.9 KB (79872 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42e95337c10301d3e0c1a1a7dd5266eb9b51919a6979351d6ab21dd694353ae3`  
		Last Modified: Tue, 21 Jan 2025 19:50:56 GMT  
		Size: 14.4 KB (14433 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:142927fc09806045217102e1fd61c9120693bb3437a64b4e53d45fff85604a29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3580250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5191a7f4b9da1db034fdb1a2a191bfdbbaf0970362273c14cea5a8d67af9c59`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
VOLUME [/spiped]
# Sun, 19 Jan 2025 13:01:46 GMT
WORKDIR /spiped
# Sun, 19 Jan 2025 13:01:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66602b26aee70855e62f399265bc3d459bc2e17fe241dc09f542aea66a732d51`  
		Last Modified: Tue, 21 Jan 2025 19:27:59 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754deefeb72f062211245a56424039263e88066669b4752e5509b96c3fc75976`  
		Last Modified: Tue, 21 Jan 2025 19:27:59 GMT  
		Size: 7.9 KB (7909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8aa827b00c14c831e4f20dad83f6c4f5e3f61faa06bd0d88a0513abd6919cb`  
		Last Modified: Tue, 21 Jan 2025 19:27:59 GMT  
		Size: 107.8 KB (107820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4247d4a0214d8ebd8f0fc13a2dda2e237375c545239c856be1deee79b6db804a`  
		Last Modified: Tue, 21 Jan 2025 19:27:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3260d2ef071d2a025027168328bd57243ca2fcb118e4eca7966966689d64c6a9`  
		Last Modified: Tue, 21 Jan 2025 19:28:00 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:4701fe7d0f9e827457a3849fd8edff76707b89ab2830cd1f661c6968daaf01a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 KB (94057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:191ca3b524a67e610d402501801e70d4ed64c7e0105ec47581b8221b04617eee`

```dockerfile
```

-	Layers:
	-	`sha256:b243e9db2d57fcb036e6456ffb5fa340acb65741007c7bdc9b4583b6a11fa23e`  
		Last Modified: Tue, 21 Jan 2025 19:27:59 GMT  
		Size: 79.8 KB (79791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cea95049f4e29abe2a4dbbe1d23dc82dc4e3bb876a61c9cb0ddcb0c6c3f53d6c`  
		Last Modified: Tue, 21 Jan 2025 19:27:59 GMT  
		Size: 14.3 KB (14266 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:02217b126efda6419d593927c1e7afedbaae32a0dfac48527891fb61e326668c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3678657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:336ce0a2b2749719b0875443f6719cc477728f9d9ca03aeb8fdd2eb80a7fd7bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
VOLUME [/spiped]
# Sun, 19 Jan 2025 13:01:46 GMT
WORKDIR /spiped
# Sun, 19 Jan 2025 13:01:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2937ae7bb7a53c30739164fd8d6b1af5449b91bdeaacb11c09da360a795e967b`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbed2b37b3a36511a8f8cde15ac74df12676c707a75cac7400604b533817a57b`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 7.9 KB (7918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78388bac15c7f0679a8f61fec0fd44039e2dc31eb14e7adb586632c8938f4558`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 95.7 KB (95740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dca0f484333f1fbdab6b9693779c9f26be5962fe67e46f46ea2db75698a3d0d`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be1274653db549fd50a72850308000f30c9517f1d7b348cb82463adc3c4cc74`  
		Last Modified: Tue, 21 Jan 2025 19:31:29 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ed3fde57e25bf38537c7f0c1d97fbc836ebf868397090410e8909472f48a710f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db83784de2b8cebf42f5efb3510f46e989e3bb222c1d74a7ada0a21d3b477c3`

```dockerfile
```

-	Layers:
	-	`sha256:d4d5a0de95eb8f06fde7d4e9a71e8f41b6cc30a14ac230b76293cb5186635d37`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 77.9 KB (77899 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f61dcb17bca36ef37c1782c7996fd97fc226af6a408695c157aae47d923bb1f1`  
		Last Modified: Tue, 21 Jan 2025 19:31:28 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:8753a779e5087f28ca4abda0cdb7c4a28fa8732bf94201fc4f1c6749cac05e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3448196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972586fe36ea4a167e8c4e3dd294a605bd9e95559c656558021b297fc6a0e7d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
VOLUME [/spiped]
# Sun, 19 Jan 2025 13:01:46 GMT
WORKDIR /spiped
# Sun, 19 Jan 2025 13:01:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
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
	-	`sha256:725fe5f1d54360199e0c323ed9105f4b968c5b4e9ac846c5c3c41c9f67026998`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 88.6 KB (88643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561e0b8832db6b203f73cdc2a06f1f927f05044848e5a4c911efd349960c1299`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53e08b4d3b18487565f895fcc2e5aa406700b2e9589117a057f0d580eda17bb`  
		Last Modified: Tue, 21 Jan 2025 19:47:11 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:433e9af8a8aae1b47091598b315936f3260b19614787199011d74195be92071c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f61d9865b72e236614e5628bcb24f39a6039f498ece96818cdbce448c511329`

```dockerfile
```

-	Layers:
	-	`sha256:79b96efba8cf867f9e9e2cb09b95054474af816599fa19ea5c5fa0ff4b799030`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 77.9 KB (77895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2249ad8997aa1b69cf185889e51eeaa77a5fbe77b0dcf1b762154def0237b80`  
		Last Modified: Tue, 21 Jan 2025 19:47:10 GMT  
		Size: 14.3 KB (14347 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:2d7e1c9817e385b181b3bc711b36578549be6951515e90c415628765f463a86f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3561031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854dee3cfd59deb9dfb570b45c1fc1a4289fa0cce595a8c460b4ff4e38de33ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Sun, 19 Jan 2025 13:01:46 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
VOLUME [/spiped]
# Sun, 19 Jan 2025 13:01:46 GMT
WORKDIR /spiped
# Sun, 19 Jan 2025 13:01:46 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Jan 2025 13:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Jan 2025 13:01:46 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2d0ea9a1061fe840c13a046b93faaeb9dbcf4357f53a37b83747a395c05279`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068b14e90f05cd3c9537d5988b4bbe6abead4cac15a8b25d1959964036cdbb13`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 7.9 KB (7909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd06766d16512bbe8f937e09b7f90223e29e8e4f0d7306052387f4bdd5243406`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 84.9 KB (84859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbdfee3855ba5896fd063d555eea5f8b0895168a4ba8162a475fce6bbb3cd631`  
		Last Modified: Tue, 21 Jan 2025 19:32:38 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb327b9c33b07ca822f14e1d5eb0e89aa67aa294ba7fc97ceb881ba83258645`  
		Last Modified: Tue, 21 Jan 2025 19:32:38 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:cf5e04de8914015fdfced9fd2350f25ae04499716af67e6870cadcaa694a5944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 KB (92164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a90ae2d8e21694ed59a7386bfdd6650236725793931430a24f9d8a8ac24fab`

```dockerfile
```

-	Layers:
	-	`sha256:a3e79339ec578c35ce808cf83d83181d2070408631264fce657e406f892754d9`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 77.9 KB (77865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d28c39be10ea42747404de7a4952b61efc3419f395d546ad85727355d0bdbd5b`  
		Last Modified: Tue, 21 Jan 2025 19:32:37 GMT  
		Size: 14.3 KB (14299 bytes)  
		MIME: application/vnd.in-toto+json
