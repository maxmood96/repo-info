## `httpd:alpine3.22`

```console
$ docker pull httpd@sha256:cc34b8bdde6ee55ea52db9819baa13ea36e4c7447eb7595db9ea720d1831851e
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

### `httpd:alpine3.22` - linux; amd64

```console
$ docker pull httpd@sha256:de7c50490625747db77c94464c38ac1e4927a7a93df14b379e5f3d979b0ad4a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20151322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600c17ecc6bc2ba36511abb7924a0430c0263217463e79af3e490faf247a8c8e`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 20:51:53 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 30 May 2025 20:51:53 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 30 May 2025 20:51:53 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 20:51:53 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 30 May 2025 20:51:53 GMT
WORKDIR /usr/local/apache2
# Fri, 30 May 2025 20:51:53 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Fri, 30 May 2025 20:51:53 GMT
ENV HTTPD_VERSION=2.4.63
# Fri, 30 May 2025 20:51:53 GMT
ENV HTTPD_SHA256=88fc236ab99b2864b248de7d49a008ec2afd7551e64dce8b95f58f32f94c46ab
# Fri, 30 May 2025 20:51:53 GMT
ENV HTTPD_PATCHES=
# Fri, 30 May 2025 20:51:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Fri, 30 May 2025 20:51:53 GMT
STOPSIGNAL SIGWINCH
# Fri, 30 May 2025 20:51:53 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 30 May 2025 20:51:53 GMT
EXPOSE map[80/tcp:{}]
# Fri, 30 May 2025 20:51:53 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35d590bf3609f032e1bbf0ee6320b123c548f3044c929e9021a7a2c40fd0b3d`  
		Last Modified: Tue, 03 Jun 2025 13:31:17 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3a2b5294e660be323502a3e5c7ae27c61ea6be3914f0043a5ec6ac1733fa42`  
		Last Modified: Tue, 03 Jun 2025 13:31:17 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d930a1e61c9d82edfa5dede6d83471c69efa72a39f213da492b125cd9b086b4`  
		Last Modified: Tue, 03 Jun 2025 13:32:36 GMT  
		Size: 10.6 MB (10598612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86175edb4cf79527e129b78ebb717862bc33164d5f9090c06005d2ebd23c4dc5`  
		Last Modified: Tue, 03 Jun 2025 13:31:19 GMT  
		Size: 5.8 MB (5754464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09da1e85e287063dd117def731cfde371f38b803ac7730478ebf3873df8ebf04`  
		Last Modified: Tue, 03 Jun 2025 13:31:19 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine3.22` - unknown; unknown

```console
$ docker pull httpd@sha256:06a7ad1a6cd94ed74e60c7191d9ec36cbf090a1ce1961ff0fe71f6c8c4c8740d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1205657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd21c2d136102b12fb7b1f985cbd390c749f258ac5a52d0313769b3059023af8`

```dockerfile
```

-	Layers:
	-	`sha256:1ae1127065389c122aaa12ba16fc2d232fa553a81e956f9cd2bbc9c2b9eead94`  
		Last Modified: Tue, 03 Jun 2025 14:19:47 GMT  
		Size: 1.2 MB (1167408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba82a01e5e13fbc4f8c1f44506f5fc72d632b76192e7e6ed861d1be37e40a84e`  
		Last Modified: Tue, 03 Jun 2025 14:19:41 GMT  
		Size: 38.2 KB (38249 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine3.22` - linux; arm variant v6

```console
$ docker pull httpd@sha256:35b228aca8e9728a4f44268f38f85d412d3cf9f0efa1c0f27a22540c0cbc2b89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (18956570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:328d467f6bf4b59d4adbbbf3b81ba8b26156e43b59b6a5cb9a0137bf8fab6fac`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 20:51:53 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 30 May 2025 20:51:53 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 30 May 2025 20:51:53 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 20:51:53 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 30 May 2025 20:51:53 GMT
WORKDIR /usr/local/apache2
# Fri, 30 May 2025 20:51:53 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Fri, 30 May 2025 20:51:53 GMT
ENV HTTPD_VERSION=2.4.63
# Fri, 30 May 2025 20:51:53 GMT
ENV HTTPD_SHA256=88fc236ab99b2864b248de7d49a008ec2afd7551e64dce8b95f58f32f94c46ab
# Fri, 30 May 2025 20:51:53 GMT
ENV HTTPD_PATCHES=
# Fri, 30 May 2025 20:51:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Fri, 30 May 2025 20:51:53 GMT
STOPSIGNAL SIGWINCH
# Fri, 30 May 2025 20:51:53 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 30 May 2025 20:51:53 GMT
EXPOSE map[80/tcp:{}]
# Fri, 30 May 2025 20:51:53 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6eb5d6cf52372e1444e46407df001d5196bebf9dab302a61bf4d5fac8f3f678`  
		Last Modified: Tue, 03 Jun 2025 14:01:38 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8daf9326fbf9409f14efefb725fa5a4ac499688beb225f5317fa20985671ea92`  
		Last Modified: Tue, 03 Jun 2025 14:01:40 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de8e1894e16077c63e6b562d4f5adb65853d3e20566d036b444575653a38374`  
		Last Modified: Tue, 03 Jun 2025 14:01:42 GMT  
		Size: 9.8 MB (9829265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47b3605d3cf6258aa85ba1d21ffb047c0e8989698f210636f8466f7282c4e26`  
		Last Modified: Tue, 03 Jun 2025 14:01:43 GMT  
		Size: 5.6 MB (5624979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd2d88c71c1a34429bcbad6beb03674117e7b213f21eca13e4dff6630f32845`  
		Last Modified: Tue, 03 Jun 2025 14:01:44 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine3.22` - unknown; unknown

```console
$ docker pull httpd@sha256:06c7a42bca0bdd235f9a241441d0c48475930a7ae4e0ac63723598b3480ed9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 KB (38178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dcf5e3c720500ca203c4d1d9b9575ff40a6add0a537563418f526077ef9794a`

```dockerfile
```

-	Layers:
	-	`sha256:d778dc129d395a9b661549e0860c5f66d6484e01a2d86dd23f07c81e5cdff71c`  
		Last Modified: Tue, 03 Jun 2025 14:01:48 GMT  
		Size: 38.2 KB (38178 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine3.22` - linux; arm variant v7

```console
$ docker pull httpd@sha256:35e62ecb2febfb389d3364cfb526c246d51ad67f25d6a72818aa807e1c5d3dae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.1 MB (18142498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5527edef4ee88551c3c4a2dc97dc5f9eabe768c30754cda3b1e77307ede17df`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 20:51:53 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 30 May 2025 20:51:53 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 30 May 2025 20:51:53 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 20:51:53 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 30 May 2025 20:51:53 GMT
WORKDIR /usr/local/apache2
# Fri, 30 May 2025 20:51:53 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Fri, 30 May 2025 20:51:53 GMT
ENV HTTPD_VERSION=2.4.63
# Fri, 30 May 2025 20:51:53 GMT
ENV HTTPD_SHA256=88fc236ab99b2864b248de7d49a008ec2afd7551e64dce8b95f58f32f94c46ab
# Fri, 30 May 2025 20:51:53 GMT
ENV HTTPD_PATCHES=
# Fri, 30 May 2025 20:51:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Fri, 30 May 2025 20:51:53 GMT
STOPSIGNAL SIGWINCH
# Fri, 30 May 2025 20:51:53 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 30 May 2025 20:51:53 GMT
EXPOSE map[80/tcp:{}]
# Fri, 30 May 2025 20:51:53 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deea24a7a8e0cd6514a2194d5af1a6bfb1e8d158179d0b19aa2dcbde869716a6`  
		Last Modified: Tue, 03 Jun 2025 14:19:49 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33e78e3423a5f77c300ef17778bb244c5e2e37289a6e6a43478fd007992c079`  
		Last Modified: Tue, 03 Jun 2025 14:19:49 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0673d87a44497dc3e6309e7411c4a275289e083114473bd68960ba522b8ad04d`  
		Last Modified: Tue, 03 Jun 2025 14:19:58 GMT  
		Size: 9.6 MB (9608152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0febb5a1465eb61b543e3a5d703158a5d269e100466b82aabe09cb21ae6045f5`  
		Last Modified: Tue, 03 Jun 2025 14:19:57 GMT  
		Size: 5.3 MB (5313764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e5da82f4c8f6d6203552141a3d2db0d0ec6ba71d04b9ec0d67dbb7aeb718e5`  
		Last Modified: Tue, 03 Jun 2025 14:19:49 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine3.22` - unknown; unknown

```console
$ docker pull httpd@sha256:a3bde97f40aa6eeb40409e304748a3b01cc2bf69ea9d2ea0e38577851aa3b1be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1208859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d2a15e2d9d2e703f3f9c18b6639c6d61d5f610ca2b7d06a1572e5a0b073c8e`

```dockerfile
```

-	Layers:
	-	`sha256:0696c16153c1fb637e6975e895c117376ec65a32c1646ded8aee934b4e0ac513`  
		Last Modified: Tue, 03 Jun 2025 14:19:56 GMT  
		Size: 1.2 MB (1170466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceb055c3fb0e2b294ffe0021e80f08ce9d87d1fb6d29ab551eb82603a9837ca7`  
		Last Modified: Tue, 03 Jun 2025 14:19:52 GMT  
		Size: 38.4 KB (38393 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:638721f23f205bb6bfc8da7b30a89515e99a631d4278e9078ab292fe8ce8a9ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20592871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7af89b46d245d21ce37e84a4a4d958dbce5a1f8395c24d50cd9f462b9a50d41`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 20:51:53 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 30 May 2025 20:51:53 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 30 May 2025 20:51:53 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 20:51:53 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 30 May 2025 20:51:53 GMT
WORKDIR /usr/local/apache2
# Fri, 30 May 2025 20:51:53 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Fri, 30 May 2025 20:51:53 GMT
ENV HTTPD_VERSION=2.4.63
# Fri, 30 May 2025 20:51:53 GMT
ENV HTTPD_SHA256=88fc236ab99b2864b248de7d49a008ec2afd7551e64dce8b95f58f32f94c46ab
# Fri, 30 May 2025 20:51:53 GMT
ENV HTTPD_PATCHES=
# Fri, 30 May 2025 20:51:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Fri, 30 May 2025 20:51:53 GMT
STOPSIGNAL SIGWINCH
# Fri, 30 May 2025 20:51:53 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 30 May 2025 20:51:53 GMT
EXPOSE map[80/tcp:{}]
# Fri, 30 May 2025 20:51:53 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55db84acc79ae87eff875e62c8e0d5fede8fa7f240871033020bf459d377f167`  
		Last Modified: Tue, 03 Jun 2025 13:33:38 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d0b88a8950af8e4ae4d137f11ab1a4bb2e1587fd6c2aa29b089af205689ba6`  
		Last Modified: Tue, 03 Jun 2025 13:33:36 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647dbe5c60c4f8b57f5763318808dd35da7256d0964bf89df9dd95bcd31a7e71`  
		Last Modified: Tue, 03 Jun 2025 13:33:39 GMT  
		Size: 10.6 MB (10593289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56fdfe45abd7cbc5dabb9b826b0d04e2f89cfd035e5a771be10c5997dce6136`  
		Last Modified: Tue, 03 Jun 2025 13:33:37 GMT  
		Size: 5.9 MB (5862242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26112e8620f7b6b177cacaf121e7ea996757c3f7ee20af4cd98f87ce81921ada`  
		Last Modified: Tue, 03 Jun 2025 13:33:34 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine3.22` - unknown; unknown

```console
$ docker pull httpd@sha256:b49d8362f2f28afa01c3d4d15668d157a8b0cd1f7fdaa2bd0d6173b9309ea221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1205958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f164211334a3ac64aea5473820ba8948ce5b5b98f3973930a2d3a8a58b6fbc3`

```dockerfile
```

-	Layers:
	-	`sha256:8f1104abf12f36b9d6a76627e8dcf1e9d28d888e0f94837e8ea140bf09b0a2db`  
		Last Modified: Tue, 03 Jun 2025 14:01:59 GMT  
		Size: 1.2 MB (1167512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8e9166e7c86ba757cd494795a13d9b486c0741b856d0e6ede2394dcbf3e1821`  
		Last Modified: Tue, 03 Jun 2025 14:02:00 GMT  
		Size: 38.4 KB (38446 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine3.22` - linux; 386

```console
$ docker pull httpd@sha256:9232cf13edc8f64b1270cb800e3c44a1236d52b22b84547df37716d4aa1d417f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19476720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e4b83c3a82af3f299a56b3e2b4c4c79c1b7ed04e5c665954528e3a9af8e2b72`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 20:51:53 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 30 May 2025 20:51:53 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 30 May 2025 20:51:53 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 20:51:53 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 30 May 2025 20:51:53 GMT
WORKDIR /usr/local/apache2
# Fri, 30 May 2025 20:51:53 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Fri, 30 May 2025 20:51:53 GMT
ENV HTTPD_VERSION=2.4.63
# Fri, 30 May 2025 20:51:53 GMT
ENV HTTPD_SHA256=88fc236ab99b2864b248de7d49a008ec2afd7551e64dce8b95f58f32f94c46ab
# Fri, 30 May 2025 20:51:53 GMT
ENV HTTPD_PATCHES=
# Fri, 30 May 2025 20:51:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Fri, 30 May 2025 20:51:53 GMT
STOPSIGNAL SIGWINCH
# Fri, 30 May 2025 20:51:53 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 30 May 2025 20:51:53 GMT
EXPOSE map[80/tcp:{}]
# Fri, 30 May 2025 20:51:53 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c08109f18908894eaaae2d29d01d1ae71e79dabdc1d172ecca2cc9f185d8c6`  
		Last Modified: Tue, 03 Jun 2025 14:19:54 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac00248845047c34ae131798d0fdbf6b3f50972fbdb09bd45de154e343497f67`  
		Last Modified: Tue, 03 Jun 2025 14:19:54 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697c9c6ee0304039e476bae239b9ed0530187df90060ad71d616b24e145045c2`  
		Last Modified: Tue, 03 Jun 2025 14:20:05 GMT  
		Size: 10.2 MB (10163271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0baff74ff1e1a2684e437e24cc7fa1872b64c52e6daa25ead9fa9b0dfd6de64e`  
		Last Modified: Tue, 03 Jun 2025 14:20:04 GMT  
		Size: 5.7 MB (5696021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7150af20f43bdd0b73599185a2cf70c989da52c15d8bc859098b84e613c33cd2`  
		Last Modified: Tue, 03 Jun 2025 14:19:54 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine3.22` - unknown; unknown

```console
$ docker pull httpd@sha256:7e9b46b213116d336e383ed41104a6917d3f1572b3f706a88ba0361b4339785d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1205554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3c7ab767b28c0e8f30b39392a3934612d0e5967374689a5c0ee8c067fdf6b6`

```dockerfile
```

-	Layers:
	-	`sha256:e4af6462cd1075feabbc6165ebd0d9d9d13b35abb1157f29692f3636285be234`  
		Last Modified: Tue, 03 Jun 2025 14:20:07 GMT  
		Size: 1.2 MB (1167363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5febad6a933d2a2cbfec3f3da04b7b179a1e12e0da7f2fc9c65c72220906682`  
		Last Modified: Tue, 03 Jun 2025 14:20:02 GMT  
		Size: 38.2 KB (38191 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine3.22` - linux; ppc64le

```console
$ docker pull httpd@sha256:093505e849685fe007716d0f9641f449e49383d09169b909f9e95448946e0c04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20710244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c735cffa71cc7c84f1937b4793ee1d4793d9d42b836afd0bf3be196e2eba49`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 20:51:53 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 30 May 2025 20:51:53 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 30 May 2025 20:51:53 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 20:51:53 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 30 May 2025 20:51:53 GMT
WORKDIR /usr/local/apache2
# Fri, 30 May 2025 20:51:53 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Fri, 30 May 2025 20:51:53 GMT
ENV HTTPD_VERSION=2.4.63
# Fri, 30 May 2025 20:51:53 GMT
ENV HTTPD_SHA256=88fc236ab99b2864b248de7d49a008ec2afd7551e64dce8b95f58f32f94c46ab
# Fri, 30 May 2025 20:51:53 GMT
ENV HTTPD_PATCHES=
# Fri, 30 May 2025 20:51:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Fri, 30 May 2025 20:51:53 GMT
STOPSIGNAL SIGWINCH
# Fri, 30 May 2025 20:51:53 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 30 May 2025 20:51:53 GMT
EXPOSE map[80/tcp:{}]
# Fri, 30 May 2025 20:51:53 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4508e4129f4311039d2352caa22c360f4e156d234477f3a12a1d11c59ed23f16`  
		Last Modified: Tue, 03 Jun 2025 14:20:04 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b59370dec533373261e79a623625f42aa03ce0583308531f36a31d6560a09e`  
		Last Modified: Tue, 03 Jun 2025 14:20:04 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bead0ccb4f11a200ca6e233ebd45a807e7ceab8cd438f668471e913c40ce3bb6`  
		Last Modified: Tue, 03 Jun 2025 14:20:15 GMT  
		Size: 10.8 MB (10843815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda3c5f78952484450e298db1d254c29d504e9f8246a05bb013d5a37ca216ae1`  
		Last Modified: Tue, 03 Jun 2025 14:20:14 GMT  
		Size: 6.1 MB (6134839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ac13601411f9feebcdf8bf9561db38bb75a8ebaf9e2d8f919ea6f62583f1e0`  
		Last Modified: Tue, 03 Jun 2025 14:20:05 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine3.22` - unknown; unknown

```console
$ docker pull httpd@sha256:7c364f39da7db7350fc0866a67205db3a50692cb22265f31fc311572d566ba8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1203837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:801a959d590d0320742eff72ea18f6ad5372824289930522e764e9d6fbe2d1be`

```dockerfile
```

-	Layers:
	-	`sha256:0f04a7e38fa23772d71c00e04350bccc504ff649ed8a3eff96babeebea35a9d7`  
		Last Modified: Tue, 03 Jun 2025 14:20:15 GMT  
		Size: 1.2 MB (1165515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46de9c2128686a9017227788265bae4230bd8d640b469beec46bdfbb16cf2b49`  
		Last Modified: Tue, 03 Jun 2025 14:20:10 GMT  
		Size: 38.3 KB (38322 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine3.22` - linux; riscv64

```console
$ docker pull httpd@sha256:ba88b20718439312e65a92d36b0294164a4abb6a5cac129828eaff96546950ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19330854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4dd8592ade01ed8ae03598062c428c36aad8c3d96dd871ef0fe3351c90e0839`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 20:51:53 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 30 May 2025 20:51:53 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 30 May 2025 20:51:53 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 20:51:53 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 30 May 2025 20:51:53 GMT
WORKDIR /usr/local/apache2
# Fri, 30 May 2025 20:51:53 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Fri, 30 May 2025 20:51:53 GMT
ENV HTTPD_VERSION=2.4.63
# Fri, 30 May 2025 20:51:53 GMT
ENV HTTPD_SHA256=88fc236ab99b2864b248de7d49a008ec2afd7551e64dce8b95f58f32f94c46ab
# Fri, 30 May 2025 20:51:53 GMT
ENV HTTPD_PATCHES=
# Fri, 30 May 2025 20:51:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Fri, 30 May 2025 20:51:53 GMT
STOPSIGNAL SIGWINCH
# Fri, 30 May 2025 20:51:53 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 30 May 2025 20:51:53 GMT
EXPOSE map[80/tcp:{}]
# Fri, 30 May 2025 20:51:53 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3a90244ea106fcbe4bde35386ce74712e3ebefdf0fe0cede7028c8a701d044`  
		Last Modified: Tue, 03 Jun 2025 14:02:03 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b75182ae83caa7688f696311876ca33545e6198625b5de195d24705566fce14`  
		Last Modified: Tue, 03 Jun 2025 14:02:04 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ab06f6836f7f66676c62a9108efc344cd4d328431158fba2d169d476cd5706c`  
		Last Modified: Tue, 03 Jun 2025 14:02:06 GMT  
		Size: 10.1 MB (10061515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d11f8add1dc66fa0db66f1af5b22f9fad63c3debb6763c950481a2f472da752`  
		Last Modified: Tue, 03 Jun 2025 14:02:08 GMT  
		Size: 5.8 MB (5754124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4b544546e7257f7bb28d7b5d8036e1fdb9e3a27f1719766f62d106c7127282`  
		Last Modified: Tue, 03 Jun 2025 14:02:09 GMT  
		Size: 289.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine3.22` - unknown; unknown

```console
$ docker pull httpd@sha256:cc94f294b8cda010a260e4a97fa02bc18c061b58e207f582694d1ca4bff60cec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1203834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7eeb79180c88598e36d95ce9092d9d06c1e5cb7e97ce70fa0cb535f8f296c8`

```dockerfile
```

-	Layers:
	-	`sha256:31274534eb0798594bbb1f73e72844124fae389cfcbb6f401f62e991e4219e8b`  
		Last Modified: Tue, 03 Jun 2025 14:02:12 GMT  
		Size: 1.2 MB (1165511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:931bc50ef8050ea4bd10105096f4d29e261f3482e8c482fa4f020370e935c4b9`  
		Last Modified: Tue, 03 Jun 2025 14:02:14 GMT  
		Size: 38.3 KB (38323 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine3.22` - linux; s390x

```console
$ docker pull httpd@sha256:3eb102c4886eaa0cc87bd6222a30a77b624005a8a94093f27af8cce8bb99b2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20812835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083d61a279c8214a9f6de280a1dc80b959157148a2d1ef992cd195932c9287bc`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Fri, 30 May 2025 20:51:53 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 30 May 2025 20:51:53 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 30 May 2025 20:51:53 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 30 May 2025 20:51:53 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 30 May 2025 20:51:53 GMT
WORKDIR /usr/local/apache2
# Fri, 30 May 2025 20:51:53 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Fri, 30 May 2025 20:51:53 GMT
ENV HTTPD_VERSION=2.4.63
# Fri, 30 May 2025 20:51:53 GMT
ENV HTTPD_SHA256=88fc236ab99b2864b248de7d49a008ec2afd7551e64dce8b95f58f32f94c46ab
# Fri, 30 May 2025 20:51:53 GMT
ENV HTTPD_PATCHES=
# Fri, 30 May 2025 20:51:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Fri, 30 May 2025 20:51:53 GMT
STOPSIGNAL SIGWINCH
# Fri, 30 May 2025 20:51:53 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 30 May 2025 20:51:53 GMT
EXPOSE map[80/tcp:{}]
# Fri, 30 May 2025 20:51:53 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f2cde5c07b420f9061c951e0e1e2ce0d4d24dae3da0cf4b28e90bd7e200705`  
		Last Modified: Tue, 03 Jun 2025 14:02:17 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955dcbe9baf9937e56e52a0525a1f5a268632cad45e9b73c4116af56f0d0d89e`  
		Last Modified: Tue, 03 Jun 2025 13:41:49 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b193f726a80421c6e3249f539d00dba50e5e394a89030a8b58772a3e215704c2`  
		Last Modified: Tue, 03 Jun 2025 14:02:20 GMT  
		Size: 11.2 MB (11197726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2ee43cc449f62a55ecda230743fdd57276ae8246900e6755d2efe0daae9b23`  
		Last Modified: Tue, 03 Jun 2025 14:02:22 GMT  
		Size: 6.0 MB (5966177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c310ba56660f857e85f6529f19984520f45ec4106bae9f25cf5fa203c582fc9d`  
		Last Modified: Tue, 03 Jun 2025 14:02:23 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine3.22` - unknown; unknown

```console
$ docker pull httpd@sha256:f5d20bd2c6e7567ba3ca752fe746481251ba51e30bedd16f431e2fe86aa3ebcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1203705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e31d924a44eda6efb3a2d827bba98d1c4fdc23e726eaad7d38931c09c178674`

```dockerfile
```

-	Layers:
	-	`sha256:4435acfffbacdee0a843e6327460eabe9d42656529f39fcbd342ed843f989287`  
		Last Modified: Tue, 03 Jun 2025 14:02:26 GMT  
		Size: 1.2 MB (1165457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3b97842d70a9511872c2244cf93ea9fe31cdd35616586cf2ca546dbf063bbf0`  
		Last Modified: Tue, 03 Jun 2025 14:02:27 GMT  
		Size: 38.2 KB (38248 bytes)  
		MIME: application/vnd.in-toto+json
