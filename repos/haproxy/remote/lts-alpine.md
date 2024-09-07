## `haproxy:lts-alpine`

```console
$ docker pull haproxy@sha256:c2aa0bd0c81c2080259ca6901be67dfd8c33a70efca44f977ababde488801ec6
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

### `haproxy:lts-alpine` - linux; amd64

```console
$ docker pull haproxy@sha256:9d7ee8d3219b5f91d7463e8b5288cbf9bf897f6f8f071fc674c825478b590c41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.1 MB (13125199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14f84530b8baed2972055cfe7b58c3a9090060ed434972b3610ba5da5945e2a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 03 Sep 2024 17:15:58 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Tue, 03 Sep 2024 17:15:58 GMT
CMD ["/bin/sh"]
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_VERSION=3.0.4
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.4.tar.gz
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_SHA256=aabfd98ada721bbfb68f7805586ced0373fb4c8d73e18faa94055a16c2096936
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
STOPSIGNAL SIGUSR1
# Tue, 03 Sep 2024 17:15:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 17:15:58 GMT
USER haproxy
# Tue, 03 Sep 2024 17:15:58 GMT
WORKDIR /var/lib/haproxy
# Tue, 03 Sep 2024 17:15:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae8b453e5c55724b7e024c8b8bae8a0d0c6bde993125d4328f65f75253f0f98`  
		Last Modified: Fri, 06 Sep 2024 23:21:43 GMT  
		Size: 290.9 KB (290882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d9542158e7b78784dabe5481dc45d8663d899dfc81414d74f4f2118e9d999b`  
		Last Modified: Fri, 06 Sep 2024 23:21:43 GMT  
		Size: 976.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3448c45c9c099252dd1b06aafe59d20064e037bd333b4b919104805cefda3c28`  
		Last Modified: Fri, 06 Sep 2024 23:21:48 GMT  
		Size: 9.2 MB (9209061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b607717f0f25ab2d4a17f7a6c917e4161b270243371ed245974a25ace737dfd`  
		Last Modified: Fri, 06 Sep 2024 23:21:43 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:587a66d0d0944c23a73d083fcccc7f31caf8d0fb30bde32cd03d98b58413b56e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.9 KB (200856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a8a4ed23ffb2f489fbdef53ad1248abcb3b48e7042774738aa686d9babcbc5b`

```dockerfile
```

-	Layers:
	-	`sha256:6504868a38bec7f967e773c5ab82afe52fb096faeb1f45b996ba2462496ca00b`  
		Last Modified: Fri, 06 Sep 2024 23:21:43 GMT  
		Size: 180.0 KB (180006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1bf44ed62a8c4cab98b6acf47d9094373a1ce064ede978aaf91771c0159ea8f`  
		Last Modified: Fri, 06 Sep 2024 23:21:43 GMT  
		Size: 20.9 KB (20850 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm variant v6

```console
$ docker pull haproxy@sha256:21634954753f94adac4660acefcd538aadea5748d1a74cca5856fbc3ebcbf699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14955108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d730afe22838bf52b439846539fbf8af5f024c794b0f8b057feaa37648d20dc8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_VERSION=3.0.4
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.4.tar.gz
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_SHA256=aabfd98ada721bbfb68f7805586ced0373fb4c8d73e18faa94055a16c2096936
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
STOPSIGNAL SIGUSR1
# Tue, 03 Sep 2024 17:15:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 17:15:58 GMT
USER haproxy
# Tue, 03 Sep 2024 17:15:58 GMT
WORKDIR /var/lib/haproxy
# Tue, 03 Sep 2024 17:15:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d6f0dfe5c3358e1e5b6f77d7acc701d406d2695bed187ed32324e5acb7a07b`  
		Last Modified: Wed, 07 Aug 2024 23:56:05 GMT  
		Size: 291.8 KB (291775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc401fb3d7d76bfa71dd901816116558cc285d883f30115c7e87e5db214d898`  
		Last Modified: Wed, 07 Aug 2024 23:56:04 GMT  
		Size: 974.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d5cb92a992f3fead93be13acd0aec2ab013c9269ddd70965c655f4333c1dbb`  
		Last Modified: Wed, 04 Sep 2024 17:58:29 GMT  
		Size: 11.3 MB (11296698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccd4718fc3f96f6ca898b6e06e8e5a91afa3563291e6d9bba4c0272aa33cbce`  
		Last Modified: Wed, 04 Sep 2024 17:58:29 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:51b4a665464dff120e946ce73ab9aded6922522e76b818e715e04a67894d1c7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05e1acbaf85272f70b0684bec34d5ed0f668d5651b760caac2a5b0cf3d6c014b`

```dockerfile
```

-	Layers:
	-	`sha256:c7d223f7c8f8e620cb8247137a37c5f5ddaed884eb8a2ed7d70bf3a9dd2fc9e3`  
		Last Modified: Wed, 04 Sep 2024 17:58:29 GMT  
		Size: 20.8 KB (20762 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm variant v7

```console
$ docker pull haproxy@sha256:fe90b213770a40adfd05939ebdf518acdeeef980f275d62897e24c9b81aeb385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.4 MB (14383134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8037eba0174be63752286e40d525e9ca39a6412e9bb397cb2a17c24ad3f808f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_VERSION=3.0.4
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.4.tar.gz
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_SHA256=aabfd98ada721bbfb68f7805586ced0373fb4c8d73e18faa94055a16c2096936
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
STOPSIGNAL SIGUSR1
# Tue, 03 Sep 2024 17:15:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 17:15:58 GMT
USER haproxy
# Tue, 03 Sep 2024 17:15:58 GMT
WORKDIR /var/lib/haproxy
# Tue, 03 Sep 2024 17:15:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69c0873e8eaf0b24cf3938ffc8354aff3a608a47c0111989c1ff571d0a3bfd0`  
		Last Modified: Wed, 24 Jul 2024 23:00:07 GMT  
		Size: 290.9 KB (290946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b4581ed3fdedb97c0d59e733859a4b2f38b6b0583f89bd2a92fd10f33455b4`  
		Last Modified: Wed, 24 Jul 2024 23:00:07 GMT  
		Size: 977.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1873d2e2bc11a9093debcc382a5e90fb2cc01dda004533f3e2262ca16c0f3beb`  
		Last Modified: Wed, 04 Sep 2024 18:00:02 GMT  
		Size: 11.0 MB (10995772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c8599faaa510023bd992dccce57ceffbc5cf336519bb1c8804bacecf1b24ea3`  
		Last Modified: Wed, 04 Sep 2024 18:00:01 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:3b928bd65fc0e78ff30a46b7d5e4cb4d3c3698fe3af80c901622bb9b2db760eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.1 KB (201055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed6c48a0e84ca73190d6c2db3478c47f0288d4d5dc50153ea8a011ea8c14c38d`

```dockerfile
```

-	Layers:
	-	`sha256:f26123a3876bed56a6f39f9d54d17d3ff4941952a4be84090941a70c31795b7a`  
		Last Modified: Wed, 04 Sep 2024 18:00:01 GMT  
		Size: 180.1 KB (180074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f9e943c710eb79fbe1ecbbb2bb514187294cb697d8a3ba71d3e58a6c9e4a2b9`  
		Last Modified: Wed, 04 Sep 2024 18:00:00 GMT  
		Size: 21.0 KB (20981 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; arm64 variant v8

```console
$ docker pull haproxy@sha256:4e6968aea3b0176c15d3b95787214682b8873ae7d5488653d6b72af50effc310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16422936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392063bb104fc2a33883c5ff7f6dd15889f0ade0ec3fa76e8314dcafc8ef0c51`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_VERSION=3.0.4
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.4.tar.gz
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_SHA256=aabfd98ada721bbfb68f7805586ced0373fb4c8d73e18faa94055a16c2096936
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
STOPSIGNAL SIGUSR1
# Tue, 03 Sep 2024 17:15:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 17:15:58 GMT
USER haproxy
# Tue, 03 Sep 2024 17:15:58 GMT
WORKDIR /var/lib/haproxy
# Tue, 03 Sep 2024 17:15:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e9a7a328f872f0189c9884977bd11340a2c12ac2f9ae0914afac85bca66e36`  
		Last Modified: Wed, 21 Aug 2024 21:04:13 GMT  
		Size: 293.5 KB (293526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d08314fb4d6bdf8d69556d4f8e74b915e7445649ce5b31396e8b53576edd2d`  
		Last Modified: Wed, 21 Aug 2024 21:04:12 GMT  
		Size: 976.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e60f55ddad4ea13808ee8305788b7f00d3393b47a40f58d5dfb7ece7f3f4c80`  
		Last Modified: Wed, 04 Sep 2024 17:59:15 GMT  
		Size: 12.0 MB (12041027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c56bb7686c898a21e1c3c260d6f72d73ab5170d09088aaebd9f662026f74bee`  
		Last Modified: Wed, 04 Sep 2024 17:59:14 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:50536ce1e6ac8b90772cee0e1b14a82d9d6b463029615c17c104fa871a86e048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.3 KB (201311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a753571a0a0757ec02d2e8a8d4258112956213af58786fa92f5c2ff7e2da38ca`

```dockerfile
```

-	Layers:
	-	`sha256:ec9e75e1d7f694a61055d3962d5eb1868074ffc45cbd5798c161dcbe61c07716`  
		Last Modified: Wed, 04 Sep 2024 17:59:14 GMT  
		Size: 180.1 KB (180110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19e5e585fc92e3d328209c17acf15c5a8a992b6fd416ec334dd6ce8c66a0d534`  
		Last Modified: Wed, 04 Sep 2024 17:59:14 GMT  
		Size: 21.2 KB (21201 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; 386

```console
$ docker pull haproxy@sha256:1bbab015ff87ae3fb7823463153b66ab5ed60e4ce6b36037de25f26f1a41b1db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.8 MB (12767484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a4cc6d1489382dee489ef831c5c1855655e5b35227895e755a8c5f0a816531a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Tue, 03 Sep 2024 17:15:58 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Tue, 03 Sep 2024 17:15:58 GMT
CMD ["/bin/sh"]
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_VERSION=3.0.4
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.4.tar.gz
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_SHA256=aabfd98ada721bbfb68f7805586ced0373fb4c8d73e18faa94055a16c2096936
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
STOPSIGNAL SIGUSR1
# Tue, 03 Sep 2024 17:15:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 17:15:58 GMT
USER haproxy
# Tue, 03 Sep 2024 17:15:58 GMT
WORKDIR /var/lib/haproxy
# Tue, 03 Sep 2024 17:15:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a98659b0de1dc01e7b72a5f743ca08ef005982e9a96932e1f54d76c46d82c6a9`  
		Last Modified: Fri, 06 Sep 2024 23:21:49 GMT  
		Size: 291.3 KB (291349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d9360d2870eca66e3944aafcbb30440132fe4a3eebe1ce21d42dc94b92a786`  
		Last Modified: Fri, 06 Sep 2024 23:21:49 GMT  
		Size: 975.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df439a5591361b85c7af1f29defd6d5b2355bade836093deb4a483347ef67c36`  
		Last Modified: Fri, 06 Sep 2024 23:21:49 GMT  
		Size: 9.0 MB (9005521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c17d4b6c80a85937782c156aec0cecb1b585fa790749789ca902939e8cd2628`  
		Last Modified: Fri, 06 Sep 2024 23:21:48 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:e59fbc0b5f9ab48971ee7b559401a003f48347ae3229579f2e9735498e663e9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.8 KB (200758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43588e1f262edddc2cf732dcd17591b206996f3ae248369e239d1a249f5d350a`

```dockerfile
```

-	Layers:
	-	`sha256:df49b1156fb54158db7bfe4b0b4c1e2ae63e05590ea6fb5893fe3ec119447fc1`  
		Last Modified: Fri, 06 Sep 2024 23:21:48 GMT  
		Size: 180.0 KB (179961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99782e41f7a91a6b90d1141a7b568abd850e0b07c3bb7f26e21db2c34559f061`  
		Last Modified: Fri, 06 Sep 2024 23:21:48 GMT  
		Size: 20.8 KB (20797 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; ppc64le

```console
$ docker pull haproxy@sha256:ae314f11c5fe2fbabbcacee9da4fac2f072a0e7b397f234709015add2cf5fb93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15882822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9b67ddfcfd53b2e7dbc811db063ddb3538baac2c2790e7e6df317a6b2aa934`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_VERSION=3.0.4
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.4.tar.gz
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_SHA256=aabfd98ada721bbfb68f7805586ced0373fb4c8d73e18faa94055a16c2096936
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
STOPSIGNAL SIGUSR1
# Tue, 03 Sep 2024 17:15:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 17:15:58 GMT
USER haproxy
# Tue, 03 Sep 2024 17:15:58 GMT
WORKDIR /var/lib/haproxy
# Tue, 03 Sep 2024 17:15:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0034f2d4c620c651b96f5e93a5481ca03d9a55f8801ecf1f7964a1fde98c47a9`  
		Last Modified: Wed, 21 Aug 2024 21:05:12 GMT  
		Size: 294.0 KB (294023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce11f53d420a05da3d24d23ed551aa83bc2143c9df666b8b02da7b6229d3382`  
		Last Modified: Wed, 21 Aug 2024 21:05:12 GMT  
		Size: 976.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8bb5907903141f09d6a9b287634bf4df526b7f817a98d3336f1a9b2d9b9f17`  
		Last Modified: Wed, 04 Sep 2024 18:00:35 GMT  
		Size: 12.0 MB (12015795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cc25b1f27f7be98ce82e00ed4ba63216c540be0baa8ef4ec2f5c59b5b21ab3`  
		Last Modified: Wed, 04 Sep 2024 18:00:34 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:16af11b3c7fa1ba5e9b6253795d7a61750c6cbde4aabdfa57e33997cdd160965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.0 KB (199029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe7e804bf234ee53c1223f57cde1561ef0dfeeda0f3ad76dccd7fe3ebe5b0d8b`

```dockerfile
```

-	Layers:
	-	`sha256:ca5063660281f4e4084109e568c08f36ee8e4325297c6b16593054ce1eed8952`  
		Last Modified: Wed, 04 Sep 2024 18:00:34 GMT  
		Size: 178.1 KB (178110 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f9c7aedb0ac3d320e419028778ded388806ffd49acedf70a3e0cbe0fd1879e9`  
		Last Modified: Wed, 04 Sep 2024 18:00:34 GMT  
		Size: 20.9 KB (20919 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; riscv64

```console
$ docker pull haproxy@sha256:eeb63a5722f17852350a9fc487e968ae702f924a70808f77385c78198497293b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14651964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdd323d51bc5e426295fa781dca432ed37a5de20543e5e9c2dc926bb03bc21cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 22 Jul 2024 22:21:00 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Mon, 22 Jul 2024 22:21:00 GMT
CMD ["/bin/sh"]
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_VERSION=3.0.4
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.4.tar.gz
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_SHA256=aabfd98ada721bbfb68f7805586ced0373fb4c8d73e18faa94055a16c2096936
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
STOPSIGNAL SIGUSR1
# Tue, 03 Sep 2024 17:15:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 17:15:58 GMT
USER haproxy
# Tue, 03 Sep 2024 17:15:58 GMT
WORKDIR /var/lib/haproxy
# Tue, 03 Sep 2024 17:15:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbcadf9915790570653c042560d73481361037ded4274fdb06956454298634b`  
		Last Modified: Wed, 24 Jul 2024 23:08:32 GMT  
		Size: 291.7 KB (291718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b3e0585fc495e4c8ffbb0a08c426d78ce45daca0f937de682b505b114e4528`  
		Last Modified: Wed, 24 Jul 2024 23:08:31 GMT  
		Size: 977.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98ff91f9c651af18f70e27f30051f62ddd344d9c2230df27cb753e6f35cc187`  
		Last Modified: Wed, 04 Sep 2024 18:34:56 GMT  
		Size: 11.0 MB (10988116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0801182f63f2eb7404aa17cd7299f73e60031d43285b04b15d0f397c8a1425`  
		Last Modified: Wed, 04 Sep 2024 18:34:54 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:ebecdc9191d1770b1c14f5c5d3b86bc7853931dae776c9ab11c743981e8d40fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.0 KB (199024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4d5fbbf7fae92a5fb1bf8fc18e55340f88207fea136d28a5e1c17f155eb504`

```dockerfile
```

-	Layers:
	-	`sha256:71df7d75cc457ba6996b5c64d095717d83cb92daed9f96299e78076779e11ba3`  
		Last Modified: Wed, 04 Sep 2024 18:34:54 GMT  
		Size: 178.1 KB (178106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38c64655bf11d09b054064cb8b35cb43180283b7e28474275ef2aa733bf365ff`  
		Last Modified: Wed, 04 Sep 2024 18:34:54 GMT  
		Size: 20.9 KB (20918 bytes)  
		MIME: application/vnd.in-toto+json

### `haproxy:lts-alpine` - linux; s390x

```console
$ docker pull haproxy@sha256:f9f9a5bdb5780c1241d92f4f4bf598b524c9c1d6eab98b3c1203232b4d5e4045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15366654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7213e3fd79ede989e8928df2500b3d32c350a761e636ee487265622434d95a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["haproxy","-f","\/usr\/local\/etc\/haproxy\/haproxy.cfg"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 	; # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 	addgroup --gid 99 --system haproxy; 	adduser 		--disabled-password 		--home /var/lib/haproxy 		--ingroup haproxy 		--no-create-home 		--system 		--uid 99 		haproxy 	; 	mkdir /var/lib/haproxy; 	chown haproxy:haproxy /var/lib/haproxy # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_VERSION=3.0.4
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_URL=https://www.haproxy.org/download/3.0/src/haproxy-3.0.4.tar.gz
# Tue, 03 Sep 2024 17:15:58 GMT
ENV HAPROXY_SHA256=aabfd98ada721bbfb68f7805586ced0373fb4c8d73e18faa94055a16c2096936
# Tue, 03 Sep 2024 17:15:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gcc 		libc-dev 		linux-headers 		lua5.4-dev 		make 		openssl 		openssl-dev 		pcre2-dev 		readline-dev 		tar 	; 		wget -O haproxy.tar.gz "$HAPROXY_URL"; 	echo "$HAPROXY_SHA256 *haproxy.tar.gz" | sha256sum -c; 	mkdir -p /usr/src/haproxy; 	tar -xzf haproxy.tar.gz -C /usr/src/haproxy --strip-components=1; 	rm haproxy.tar.gz; 		makeOpts=' 		TARGET=linux-musl 		USE_GETADDRINFO=1 		USE_LUA=1 LUA_INC=/usr/include/lua5.4 LUA_LIB=/usr/lib/lua5.4 		USE_OPENSSL=1 		USE_PCRE2=1 USE_PCRE2_JIT=1 		USE_PROMEX=1 				EXTRA_OBJS=" 		" 	'; 		nproc="$(getconf _NPROCESSORS_ONLN)"; 	eval "make -C /usr/src/haproxy -j '$nproc' all $makeOpts"; 	eval "make -C /usr/src/haproxy install-bin $makeOpts"; 		mkdir -p /usr/local/etc/haproxy; 	cp -R /usr/src/haproxy/examples/errorfiles /usr/local/etc/haproxy/errors; 	rm -rf /usr/src/haproxy; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .haproxy-rundeps $runDeps; 	apk del --no-network .build-deps; 		haproxy -v # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
STOPSIGNAL SIGUSR1
# Tue, 03 Sep 2024 17:15:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Sep 2024 17:15:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Sep 2024 17:15:58 GMT
USER haproxy
# Tue, 03 Sep 2024 17:15:58 GMT
WORKDIR /var/lib/haproxy
# Tue, 03 Sep 2024 17:15:58 GMT
CMD ["haproxy" "-f" "/usr/local/etc/haproxy/haproxy.cfg"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c416a09f320ac9c505548293654c09afa120f44d8391aee48ea16d87f82ab1`  
		Last Modified: Wed, 21 Aug 2024 21:06:08 GMT  
		Size: 291.9 KB (291894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab311452b242aca14305fda0c6169e3f8e2af816b4d1699c44cd1f74e18349a1`  
		Last Modified: Wed, 21 Aug 2024 21:06:08 GMT  
		Size: 978.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec9aea060ca1faddcb8df00978aa045b38f6347e891849a6e99a89f4f060d64`  
		Last Modified: Wed, 04 Sep 2024 18:04:13 GMT  
		Size: 11.6 MB (11612242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846293d07580fb43dcb2857a7429bec488e49204108ceae4899f3c575222ba41`  
		Last Modified: Wed, 04 Sep 2024 18:04:12 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haproxy:lts-alpine` - unknown; unknown

```console
$ docker pull haproxy@sha256:54bd6c58f57dc416f3b2092e2d2ea16da9924008dc4e71f2f7ce018703c49109
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.9 KB (198905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69f2f1f7bc6793ea91bd00e79462d6c70afa0bd1c6e95a12787e317fd1d62b8`

```dockerfile
```

-	Layers:
	-	`sha256:17637b2cabcb837a9f7191639cf165fe55c7ac8bd778f07bebe91b347473cc5a`  
		Last Modified: Wed, 04 Sep 2024 18:04:12 GMT  
		Size: 178.1 KB (178052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33dea514505b85c1651753fbeeddaf1d7e5514bb57d11f0811da621ee2b49aef`  
		Last Modified: Wed, 04 Sep 2024 18:04:12 GMT  
		Size: 20.9 KB (20853 bytes)  
		MIME: application/vnd.in-toto+json
