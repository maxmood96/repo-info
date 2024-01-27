## `httpd:2-alpine3.19`

```console
$ docker pull httpd@sha256:0517bd51e9cf9f01b13651ee8542be11f8474620126b926834bee187223166ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `httpd:2-alpine3.19` - linux; amd64

```console
$ docker pull httpd@sha256:faaa3c93157a9c34ac00190b859e7a22975cbc6dd79f357609db03e17f0db178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18892647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad88fc1ec140eccee1806223c22cdca359319b54686c1803f695bfd5ba6ae314`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 09 Dec 2023 15:10:42 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 09 Dec 2023 15:10:42 GMT
CMD ["/bin/sh"]
# Sat, 09 Dec 2023 15:10:42 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Sat, 09 Dec 2023 15:10:42 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 15:10:42 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
WORKDIR /usr/local/apache2
# Sat, 09 Dec 2023 15:10:42 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
ENV HTTPD_VERSION=2.4.58
# Sat, 09 Dec 2023 15:10:42 GMT
ENV HTTPD_SHA256=fa16d72a078210a54c47dd5bef2f8b9b8a01d94909a51453956b3ec6442ea4c5
# Sat, 09 Dec 2023 15:10:42 GMT
ENV HTTPD_PATCHES=
# Sat, 09 Dec 2023 15:10:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
STOPSIGNAL SIGWINCH
# Sat, 09 Dec 2023 15:10:42 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
EXPOSE map[80/tcp:{}]
# Sat, 09 Dec 2023 15:10:42 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9768c1f09fcb02774013ff5705170801ac5197467d5484a77ddcf617d5af0fc`  
		Last Modified: Sat, 27 Jan 2024 00:54:01 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6462d37b50ead524cb5ccec1a5f9ba5296f35f2b95a8bb2edc67d3bcfec85651`  
		Last Modified: Sat, 27 Jan 2024 00:54:01 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225356f4c3990a5a59575e66df0ec48af0d41155c2f00c4f76d1f6ae79b080e0`  
		Last Modified: Sat, 27 Jan 2024 00:54:01 GMT  
		Size: 10.4 MB (10383548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146f0eb9dbb081636201e581bb17363a2d273fed2f4b870c180a8143b2fb013d`  
		Last Modified: Sat, 27 Jan 2024 00:54:01 GMT  
		Size: 5.1 MB (5098673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da77fd22df1e166d640db9cb1b306bfadcf82e4863de33e072311d295746adf`  
		Last Modified: Sat, 27 Jan 2024 00:54:02 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:78256808677cacf2eed64d0bf07f43add1db90355ed87ebe88a730ffa9fb7697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **932.3 KB (932299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cbced703184f3524b6cac427e11895df2cfe42c18b97aaff881cf1a0ecc8c2e`

```dockerfile
```

-	Layers:
	-	`sha256:242f0dd55df32be0882978d7a53996bf9d0d612c3601e7114816248ed600260b`  
		Last Modified: Sat, 27 Jan 2024 00:54:01 GMT  
		Size: 894.1 KB (894146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:846916ba180c00e2a3e8046ec76b13491fc2316029267250bda43a604b8339ec`  
		Last Modified: Sat, 27 Jan 2024 00:54:01 GMT  
		Size: 38.2 KB (38153 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-alpine3.19` - linux; arm variant v6

```console
$ docker pull httpd@sha256:493dc82a06456d4e5f06796c8afe8276aea8b37bbe264720643b18e6942bae9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.7 MB (17748448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0249fcd29fbd001b99c0ae2be28b3c1e350499da2d33a085e44bed7a1694de81`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Sat, 09 Dec 2023 15:10:42 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Sat, 09 Dec 2023 15:10:42 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 15:10:42 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
WORKDIR /usr/local/apache2
# Sat, 09 Dec 2023 15:10:42 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
ENV HTTPD_VERSION=2.4.58
# Sat, 09 Dec 2023 15:10:42 GMT
ENV HTTPD_SHA256=fa16d72a078210a54c47dd5bef2f8b9b8a01d94909a51453956b3ec6442ea4c5
# Sat, 09 Dec 2023 15:10:42 GMT
ENV HTTPD_PATCHES=
# Sat, 09 Dec 2023 15:10:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
STOPSIGNAL SIGWINCH
# Sat, 09 Dec 2023 15:10:42 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
EXPOSE map[80/tcp:{}]
# Sat, 09 Dec 2023 15:10:42 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d41ff686ec6fa3c20dc7a2050b07b87612d7d4797e349e3cb6015e7c932362`  
		Last Modified: Wed, 13 Dec 2023 20:13:40 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dead0ad230f3e39b78561f812d63062c51c3d52a2e4cf2cfa68c2cce97d792a3`  
		Last Modified: Wed, 13 Dec 2023 20:13:40 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135a383a42b423adbaa5f7882b63d85f61adec95633612345b9604960a227a3d`  
		Last Modified: Wed, 13 Dec 2023 20:13:41 GMT  
		Size: 9.6 MB (9568561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb3e20a0534d28f320474cd69da8b04921979c8e0ce605e75f03d9bb768ea97`  
		Last Modified: Wed, 13 Dec 2023 20:13:41 GMT  
		Size: 5.0 MB (5013042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9011caedd8cbf4964163d01f8118ed886009923a93c2bf0636975444a63f6c87`  
		Last Modified: Wed, 13 Dec 2023 20:13:41 GMT  
		Size: 289.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:52a35110811465b03d44abbb74aa3bd5ce1abf7ba963064917c80e013eba1f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35495c38fbdb384ba41607955c44364415417db052cc696b046f8db7a92399ac`

```dockerfile
```

-	Layers:
	-	`sha256:61010a9256a178958f1b22682e89520f8248ebc5a7e6d2e308955b9d5a37b85e`  
		Last Modified: Wed, 13 Dec 2023 20:13:40 GMT  
		Size: 37.9 KB (37910 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-alpine3.19` - linux; arm variant v7

```console
$ docker pull httpd@sha256:9f62732fc71c0b47d51b2f740239d7ddc27c4546fc67dcfc63b01d4bb0ec58ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16981852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d80eefdc9108c7f9defb1ff39109e972979e0d68b9fcf2ae6af737fb5abe8f9`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 09 Dec 2023 15:10:42 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 09 Dec 2023 15:10:42 GMT
CMD ["/bin/sh"]
# Sat, 09 Dec 2023 15:10:42 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Sat, 09 Dec 2023 15:10:42 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 15:10:42 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
WORKDIR /usr/local/apache2
# Sat, 09 Dec 2023 15:10:42 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
ENV HTTPD_VERSION=2.4.58
# Sat, 09 Dec 2023 15:10:42 GMT
ENV HTTPD_SHA256=fa16d72a078210a54c47dd5bef2f8b9b8a01d94909a51453956b3ec6442ea4c5
# Sat, 09 Dec 2023 15:10:42 GMT
ENV HTTPD_PATCHES=
# Sat, 09 Dec 2023 15:10:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
STOPSIGNAL SIGWINCH
# Sat, 09 Dec 2023 15:10:42 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
EXPOSE map[80/tcp:{}]
# Sat, 09 Dec 2023 15:10:42 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b3c5e5d01e7ad25d269099bedc9c7078b2fd640ef163f068385ffd7132f07b`  
		Last Modified: Sat, 27 Jan 2024 15:52:24 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed07ef51aec215f499a9b2e74faeb1aeda745af00a20ecee193fb39b1a3feaf8`  
		Last Modified: Sat, 27 Jan 2024 15:52:24 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ab12c74ffd46d313c3502c31a794e197eeb5773311d36f7c2be2c00f55d6a2`  
		Last Modified: Sat, 27 Jan 2024 15:52:25 GMT  
		Size: 9.3 MB (9334713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10d1639cbc616b6a66af708673df23e96a3e827b88f9f5834a887e10c963fc4`  
		Last Modified: Sat, 27 Jan 2024 15:52:25 GMT  
		Size: 4.7 MB (4726539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518099f9557e0f3d4f4daf111acb231e36c8759ca066c502b687b29b15d00767`  
		Last Modified: Sat, 27 Jan 2024 15:52:25 GMT  
		Size: 290.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:b75a3339a02a9abf7c5111cc8da5f71a75c56d2172865ce00fd7209cb1d0b1ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **934.8 KB (934811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a1ce5316ce578fdc8ac1d15fdee13847146ab95a692d9fde92059a48bfa162`

```dockerfile
```

-	Layers:
	-	`sha256:c7af1326b645012d4de7dcb6df27d65c925f285458c1d54154cf7c4aa0d54e3d`  
		Last Modified: Sat, 27 Jan 2024 15:52:24 GMT  
		Size: 896.7 KB (896686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c42d145937be8d57cda181613460c5b1ce4309a2e45741461578108376c3c6b`  
		Last Modified: Sat, 27 Jan 2024 15:52:24 GMT  
		Size: 38.1 KB (38125 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:6a467f1adbcfe9e0c752e2e0004489ec75a1f7e78452e1b992333cb4a668c50d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (18969636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c3edec489006159bdd745d4debfdbb89c138b606206836d29ca5a8617f935e`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Sat, 09 Dec 2023 15:10:42 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Sat, 09 Dec 2023 15:10:42 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 15:10:42 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
WORKDIR /usr/local/apache2
# Sat, 09 Dec 2023 15:10:42 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
ENV HTTPD_VERSION=2.4.58
# Sat, 09 Dec 2023 15:10:42 GMT
ENV HTTPD_SHA256=fa16d72a078210a54c47dd5bef2f8b9b8a01d94909a51453956b3ec6442ea4c5
# Sat, 09 Dec 2023 15:10:42 GMT
ENV HTTPD_PATCHES=
# Sat, 09 Dec 2023 15:10:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
STOPSIGNAL SIGWINCH
# Sat, 09 Dec 2023 15:10:42 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
EXPOSE map[80/tcp:{}]
# Sat, 09 Dec 2023 15:10:42 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4555325946067ad19631275de49a7b6d8acb66b3205c0caec5e96567ac01e741`  
		Last Modified: Wed, 13 Dec 2023 20:46:10 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68e425d3c306576068f03043a84b6722fe3c8752cb1d6e779c442ebab0113e7`  
		Last Modified: Wed, 13 Dec 2023 20:46:10 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01a30ce8151fc3cf93ee48071b1b332a25c6ee6e35fcf1cd20064cc99c8bcd9`  
		Last Modified: Wed, 13 Dec 2023 20:46:11 GMT  
		Size: 10.4 MB (10388654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa39ce87ec2ff0731d51a2c2e34d2c9c9875c4b9dd340e3683bdf868b7b8535`  
		Last Modified: Wed, 13 Dec 2023 20:46:11 GMT  
		Size: 5.2 MB (5231495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781ffbc5f3f463b67d2a9f24ea0253f56cfbc13829633dca83cfab38c7edc4e8`  
		Last Modified: Wed, 13 Dec 2023 20:46:11 GMT  
		Size: 282.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:04a4412ed7694f2e0cd4d910f380cd2aee8285308e8c97ae771236c4d41c14b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **932.2 KB (932161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15333071cb66620aa26d8376474ba686d2d44c29a2613218240034093d937b9f`

```dockerfile
```

-	Layers:
	-	`sha256:2e02da02eee3fd78daef00d84cea21418e40837de29a5f3a7bfb77cd4acc382f`  
		Last Modified: Wed, 13 Dec 2023 20:46:10 GMT  
		Size: 894.2 KB (894158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0fa087905b63b140af0f09f6fbdba9dea327a9fd7e8739ee49870f987a61bb3`  
		Last Modified: Wed, 13 Dec 2023 20:46:10 GMT  
		Size: 38.0 KB (38003 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-alpine3.19` - linux; 386

```console
$ docker pull httpd@sha256:380a720d105fdbf902f5afcf4a23b41470180793c359496d02fab77afd36d050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18149072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1a0f82d1a4aa9920afcbb7194687a8056dd97069e7a2fb787e22f5686ff8da`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 09 Dec 2023 15:10:42 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 09 Dec 2023 15:10:42 GMT
CMD ["/bin/sh"]
# Sat, 09 Dec 2023 15:10:42 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Sat, 09 Dec 2023 15:10:42 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 15:10:42 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
WORKDIR /usr/local/apache2
# Sat, 09 Dec 2023 15:10:42 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
ENV HTTPD_VERSION=2.4.58
# Sat, 09 Dec 2023 15:10:42 GMT
ENV HTTPD_SHA256=fa16d72a078210a54c47dd5bef2f8b9b8a01d94909a51453956b3ec6442ea4c5
# Sat, 09 Dec 2023 15:10:42 GMT
ENV HTTPD_PATCHES=
# Sat, 09 Dec 2023 15:10:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
STOPSIGNAL SIGWINCH
# Sat, 09 Dec 2023 15:10:42 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
EXPOSE map[80/tcp:{}]
# Sat, 09 Dec 2023 15:10:42 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e95cb0b12c7f17c125cd0b4656e2ec3e2ba844189d483222a984ff16b683d0`  
		Last Modified: Sat, 27 Jan 2024 01:55:11 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509c070e195fc4f7a6be2f10e45df0e746c7a18e2a7f29bca860dca6d26cb5b7`  
		Last Modified: Sat, 27 Jan 2024 01:55:11 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:140b341f3fc27c61de22bf8f926cf32ad93b97992dcfa4b3b8e779af025c32ef`  
		Last Modified: Sat, 27 Jan 2024 01:55:12 GMT  
		Size: 9.9 MB (9863696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9813f4a92712bd998725f1005bcf5747eb6a815cc73510d6dc4aa5db5a361555`  
		Last Modified: Sat, 27 Jan 2024 01:55:12 GMT  
		Size: 5.0 MB (5039588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a85216b3464d3e83d06cf84564deca5b427d6dea4c8f03e220c3ff458346e9`  
		Last Modified: Sat, 27 Jan 2024 01:55:12 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:cd8f458bc00c5b98c182285d319465a8f2c03634c74778429011d5b0c838eb24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **932.2 KB (932196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56619df97083978e78ad1aac2b9279bb0cd107f440bc50a1272d9731c2ac66d1`

```dockerfile
```

-	Layers:
	-	`sha256:879bf565633a01b44b215de2896a8058d28977ca8b18741e22270066fb094342`  
		Last Modified: Sat, 27 Jan 2024 01:55:12 GMT  
		Size: 894.1 KB (894101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08e41ae2205e0dca15cbc38ce8a9b91256e4d91f66e5c07be14502537484979a`  
		Last Modified: Sat, 27 Jan 2024 01:55:11 GMT  
		Size: 38.1 KB (38095 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-alpine3.19` - linux; ppc64le

```console
$ docker pull httpd@sha256:8740443233fde342dd62e4f3dabf61963e836a82056c83c5140416e73fa957ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19395288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d7b8ada09f430ba0910efd87b0d1d939b239e71d60fd9e472f1f69f6ac2868`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 09 Dec 2023 15:10:42 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 09 Dec 2023 15:10:42 GMT
CMD ["/bin/sh"]
# Sat, 09 Dec 2023 15:10:42 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Sat, 09 Dec 2023 15:10:42 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 15:10:42 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
WORKDIR /usr/local/apache2
# Sat, 09 Dec 2023 15:10:42 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
ENV HTTPD_VERSION=2.4.58
# Sat, 09 Dec 2023 15:10:42 GMT
ENV HTTPD_SHA256=fa16d72a078210a54c47dd5bef2f8b9b8a01d94909a51453956b3ec6442ea4c5
# Sat, 09 Dec 2023 15:10:42 GMT
ENV HTTPD_PATCHES=
# Sat, 09 Dec 2023 15:10:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
STOPSIGNAL SIGWINCH
# Sat, 09 Dec 2023 15:10:42 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
EXPOSE map[80/tcp:{}]
# Sat, 09 Dec 2023 15:10:42 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3130c768149e816c4be04d6b80ffc6005016b3f580100f62a2ee337e6be19c`  
		Last Modified: Sat, 27 Jan 2024 09:46:15 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbeab2d176215f7c81f6aeea42fc955b415e58e69c76891216c1544ca3270778`  
		Last Modified: Sat, 27 Jan 2024 09:46:15 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e48205b3648c34471d56c0ebbb966c6bad5f0e15e6a1cfae140b384e8a6a3f`  
		Last Modified: Sat, 27 Jan 2024 09:46:16 GMT  
		Size: 10.6 MB (10626764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24dfda6451479e239e4d2c3a97618191ca4e4ca40fd8736b6dc1badba5b40af1`  
		Last Modified: Sat, 27 Jan 2024 09:46:16 GMT  
		Size: 5.4 MB (5408466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2a6ccd43b6086255f82cac981e53ebe4010d852071bb910fbf77c6cf62d919`  
		Last Modified: Sat, 27 Jan 2024 09:46:16 GMT  
		Size: 290.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:feb80b3321535f215872a8b0d5cc61e7dbfc636f346868d82466cdd1674158a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **930.6 KB (930623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9935c15ded741e8eb81a2e2b56932a5fe9d2bea9ef11768cfe5797a6efee768`

```dockerfile
```

-	Layers:
	-	`sha256:c0bc5f26ad194dd06a137be61c4ea98cc5390de047dfdbaa46375414a18d1b41`  
		Last Modified: Sat, 27 Jan 2024 09:46:16 GMT  
		Size: 892.6 KB (892568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09a5b23bb0e25ff9accd06df7f7b22ff593c0578038c0e47304feaf2d7fd6bfb`  
		Last Modified: Sat, 27 Jan 2024 09:46:15 GMT  
		Size: 38.1 KB (38055 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-alpine3.19` - linux; s390x

```console
$ docker pull httpd@sha256:05690ef4bee1aaf7bf39fd9e1474223d183113bc286a04916427931ef9801f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19479937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebb7eea5540b498f4a3e7199dfcb92552abbb474f4158f7b77b4667e2834f52`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Sat, 09 Dec 2023 15:10:42 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Sat, 09 Dec 2023 15:10:42 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 Dec 2023 15:10:42 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
WORKDIR /usr/local/apache2
# Sat, 09 Dec 2023 15:10:42 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
ENV HTTPD_VERSION=2.4.58
# Sat, 09 Dec 2023 15:10:42 GMT
ENV HTTPD_SHA256=fa16d72a078210a54c47dd5bef2f8b9b8a01d94909a51453956b3ec6442ea4c5
# Sat, 09 Dec 2023 15:10:42 GMT
ENV HTTPD_PATCHES=
# Sat, 09 Dec 2023 15:10:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
STOPSIGNAL SIGWINCH
# Sat, 09 Dec 2023 15:10:42 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Sat, 09 Dec 2023 15:10:42 GMT
EXPOSE map[80/tcp:{}]
# Sat, 09 Dec 2023 15:10:42 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7125f99a608865f41789a4906b1355220e55a9883f30809a367ac1e8cefcd874`  
		Last Modified: Wed, 13 Dec 2023 20:12:58 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f985eda03fa9c96795e2d03ff142d091d55293aa97bce0d037cf4339c9ad30`  
		Last Modified: Wed, 13 Dec 2023 20:12:58 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7978195e08315ae8e4dd61a055a8c222732a418c687a66a40f2cf3005bbcf528`  
		Last Modified: Wed, 13 Dec 2023 20:12:59 GMT  
		Size: 11.0 MB (10984912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9cccbc38775e9980cfc0a609259bac68b6faf9bd8156d1eada136fcf9750207`  
		Last Modified: Wed, 13 Dec 2023 20:12:58 GMT  
		Size: 5.3 MB (5250996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3af0e21025a2379f055aa2c67eb10aca6bb200ae674cc47cd5765c71394a54cd`  
		Last Modified: Wed, 13 Dec 2023 20:12:59 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:0bc52da2b559e78dac9923a3f1343e69878f08c73fc230b24c8531642532d985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **930.5 KB (930490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3948207c3ed2cdf08bdf495dd3bae9971fcb299121ea28697ae7446eadb23686`

```dockerfile
```

-	Layers:
	-	`sha256:ea54739916d5e7b95f006e38003056eb46aa3104f102588592c32a2a5b17634f`  
		Last Modified: Wed, 13 Dec 2023 20:12:58 GMT  
		Size: 892.5 KB (892503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec734616b7b690a2bf34d17684b8ae6a4b716b8285c3736bc19935df6635e2fb`  
		Last Modified: Wed, 13 Dec 2023 20:12:58 GMT  
		Size: 38.0 KB (37987 bytes)  
		MIME: application/vnd.in-toto+json
