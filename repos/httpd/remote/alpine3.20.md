## `httpd:alpine3.20`

```console
$ docker pull httpd@sha256:18949987e38e84a79cbbd2afb4c072fe18e8b00cc10e2f52fdbc539176fa9d21
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

### `httpd:alpine3.20` - linux; amd64

```console
$ docker pull httpd@sha256:38b383b01b09862ddd5d5739cda75a508f7935bdc05e408f5a1f8024c00eb093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19599225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7ccaadd632cf0d0af3a00528a83a486f52a1c1f7b9f2262c3ff15eb52d43f01`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 17 Jul 2024 23:31:14 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Wed, 17 Jul 2024 23:31:14 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Wed, 17 Jul 2024 23:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jul 2024 23:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
WORKDIR /usr/local/apache2
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_VERSION=2.4.62
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_SHA256=674188e7bf44ced82da8db522da946849e22080d73d16c93f7f4df89e25729ec
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_PATCHES=
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
STOPSIGNAL SIGWINCH
# Wed, 17 Jul 2024 23:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Jul 2024 23:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d4b7713ec822cf188a83e1b083d2679a87ef2dec36f04ac5f23ce1b168c6fb`  
		Last Modified: Fri, 06 Sep 2024 23:22:29 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72fcafaf757d8e4775b424d253546325bdd7a4e75cdbdbbd15369e44668b452`  
		Last Modified: Fri, 06 Sep 2024 23:22:29 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c8348b64df944fdc8ed7ef66cf34dc39ef9a61c3bdcea1629fda7cfb9ba8d6`  
		Last Modified: Fri, 06 Sep 2024 23:22:29 GMT  
		Size: 10.4 MB (10383164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d0e026f7379c6ec00ad1abfbba3814baf8db9ea26d75af3971dae854ac3fb5`  
		Last Modified: Fri, 06 Sep 2024 23:22:29 GMT  
		Size: 5.6 MB (5590845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f69efd7f51793f857f5ed298167f5765829e67f79383bda99479788636e186b`  
		Last Modified: Fri, 06 Sep 2024 23:22:30 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine3.20` - unknown; unknown

```console
$ docker pull httpd@sha256:0afcaf5812bc3429a470054a544f5cee64468e810ab16f1dab64b54cb1be7840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1112107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf14dc7314b0158bcaa7e2e4dc49ae8b120c075d99023a993627cb8454903e9`

```dockerfile
```

-	Layers:
	-	`sha256:c7908cad69873b4ef7cd1ff92e00777da7904197b19ac469e38b67fff87d6831`  
		Last Modified: Fri, 06 Sep 2024 23:22:29 GMT  
		Size: 1.1 MB (1074074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7798d0c8b9ae384519bf9f6adb52bca58b194d5484ca997dec2fa71e68d4c1ff`  
		Last Modified: Fri, 06 Sep 2024 23:22:29 GMT  
		Size: 38.0 KB (38033 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine3.20` - linux; arm variant v6

```console
$ docker pull httpd@sha256:d5b244e96e4eefa7219fc3803a3be0e7d2791bcbde6d35aa8b3d6bf65918452e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20520989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b684a5861766776a6587d5b6691800970e54fb03f0d6d6b0193fca797826b0`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 17 Jul 2024 23:31:14 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Wed, 17 Jul 2024 23:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jul 2024 23:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
WORKDIR /usr/local/apache2
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_VERSION=2.4.62
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_SHA256=674188e7bf44ced82da8db522da946849e22080d73d16c93f7f4df89e25729ec
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_PATCHES=
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
STOPSIGNAL SIGWINCH
# Wed, 17 Jul 2024 23:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Jul 2024 23:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17894a1c0fd5d7d929dbda59a6642eba179276b936fcb0cfb0a842f19377546c`  
		Last Modified: Tue, 12 Nov 2024 02:42:29 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f6fd3bb05da8b50a6d2407d46e343215f2324c2388a7dc008254b5e8101b21`  
		Last Modified: Tue, 12 Nov 2024 02:42:29 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e537a4bc08f4d0418fec092450f42377764325642a9cac60ff943d9340d19b`  
		Last Modified: Tue, 12 Nov 2024 02:42:30 GMT  
		Size: 9.6 MB (9575152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c38c5eee609c7d095ab2b3d78d6d1ea0c074be94fe00ca55d3a74a4c8c7fec`  
		Last Modified: Tue, 12 Nov 2024 02:42:30 GMT  
		Size: 7.6 MB (7577832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44164c0dcc87cb692b9d62aad9b1f9015269fb36b6d29b25c24e04d87774d714`  
		Last Modified: Tue, 12 Nov 2024 02:42:30 GMT  
		Size: 285.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine3.20` - unknown; unknown

```console
$ docker pull httpd@sha256:d0594f316abccc4d05e1c4c0cb62d86c0c4eae76253ac0b31963d8c2a28746e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2270b9a55fd3a49cf4f174fda8f7a994ab2ef94845beb79bc5d07d214a5821`

```dockerfile
```

-	Layers:
	-	`sha256:6b337ac48a1ddc6dc173466fd530ca96652df4d3611ea187c56e1673ba150f54`  
		Last Modified: Tue, 12 Nov 2024 02:42:29 GMT  
		Size: 38.2 KB (38178 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine3.20` - linux; arm variant v7

```console
$ docker pull httpd@sha256:5561a8980b1b2f4361bab433aa331457bf9dcfcf56f4fca3fef5d3ccc726ce92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19544010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5d36b344e8e05d7604ca92ad50e109792ace5d803617f1dd8fe0bcec070a780`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 17 Jul 2024 23:31:14 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Wed, 17 Jul 2024 23:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jul 2024 23:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
WORKDIR /usr/local/apache2
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_VERSION=2.4.62
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_SHA256=674188e7bf44ced82da8db522da946849e22080d73d16c93f7f4df89e25729ec
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_PATCHES=
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
STOPSIGNAL SIGWINCH
# Wed, 17 Jul 2024 23:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Jul 2024 23:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3d2f4260716e2aa12ad4bbcd0de334b42a24970a7438ae0b96bd58dca9e0af`  
		Last Modified: Tue, 12 Nov 2024 02:45:16 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b785e40c4230f34fc33bdcd643850ba43a3f91162fb9206a5e97f54557e1b27`  
		Last Modified: Tue, 12 Nov 2024 02:45:16 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae79bad81a47f01df2ab640f1932c232de477e54d4ce8146f36284c57c13809`  
		Last Modified: Tue, 12 Nov 2024 02:45:17 GMT  
		Size: 9.3 MB (9340536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8b8939a441351b6c6193f8e57b8bc589f6d8e80a10c485cd2771eaa2a448fe`  
		Last Modified: Tue, 12 Nov 2024 02:45:17 GMT  
		Size: 7.1 MB (7106579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8004a2a713ea87c26d31275982c1f99fcebed9b83a95315f054a48d493d7e5c`  
		Last Modified: Tue, 12 Nov 2024 02:45:16 GMT  
		Size: 284.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine3.20` - unknown; unknown

```console
$ docker pull httpd@sha256:2a8d7eb84a83053e0cd3f81d7a3e2d4dc30dbf3ab1cbb3b166af517a60e22d86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1115616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:742f7729b6b74a326a55b5391277231256ced79ec9a27c6ca0fefa086a5fbf82`

```dockerfile
```

-	Layers:
	-	`sha256:4c4b8193606b2b35d66c7c0d8e52d565fdcfc69a002e09aaa4ab8fea86bff05f`  
		Last Modified: Tue, 12 Nov 2024 02:45:16 GMT  
		Size: 1.1 MB (1077223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e660fdc785b9aa755c38c1d9731ae63ad92e3ce19415be369903ec4d382a6b3`  
		Last Modified: Tue, 12 Nov 2024 02:45:16 GMT  
		Size: 38.4 KB (38393 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:c19e9c128323a693c35151754128b2a8281a3cd03237b4a914ee79938f470b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20211907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1313e9e6d6a0d115d9416461c893c3ef1f0ab263d7831ad08802ac2056c4d6d`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 17 Jul 2024 23:31:14 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Wed, 17 Jul 2024 23:31:14 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Wed, 17 Jul 2024 23:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jul 2024 23:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
WORKDIR /usr/local/apache2
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_VERSION=2.4.62
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_SHA256=674188e7bf44ced82da8db522da946849e22080d73d16c93f7f4df89e25729ec
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_PATCHES=
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
STOPSIGNAL SIGWINCH
# Wed, 17 Jul 2024 23:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Jul 2024 23:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e9c66bcda30d203c92d5b38f87a383086052fb5abfaf84a37de39c99500c18`  
		Last Modified: Sat, 07 Sep 2024 05:26:43 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063d4029aede50174c28d565e61fcad8a41c3af5d5c423cb38489c476db0c192`  
		Last Modified: Sat, 07 Sep 2024 05:26:43 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da77873906d00ef3fe467576e799095186f61bfb7429a78deffb69bb361dfb18`  
		Last Modified: Sat, 07 Sep 2024 05:26:44 GMT  
		Size: 10.4 MB (10394971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938c6be3b1d9075f430752f7760da41e44bdc2870ad17e4575dd873bcd48751c`  
		Last Modified: Sat, 07 Sep 2024 05:26:44 GMT  
		Size: 5.7 MB (5727880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d96749909226a6c69cd4bd74af9baa281920c7e2b08b6077b31eaa7044d5c76`  
		Last Modified: Sat, 07 Sep 2024 05:26:44 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine3.20` - unknown; unknown

```console
$ docker pull httpd@sha256:e1bc62f8ff4506e8afe58dbb8c91f8a62dcc25eb9cb47351107a4d64dc02b574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1112560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7120bc797a1e471d773d8b58f33ae506f58a811468e0d4da434c76978ad05767`

```dockerfile
```

-	Layers:
	-	`sha256:af1c67509e958fd7044c77fc24b4a7354e5e8aa1484ddf1f209fe534c39217ee`  
		Last Modified: Sat, 07 Sep 2024 05:26:44 GMT  
		Size: 1.1 MB (1074178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:028f00dcef2629b3d0475b90cce3eb8ba99e9c639970bb616cd62cdbc5b3a246`  
		Last Modified: Sat, 07 Sep 2024 05:26:43 GMT  
		Size: 38.4 KB (38382 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine3.20` - linux; 386

```console
$ docker pull httpd@sha256:569e4b894f39c7a43e73ff800ae1bb54871528ce6097869dbc50ac96f548bd17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21111454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddc52043bc9cdab813fb8590046845d4b7be3031716c29325e698e267caf4bd0`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 17 Jul 2024 23:31:14 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Wed, 17 Jul 2024 23:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jul 2024 23:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
WORKDIR /usr/local/apache2
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_VERSION=2.4.62
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_SHA256=674188e7bf44ced82da8db522da946849e22080d73d16c93f7f4df89e25729ec
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_PATCHES=
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
STOPSIGNAL SIGWINCH
# Wed, 17 Jul 2024 23:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Jul 2024 23:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d58d400ab0cddf8a9289737f14dc80938489ab32b22627fc8800ff8a7029174`  
		Last Modified: Tue, 12 Nov 2024 02:03:51 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b61be6c81d775e99ce4ec310699f1fffba433112c89a0377292cc7739472ac`  
		Last Modified: Tue, 12 Nov 2024 02:03:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b01254b33f1361bdda8785be69c90b955658b535911fe524df968ea6c5cc808`  
		Last Modified: Tue, 12 Nov 2024 02:03:51 GMT  
		Size: 9.9 MB (9863059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41f8b934fa2b1826d76cc2567abc4e8ce97159702ff5e33cdddc0f696213e91`  
		Last Modified: Tue, 12 Nov 2024 02:03:51 GMT  
		Size: 7.8 MB (7777761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338e582c2c627bfe1e9b77973527728f074bc6100b6920fab34ecd6d12f26689`  
		Last Modified: Tue, 12 Nov 2024 02:03:51 GMT  
		Size: 289.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine3.20` - unknown; unknown

```console
$ docker pull httpd@sha256:c15335e4571751975807b2f95be76d82ad9b293c4475c9c8530c69b8d0a4965d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1112434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c092e7c3cc943c2943b5405e03d828f2ede32c3f2451890432f3079cf638980`

```dockerfile
```

-	Layers:
	-	`sha256:a59865cbff3d1b3be4055984cd08599a1a6647d035bd4421f79ec860cba5a44f`  
		Last Modified: Tue, 12 Nov 2024 02:03:51 GMT  
		Size: 1.1 MB (1074246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a1085ae29d08fc5c711992b4105a0f635489e559b5eda2abe1a3df493a971dd`  
		Last Modified: Tue, 12 Nov 2024 02:03:51 GMT  
		Size: 38.2 KB (38188 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine3.20` - linux; ppc64le

```console
$ docker pull httpd@sha256:0c4dc1be9bed722a393264a2bfc23204a6e159adad76c9b8aa64e623eca8065a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20158138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b80292bc8bca180d5d4a4853ebd404ada1fa88de0aae4683e3f8ecf2ac27be1`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 17 Jul 2024 23:31:14 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Wed, 17 Jul 2024 23:31:14 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Wed, 17 Jul 2024 23:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jul 2024 23:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
WORKDIR /usr/local/apache2
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_VERSION=2.4.62
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_SHA256=674188e7bf44ced82da8db522da946849e22080d73d16c93f7f4df89e25729ec
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_PATCHES=
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
STOPSIGNAL SIGWINCH
# Wed, 17 Jul 2024 23:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Jul 2024 23:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1967ff892acfe268c1589090097f1214d864215f56e511bc2a6e9cfbb6f46f`  
		Last Modified: Sat, 07 Sep 2024 07:01:40 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70db2ed8f2c23e8a273ebe21ae49b79807678b503be44f08956404221c4e92da`  
		Last Modified: Sat, 07 Sep 2024 07:01:40 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176f482d5e72c78691b646cbba6ab439950c356457838266662ff524d8db4a86`  
		Last Modified: Sat, 07 Sep 2024 07:01:41 GMT  
		Size: 10.6 MB (10638607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9fafa357d2da8640821c2dea5a6925c854720684f6488f623a56ee9be44954`  
		Last Modified: Sat, 07 Sep 2024 07:01:41 GMT  
		Size: 5.9 MB (5945699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b6574f586030cc2de60be632d0f1e819144b3016289f2ada95fe9c52c23ae0`  
		Last Modified: Sat, 07 Sep 2024 07:01:41 GMT  
		Size: 290.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine3.20` - unknown; unknown

```console
$ docker pull httpd@sha256:b906b460949a05cedae56c8c33162de002edf7ba52081ebc72c903fc52823c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1110280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981b22f0a70f6db114a51899bb6b6121d79b30ed13d4c5927909f79e56e390a1`

```dockerfile
```

-	Layers:
	-	`sha256:ff3d1d15291a6d7194d8d160d911d91f6184b5099953ff26211e9e9d30c12eff`  
		Last Modified: Sat, 07 Sep 2024 07:01:41 GMT  
		Size: 1.1 MB (1072178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b518403ea549f677e06c0b83c713ef3c1baab5d713008feb56c53b95f1329c5`  
		Last Modified: Sat, 07 Sep 2024 07:01:40 GMT  
		Size: 38.1 KB (38102 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine3.20` - linux; riscv64

```console
$ docker pull httpd@sha256:1d077e2ec610c2f869b4b74653fe0d67421908ca297dc8c874fb4643e98252c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18833552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f856d4c1c21076c31875e9f0aeabf3e8f7f23405814ff3f3833b4759e86ec782`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 17 Jul 2024 23:31:14 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Wed, 17 Jul 2024 23:31:14 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Wed, 17 Jul 2024 23:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jul 2024 23:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
WORKDIR /usr/local/apache2
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_VERSION=2.4.62
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_SHA256=674188e7bf44ced82da8db522da946849e22080d73d16c93f7f4df89e25729ec
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_PATCHES=
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
STOPSIGNAL SIGWINCH
# Wed, 17 Jul 2024 23:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Jul 2024 23:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44ab562c5c686e5ce4273382681f5007804ff4e9c5008e7088c9f8f60cba896`  
		Last Modified: Sat, 07 Sep 2024 20:17:09 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80eaf25291b949a09ef1c8d8a924a254439f5dc6ad92103f8edc7892802aff5`  
		Last Modified: Sat, 07 Sep 2024 20:17:09 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2334b3bb1832a4fb1efd90ece9c4e3f5850b80dfe22dc226cf7edd021f080784`  
		Last Modified: Sat, 07 Sep 2024 20:17:11 GMT  
		Size: 9.9 MB (9870884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd23253c3d035385ba345f3ddd649967ae5cecd3e57341fa25b8c6d9ef82354`  
		Last Modified: Sat, 07 Sep 2024 20:17:10 GMT  
		Size: 5.6 MB (5589803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f7f790b8ee2609fcd33c2f2a50847b8151df79cfbff8baded442c8e6514728`  
		Last Modified: Sat, 07 Sep 2024 20:17:10 GMT  
		Size: 289.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine3.20` - unknown; unknown

```console
$ docker pull httpd@sha256:740d3cab72042e869d7fc048d49326470ec2544df286c595ce11d0ac2f0dde78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1110273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df44f568a572bc55afe274b93f1f728f13d8e5bc11cb3dbb54d119c3bc135cf6`

```dockerfile
```

-	Layers:
	-	`sha256:fec3c077142b1a4c4a5d8ae2a328929cf46ee796bd5719cdbe77b3473e4d6672`  
		Last Modified: Sat, 07 Sep 2024 20:17:09 GMT  
		Size: 1.1 MB (1072174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20f009fb9d0f5834960910730b426351604f80405a3e5fb2f7c5563fd2ff86ba`  
		Last Modified: Sat, 07 Sep 2024 20:17:09 GMT  
		Size: 38.1 KB (38099 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine3.20` - linux; s390x

```console
$ docker pull httpd@sha256:5b3baa2f3b852e87bdae55fdd8b02414d80b813f22b5ab717f7e210fc10f49ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.4 MB (22399132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91c39b1cea00bb213b1690c0c0dbac833fefec08a1797964f3c4632f6cd6b70e`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 17 Jul 2024 23:31:14 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
CMD ["/bin/sh"]
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Wed, 17 Jul 2024 23:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jul 2024 23:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
WORKDIR /usr/local/apache2
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_VERSION=2.4.62
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_SHA256=674188e7bf44ced82da8db522da946849e22080d73d16c93f7f4df89e25729ec
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_PATCHES=
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
STOPSIGNAL SIGWINCH
# Wed, 17 Jul 2024 23:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Jul 2024 23:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca1bbba1fd2bab55619a83c8257f4b7b249ebd607027166dfa1d8070714870c9`  
		Last Modified: Tue, 12 Nov 2024 02:46:15 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:457ca91b516ba912a03d7bf04176849ab02e93fc442998f87ca239164c827cdf`  
		Last Modified: Tue, 12 Nov 2024 02:46:15 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be965d623756aa18ad51260e843afa15718f10b95fdf673a74d82129a0d4393`  
		Last Modified: Tue, 12 Nov 2024 02:46:15 GMT  
		Size: 11.0 MB (10988695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5d58bd0e790afecf3ee15418184e45e840a16ef672c078fe1f5d0f75a525a8`  
		Last Modified: Tue, 12 Nov 2024 02:46:16 GMT  
		Size: 7.9 MB (7947415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3a733533f4177882f9a35abbf3b24c1687807a8f1b1dd34b86ec92a267b701`  
		Last Modified: Tue, 12 Nov 2024 02:46:15 GMT  
		Size: 289.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine3.20` - unknown; unknown

```console
$ docker pull httpd@sha256:932419fcc629c88f644e12441cc74c17da11dab0279ebb28da7f03ea1e5cfe49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1110586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ce82ececf1b31874f527f598c283047db6656515faaa4769244ef3f45c458a2`

```dockerfile
```

-	Layers:
	-	`sha256:422eda8be5b9c74e918936e5ad73a60bc11d628807af9f89f228608f7895ed0d`  
		Last Modified: Tue, 12 Nov 2024 02:46:15 GMT  
		Size: 1.1 MB (1072337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a815a2a7d117ab6754bda6078bd980d34f74434bd75924d37a2ca62163165e1`  
		Last Modified: Tue, 12 Nov 2024 02:46:14 GMT  
		Size: 38.2 KB (38249 bytes)  
		MIME: application/vnd.in-toto+json
