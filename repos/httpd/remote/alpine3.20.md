## `httpd:alpine3.20`

```console
$ docker pull httpd@sha256:def5b90f2a8817b27af2e46bbe937dc808c156bed0925bfb577302d4c9398410
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
$ docker pull httpd@sha256:a94a5cdbcd508ae65eee0d365d5ee090619f424402e5cba5dada264f29e0a80f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (21998151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef6f85a3507574c7f2c2c17dea4d0685bf9d253c246e3353f35407a5af6af89`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
CMD ["/bin/sh"]
# Mon, 01 Jul 2024 11:31:13 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 01 Jul 2024 11:31:13 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 01 Jul 2024 11:31:13 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Jul 2024 11:31:13 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 01 Jul 2024 11:31:13 GMT
WORKDIR /usr/local/apache2
# Mon, 01 Jul 2024 11:31:13 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 01 Jul 2024 11:31:13 GMT
ENV HTTPD_VERSION=2.4.60
# Mon, 01 Jul 2024 11:31:13 GMT
ENV HTTPD_SHA256=7b1ec7ec5635da7cb01550513215a90f8b2f52bb7c90cf3e97ede936d3e55b0f
# Mon, 01 Jul 2024 11:31:13 GMT
ENV HTTPD_PATCHES=
# Mon, 01 Jul 2024 11:31:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 01 Jul 2024 11:31:13 GMT
STOPSIGNAL SIGWINCH
# Mon, 01 Jul 2024 11:31:13 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 01 Jul 2024 11:31:13 GMT
EXPOSE map[80/tcp:{}]
# Mon, 01 Jul 2024 11:31:13 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38733b50d26b8badb0f1af1813e781c9fdb80c3434e4517110cf55ed0fd0368`  
		Last Modified: Tue, 02 Jul 2024 00:58:20 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36096d1dc2cf81e7b4f249f9fbf00efc4b55a88fe8b9d8a84e4724d6928a5ec7`  
		Last Modified: Tue, 02 Jul 2024 00:58:20 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247389bbeaf162b851fec1fbf0fd06e1effb1b4dae509c3db3f40b95970c20a6`  
		Last Modified: Tue, 02 Jul 2024 00:58:20 GMT  
		Size: 10.4 MB (10385424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ae30a5ddd307729009e219267ad896caefcc31ee39651c178ade08156cb81d`  
		Last Modified: Tue, 02 Jul 2024 00:58:21 GMT  
		Size: 8.0 MB (7987473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93ad0bafa08e556ea5a11f59372c97cab867664293fad57ec8a57ab2d6ec8ea`  
		Last Modified: Tue, 02 Jul 2024 00:58:20 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine3.20` - unknown; unknown

```console
$ docker pull httpd@sha256:513921bf475d0851850e192cc407f43c3bf8543019b63411b793efa8e55e9159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1104305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8635513281e70fafe67f4064f6fd69070a13d110a3968c80731ee109c56036d3`

```dockerfile
```

-	Layers:
	-	`sha256:28ca2daf21a588ef8fa012cbfedaed11f49f5ccfe06081268728d57944d08d00`  
		Last Modified: Tue, 02 Jul 2024 00:58:20 GMT  
		Size: 1.1 MB (1066271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfecf5c8b03a832802e15e5d6c7c5e628cde701e531d12bc30880d4cefc95675`  
		Last Modified: Tue, 02 Jul 2024 00:58:20 GMT  
		Size: 38.0 KB (38034 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine3.20` - linux; arm variant v6

```console
$ docker pull httpd@sha256:816d1a0afd6037991d58a37016537f2c92625a1a410702738a2fd5223cacd33e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20506435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc098de801cf3968314cfd1a3ef351f54bc1b30483f561a492163f3045f7e1e5`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:15 GMT
ADD file:ef2635f09c1d2632408805d106fbc5d27fb307cb5f584bddc699b4b5ae577623 in / 
# Thu, 20 Jun 2024 17:49:15 GMT
CMD ["/bin/sh"]
# Mon, 01 Jul 2024 11:31:13 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 01 Jul 2024 11:31:13 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 01 Jul 2024 11:31:13 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Jul 2024 11:31:13 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 01 Jul 2024 11:31:13 GMT
WORKDIR /usr/local/apache2
# Mon, 01 Jul 2024 11:31:13 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 01 Jul 2024 11:31:13 GMT
ENV HTTPD_VERSION=2.4.60
# Mon, 01 Jul 2024 11:31:13 GMT
ENV HTTPD_SHA256=7b1ec7ec5635da7cb01550513215a90f8b2f52bb7c90cf3e97ede936d3e55b0f
# Mon, 01 Jul 2024 11:31:13 GMT
ENV HTTPD_PATCHES=
# Mon, 01 Jul 2024 11:31:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 01 Jul 2024 11:31:13 GMT
STOPSIGNAL SIGWINCH
# Mon, 01 Jul 2024 11:31:13 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 01 Jul 2024 11:31:13 GMT
EXPOSE map[80/tcp:{}]
# Mon, 01 Jul 2024 11:31:13 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:3d2af5f613c84e549fb09710d45b152d3cdf48eb7a37dc3e9c01e2b3975f4f76`  
		Last Modified: Thu, 20 Jun 2024 17:49:36 GMT  
		Size: 3.4 MB (3367154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d823dfe33bf0238ed14096fc83fae491d0c7e1db7fb9d75cf2ece138e8a437c`  
		Last Modified: Tue, 02 Jul 2024 00:58:32 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5768a97a18ce68ced5063ff84bc1c39a0589b7111cccf3b7930518b44c98e1d2`  
		Last Modified: Tue, 02 Jul 2024 00:58:32 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b726441dbfc7d26d272d15818af4d87e28469d8a3e69b98af4d5742ad223ce95`  
		Last Modified: Tue, 02 Jul 2024 00:58:33 GMT  
		Size: 9.6 MB (9578604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0548806dace2af49006d39dae37b553b6c055463617a7f4317f133860053a3`  
		Last Modified: Tue, 02 Jul 2024 00:58:33 GMT  
		Size: 7.6 MB (7559264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdec7c71e5605fdf0824db32bfbb44f2b4eabc40fb4efb364f1a2faf0e7cea7`  
		Last Modified: Tue, 02 Jul 2024 00:58:33 GMT  
		Size: 289.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine3.20` - unknown; unknown

```console
$ docker pull httpd@sha256:0872e101837db8a57307c328f4c2f9ff523c40622fb4913c5a6314536dab44ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 KB (37953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9383ca917341972b2b9e7505c6ad17f341905d2a66b900884c459cf0c052452f`

```dockerfile
```

-	Layers:
	-	`sha256:27e53d30f46744cb270ee25b183ce4c3f0a745875239b796b1bf3fde37b95041`  
		Last Modified: Tue, 02 Jul 2024 00:58:32 GMT  
		Size: 38.0 KB (37953 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine3.20` - linux; arm variant v7

```console
$ docker pull httpd@sha256:0d687c421d90ac29044f6974ec72c4a702b07bede571922a631051e46a87bbb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19527530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36433b00bce8de3543ca7e3c3af8f27ba31949f58b84df2c424906d18abf04f5`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Mon, 01 Jul 2024 11:31:13 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 01 Jul 2024 11:31:13 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 01 Jul 2024 11:31:13 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Jul 2024 11:31:13 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 01 Jul 2024 11:31:13 GMT
WORKDIR /usr/local/apache2
# Mon, 01 Jul 2024 11:31:13 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 01 Jul 2024 11:31:13 GMT
ENV HTTPD_VERSION=2.4.60
# Mon, 01 Jul 2024 11:31:13 GMT
ENV HTTPD_SHA256=7b1ec7ec5635da7cb01550513215a90f8b2f52bb7c90cf3e97ede936d3e55b0f
# Mon, 01 Jul 2024 11:31:13 GMT
ENV HTTPD_PATCHES=
# Mon, 01 Jul 2024 11:31:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 01 Jul 2024 11:31:13 GMT
STOPSIGNAL SIGWINCH
# Mon, 01 Jul 2024 11:31:13 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 01 Jul 2024 11:31:13 GMT
EXPOSE map[80/tcp:{}]
# Mon, 01 Jul 2024 11:31:13 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e10705b5c314e515ce5d4fe1fe6c181cafedf75c636f4263634710d34b7e698`  
		Last Modified: Tue, 02 Jul 2024 01:10:06 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2abe1bf3107f7e1e418c5862feed0bed3be7be3dd6df0274a13ccc85b7eb621`  
		Last Modified: Tue, 02 Jul 2024 01:10:06 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bf1c714123f4a7c0a513b2e575f7f1e617aeb42e7c2e5d3b131eaa8582501a`  
		Last Modified: Tue, 02 Jul 2024 01:10:07 GMT  
		Size: 9.3 MB (9344963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aafec9825db4574af6ed66f46194c04c29bda3b261fa6cae77ec5eee975c9354`  
		Last Modified: Tue, 02 Jul 2024 01:10:07 GMT  
		Size: 7.1 MB (7086301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3db2b921e1d601486aa239e687e2dd81dda9cd8b8f2fa6b69ffcc3394da280`  
		Last Modified: Tue, 02 Jul 2024 01:10:07 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine3.20` - unknown; unknown

```console
$ docker pull httpd@sha256:ee23198a0ebbb21ecf538b2211b590d77565ee82acf34ee4db1d352de5e88a35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1107089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf6ef8bb04874dc2686556aabe66da8c206bf587b67e4d9074e5d1ddecb18bc`

```dockerfile
```

-	Layers:
	-	`sha256:16ec765173c85f28e150007d2115cd2b3e289a4dbdfb50eaef25344e38bdaaaf`  
		Last Modified: Tue, 02 Jul 2024 01:10:06 GMT  
		Size: 1.1 MB (1068917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6309d24df788eec9b16aaee785873966e427f3e4af27a4619c7074b094e5170d`  
		Last Modified: Tue, 02 Jul 2024 01:10:06 GMT  
		Size: 38.2 KB (38172 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:4fdc028ff79817efbe3df4c81f7a4e6b9a641c31f0d5af8ef867a98d8fc56985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20194919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4c534ddad09884d2b43dd32e3abf5eda253d8282d407fe2fd59a29def6310de`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Thu, 30 May 2024 14:24:56 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 30 May 2024 14:24:56 GMT
CMD ["/bin/sh"]
# Thu, 30 May 2024 14:24:56 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 30 May 2024 14:24:56 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 30 May 2024 14:24:56 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 14:24:56 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 30 May 2024 14:24:56 GMT
WORKDIR /usr/local/apache2
# Thu, 30 May 2024 14:24:56 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 30 May 2024 14:24:56 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 30 May 2024 14:24:56 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 30 May 2024 14:24:56 GMT
ENV HTTPD_PATCHES=
# Thu, 30 May 2024 14:24:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 30 May 2024 14:24:56 GMT
STOPSIGNAL SIGWINCH
# Thu, 30 May 2024 14:24:56 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 30 May 2024 14:24:56 GMT
EXPOSE map[80/tcp:{}]
# Thu, 30 May 2024 14:24:56 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb160a9adce2b08a69a097d7c3caee33c1cbad9f71dbe74d7e083109a9f77b12`  
		Last Modified: Fri, 21 Jun 2024 05:12:16 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9372e7b75a693d351c84d4591d0a69ad2985967b6216db0cefc8b4e161b155e6`  
		Last Modified: Fri, 21 Jun 2024 05:12:16 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f39c99ae717c59d429f033bfe672a0de59e94b8bcbd54314fc278c476c5823`  
		Last Modified: Fri, 21 Jun 2024 05:12:17 GMT  
		Size: 10.4 MB (10397199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196c1b64c090496682d63f5a006647a88b2b85367f659d2056a010542515e567`  
		Last Modified: Fri, 21 Jun 2024 05:12:17 GMT  
		Size: 5.7 MB (5707507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b146f3477bc1a8b33fa378c5bffa6e935c8fbf1a42f026dd4c4e1a146ab3c6`  
		Last Modified: Fri, 21 Jun 2024 05:12:17 GMT  
		Size: 290.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine3.20` - unknown; unknown

```console
$ docker pull httpd@sha256:ce872637aaa7f60fd2c535a8b43caf2aefe1ae17c045838a31d97dc31fabff9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1104757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c57a974e00c7abdf13d8f055e5fc248510537ed9f566d25f0cc6fe9f6bae16`

```dockerfile
```

-	Layers:
	-	`sha256:c375cec7fc9a141c0bf4f74807c58a48c359a94856644ce409e834045b5d739a`  
		Last Modified: Fri, 21 Jun 2024 05:12:17 GMT  
		Size: 1.1 MB (1066375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed89014de7cdf1ef92b4b0f6b6d038557678820af8fce33938bda32130f5e349`  
		Last Modified: Fri, 21 Jun 2024 05:12:16 GMT  
		Size: 38.4 KB (38382 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine3.20` - linux; 386

```console
$ docker pull httpd@sha256:caacad4053353cdf6939bc4839b9483e92a6e294cf528631262d41bf950c3486
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21086392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8855a33b6a8126125e6d92f72125608a2a2f148beb79cd26d8a9898a65a74b`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Thu, 20 Jun 2024 17:38:24 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
# Thu, 20 Jun 2024 17:38:25 GMT
CMD ["/bin/sh"]
# Mon, 01 Jul 2024 11:31:13 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 01 Jul 2024 11:31:13 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 01 Jul 2024 11:31:13 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Jul 2024 11:31:13 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 01 Jul 2024 11:31:13 GMT
WORKDIR /usr/local/apache2
# Mon, 01 Jul 2024 11:31:13 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 01 Jul 2024 11:31:13 GMT
ENV HTTPD_VERSION=2.4.60
# Mon, 01 Jul 2024 11:31:13 GMT
ENV HTTPD_SHA256=7b1ec7ec5635da7cb01550513215a90f8b2f52bb7c90cf3e97ede936d3e55b0f
# Mon, 01 Jul 2024 11:31:13 GMT
ENV HTTPD_PATCHES=
# Mon, 01 Jul 2024 11:31:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 01 Jul 2024 11:31:13 GMT
STOPSIGNAL SIGWINCH
# Mon, 01 Jul 2024 11:31:13 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 01 Jul 2024 11:31:13 GMT
EXPOSE map[80/tcp:{}]
# Mon, 01 Jul 2024 11:31:13 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf233b9717d7212e3c0f7123fa3210036b2aadc96eb015eabbd40a1a67963ab`  
		Last Modified: Tue, 02 Jul 2024 00:58:21 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8360dc57be6c73ac21664ec4cf159292bdef55e4d6752482bae3ff24e09e5de7`  
		Last Modified: Tue, 02 Jul 2024 00:58:21 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd2a952f8307f70b4889f26e450ec5c41956ed63788d96d4dc677a19d6fa704`  
		Last Modified: Tue, 02 Jul 2024 00:58:21 GMT  
		Size: 9.9 MB (9862623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e9526e346ba5d081abc77d8c44efa8b54020254270328722a4f2071586bcce`  
		Last Modified: Tue, 02 Jul 2024 00:58:22 GMT  
		Size: 7.8 MB (7752888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814e953380afbc1083a32f043d80acd05c8a9b629a21808dbac2fe8324695987`  
		Last Modified: Tue, 02 Jul 2024 00:58:22 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine3.20` - unknown; unknown

```console
$ docker pull httpd@sha256:bfdc8782c31301c9d60fc68e2768eae1572f36e50e5697133fd6b81ea5d098e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1104202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5473749637cb8a7efc5f3762f821e647b8cdcde029485eddb7ca011c61592e`

```dockerfile
```

-	Layers:
	-	`sha256:70dc15239a3e909deca4193550906b7284d44705dc8a4ccbd889f69f46ac51a3`  
		Last Modified: Tue, 02 Jul 2024 00:58:21 GMT  
		Size: 1.1 MB (1066226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b2ecaf7f88d5b963c228988916ccda5242e315711bfd3fd397ed40a1ecedfe4`  
		Last Modified: Tue, 02 Jul 2024 00:58:21 GMT  
		Size: 38.0 KB (37976 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine3.20` - linux; ppc64le

```console
$ docker pull httpd@sha256:7d32f41d0425cdd1e29f03fa7084a6e9c276d11bce0619c71cb3866364f37023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.4 MB (22419424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f62e1f503f8a2ef4394b3084fc64a62fb438d3a0abd08c657267d831e27f008c`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
CMD ["/bin/sh"]
# Mon, 01 Jul 2024 11:31:13 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 01 Jul 2024 11:31:13 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 01 Jul 2024 11:31:13 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Jul 2024 11:31:13 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 01 Jul 2024 11:31:13 GMT
WORKDIR /usr/local/apache2
# Mon, 01 Jul 2024 11:31:13 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 01 Jul 2024 11:31:13 GMT
ENV HTTPD_VERSION=2.4.60
# Mon, 01 Jul 2024 11:31:13 GMT
ENV HTTPD_SHA256=7b1ec7ec5635da7cb01550513215a90f8b2f52bb7c90cf3e97ede936d3e55b0f
# Mon, 01 Jul 2024 11:31:13 GMT
ENV HTTPD_PATCHES=
# Mon, 01 Jul 2024 11:31:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 01 Jul 2024 11:31:13 GMT
STOPSIGNAL SIGWINCH
# Mon, 01 Jul 2024 11:31:13 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 01 Jul 2024 11:31:13 GMT
EXPOSE map[80/tcp:{}]
# Mon, 01 Jul 2024 11:31:13 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9eaa28be5220f174c394da65af3287cba76cb6a3162bcc0d50402bd77597719`  
		Last Modified: Tue, 02 Jul 2024 01:01:47 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68428b772fbaf4b3917a0026d99c5e7b9a5e2260060d1973395ffc42ad566a73`  
		Last Modified: Tue, 02 Jul 2024 01:01:47 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fcb6ca8937ba8ca0f619a065263f83f35c0848f950f5496dd60869d19b116b7`  
		Last Modified: Tue, 02 Jul 2024 01:01:49 GMT  
		Size: 10.6 MB (10639251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4ddb6cc4656587fb36455ff330f7875cf6456fcb7c0a9a8a9fa00c977a9b51`  
		Last Modified: Tue, 02 Jul 2024 01:01:48 GMT  
		Size: 8.2 MB (8207066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34ab4226ff29b5b736a814cd2e3e80ca5885513de0536cd174c8b8510e332c2`  
		Last Modified: Tue, 02 Jul 2024 01:01:48 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine3.20` - unknown; unknown

```console
$ docker pull httpd@sha256:847abb91ff69d79494334dbd0b445f3df67bdfeea4662e7bedf753c310dc9286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1102476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e850ab4c3e9c0886b85589f812e075859f43ae54e04ef594133cc81df712e567`

```dockerfile
```

-	Layers:
	-	`sha256:f7c7ec213fa663ac89096671731f85a6e12bae40f511e82dadb98aaa4faa254f`  
		Last Modified: Tue, 02 Jul 2024 01:01:47 GMT  
		Size: 1.1 MB (1064375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8662d9e36b62ac329cd37172dbc51e7e8550252d67630911c29ab6c15de41542`  
		Last Modified: Tue, 02 Jul 2024 01:01:47 GMT  
		Size: 38.1 KB (38101 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine3.20` - linux; riscv64

```console
$ docker pull httpd@sha256:abb5a16cc76e52f10fc37cf13e0ab560478d375a0fab6a865c8cc5ef020da7de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.8 MB (18818468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0378e81ff1e376ba77369a5a1760db62119900445c6352b720f59a0c03ef0d9`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Thu, 30 May 2024 14:24:56 GMT
ADD file:851dbd05bad08468ee2a960e5f9f0aa9b19f1114ec52c39d1a28cd427344d0ef in / 
# Thu, 30 May 2024 14:24:56 GMT
CMD ["/bin/sh"]
# Thu, 30 May 2024 14:24:56 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 30 May 2024 14:24:56 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 30 May 2024 14:24:56 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 May 2024 14:24:56 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 30 May 2024 14:24:56 GMT
WORKDIR /usr/local/apache2
# Thu, 30 May 2024 14:24:56 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 30 May 2024 14:24:56 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 30 May 2024 14:24:56 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 30 May 2024 14:24:56 GMT
ENV HTTPD_PATCHES=
# Thu, 30 May 2024 14:24:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 30 May 2024 14:24:56 GMT
STOPSIGNAL SIGWINCH
# Thu, 30 May 2024 14:24:56 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 30 May 2024 14:24:56 GMT
EXPOSE map[80/tcp:{}]
# Thu, 30 May 2024 14:24:56 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:d4714cc4c8bb5ceda619fceb44b088091082a8d2407d2008123fe93478722d1a`  
		Last Modified: Thu, 20 Jun 2024 18:18:22 GMT  
		Size: 3.4 MB (3371037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0108dc7b31e2172268cb0a8f5b64a64faa631a69137f05aa5ff9419e3ff14d28`  
		Last Modified: Fri, 21 Jun 2024 09:05:17 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9adc5547c5b459c900ff7bca415af2fcf8c36dee0421969a856dd86cb48a57`  
		Last Modified: Fri, 21 Jun 2024 09:05:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79e2aebed40f09e60b2be63bd46fa950491e95dda2d67d0106ca641511007c97`  
		Last Modified: Fri, 21 Jun 2024 09:05:19 GMT  
		Size: 9.9 MB (9875370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0af0d85a5d699b58082717ceb306a225e44f9f29d6e133387031071bcdd0862`  
		Last Modified: Fri, 21 Jun 2024 09:05:18 GMT  
		Size: 5.6 MB (5570643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d741ea27a84af80eff06c6daf2f13707e3cd70e64b984529efebc6e2dca6a6`  
		Last Modified: Fri, 21 Jun 2024 09:05:18 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine3.20` - unknown; unknown

```console
$ docker pull httpd@sha256:4e0e260a2f570984681ec0b5b1262f62d4c3cb573eb78a36ec535085dce46298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1102470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e10fc05320be59b93889712ad2dbdf489c3418818fbc5ba39b7feadff8bfd67`

```dockerfile
```

-	Layers:
	-	`sha256:cedd4b6021f6330763e61025ec481c1dfd2c159447d6860bbe686563960b2f1a`  
		Last Modified: Fri, 21 Jun 2024 09:05:17 GMT  
		Size: 1.1 MB (1064371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d9ea500dd1652002451839c9fe6f5ff36a431e4ac3ffc31aaf72c7216016d6a`  
		Last Modified: Fri, 21 Jun 2024 09:05:17 GMT  
		Size: 38.1 KB (38099 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine3.20` - linux; s390x

```console
$ docker pull httpd@sha256:8dacb8b1a207a1cf06bcdb82547d4ffa172fcde107e36a6d5b38408559a4444e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.4 MB (22377536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b943f70f0ba175164e025db082745997e31435196438321c31bc2ffdbc979fcb`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
CMD ["/bin/sh"]
# Mon, 01 Jul 2024 11:31:13 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 01 Jul 2024 11:31:13 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 01 Jul 2024 11:31:13 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Jul 2024 11:31:13 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 01 Jul 2024 11:31:13 GMT
WORKDIR /usr/local/apache2
# Mon, 01 Jul 2024 11:31:13 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 01 Jul 2024 11:31:13 GMT
ENV HTTPD_VERSION=2.4.60
# Mon, 01 Jul 2024 11:31:13 GMT
ENV HTTPD_SHA256=7b1ec7ec5635da7cb01550513215a90f8b2f52bb7c90cf3e97ede936d3e55b0f
# Mon, 01 Jul 2024 11:31:13 GMT
ENV HTTPD_PATCHES=
# Mon, 01 Jul 2024 11:31:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 01 Jul 2024 11:31:13 GMT
STOPSIGNAL SIGWINCH
# Mon, 01 Jul 2024 11:31:13 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 01 Jul 2024 11:31:13 GMT
EXPOSE map[80/tcp:{}]
# Mon, 01 Jul 2024 11:31:13 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20628ca8294b6db6a49614e97e3ab4dcf6b42c8165d79114fab6090eb057a719`  
		Last Modified: Tue, 02 Jul 2024 00:59:53 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ab3e489126230b4092f27f9e9af3d0ada3642241b4a2e21434c59f6b86e5c3`  
		Last Modified: Tue, 02 Jul 2024 00:59:53 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39f32f98db63549cf88ba1610be9983fc695e29565ce7e95df9f862bd3f5707`  
		Last Modified: Tue, 02 Jul 2024 00:59:54 GMT  
		Size: 11.0 MB (10989163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b870693427026a8fe604b937e48bcc13f9b294986364a74cc1a35334d4b0d3ad`  
		Last Modified: Tue, 02 Jul 2024 00:59:54 GMT  
		Size: 7.9 MB (7925105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb7c5c1b78a131eb78104795edc3b0cc94e38fc1ffd6ae527b77ae7e9a2f66`  
		Last Modified: Tue, 02 Jul 2024 00:59:54 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine3.20` - unknown; unknown

```console
$ docker pull httpd@sha256:5cbfd13c54a4c6c049e65304b399de7c0ae37d5ac0b9961724bfc2d8203f0275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1102351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fbd34a47d076cae4df9d0393932a016eaeccb647149ded53db1a382d66fe926`

```dockerfile
```

-	Layers:
	-	`sha256:f68a8f1b876f3676f70d37234dc208a2e4c73c7d722183261822297e6df0128e`  
		Last Modified: Tue, 02 Jul 2024 00:59:54 GMT  
		Size: 1.1 MB (1064317 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65a47c406bf4e84653930c0647a56eceb65bffaaf2c3cbd3d67ab5b3dbe28eb3`  
		Last Modified: Tue, 02 Jul 2024 00:59:53 GMT  
		Size: 38.0 KB (38034 bytes)  
		MIME: application/vnd.in-toto+json
