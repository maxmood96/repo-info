## `nats:2-alpine`

```console
$ docker pull nats@sha256:28de350897b589b46cbe9be25abd075eaad0faeb45ab4b1c832d1fa0dcf28d6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:1fd834581735b304465d440d706f668b245fa15c90864a8110d0069628504799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (10017410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69bad2eb78b7ad191ae578a8cd1a90bb014cd770b959fdf75228696af9e957b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3eb8f37ad7a3d0e0d42022d3b399dbeb45f39b9a36dd95f9c74eb3ee4ff505`  
		Last Modified: Tue, 10 Dec 2024 23:27:27 GMT  
		Size: 6.4 MB (6371998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d30e571e9a33b90d53adc364b75dc4175a04f59de9d03895a30448068789fd`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64e4621359f08beab60eaf8e077f6f6ab0cec1ab6c999d1fdb4b35235662973`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:205d307881aedf2bd51cd9499b2e7cab47ada6b75a95df123216ad185b195a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9195c0eaed762824d5c53e56fe0b79a7d0d6375197aea07ffe383a513bb9a998`

```dockerfile
```

-	Layers:
	-	`sha256:069960ecffcdfc8e80d9352cfbe93b35fda077faf6c558950c05b3be76d07796`  
		Last Modified: Tue, 10 Dec 2024 23:27:26 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:3569b3c6c6049c65c064d2c1638f58c6373d9779bfbafa529c82b117df449f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9387859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c78fb87af3390f4d569e90248e5ef868c71ea224696608d9676420a21f08204f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d491d6ae32f791b6c6ee444da2433c3fe5f68f95a28a063e08fba789ebeb3f1`  
		Last Modified: Tue, 10 Dec 2024 23:27:13 GMT  
		Size: 6.0 MB (6019710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865e30e55f10109ec4fa649ff5598bb63785974f48e3467909963032f1b75bf3`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e27652e6cdf62ea6391042bda7e59583d83826301e119078799dc7674d5f916`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:5c9032bdc8ef63d822723910e03076cf5c904847843dde7aa3597eb73c844ad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d4723e93aa61b1d00a73afea3fa2d282ca9b9cfbf288b20c9edb846ddc14746`

```dockerfile
```

-	Layers:
	-	`sha256:e07ee39720e7781ee4b9ccfe13bf58df6e7045efc1ed482c9f6a811ceb5c4cb0`  
		Last Modified: Tue, 10 Dec 2024 23:27:12 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a0825f66cb5b9d7837459726ec6ca63a60b3888e8b67c655c7bd4c0ba05448cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 MB (9108253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9dd517c3a03af5824c23a81cedeed2598c4db1f301b3bc2e9bc40f4ab1bd618`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c84334747ecb5ce1375e80f91f5c140846eb6d7d51f9f6e6706641e1534c47`  
		Last Modified: Tue, 10 Dec 2024 23:27:11 GMT  
		Size: 6.0 MB (6007249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8010f8f3390c5e4323711c7f680070162d24e7fe3a14cf0e3d4670bd86647f9f`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573b54805f27aadae125876129ffbe488c10a85a15c36f50824d9ea4120537db`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6332c66401722e3837a6d186f7f9e1998a51350aa4b0af94507fbabb700ebb51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8a5df688f658118f4802867e4073818b174fd568574578a38138431bcbe412`

```dockerfile
```

-	Layers:
	-	`sha256:90edcaab6c14939090cda88a4bafbf0f09deddae7ca690ec3b1cda3e66db02a9`  
		Last Modified: Tue, 10 Dec 2024 23:27:10 GMT  
		Size: 14.4 KB (14430 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:44905153cfe19be67e2baf248d1fe4a687aa2542e28efbff0f08f466e8749d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9912066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18b42869bfcbe5193535e39dc5571d303f0fcfd8c8fef4c6bb885ebe9b16b70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab592abba0f5f4ec119ae6d68f1206012d0485e97bb32949ec2a5bd04eb22f6`  
		Last Modified: Tue, 10 Dec 2024 23:27:05 GMT  
		Size: 5.9 MB (5917911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83961d61cdbd8298afd926b21e9e703be42edad95c17d626d5b2c8f8bdfafca`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403efcdcd91f4b94baeb36d579d722af0241889ee36afa8b92229b2c6eb937b4`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:a25a621ca70ce2b0b97e30ce8ff0dbaed26cdf192d3a9f357bee0ee044c610d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.5 KB (14474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850950126604011113cf97360a1b385355861ecabbe661483a1173cd8dd61172`

```dockerfile
```

-	Layers:
	-	`sha256:92f99c76a992a8785e402afdc8c8fee96331b60410b4a73baacc424b5d4ef722`  
		Last Modified: Tue, 10 Dec 2024 23:27:04 GMT  
		Size: 14.5 KB (14474 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; ppc64le

```console
$ docker pull nats@sha256:d23003b22072b07cea7c57403d30519c9974445420181d8e174fbfa45fa533ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9312362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b0b23cf06fe3a7a78cbf9050f6de38b3cbd86fd9eadd9aa0b576d10af31480`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
ENV NATS_SERVER=2.10.22
# Thu, 17 Oct 2024 18:08:35 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='b4da77b2b194dc5fcf13a1df0dad59ba7e87ae4423f254c50534015b7c8a2369' ;; 		armhf) natsArch='arm6'; sha256='93517bace32ca5a3f11ac7d2e2583b8400d97d5b2d1568de118046471704785a' ;; 		armv7) natsArch='arm7'; sha256='031933280a989142845a99bc381de160404322b7910c154dbad1b171b5c7eeaa' ;; 		x86_64) natsArch='amd64'; sha256='db0b3ccbe4cbdd3872ae7486ec4f6b0f85824632a0789f4da2e0a8518390483e' ;; 		x86) natsArch='386'; sha256='222c2a1069793768ab79812f01eea2497e0fbf3bcc5bcb9638f5be41177c73b3' ;; 		s390x) natsArch='s390x'; sha256='8a3701c677287146e92aab75d037b7655b602a0071872f38d901b63011f6ead9' ;; 		ppc64le) natsArch='ppc64le'; sha256='c03c1186439c7960b99c721a8461c613bea727654582808fd51c773b08a975d0' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Thu, 17 Oct 2024 18:08:35 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Thu, 17 Oct 2024 18:08:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Oct 2024 18:08:35 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aaaa26dccaea10b5b83d01ed56f7a196c902179c89f7b031693a66884d17aef`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 5.7 MB (5738932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bd34510b2845266284f593caae986bea90464fb438d79811c16c21afc268db9`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 560.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beb0025099f5180f9671beb5f58c8b9fb8950f5971472ca2aded6d8c086dfcc`  
		Last Modified: Tue, 12 Nov 2024 03:03:02 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:6ff0dd9b59f440e98ec6d6043cae3c81909695d9cf72e4f75ee2729e8104db86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 KB (14390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72e08b6ff60c9977edbbe63a98b79f532617da8c1b3435d620244dd54347bea`

```dockerfile
```

-	Layers:
	-	`sha256:5f8a5a969359fee4a9f6bfec8cf77271b3a9243079c36ba7fbda1fadd5e0130c`  
		Last Modified: Tue, 12 Nov 2024 03:03:03 GMT  
		Size: 14.4 KB (14390 bytes)  
		MIME: application/vnd.in-toto+json

### `nats:2-alpine` - linux; s390x

```console
$ docker pull nats@sha256:d62285e97415380d73c75ff154d35fa1c6d6bec23a71995a671e665405d855b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9687191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:658e5ca2d2437afce8173f52960e6280cfc673cd68edd78c9b60d8e50f94624b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
ENV NATS_SERVER=2.10.23
# Tue, 10 Dec 2024 19:41:25 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='a267a45cb12deb5bbe5c849ae26b2fc020a86109d62fe94538f6b6550cad620a' ;; 		armhf) natsArch='arm6'; sha256='ad01e4689d6c34a7884f8ffce3ae096b898d466c1bccf1f7f3202002556ed89c' ;; 		armv7) natsArch='arm7'; sha256='a456380e4616be5b3f9afc6eecf1343050eb1ffc4fa73c848df009ff44710468' ;; 		x86_64) natsArch='amd64'; sha256='a79fd5a82ff9fc02f0a9619b121bbdf28f02002163170abef31c81c19a1d3014' ;; 		x86) natsArch='386'; sha256='f40c95d2a1c4133e45421f14c46919427e293ef69ac1b45f63e5b79d2dd09021' ;; 		s390x) natsArch='s390x'; sha256='fa6a5dfa508bec90392754db648d497c8e00192fecf9e36a02a12f757097693c' ;; 		ppc64le) natsArch='ppc64le'; sha256='539a945e9dea88435cd7124afa516a7150c05cbb3e279eb6ac7c359688f970e5' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates tzdata; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY nats-server.conf /etc/nats/nats-server.conf # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
COPY docker-entrypoint.sh /usr/local/bin # buildkit
# Tue, 10 Dec 2024 19:41:25 GMT
EXPOSE map[4222/tcp:{} 6222/tcp:{} 8222/tcp:{}]
# Tue, 10 Dec 2024 19:41:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 10 Dec 2024 19:41:25 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f889b72b6e6f2f7a8f55853722d58f9f51fb766899e07465539676a22f0ca84`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 6.2 MB (6216702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:995a4bc6424d4d94211f245dfd6f8f7975eea36b074521a866fbb75000ae79cd`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 561.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2990cf750e1e6ae965cb5ee3aa09fb5555f8709d7b9fd091ff70f124dd53a69d`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nats:2-alpine` - unknown; unknown

```console
$ docker pull nats@sha256:ef1002190acf6bcefe4da93459355df9b9bd492b52bf5895f710fadb82698c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 KB (14322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bbee94701029b1f45fcbe9dbe8783e933466d45dd6eeefdb23d66cbb64483b5`

```dockerfile
```

-	Layers:
	-	`sha256:8c627f5f6e115176dd03af0a018e19fad71b8bb00277a4792730d383bd1e9868`  
		Last Modified: Tue, 10 Dec 2024 23:30:11 GMT  
		Size: 14.3 KB (14322 bytes)  
		MIME: application/vnd.in-toto+json
