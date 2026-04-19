## `spiped:alpine`

```console
$ docker pull spiped@sha256:10785aa58079387363e472d7e20eb96bd01f12b9850476a066e124d57be1a8cc
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
$ docker pull spiped@sha256:6a78a135961dde77e0a3e9171928717694804d7cfb3d6aedbebfadb42bf4f3e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3925151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f599634d068048f3fcd01d27356e8cc57fb8937f8bbf03cfccaebddd3b1e24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:14:35 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:14:36 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:14:45 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:14:45 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:14:45 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:14:45 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:14:45 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:14:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:14:45 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09629d4032ef7ab1ef9db974170b9cf0e98f6c5d68cb9f3d0e21a37889d50030`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad68e6c6d9b805cb5d27e526a335f55ae1e22e51fb78ed5cd842984966ec752`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 7.9 KB (7942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0097cdb4e276728ffaa69c00b45edf54d761118176e68ef12d68092b7417f986`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 107.6 KB (107638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bc806c3d4f80593516df4d73efec6cd1cf16dfd200d5fd6adda41910072975`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d250500ebc740f642b6509ef0a3f0576fe4b93cb687a514ceede64292cd717f`  
		Last Modified: Fri, 17 Apr 2026 00:14:51 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:dcf1f88cd35b0648a36b53371be8057efc788150c247273946f22f226c8922f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 KB (96450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b695771cd59164f79af4e3d51a194af63f71274fa2ca45642700481f66706680`

```dockerfile
```

-	Layers:
	-	`sha256:9047c6064b6fcd9efa90aa0c959722cd5d0677dd3e15d576484c71664c66a025`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 82.2 KB (82192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1ebf9604f23105cb6660c6767d301a937a4b9d6d85433f32e35ffb2ba1e86d8`  
		Last Modified: Fri, 17 Apr 2026 00:14:50 GMT  
		Size: 14.3 KB (14258 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:e61a3952e5718375c379136684659c21136328808a6c3f88e9585943251e9a16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3605859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c576e8f7269c2ef4826f92b4a22494225a6cd470d17d9f30f01d9cc229e696f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:28:09 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:28:10 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:28:20 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:28:20 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:28:20 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:28:20 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:28:20 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:28:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:28:20 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a28595f303e8390d8534900bd78b38647a907732d3d3e842c7b3a9caf747dfa`  
		Last Modified: Fri, 17 Apr 2026 00:28:24 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a2d882259c543692d98198b2c8f098f64b95d9b8018fbe3daf4bce16ccdea8`  
		Last Modified: Fri, 17 Apr 2026 00:28:24 GMT  
		Size: 7.9 KB (7941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750bf6b03a38c9f5493952dd7c83dba844fa70e86926b54303c228f996e864fb`  
		Last Modified: Fri, 17 Apr 2026 00:28:24 GMT  
		Size: 89.2 KB (89153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb0b56fb727ea9f7a3dad23a396c81b60139284396a263e6658329c844b5dad`  
		Last Modified: Fri, 17 Apr 2026 00:28:23 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e6b266845306bbbcbee6801a12889b7c152b510808934deb45a090cedc3a06`  
		Last Modified: Fri, 17 Apr 2026 00:28:25 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:e8ab0469cf1a0658dd7f777f120002189b116eedc60e2d13004809373539fd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 KB (14144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfbd38bcf39cf976d74f4ea0d61a864e9b890815035438f477a99caff10eae99`

```dockerfile
```

-	Layers:
	-	`sha256:acf29d68d1e7fa30dc5742c4211ffe81430df68660be1f3d0207d5a94d98bc39`  
		Last Modified: Fri, 17 Apr 2026 00:28:23 GMT  
		Size: 14.1 KB (14144 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:147fe0124aa237fa168a69becb6a2db57f4a9ad7144beb44a52a7735a75ed88f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3316848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fac8ff5e55f7bb423942ebc9a0dcfe62ab45560df8acbf81f20fce40adfb0d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:13:44 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:13:45 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:13:54 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:13:54 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:13:54 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:13:54 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:13:54 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:13:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:13:54 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e48112adbff0844ea29be59655ce36bdc68db268960b43349a213160861be5b`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b71c7a3ae36749950f95514df7064116e47fac5d0e8f2b2a7465a08ec730b1`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 7.9 KB (7949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90dbc42fa35611c27c8478a77677c7599958f859178a2ae432cdeea23ff283fe`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 81.7 KB (81682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d17f9759dca0bc64327214acbd9fd3deb78375c7afd7010e30d54ffe9eafdb6`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87eff9de0017984f4c4aceb50f22ba5600d01062af116b4a3d8666f104982e79`  
		Last Modified: Fri, 17 Apr 2026 00:14:00 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:87b16d20b49f4fd531d2a7882ebf70ab433c78455a68ecb63229df2b111b80e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db1828da7718e04747ebb0f602b5974b0a7a0da76481d2a933ecbb6b1869fd9`

```dockerfile
```

-	Layers:
	-	`sha256:32fd82b374cd8966ecaddf73d35913d341f1bf089acec4758b0eddc9ae15bf6c`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 82.2 KB (82228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:451cb443bac28fadec04af355b08de89c30845228bcead9735b3be6a627381f6`  
		Last Modified: Fri, 17 Apr 2026 00:13:59 GMT  
		Size: 14.4 KB (14362 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:1fd688a89197aa9ec5aa2ecf456f856d56b46639e5d0733ee167c8e1f1f67c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4251815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3e3a3494482e2c117fe69680a253048739b96db6b666e0ba693d69f12f3cffa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:30 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:23:30 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:23:40 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:23:40 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:23:40 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:23:40 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:23:40 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:23:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:23:40 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b70cf46309ade34c5a66991fc83a20e95c2a2ca7662393d07532b98169b897`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa5fdf2c2bb57fb12d420f1ebc379b73a6a07a076dd649edbdfb2ec65e9b52f`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 7.9 KB (7939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bde94e8b5d108bfaf26624adc0087452e38a2a8176cc98ece876fe2117fc72`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 100.6 KB (100601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5b88c8155b1bdcaf3ceb67be1cd60eac4d053dbde4189b58b41e709ce71a5d`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb330bcfc9ca5ba0cfa2155b2866b977ad2c3ce1d9ae151d07e639bbada8ed2`  
		Last Modified: Fri, 17 Apr 2026 00:23:46 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:fc73de67fe7f5bcda008d343140166980bf4176b3096a535d83f3dcd2d534e5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 KB (96641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a18fe2b2319a581866e1c86ace119888f0e7b9a60b55a3ce6b779f28fe92710`

```dockerfile
```

-	Layers:
	-	`sha256:a96c2085f2ac76644e77254bfa9bf6d1b56c67d9d9405eaa8416f74fcba97701`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 82.2 KB (82248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7d5f7f4737f85a0e24460592078844c64dafe02803bdf87581c20f597e952bb`  
		Last Modified: Fri, 17 Apr 2026 00:23:45 GMT  
		Size: 14.4 KB (14393 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; 386

```console
$ docker pull spiped@sha256:60c2f83afdec0385615a7286994daa8f205766ef71d83fa8ddc2e700ac81936f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3754157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdc7573391c8c621e1b2f987722ca168aebbe555b0499e62e86738da10c96e58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 05:54:58 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 05:54:58 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 05:55:09 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 05:55:09 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 05:55:09 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 05:55:09 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 05:55:09 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 05:55:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 05:55:09 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f934ad8efa54d7383ed1d7daf8f07d69a316c785b55e29d855f59724767ac5`  
		Last Modified: Fri, 17 Apr 2026 05:55:13 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fad6a50d64bebedb5b11ecc9dbad14debf2baa30235c5ed093775151dd20c5f`  
		Last Modified: Fri, 17 Apr 2026 05:55:13 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e9ad205a738e9a190290cb841b91a7516b90d39ccefc8a464803a80e5d3bf2`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 120.1 KB (120105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13bce07410da4d5d2d2271580461ed3ae19008e5249df3c1003a06c213c180b`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d30a682d686a1255ac7f31b311acf6f01b819da6af05a18bb59cf9285441247`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:499b7ec7b9c4e4eec426321c8934ac7fac003aeff1b6247ccf002c546cd6a262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.4 KB (96390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9072722cf70bdbdd1bd5420a6744bc8ca176440a12571a40e33ce18862067a55`

```dockerfile
```

-	Layers:
	-	`sha256:dd1f08b2c21c938da19a9533a1b9dcb5f15e078dab41c9a4bd4ab244cd979858`  
		Last Modified: Fri, 17 Apr 2026 05:55:13 GMT  
		Size: 82.2 KB (82167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:517f76f905b9dca96e65eec9ad79a6211e1b541723537e827a226d4839aa2649`  
		Last Modified: Fri, 17 Apr 2026 05:55:14 GMT  
		Size: 14.2 KB (14223 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:cd9ed7a248ccd86ed221ed62ccb5fccc85d88f92bb07eacf32a54aa285d3baef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3858669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b17425a87a9b3f6cf310b87ae46b1234772bd0b80ea164489da909a148229e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 01:13:47 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 01:13:49 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 01:14:13 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 01:14:13 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 01:14:13 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 01:14:15 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 01:14:15 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 01:14:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 01:14:15 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d4eb2b31b373fa4117e61ee4973c717af31bc2e3376684ddf64780f6a0cfbf2`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5bc892fe10dffc5824aa6f02e4a3fd2d8872fcc548dc32d8271fbeda871d54`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 8.0 KB (7951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0f69169c64986eaf44f560100f0ace1b79586cff5d1f517fcf6f2810fcf476`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 112.7 KB (112676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecc1153f644e2e26a00aa90bf9b03917ab7f9ec331b32bd9bc295281cee7151`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94785087e434424ecd2b2a79b34d04d7aa53bdc943265138216cadd6badf5495`  
		Last Modified: Fri, 17 Apr 2026 01:14:37 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:42b060f58ef29347aa95f2a95a49a750c85e6dc1283a7429bdbd08cbb35d8c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aeddc4f5e06133647f4d77b87d5471240c741e9ac4581ee0469cd5e684bde41`

```dockerfile
```

-	Layers:
	-	`sha256:8054970ddb854b9dbe87ad8cc6cb52f8ac69bae6393895a2cc0ec179d9890648`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 80.3 KB (80275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cf789792086c7df442c741fa726e1c634b400a002527085dcc36c87a5bdd724`  
		Last Modified: Fri, 17 Apr 2026 01:14:36 GMT  
		Size: 14.3 KB (14307 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:eaf86ffaae6edde3dcb5bc958a07fa09bfe7cf9bcd05be9ace676e83efe5f761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:508a25834d52056b9c731fc2100ea35e54d563c093104a90eef8c05cb0cd1cf9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Fri, 17 Apr 2026 07:18:45 GMT
ADD alpine-minirootfs-3.22.4-riscv64.tar.gz / # buildkit
# Fri, 17 Apr 2026 07:18:45 GMT
CMD ["/bin/sh"]
# Sun, 19 Apr 2026 03:43:32 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Sun, 19 Apr 2026 03:43:36 GMT
RUN apk add --no-cache libssl3 # buildkit
# Sun, 19 Apr 2026 03:45:16 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Sun, 19 Apr 2026 03:45:16 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Sun, 19 Apr 2026 03:45:16 GMT
VOLUME [/spiped]
# Sun, 19 Apr 2026 03:45:16 GMT
WORKDIR /spiped
# Sun, 19 Apr 2026 03:45:17 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Sun, 19 Apr 2026 03:45:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 19 Apr 2026 03:45:17 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:fbc07c8b85a3c60e503ffd0cbe3e1b3947fd65764784e1bd9d943ac21097cce7`  
		Last Modified: Fri, 17 Apr 2026 07:19:08 GMT  
		Size: 3.5 MB (3520880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f6ee73726995fef9f6ea4faf4767bcea48e04bfd71f1eea0bd05f9534d43f8`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce2dd3bcf1d4c6316b374da1b2790b7de4b60cf8e6512e5f30f8d7b2d7a3b38`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 7.9 KB (7940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e66ca15c2a84ed0ad5aac95f1257383ec006115c07282942c1fd6f06bc2b26`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 98.8 KB (98844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a854d7ad8f0e7a7a6274e5c362b1a896bd76e462c14408778ba02dff83d37b`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ff5f61469b0ef7c1c8bf56662d9b762181e909bc3c749eacbaaecf7bb475ab`  
		Last Modified: Sun, 19 Apr 2026 03:45:39 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f21b45950838bc0c80c8410cc4f2814b68f96ecad1e19be90b06994c99afbf58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 KB (94574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1abe71f567ae68daf6e6dfeaafd74f8104d7a6958082dd986f64838b44c12b9f`

```dockerfile
```

-	Layers:
	-	`sha256:e9f4f6fe1bacdcf68608f4eb99bf2115bae97f39b1056b72d36c08b63e32ef42`  
		Last Modified: Sun, 19 Apr 2026 03:45:37 GMT  
		Size: 80.3 KB (80271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5e5c1e0a1d68c8bdb360c97f9072a3c973409b2f9afe7ff5795d523cae5119b`  
		Last Modified: Sun, 19 Apr 2026 03:45:38 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:alpine` - linux; s390x

```console
$ docker pull spiped@sha256:d63a333156f14c550016968b48b61e03d6ffa7cdadeb4dc11994993be83c667f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3760132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:425f883e0aba651c328e78b42abc6210940d11022f1ee5d1ff5258ebca42e51f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:41:11 GMT
RUN set -x &&	addgroup -S spiped &&	adduser -S -G spiped spiped # buildkit
# Fri, 17 Apr 2026 00:41:12 GMT
RUN apk add --no-cache libssl3 # buildkit
# Fri, 17 Apr 2026 00:41:19 GMT
ENV SPIPED_VERSION=1.6.4 SPIPED_DOWNLOAD_SHA256=424fb4d3769d912b04de43d21cc32748cdfd3121c4f1d26d549992a54678e06a
# Fri, 17 Apr 2026 00:41:19 GMT
RUN set -x &&	apk add --no-cache --virtual .build-deps 		curl 		gcc 		make 		musl-dev 		openssl-dev 		tar &&	curl -fsSL "https://www.tarsnap.com/spiped/spiped-$SPIPED_VERSION.tgz" -o spiped.tar.gz &&	echo "$SPIPED_DOWNLOAD_SHA256 *spiped.tar.gz" |sha256sum -c - &&	mkdir -p /usr/local/src/spiped &&	tar xzf "spiped.tar.gz" -C /usr/local/src/spiped --strip-components=1 &&	rm "spiped.tar.gz" &&	CC=gcc make -C /usr/local/src/spiped &&	make -C /usr/local/src/spiped install &&	rm -rf /usr/local/src/spiped &&	apk del --no-network .build-deps # buildkit
# Fri, 17 Apr 2026 00:41:19 GMT
VOLUME [/spiped]
# Fri, 17 Apr 2026 00:41:19 GMT
WORKDIR /spiped
# Fri, 17 Apr 2026 00:41:19 GMT
COPY *.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 00:41:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 00:41:19 GMT
CMD ["spiped"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c5658f716398e67bcdf451aa62d9268badc01207fb2761dde286827e782131`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d837fc0069a0ae8449bb0adb9f65b43fff5ff059948bf845ea728a30d3eaca0`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 7.9 KB (7947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:669f2f936af1acb505aa131fbad0547df0d36ff3dc9c4f8c3a396c9877b87798`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 96.9 KB (96930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33930e4a86d8157d355b84eecf720d4f20b38ee3502ab3baa6329d6c6acac811`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27970db5cca98e64b9bdffc3b4445e18a503e3e0dc858c6ae91eff10bccd50bd`  
		Last Modified: Fri, 17 Apr 2026 00:41:29 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:3a63421a60ad516e8ae99df7c008ce97158220da99f3e592d9090f762eb254c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.5 KB (94497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03ae27771b3c7505fb78b0f0546a7416b11e879220de4dc6090bf643dedf8614`

```dockerfile
```

-	Layers:
	-	`sha256:c6abf9efd631a7212221f0b771ec35e734885be3d3a6755a004bba8bd46cc068`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 80.2 KB (80241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:033e56e9f47fa0453060710502d5ab3daddcba0cc4e51e5e138a57faf3e873d6`  
		Last Modified: Fri, 17 Apr 2026 00:41:28 GMT  
		Size: 14.3 KB (14256 bytes)  
		MIME: application/vnd.in-toto+json
