## `memcached:1-alpine3.20`

```console
$ docker pull memcached@sha256:2b6d013398d4378725160b72146e1474f1fff972f20007e9be35462f788106fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `memcached:1-alpine3.20` - linux; amd64

```console
$ docker pull memcached@sha256:4f636331d99e7859ede8d7dd014cfa53a5e92eaf3777f093d89d3983720dfcb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6960134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936dbfa3fd1abfad39b7b0fdea52dc9058f57a2ab20386ba8fbe0f7f24ce787b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26b915f1b9543f0886910e63fe988f08899ef9f0f344868c656abe60285a185`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c665f9336f93364242fde9455359a2b93e137d737e487f9b841a91534dd1368a`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 103.8 KB (103828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e954354cda89cb935181b0a348fd6f41f4d992c43197804105e6d03be748672`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 3.2 MB (3231096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18046f40002ec111298b116ce4e8d3d3a2b4971bff73e16b695fc3ca53a74c1c`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 281.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99802c96d1fa5b996ad1cfd9ad3452d835ff1e09b731d9c28deb0e6690e7a4b0`  
		Last Modified: Tue, 02 Jul 2024 01:00:23 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:73d7a518f76ec25277d9d79b4963737f0dabc086017bf8b2a7024b623eea5db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 KB (103621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a8d05aae8e5c34a4ca9aeb538f7ea4369e247e0d2fdadd86c6d63a1734f8d78`

```dockerfile
```

-	Layers:
	-	`sha256:9da5fa316b98980df5043bbf4cf4413801ed2e446f4cdb8092af309610f6c97b`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 84.3 KB (84268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0edbab2e6b88780fdcd56a1b9aabb3b1bd2b16daa2d00d77db6e95d9ff0b7f7`  
		Last Modified: Tue, 02 Jul 2024 01:00:22 GMT  
		Size: 19.4 KB (19353 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:35eac1f5b7835d1c3c98701795d2f1005ab38f09a9b9087bcd293aa42a17e04f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5170062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ca771b3c7ebcc981d572fbb09ad635a3aadab6879bf08706473926a1f59e1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 31 May 2024 18:54:13 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Fri, 31 May 2024 18:54:13 GMT
CMD ["/bin/sh"]
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN apk add --no-cache libsasl # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_VERSION=1.6.28
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.28.tar.gz
# Fri, 31 May 2024 18:54:13 GMT
ENV MEMCACHED_SHA1=d7857f9bf51abb2d2106fc6c278682d2f5d7471b
# Fri, 31 May 2024 18:54:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Fri, 31 May 2024 18:54:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 May 2024 18:54:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 31 May 2024 18:54:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 May 2024 18:54:13 GMT
USER memcache
# Fri, 31 May 2024 18:54:13 GMT
EXPOSE map[11211/tcp:{}]
# Fri, 31 May 2024 18:54:13 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db67119e77a171fc68890b30cc22770bed30655ebbeefb6978944d6a117a2bc4`  
		Last Modified: Fri, 21 Jun 2024 05:16:13 GMT  
		Size: 963.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74de22a0366c9bf3e3b174ac5b5d634659b6a1e8eff30e3912c1b5d83ced143f`  
		Last Modified: Fri, 21 Jun 2024 05:16:13 GMT  
		Size: 121.0 KB (121022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc55b8ea0a947fde87113a8814af4ffcf4e07cd724dd7fa156bfaeffac5baea6`  
		Last Modified: Fri, 21 Jun 2024 05:16:13 GMT  
		Size: 958.9 KB (958876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd57044a4703b57d0af563332fc647988609bab2826904490946c888a72dc1a`  
		Last Modified: Fri, 21 Jun 2024 05:16:13 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a6e1dbb865595f24d92b7d974a5011cd110c67f785e7707484810f93885241`  
		Last Modified: Fri, 21 Jun 2024 05:16:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:69165796fd00c29b0ce1c7263d265a991c0559338fb09617b369b072e95f91ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 KB (104070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e181f3e9f0847fcd48fdb9ae0bcc8f75fe9751dbe30f9be7b1c62bd8412dc7c`

```dockerfile
```

-	Layers:
	-	`sha256:a3c082695151f6d795737444a705cdd16ed7a614d69d7d80e2f8d6f13106b465`  
		Last Modified: Fri, 21 Jun 2024 05:16:13 GMT  
		Size: 84.4 KB (84372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ab958b1a4dc6f55956e790cf992b06078d328ed32dee98786bb2e06ae1edcab`  
		Last Modified: Fri, 21 Jun 2024 05:16:13 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; 386

```console
$ docker pull memcached@sha256:8d7fbdd5d6877ccb4a574cf5c9de3d59feaac705bfd587d6c24fb615fdc6e8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6641835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6abaf93cf24e7875f37cf12d93bfb58e05c011eb2e3754b645bb625a96fee6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 17:38:24 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
# Thu, 20 Jun 2024 17:38:25 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435b3e81c95c2b8079972c787cc83f55c78bb0bf2ad85b04fb4aface4e18eed7`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 964.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c519a886b125ff54b3b46ca4905c0a9ec42fc38e81ea4bd3e70cdf3c52407763`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 109.0 KB (108961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823f9499beaa9fdf553572a7df5803de76327a430f67c096137cfeb6dfa754bf`  
		Last Modified: Tue, 02 Jul 2024 01:00:31 GMT  
		Size: 3.1 MB (3062044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc82753d22b3be2306600440be270aee9a23111c22fc381190b65e52e98e1805`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830e0491c4ff9b45588516ceb945b8d0eaf53caa87badf7a3fd3173b664fd28e`  
		Last Modified: Tue, 02 Jul 2024 01:00:32 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:6ca0f87db1aacc6fcc7c7ac740861fa72e5f1959446565b95af596edd530d869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 KB (103521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b62821656353ae9b32793c8f0b9eb5bda543c9960f354015df0973d6464644`

```dockerfile
```

-	Layers:
	-	`sha256:f163be15c2f7b9baf4ebe37b9b01a9849b85912c568b77edeb65e65f428f57e6`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 84.2 KB (84223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62349caa5c8650003d94d89153b9a6447db9afa949ad55217dc1457531a9c601`  
		Last Modified: Tue, 02 Jul 2024 01:00:30 GMT  
		Size: 19.3 KB (19298 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; ppc64le

```console
$ docker pull memcached@sha256:acaa13015e805270042873fe3ab36bc648fe80eb0f14969acec553e753cb4304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6831632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a500d9af4e3b668d8e0d6638c73bfae52a7fa36acba301c8aa636534ec9b19`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be673a42f513c87d1df78721dbf22ce16e0cdd6635a1e3509a6d4135ad00c33b`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb66a45830fad4f1aa3cd411c03b83c12ccbb75074cdf9b831fd28340dd84a07`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 123.0 KB (122994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39e7f04805ab761f637d2439b5c0d95fa4db9ae87dbb08e33dddbb74e06d5ab`  
		Last Modified: Tue, 02 Jul 2024 01:08:32 GMT  
		Size: 3.1 MB (3135577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091a27d347d24006872ebcbc24fde59752ef8d9fdac839e612678f627e7eaa1d`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 275.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6152609bf78ec2f64035ac542bb1cdc5fa7acc1669db438baff1f13f4efa6c8`  
		Last Modified: Tue, 02 Jul 2024 01:08:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:e082cee761f778adbf332947e62a468703f0d9e9f776c924e1ddd512df866fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 KB (101793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b416173d2be29e240277035a900838b4cf735321229a8ddbd664ad2238bd0b67`

```dockerfile
```

-	Layers:
	-	`sha256:6976662e641ec1e08c7133fb5d217938f983cdc0444f291ee712e55a3140832d`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 82.4 KB (82372 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44111989f4a502518076daba1776444a6fd8f1c927a5d40ffc9e3b4fddcda176`  
		Last Modified: Tue, 02 Jul 2024 01:08:31 GMT  
		Size: 19.4 KB (19421 bytes)  
		MIME: application/vnd.in-toto+json

### `memcached:1-alpine3.20` - linux; s390x

```console
$ docker pull memcached@sha256:79ba7698dbb12f66e8bd1e05cdb46e16de9695a4eef498df74072a0f3c60e802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6587362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d35ab978fc41013595cb9b1b40163f5444ec5845a71c118f23ed5299d97d52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
CMD ["/bin/sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 	addgroup -g 11211 memcache; 	adduser -D -u 11211 -G memcache memcache # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN apk add --no-cache libsasl # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_VERSION=1.6.29
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_URL=https://memcached.org/files/memcached-1.6.29.tar.gz
# Sat, 29 Jun 2024 00:54:11 GMT
ENV MEMCACHED_SHA1=a9699aed111d86b6e37b3ce5e6ef4e7539582d5f
# Sat, 29 Jun 2024 00:54:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		linux-headers 		make 		openssl 		openssl-dev 		perl 		perl-io-socket-ssl 		perl-utils 	; 		wget -O memcached.tar.gz "$MEMCACHED_URL"; 	echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c -; 	mkdir -p /usr/src/memcached; 	tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1; 	rm memcached.tar.gz; 		cd /usr/src/memcached; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-extstore 		--enable-sasl 		--enable-sasl-pwdb 		--enable-tls 	; 	nproc="$(nproc)"; 	make -j "$nproc"; 		make test PARALLEL="$nproc"; 		make install; 		cd /; 	rm -rf /usr/src/memcached; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .memcached-rundeps $runDeps; 	apk del --no-network .build-deps; 		memcached -V # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Sat, 29 Jun 2024 00:54:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 29 Jun 2024 00:54:11 GMT
USER memcache
# Sat, 29 Jun 2024 00:54:11 GMT
EXPOSE map[11211/tcp:{}]
# Sat, 29 Jun 2024 00:54:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c88cd949338fc314738321b04206f0dade9407beae10c84ef951da45320b0f0`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 965.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdc0f646e8f002c12065d3d6678a658a7e5c45d903390745e995e3fe7d545f3`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 112.7 KB (112743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba08ac28e1e4e9d691e4703636b1f5ed17f0031100de4ff2708dda3f05ce84a`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 3.0 MB (3011397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3390252ac7d763585517b6d0efd5e3c16d91980867376a21b0b30125a9e8f437`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 279.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66216b6d2fdb3da52ff10bbd790a95600a947f47dc117b2640748b6fe7ccd773`  
		Last Modified: Tue, 02 Jul 2024 01:06:59 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `memcached:1-alpine3.20` - unknown; unknown

```console
$ docker pull memcached@sha256:d05a0a576e0c9d768363d44ca9903d69f0996ccc0f957b04c526a8b88bb6eb33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 KB (101667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1ed4df7995b466c25b025417336d03a73e1c833732975af37688dfc68200b1`

```dockerfile
```

-	Layers:
	-	`sha256:7aed2fc94933371cd77630957262436c09b3922948fe9ea021d5b9f56f0453d9`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 82.3 KB (82314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8597aee1aa9d498f3eb910d5634ff7b6c00437da2b7bd3a6c19a7d4389d4003d`  
		Last Modified: Tue, 02 Jul 2024 01:06:58 GMT  
		Size: 19.4 KB (19353 bytes)  
		MIME: application/vnd.in-toto+json
