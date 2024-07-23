## `spiped:alpine`

```console
$ docker pull spiped@sha256:7e17bda491feb9832836ead088d09ed441acbec0f930fbea5854cf3a2d5ecf73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 11
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `spiped:alpine` - linux; amd64

```console
$ docker pull spiped@sha256:7a563dc25361cd54df387146058b72bb5f92a3635b9f1fe09bf64ec7e257d1ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3855343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37e74ca410a443720a8fdb372026e0db637b685d3cc12c7ba2a57cac246bcdf0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686cdbffe70ad2214af54207fa1ac5da7688096a06ff3de7357652cfc8335a88`  
		Last Modified: Mon, 22 Jul 2024 23:04:25 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e917e6d7343db0db31111d015ae768d8426dcd520cd3a874a1971484925929af`  
		Last Modified: Mon, 22 Jul 2024 23:04:25 GMT  
		Size: 7.5 KB (7545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b614d9036c021bd10dfb8357b380c1d2cf21ffa70af62e8885b407d75e7343`  
		Last Modified: Mon, 22 Jul 2024 23:04:26 GMT  
		Size: 223.5 KB (223511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f403f02a700d07fba1b7f1a4297abed8a172b7572c4a8defb3263c656c6b98a`  
		Last Modified: Mon, 22 Jul 2024 23:04:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9934e460b316808d2e9f0aa3c32065e1aed92e9176c0225195432a91f94f2a70`  
		Last Modified: Mon, 22 Jul 2024 23:04:26 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:700a9d5d54bd49e2ec49cd32aee6dc0fd5705fd69923fde270addf1babcb567c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 KB (88050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0a444f523bcf3802be2b509d67bb3e47a38ea9cebdb6778d8b51b92be39978c`

```dockerfile
```

-	Layers:
	-	`sha256:868ae72c352c08135914f06da5fb294537fb4dd0970a9817a65b828e28dc05a1`  
		Last Modified: Mon, 22 Jul 2024 23:04:26 GMT  
		Size: 74.0 KB (73969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0644e8f7cb531ad77acff73ac240cc6f451c6c00425ca4a1e7bbaa222eaf077e`  
		Last Modified: Mon, 22 Jul 2024 23:04:25 GMT  
		Size: 14.1 KB (14081 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:ef938ee637be73ea21b0937d185ae8e417312700f16e2bce9d3ae87ccadb793d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3582337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59fb7358369ccefd209908c33784a2da06af719c27799b88528c2db4e62f79f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e240c5fcb47b60ba4a95071138487e774604b870f2b56f1494f653bf7048d4d2`  
		Last Modified: Tue, 23 Jul 2024 11:49:12 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2d47428092c941e590a8d01329b024dc1e9582a3f6a51608566a7132e7b79c`  
		Last Modified: Tue, 23 Jul 2024 11:49:12 GMT  
		Size: 7.6 KB (7555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d52a943861caa159702a0434687ccb6469ed9c6c05766de49acc8c03a2b685`  
		Last Modified: Tue, 23 Jul 2024 11:49:12 GMT  
		Size: 208.2 KB (208199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7431484beebf1d505eff760af8be3a322614790f268b70013bf9eb2d04b5809e`  
		Last Modified: Tue, 23 Jul 2024 11:49:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bac75927bb4772cef909fa64d933106b4e0938486bc763f8ffe71b28e57719c`  
		Last Modified: Tue, 23 Jul 2024 11:49:13 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:34a42b86465bcae6352f84bb79989055ddd4e318c70270d4e0cfe42c7a121ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 KB (13957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c952dffc0fd9f1d21df2f86bc882a7f8a843dc06a0a3ad529fab9c16dfb476ad`

```dockerfile
```

-	Layers:
	-	`sha256:d574698b971033158fb791807762e4d3a212227c8afc10bbc7e306d929c4986e`  
		Last Modified: Tue, 23 Jul 2024 11:49:12 GMT  
		Size: 14.0 KB (13957 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:8ecb35a22db1431c4c953fff2d1196bfc12856d4e1d391389780f6e126ebe55c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3305887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d33987687a2537678674e2a2abc0893e4f852cdee5a3c66fd91a732903acd3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 01:24:37 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 23 Jul 2024 01:24:38 GMT
RUN apk add --no-cache libssl3
# Tue, 23 Jul 2024 01:24:38 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 23 Jul 2024 01:24:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 23 Jul 2024 01:24:47 GMT
VOLUME [/spiped]
# Tue, 23 Jul 2024 01:24:47 GMT
WORKDIR /spiped
# Tue, 23 Jul 2024 01:24:47 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 23 Jul 2024 01:24:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 01:24:48 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27484b82b33e38617e8da83d667a52486b7234d31ceb2a15658439ba77e89581`  
		Last Modified: Tue, 23 Jul 2024 01:24:57 GMT  
		Size: 960.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5770b7e617086909f9cc9a23600ab19bad7f917acf07c5c1f38201aa4fc5c072`  
		Last Modified: Tue, 23 Jul 2024 01:24:57 GMT  
		Size: 7.6 KB (7584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd189a1339152dcb34625b2506d22caba796170f398dfbae66701679599f9c9`  
		Last Modified: Tue, 23 Jul 2024 01:24:57 GMT  
		Size: 201.9 KB (201949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d431ea9598a0070565ff07dcbaa622d8766a79fc7a75da9054a5ad62a769354f`  
		Last Modified: Tue, 23 Jul 2024 01:24:57 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55caac18a2d8e9c4868abc59501f5c9da0dcfda501e76bbc410c0611e8e866d4`  
		Last Modified: Tue, 23 Jul 2024 01:24:57 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:bf1a336c493ff2e57235f1242ae0d50550b01c23d68482b43ec1a2e9b0e9bef2
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b83b4e66609f16fdac096ad1145302fc5a34aeefa8ebafcdd8ffc9ad2f2ab7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 02:35:22 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 23 Jul 2024 02:35:23 GMT
RUN apk add --no-cache libssl3
# Tue, 23 Jul 2024 02:35:23 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 23 Jul 2024 02:35:31 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 23 Jul 2024 02:35:31 GMT
VOLUME [/spiped]
# Tue, 23 Jul 2024 02:35:31 GMT
WORKDIR /spiped
# Tue, 23 Jul 2024 02:35:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 23 Jul 2024 02:35:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 02:35:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d70c016eae148bb030892121f30a6a32dc82bf8b2a87144f7a5406f93424ea`  
		Last Modified: Tue, 23 Jul 2024 02:35:42 GMT  
		Size: 960.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2a433ae6ad2a6439fb49e9746a9e0d6fb326aead41f6f304f14d8905a0ca02`  
		Last Modified: Tue, 23 Jul 2024 02:35:42 GMT  
		Size: 7.6 KB (7588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc26cd2f7f696b748b6a9fa2b11908875e92c8448f203fbdf6d554d26e5456c7`  
		Last Modified: Tue, 23 Jul 2024 02:35:42 GMT  
		Size: 218.4 KB (218420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c31a402e26a6606e4ab0aea5cd6a38f42b1ffa9f0136562c507cb772d59a83`  
		Last Modified: Tue, 23 Jul 2024 02:35:42 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2491ad8d2ad8b93ce497457fbfb8f24104d585b9cd7e8ae7c7d05d28a49fb1`  
		Last Modified: Tue, 23 Jul 2024 02:35:42 GMT  
		Size: 339.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:7544e84759cdc149a4e129b642f25a8d2dd4eb05b2b3ba3f6c628bab5c8c3025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3710909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d3e81cd6e4cd17e7e3a44c3df6ffe8d5b54b77b2e2eec98c0f879dcd218131`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Thu, 23 May 2024 19:15:47 GMT
CMD ["/bin/sh"]
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Thu, 23 May 2024 19:15:47 GMT
RUN apk add --no-cache libssl3 # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Thu, 23 May 2024 19:15:47 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Thu, 23 May 2024 19:15:47 GMT
VOLUME [/spiped]
# Thu, 23 May 2024 19:15:47 GMT
WORKDIR /spiped
# Thu, 23 May 2024 19:15:47 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Thu, 23 May 2024 19:15:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 May 2024 19:15:47 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f82ca5facfb51230debdf0fe63bdd3011952b7e5d8bc2bfeaed08b96831a83`  
		Last Modified: Mon, 22 Jul 2024 22:07:34 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d139fa209297494b082fe390286fabcbb62b5e12d1e6b99736c04a65eee2dc4`  
		Last Modified: Mon, 22 Jul 2024 22:07:34 GMT  
		Size: 7.6 KB (7554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2193b1b1fcb58b38dc260f178786a6712c9d089610325f828e52010368039e`  
		Last Modified: Mon, 22 Jul 2024 22:07:34 GMT  
		Size: 233.9 KB (233892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec359e319af75c03e9467a4a59cd1467738dc69be39f2cbf918b3947c6b82af`  
		Last Modified: Mon, 22 Jul 2024 22:07:34 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e98bed6eaaa593e3650e69f96da987f713ae815bfbd482c78c48bf931913926`  
		Last Modified: Mon, 22 Jul 2024 22:07:34 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:6e3ae5e886c82675bdb34a432eb9d8a7f0240e7c5db970c19fdea8f7e16c4018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 KB (87992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ee39bff21c856207add04e6e925ef38a7fa640bb0ff1cb33fd56fd12daca1d`

```dockerfile
```

-	Layers:
	-	`sha256:772974c39aff5028b180d2b7787b3662997f294573da8615d7b10af9e76d606a`  
		Last Modified: Mon, 22 Jul 2024 22:07:34 GMT  
		Size: 73.9 KB (73944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87c940ded2a9e5abcbb64496e225b523b1e8c0c36509d85b7d4f479b6380a8a0`  
		Last Modified: Mon, 22 Jul 2024 22:07:34 GMT  
		Size: 14.0 KB (14048 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:79049fd912edd849604e3af8e72e0c356c44e91632aef9714c3e175131ecefb8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3802792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:012d2294385cec6dff48c560abb8bb181203208a1470cbabb9fbfeb2338d13a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 00:01:42 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 23 Jul 2024 00:01:43 GMT
RUN apk add --no-cache libssl3
# Tue, 23 Jul 2024 00:01:44 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 23 Jul 2024 00:01:53 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 23 Jul 2024 00:01:54 GMT
VOLUME [/spiped]
# Tue, 23 Jul 2024 00:01:54 GMT
WORKDIR /spiped
# Tue, 23 Jul 2024 00:01:54 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 23 Jul 2024 00:01:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 00:01:55 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8182f0f9e1ab782a859b42ed596f6e3b6f0787bc0bfe10bec1e150f640119fbe`  
		Last Modified: Tue, 23 Jul 2024 00:02:05 GMT  
		Size: 961.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae789766f9b133a83a6069ad28511e5815c7395748bc297db22f7f73fd122c5`  
		Last Modified: Tue, 23 Jul 2024 00:02:05 GMT  
		Size: 7.6 KB (7583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296508fccc33cad6d8f4a50cb55dbf9874248ecbcd80e95fde674cdf022c2b3d`  
		Last Modified: Tue, 23 Jul 2024 00:02:06 GMT  
		Size: 222.3 KB (222260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e98c659e933b4dd9faaee36fca0b96c252982f6d0e3163cac917a6f24d3d42`  
		Last Modified: Tue, 23 Jul 2024 00:02:05 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8323855c0c72f94227a105dc9e2a01e34e73a5886939d618dd795c1da2682a5a`  
		Last Modified: Tue, 23 Jul 2024 00:02:05 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:0927923e6ba9f170a8c8397f0937a10123d5ce2030d1cc8a4616648f1843ecec
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3594399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e6eba522d11b938e4a5a0fd13fe9a7ed4913808dbb9b0e12e57ac40a08b1dfd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 22 Jul 2024 22:21:00 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Mon, 22 Jul 2024 22:21:00 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 12:40:32 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Tue, 23 Jul 2024 12:40:38 GMT
RUN apk add --no-cache libssl3
# Tue, 23 Jul 2024 12:40:38 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Tue, 23 Jul 2024 12:42:28 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Tue, 23 Jul 2024 12:42:29 GMT
VOLUME [/spiped]
# Tue, 23 Jul 2024 12:42:29 GMT
WORKDIR /spiped
# Tue, 23 Jul 2024 12:42:31 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Tue, 23 Jul 2024 12:42:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 12:42:32 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefcb64618c152cdbd696579659781b5c5b6fa2819b69ffcfbce51682864688a`  
		Last Modified: Tue, 23 Jul 2024 12:42:51 GMT  
		Size: 960.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e21b43a9d5d099e4dd64101b9d967ae1f7e8fca94bfada0b0b3af18d569e1cc`  
		Last Modified: Tue, 23 Jul 2024 12:42:51 GMT  
		Size: 7.6 KB (7589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8107a44cdf2128a4b4ffbd306fc0e191b05303a16fcb586cd05f8de7de0fdd5`  
		Last Modified: Tue, 23 Jul 2024 12:42:52 GMT  
		Size: 214.7 KB (214740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19926369b0ea15193d239955199a9730efca60cf8748884f9f9cfb2788147040`  
		Last Modified: Tue, 23 Jul 2024 12:42:51 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2d4386a624aed67b9315348b90ec0d8b41a60e4a36c8a1e03c09ece2945261`  
		Last Modified: Tue, 23 Jul 2024 12:42:51 GMT  
		Size: 342.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:a65d9fa900d6612f557bf8de548d302ce35ced2428ddd51bae8855b5dcbfa382
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3681074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc45b2989b70b3355101be6ed2bdf0c8907ddf3bb1cf447401294223311c0223`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:31:06 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped
# Mon, 22 Jul 2024 22:31:09 GMT
RUN apk add --no-cache libssl3
# Mon, 22 Jul 2024 22:31:09 GMT
ENV SPIPED_VERSION=1.6.2 SPIPED_DOWNLOAD_SHA256=05d4687d12d11d7f9888d43f3d80c541b7721c987038d085f71c91bb06204567
# Mon, 22 Jul 2024 22:31:20 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps
# Mon, 22 Jul 2024 22:31:21 GMT
VOLUME [/spiped]
# Mon, 22 Jul 2024 22:31:22 GMT
WORKDIR /spiped
# Mon, 22 Jul 2024 22:31:22 GMT
COPY multi:5bc169de21988025d207318e8462faac29a47f22ea391b38427ea86b5aba8f5a in /usr/local/bin/ 
# Mon, 22 Jul 2024 22:31:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:31:24 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bd6d407196a4cead6a9f2cc24ea12aca7c53bd44033ff736ed615622f0ddc18`  
		Last Modified: Mon, 22 Jul 2024 22:31:38 GMT  
		Size: 960.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6fa051a14b49545502b49f583fc16c38da96912f45a45cdeb92e26b5c20504`  
		Last Modified: Mon, 22 Jul 2024 22:31:38 GMT  
		Size: 7.6 KB (7592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc4fff4936fbe0b61f796eb5834f8d024d00faa9fdbb3321c342de03778b135`  
		Last Modified: Mon, 22 Jul 2024 22:31:38 GMT  
		Size: 211.0 KB (211020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa7ecff8f0066c5c8f8fae607194d409fb27b9b78555ee424d8332d40b92f6b`  
		Last Modified: Mon, 22 Jul 2024 22:31:38 GMT  
		Size: 95.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e357c7e339e19cd0f57b978d487b3d4c4422b7cd3d4431ab2bd0d5b0e747ab`  
		Last Modified: Mon, 22 Jul 2024 22:31:38 GMT  
		Size: 341.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
