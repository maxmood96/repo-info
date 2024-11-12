## `spiped:1-alpine`

```console
$ docker pull spiped@sha256:276b03c59517451c42587f11be1daee1b305428b9c1028ed9c580f1cabd7a3a2
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
$ docker pull spiped@sha256:daefb5299ff2e9476112aa9c609b5264e2c34f92126f0bb20e29d5c14ef90fee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6132905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29aab44abfc742685430558f3458335cf0cd806c6d386b3eed8c756a4666be89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
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
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44372b8a42e415e28022098de7f58892719831ddb3b69d1982475c01e1ebcee9`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4d3d0195931e82893a059b29aa5e09859b561a5699199003caa76db025a103`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 7.6 KB (7552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faaff9889bcd7686a7e389188c9b1da11b944593c3f367ce73321c9cd1f9f4d3`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 2.5 MB (2500052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742ceb23f0c29b5b00035c6ae582d5ff76d9120d036d2c2963228c0b95b636c1`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcda00b0c3a86b025e7acc0393e7b903b2a7e0174aa346d91d7ec0647b02082d`  
		Last Modified: Tue, 12 Nov 2024 02:37:27 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:dd862b700b2f279233f9ae16d5c25154680ee1dfcd86f522a853623380c7e63f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 KB (88486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d60c4488d7285be9cc92fe8c34981fd09686e9eece95b44097621805a9422d86`

```dockerfile
```

-	Layers:
	-	`sha256:0c0c153d8884f2d689fb54feef58d5b3f507c9257a4da7ef17c63cc34edfbab7`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 74.2 KB (74181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f273e32436d0f59afb7e53948d572f8c2a58adad3690545a558a4a9074424b5`  
		Last Modified: Tue, 12 Nov 2024 02:37:26 GMT  
		Size: 14.3 KB (14305 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v6

```console
$ docker pull spiped@sha256:5b42c6f2c6f6d4daf16d2b7f02566b892213498a607898ec86fe4f13ba174433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5530602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae2a9c2c8102d9dfaf0e25652471e9e17f0128392eb62b35fd98ecf2ae3a790b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
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
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2124325dc5cb0e691b81062d52602d82e66cf4a54d05d890bdf506e6eb914835`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8bc56b9fe431e43e990d6ce1df319af96d7a3c550c23870b2c1051a27fbe06`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 7.6 KB (7555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4007f0c3a790e3d7107168b4005f37de82f1c1c5d974f34ba3933bbc0419ea4a`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 2.2 MB (2155051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11376d8ca4651e301f66a4e1203da53694eb1be5d78239a60c000768c941525`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a2a3ed2d5ea66800cdf4bb8bb04faca0e1725b756688c0d63daf5bcca2d310`  
		Last Modified: Tue, 12 Nov 2024 06:29:08 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:66e0dc5536fdbd525be5c4d9f9f3ae6c4cffce04ff577a831143d54d7876dc1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cf059becbf5ff9f78307636057df7a043c0d5e6d27cb25c8d761b7fba67b075`

```dockerfile
```

-	Layers:
	-	`sha256:2e10f6bc35866f5a553ae9a114eafa57e88f05f4423cbac2a76088422ce325c0`  
		Last Modified: Tue, 12 Nov 2024 06:29:07 GMT  
		Size: 14.2 KB (14192 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm variant v7

```console
$ docker pull spiped@sha256:161201451dae6d4907ca596a7927b7b39ff298b1b989ae07301a6da6e9caaa00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3306247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1231bb39d5253343162952cb3cc8917b6c045df096d18ac857630ba491cda03`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
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
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98f533a77903fd8a03af52595b5de03c878989df6519d84538b6eaf3b5b2641`  
		Last Modified: Sat, 07 Sep 2024 13:05:35 GMT  
		Size: 962.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12376083ab2660c02129efa85f679a7ab2da2f8a1134143518d085ce6923f0d1`  
		Last Modified: Sat, 07 Sep 2024 13:05:35 GMT  
		Size: 7.6 KB (7563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef71d51de932d94cad045963fd6c9f6d23b6131f6ac382b8cae6d63d5743b82a`  
		Last Modified: Sat, 07 Sep 2024 13:05:35 GMT  
		Size: 201.8 KB (201787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c043580e61acb1624006d0a8cd483135cfd738b0c14c63ee82bd9fd4871154`  
		Last Modified: Sat, 07 Sep 2024 13:05:35 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df83588dc27b5db3ec08ad8cd7d244291d386db62f2ccc0c1aa11cc2e7c5715e`  
		Last Modified: Sat, 07 Sep 2024 13:05:36 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:1aa185e2658541eec1ab6ebfef7335c36b84ef32a0426fb9b6d38d0fff5198ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 KB (88181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6359f2731732e3f2c62ceb19da84ed6fee0d35da1405ee671cc30346f4a98f8`

```dockerfile
```

-	Layers:
	-	`sha256:5000164e37bf0b63663b7ad51aba190e24ea650aa565186be566d117956b0453`  
		Last Modified: Sat, 07 Sep 2024 13:05:34 GMT  
		Size: 74.0 KB (74005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d38a4187c32d7c9a1c5cab6b23f72f7d35ddf9fa94427b042f4efee8f7cc0e1`  
		Last Modified: Sat, 07 Sep 2024 13:05:35 GMT  
		Size: 14.2 KB (14176 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; arm64 variant v8

```console
$ docker pull spiped@sha256:083c6333ddfea28a49a285ef8800cb1c150cb7aba7426aa9431d5c73207dbe64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4314874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f750b9d67e7649a84bfa81bf12529452df480e28211ef9ef02adf5813222ec2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba48cd68a380a962fb21dc9a60b53cdf8a5f074de589ed64f30342e034064084`  
		Last Modified: Sat, 07 Sep 2024 11:57:18 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650772ebdc0ec7428ea184403385f48eead76d50c6cec6f0e64f53ce6d441b21`  
		Last Modified: Sat, 07 Sep 2024 11:57:18 GMT  
		Size: 7.6 KB (7560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c55b3a6bf29494a265217dcd433c380f8206d47a7104b9fded2de78405372af`  
		Last Modified: Sat, 07 Sep 2024 11:57:18 GMT  
		Size: 218.3 KB (218272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d81fed18646ded34d11d2443a645f7c215a516b8b7059795db4800be875330`  
		Last Modified: Sat, 07 Sep 2024 11:57:18 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7e51966599430c170a8014b930e6112b2bd2eae3d2eb4d0bbc1ee585983672`  
		Last Modified: Sat, 07 Sep 2024 11:57:19 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:2efdd61d63b3e554962cab48448620e3fb74228f7a7387bcfc77d69dbf7e01b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 KB (88406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec45104e3a030499a2b49aa62b8628d3d4d09a36271cbb2c6126946148041ec7`

```dockerfile
```

-	Layers:
	-	`sha256:99198e1d78acac6d82b6c3dad010da870e1adde6e785e0dd3bc5edb9c448fe49`  
		Last Modified: Sat, 07 Sep 2024 11:57:18 GMT  
		Size: 74.0 KB (74025 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e39f3225560954616d3962bf01a96da278177914644626d7e5c973a9f940c8d8`  
		Last Modified: Sat, 07 Sep 2024 11:57:18 GMT  
		Size: 14.4 KB (14381 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; 386

```console
$ docker pull spiped@sha256:6d46f04e30a3105fc3141267e91ffb5ba3050aa7be87148dcc59dd960122b8d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5825462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bbcb7b0f29ba9dab0f0c1726527e43ed4016181bd95ab9debba9300da8dad8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
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
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97a6fd63828fbfe315eb146a6e09131a00451eb6df7364f89b2838fc8967506`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71549e122188c29598764406aede3a2d7f39ee116980cb024522fa714099248e`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 7.6 KB (7562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9082d20944f15111e92d68546d0843fef30343a5d20401f9dbbbaa559107f7`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 2.3 MB (2347284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a12d1f809df9acb5e86279c66f9f620f87d4359dd8b552217833aabf984c725`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565e15916b0ca46193b8a9e1c83bc74904a8fd5ac8d51710d11a9cd1974c67f2`  
		Last Modified: Tue, 12 Nov 2024 02:10:45 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:ae024814f19ccf108f4c49012d543026dcebbcda6cf432b72e679e80eac307c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 KB (88425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f85c7eb8498f8dab641cf09ac2320681a6bfeb6471034d0b8f17c0413c26f96`

```dockerfile
```

-	Layers:
	-	`sha256:c338f2f328277430db1def5c4614e72997853bf84529ed6d44202ce3949aad37`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 74.2 KB (74156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5902723b69c008d179c3e0da07749f803cb6ad90ba97a9c3feb151d76dadba00`  
		Last Modified: Tue, 12 Nov 2024 02:10:44 GMT  
		Size: 14.3 KB (14269 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; ppc64le

```console
$ docker pull spiped@sha256:8afb3bf99c94a591d0eba15d96253b003415424195f369f761365ded0250911e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5946540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c165f7c09f005647071973ca64009e4fcfbb357266bce909503a70125b3cc603`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
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
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acff226d267e2f526a684557f036f58a914c59247be39068651a3bbb5be99c8`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8522a836c3199ccf9b49cd625b0801b4893ca92b819606a20a60eef862d763fa`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0aca5aa27b0c34935f8383d3017c2e1b574336e405b6e683e2fd18f0544bc9d`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 2.4 MB (2365118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39730da67a08ee98eba5461d059c4ae17310847df8147206ae9dd3c915a2a053`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1466bf84e7abe5d6dc8431df5577ea2e1eb5767f85402df0d10e38bd9b21175`  
		Last Modified: Tue, 12 Nov 2024 08:08:13 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:68986bada3dc3e301441051f41dd84386659fa6521bcfba1865e24368e919451
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 KB (86614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbbad23dc8d88c7da7f63057b1a78301962cad8edf146f8c53a7fdcd9a7b558`

```dockerfile
```

-	Layers:
	-	`sha256:8af705f7ad2b931357ae0f8d34cff42c83b9ea58f0a34298a04cbebcab791e59`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 72.3 KB (72261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90553d9dcd0f0a8f53c333aed2eed7edd767d790498bd322ce254e64fa3dd8cb`  
		Last Modified: Tue, 12 Nov 2024 08:08:12 GMT  
		Size: 14.4 KB (14353 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; riscv64

```console
$ docker pull spiped@sha256:fc73e7236b6bef7ae4e927b48b5f9664ec1649c147bea9f2a1c59a6873ba7f73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3594989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe942b3c121009cdd9974db0f5820e5602448acd7a0a008460216b96b9d45b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
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
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd35a75d4c2c9ec2f11caded5eb8c328382a7514f10e36cd88d52b7833c72a43`  
		Last Modified: Sun, 08 Sep 2024 17:35:43 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1753ce898cf51bfb141701861e58962bcfbf488858498f19dfced7295ff1964d`  
		Last Modified: Sun, 08 Sep 2024 17:35:43 GMT  
		Size: 7.6 KB (7566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdeab123af8ffdd5fee87d27bba647137362da0d65b8e1efec942f7b9a4cf7a`  
		Last Modified: Sun, 08 Sep 2024 17:35:43 GMT  
		Size: 214.6 KB (214574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3e52678b5331c28014609747ec3773ee7f655677938ee75bd7a9cba76cfa30`  
		Last Modified: Sun, 08 Sep 2024 17:35:43 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c1898347b383d4b061e159823944d559655b0436512cbadefacf4db2805911`  
		Last Modified: Sun, 08 Sep 2024 17:35:44 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:f87ef4375f368e30c6154a357caaf21da5ebbabeac773e74984b92d4ec45af8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.2 KB (86167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b718e7b3d1ec3e5cd424eea757ac306bac092cc4ff50649efa5c991ad7d4ecf`

```dockerfile
```

-	Layers:
	-	`sha256:74ca122aff7cd1770a8f2ad1bbe9efd239ef1ef2fccf3f4238b761f6ba4efbb9`  
		Last Modified: Sun, 08 Sep 2024 17:35:43 GMT  
		Size: 72.0 KB (72045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb44c59ce40148f46174cd2792c75bf5cdba058bc968551a0bffedd77dc30ae7`  
		Last Modified: Sun, 08 Sep 2024 17:35:43 GMT  
		Size: 14.1 KB (14122 bytes)  
		MIME: application/vnd.in-toto+json

### `spiped:1-alpine` - linux; s390x

```console
$ docker pull spiped@sha256:30464ff5097e65f47e6a755c9c779d3075ff07a1e9de556d11e7c96a7a94bd7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5713802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb33bd33066b8fc5173e375f27f7f9452ab4ccf03a15c2a86c9ee2c7b389d04`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["spiped"]`

```dockerfile
# Thu, 23 May 2024 19:15:47 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
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
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8899981d6f06508315b3001ebf4f1bde53ab20235caaa013f5ba8c77a73e8adb`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6687c63f48eb23b685aac39d34fd10d946be39a35d263efb7f96ab22c27e5540`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 7.6 KB (7564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acea042cc930aa404c9b71350854bad5f8f7641916069b37d0d586596d4bbd2d`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 2.2 MB (2243236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43854f54c63f7333c81ead906bd289eb4a3559aed20097234270a6b9ac8a472c`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 96.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d137c29c807dddaad7226bf07aa3e0a203dd1839e595b93c07975336ff0379`  
		Last Modified: Tue, 12 Nov 2024 08:43:36 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `spiped:1-alpine` - unknown; unknown

```console
$ docker pull spiped@sha256:0eae92830e9bc1adf13eac44f18f428cde18ca2b63aae15579bcf3fef67941d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 KB (86532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d8e6d1cfce745a53aeb2213c583ad2b0372bccd118edc86a78c30b8dc0d5b8`

```dockerfile
```

-	Layers:
	-	`sha256:511653a9b9e8708d56eb05048ec62f75f94b92d11463839efcc6c8f9d950ddbd`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 72.2 KB (72227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23d284526c8ef1bc8f766ba9f4b30d40ffacde5f0411805933554ef0edf6dc33`  
		Last Modified: Tue, 12 Nov 2024 08:43:35 GMT  
		Size: 14.3 KB (14305 bytes)  
		MIME: application/vnd.in-toto+json
