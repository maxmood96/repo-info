## `httpd:trixie`

```console
$ docker pull httpd@sha256:ed59784cd9fb30d2fb75d4a2a49f7faca1c47200bd36385e8d1a15d53921f744
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
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

### `httpd:trixie` - linux; amd64

```console
$ docker pull httpd@sha256:2fe8d2c5afb94e63f8250b8436ff6b2436492996ce0a90e595a6eb5849895370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45206985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a4fe18d08d26a61b32d6aa5d17b2417c4f4de63e8460abf4cd824b911b9de88`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:05:09 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Tue, 04 Nov 2025 04:05:09 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:05:09 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Tue, 04 Nov 2025 04:05:09 GMT
WORKDIR /usr/local/apache2
# Tue, 04 Nov 2025 04:05:15 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 04:05:15 GMT
ENV HTTPD_VERSION=2.4.65
# Tue, 04 Nov 2025 04:05:15 GMT
ENV HTTPD_SHA256=58b8be97d9940ec17f7656c0c6b9f41b618aac468b894b534148e3296c53b8b3
# Tue, 04 Nov 2025 04:05:15 GMT
ENV HTTPD_PATCHES=
# Tue, 04 Nov 2025 04:07:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Tue, 04 Nov 2025 04:07:19 GMT
STOPSIGNAL SIGWINCH
# Tue, 04 Nov 2025 04:07:19 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:07:19 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 04:07:19 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab98c44430d1e14fc5e19f72910bdc2eb900c4a01fc7d5dcf7406ec21069339`  
		Last Modified: Tue, 04 Nov 2025 04:07:34 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c22d886563a136b3d65a3436990de48bd74c3af05cb436ac25f5d80008327e`  
		Last Modified: Tue, 04 Nov 2025 04:07:34 GMT  
		Size: 2.0 MB (1997493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4870f70a855683ee5faba1634768946011acfcf21707fc5035ba31dd45b6c221`  
		Last Modified: Tue, 04 Nov 2025 04:07:35 GMT  
		Size: 13.4 MB (13430921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233dec01418cb9ac2e266891986e2f614fa25242452b0a87fe6a0cc0069ea106`  
		Last Modified: Tue, 04 Nov 2025 04:07:34 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:230d98f0484bcbb8c1fdcf2aed922c84f0157caae3eee692235de0adaaf57295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2329786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48361110ab2f378c643eec4214763657b84d106991070d046cab58f488f3ef11`

```dockerfile
```

-	Layers:
	-	`sha256:a654ee36d9995a99dd6850d80ce3c3e45ad9b09e39fa4c516d11ccb11ff8bc5b`  
		Last Modified: Tue, 04 Nov 2025 09:52:35 GMT  
		Size: 2.3 MB (2292176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5a546c8d22a13d1a6f0f9bbecba928d8db392b59891ffd0698c0cc80f5fe680`  
		Last Modified: Tue, 04 Nov 2025 09:52:36 GMT  
		Size: 37.6 KB (37610 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:trixie` - linux; arm variant v5

```console
$ docker pull httpd@sha256:430f92c3d7b85c6aae2a7c4800d7b0e8c62f8a689875230d995f207fbca95abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42831344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38e549de2b122f9a4da0fe3c8e29efe8eb9fc0569700c30759a5e1ad97c5d17`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 00:23:48 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Tue, 04 Nov 2025 00:23:48 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:23:48 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Tue, 04 Nov 2025 00:23:48 GMT
WORKDIR /usr/local/apache2
# Tue, 04 Nov 2025 00:23:58 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 00:23:58 GMT
ENV HTTPD_VERSION=2.4.65
# Tue, 04 Nov 2025 00:23:58 GMT
ENV HTTPD_SHA256=58b8be97d9940ec17f7656c0c6b9f41b618aac468b894b534148e3296c53b8b3
# Tue, 04 Nov 2025 00:23:58 GMT
ENV HTTPD_PATCHES=
# Tue, 04 Nov 2025 00:26:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Tue, 04 Nov 2025 00:26:36 GMT
STOPSIGNAL SIGWINCH
# Tue, 04 Nov 2025 00:26:36 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:26:36 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 00:26:36 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:453afc2258d7bc5729fed5672fb95bafa092e30a933b4377a12034be940a671b`  
		Last Modified: Tue, 04 Nov 2025 00:13:12 GMT  
		Size: 27.9 MB (27946438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a192f30e7c542adddc7528b47dd29142e75364cb544492c9fdf12f3b519be62`  
		Last Modified: Tue, 04 Nov 2025 00:26:49 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98463e3f08983d7895fe1d29c26e071277c9377bc5724ef183f86027c68306e6`  
		Last Modified: Tue, 04 Nov 2025 00:26:50 GMT  
		Size: 1.9 MB (1911838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31eb874918725eee4d27e890dd8da7db31bbed4abba5e6b41a8f8a394d850c3f`  
		Last Modified: Tue, 04 Nov 2025 00:26:51 GMT  
		Size: 13.0 MB (12972602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5ffe656497ebeb36ab48fda147f15e876ebf0dbb45a262b9cad2df44a12912`  
		Last Modified: Tue, 04 Nov 2025 00:26:49 GMT  
		Size: 289.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:84df3ce64d7fba10941ae603f0b5a2e4a12ee0f26bb851dfda46036ec5f6b450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2332956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9693696b71bbef549ef8dc738a9080936c5c6ff6929e257cb5f63af6f3c592`

```dockerfile
```

-	Layers:
	-	`sha256:ebbdd88022f989d6685cd8c1cb5cb4d385356b2858e0e0e57abcd6aa53567b4b`  
		Last Modified: Tue, 04 Nov 2025 09:52:39 GMT  
		Size: 2.3 MB (2295208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfc22dd100058710df202dd6b4b3b99765bc3ce23de709d326c6afe495609201`  
		Last Modified: Tue, 04 Nov 2025 09:52:40 GMT  
		Size: 37.7 KB (37748 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:trixie` - linux; arm variant v7

```console
$ docker pull httpd@sha256:e2161269026f3085ce29b157f9267ec88db6a4fbba490a2b0165e10b05dace4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40536297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb64fb771cfbad1832265325ed93ed0a445d339995a9314a58694ca72207e646`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:06:36 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Tue, 04 Nov 2025 02:06:36 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 02:06:36 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Tue, 04 Nov 2025 02:06:36 GMT
WORKDIR /usr/local/apache2
# Tue, 04 Nov 2025 02:06:43 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:06:43 GMT
ENV HTTPD_VERSION=2.4.65
# Tue, 04 Nov 2025 02:06:43 GMT
ENV HTTPD_SHA256=58b8be97d9940ec17f7656c0c6b9f41b618aac468b894b534148e3296c53b8b3
# Tue, 04 Nov 2025 02:06:43 GMT
ENV HTTPD_PATCHES=
# Tue, 04 Nov 2025 02:09:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Tue, 04 Nov 2025 02:09:07 GMT
STOPSIGNAL SIGWINCH
# Tue, 04 Nov 2025 02:09:07 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 02:09:07 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 02:09:07 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354f9232f2b892450f56d386d36ad52880052a0e5306fc046c01d46f800395d6`  
		Last Modified: Tue, 04 Nov 2025 02:09:25 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5b5c481d6bf52470f7474e7a9a7ab15af2b9b7c79775f39933d851ac1553fd`  
		Last Modified: Tue, 04 Nov 2025 02:09:25 GMT  
		Size: 1.8 MB (1822635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfcf41769571c24c2ae7905b63233618feaedf990bc4e0594a31ed2967b5684`  
		Last Modified: Tue, 04 Nov 2025 02:09:27 GMT  
		Size: 12.5 MB (12500155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d33ea80fffb29fd8b7cbbe3b5ecc788e01383d9e980c76e1950ca1871031af`  
		Last Modified: Tue, 04 Nov 2025 02:09:25 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:c2d3b71df4e960e732c4c65da3de54185b47efc57d12638bf3e3e9ad1f751b1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2331472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:321c8f9fbf010074dd9bf722d3e8cd72b17cdbad48f17fd922f658e2fbb5cb8f`

```dockerfile
```

-	Layers:
	-	`sha256:0af6f6fb499f3514742fbf1fbd54e28be218ddbd581f603f559f8f14fb67ec1a`  
		Last Modified: Tue, 04 Nov 2025 09:52:45 GMT  
		Size: 2.3 MB (2293723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6cb92da34d5fc9f22173239b4e573cfff8ec070608760bdb85d0ccecf6acf91`  
		Last Modified: Tue, 04 Nov 2025 09:52:45 GMT  
		Size: 37.7 KB (37749 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:trixie` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:71acf1df956b23396740ed873e45d66322ec500277b47e2207d7f6ba7d3e553f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45486358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ce40212918004944d1681499818c032570dd41684872026692169a2c6a8a9b`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 08 Aug 2025 19:04:23 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Fri, 08 Aug 2025 19:04:23 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 08 Aug 2025 19:04:23 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 19:04:23 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 08 Aug 2025 19:04:23 GMT
WORKDIR /usr/local/apache2
# Fri, 08 Aug 2025 19:04:23 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Fri, 08 Aug 2025 19:04:23 GMT
ENV HTTPD_VERSION=2.4.65
# Fri, 08 Aug 2025 19:04:23 GMT
ENV HTTPD_SHA256=58b8be97d9940ec17f7656c0c6b9f41b618aac468b894b534148e3296c53b8b3
# Fri, 08 Aug 2025 19:04:23 GMT
ENV HTTPD_PATCHES=
# Fri, 08 Aug 2025 19:04:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Fri, 08 Aug 2025 19:04:23 GMT
STOPSIGNAL SIGWINCH
# Fri, 08 Aug 2025 19:04:23 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 19:04:23 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 Aug 2025 19:04:23 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b4b6ad9b71a5cd44e037148c0de51763afbb138b2ddf9c752c890db8b3ed54`  
		Last Modified: Tue, 21 Oct 2025 01:18:16 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea5feec9b01d0eb1dafe091cff35dc305c8e5817e0e7d4454ba2e9a1df57dd5`  
		Last Modified: Tue, 21 Oct 2025 01:18:17 GMT  
		Size: 2.0 MB (1970324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6b5eb56880a89f8839298b6974bd366d27ef4cf0f8cb8c36f354f46cabf98f`  
		Last Modified: Tue, 21 Oct 2025 01:18:18 GMT  
		Size: 13.4 MB (13373439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5767d64c333ce5ffec7089dfc527532f6ef5cd327fda4c0516b6ce991770f27`  
		Last Modified: Tue, 21 Oct 2025 01:18:16 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:60665e5e7a2c0b886d96471cb1e00736da6291e96d2390d710e59bbca2ef3c8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915fa56b3707b672490b467577072274aa8c911e715ce674b86cd99c320c974d`

```dockerfile
```

-	Layers:
	-	`sha256:32d58634a3a9135879a8d08a7bd350621f7f445cdd55134a54273ed91cc262b3`  
		Last Modified: Tue, 21 Oct 2025 08:52:34 GMT  
		Size: 2.3 MB (2292521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:363f38670f8a5b585d3db3cfcab3a46c3d0eb0731128baa931e29f8900441807`  
		Last Modified: Tue, 21 Oct 2025 08:52:35 GMT  
		Size: 37.8 KB (37836 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:trixie` - linux; 386

```console
$ docker pull httpd@sha256:b0a5f2ed8c5bfa6f9336d46a17f82ea99f912bebcaf1be8142b77621e0170988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46549900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0851aa4babd0e8a11baae36cddea54e2108bdf78cb89d8329120d034da083777`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:19:24 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Tue, 04 Nov 2025 01:19:24 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:19:24 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Tue, 04 Nov 2025 01:19:24 GMT
WORKDIR /usr/local/apache2
# Tue, 04 Nov 2025 01:19:29 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 01:19:29 GMT
ENV HTTPD_VERSION=2.4.65
# Tue, 04 Nov 2025 01:19:29 GMT
ENV HTTPD_SHA256=58b8be97d9940ec17f7656c0c6b9f41b618aac468b894b534148e3296c53b8b3
# Tue, 04 Nov 2025 01:19:29 GMT
ENV HTTPD_PATCHES=
# Tue, 04 Nov 2025 01:21:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Tue, 04 Nov 2025 01:21:27 GMT
STOPSIGNAL SIGWINCH
# Tue, 04 Nov 2025 01:21:27 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:21:27 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 01:21:27 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25d9a803a7b41474a130575ab06f532799a4d057b15ab8faaa28a0cfa3f42f9`  
		Last Modified: Tue, 04 Nov 2025 01:21:40 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c910f671eee3f9891a9bbbcc358f2281a12ae0fe42f7ef7303c5f18192ab11fe`  
		Last Modified: Tue, 04 Nov 2025 01:21:40 GMT  
		Size: 2.1 MB (2055252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2bb0d6273280d042b7eb67778be9f751dbb6d888d261d84006f858306c344b3`  
		Last Modified: Tue, 04 Nov 2025 01:21:41 GMT  
		Size: 13.2 MB (13199397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5288ed78347b91f8211d712fa18f445c5d5a25531659e53733fc646eace34f26`  
		Last Modified: Tue, 04 Nov 2025 01:21:40 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:39f1b82b42bf1847f1edecb8d93aa28cef3110933895b3471a4c3dc0097c0d54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2326830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:003b84fc02b7bcb4ad1d7f0dcd783b362591a94523c7ecef86ca482081fa4ca8`

```dockerfile
```

-	Layers:
	-	`sha256:9c314e8b220006076f1e46c68af10e11dcb9eb040998edb23dc1fa51e50fbaab`  
		Last Modified: Tue, 04 Nov 2025 09:52:51 GMT  
		Size: 2.3 MB (2289275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a5dc7394e23992267ad5b443d65e43a47bc44186a1a894ad1398725978425ad`  
		Last Modified: Tue, 04 Nov 2025 09:52:52 GMT  
		Size: 37.6 KB (37555 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:trixie` - linux; ppc64le

```console
$ docker pull httpd@sha256:3d4acd777a25f6226df7407a956e5208bf12904c2957ebe31c27df7de85911c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50137863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:412446a4060d35c13ca1ebd57934dd39da019ec2dadae57d485f3d9980503672`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:34:56 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Tue, 04 Nov 2025 01:34:56 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:34:56 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Tue, 04 Nov 2025 01:34:57 GMT
WORKDIR /usr/local/apache2
# Tue, 04 Nov 2025 01:35:07 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 01:35:07 GMT
ENV HTTPD_VERSION=2.4.65
# Tue, 04 Nov 2025 01:35:07 GMT
ENV HTTPD_SHA256=58b8be97d9940ec17f7656c0c6b9f41b618aac468b894b534148e3296c53b8b3
# Tue, 04 Nov 2025 01:35:07 GMT
ENV HTTPD_PATCHES=
# Tue, 04 Nov 2025 01:38:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Tue, 04 Nov 2025 01:38:42 GMT
STOPSIGNAL SIGWINCH
# Tue, 04 Nov 2025 01:38:42 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:38:42 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 01:38:42 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528ba6e5557e998749f79b08274b9d88e1e14d6686522bd226bc184f8a1f1b31`  
		Last Modified: Tue, 04 Nov 2025 01:39:12 GMT  
		Size: 143.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2717e36e211007f608953d4167c6dd19e4dd5351d40a556e0d679b0e6374d8`  
		Last Modified: Tue, 04 Nov 2025 01:39:13 GMT  
		Size: 2.1 MB (2138512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d43b4e5d6de9ea1850e5d2436fe56c8f275e871aa535af2768cd8f9b3166671`  
		Last Modified: Tue, 04 Nov 2025 01:39:18 GMT  
		Size: 14.4 MB (14400239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4433cf29c794e20ff1853ffdf89ce86f12d3ffbc574a9c03d0b4ab5f4928ea38`  
		Last Modified: Tue, 04 Nov 2025 01:39:12 GMT  
		Size: 290.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:f43ccbed65b8516536df426e6d0079915d924a1e9aa0623faae374f767f1f655
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a82695f73a6d9cb9e6bd6e81e54c59bb14b7aa98803c9848070a6494b30132c`

```dockerfile
```

-	Layers:
	-	`sha256:4109b6d6b1f6a0e98d8e67d509e9a42419e850fc7af65261f3843676480042fe`  
		Last Modified: Tue, 04 Nov 2025 09:52:55 GMT  
		Size: 2.3 MB (2296026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8a2c455ac843de1c9d846530211766d9f1cdeaf6dba916eeb031dcb81073494`  
		Last Modified: Tue, 04 Nov 2025 09:52:56 GMT  
		Size: 37.7 KB (37683 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:trixie` - linux; riscv64

```console
$ docker pull httpd@sha256:96866a20094509c8073562abadd23b91d565c0d238ad1ef945dfa094449f8148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43370770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d10d0f5701fab7a49cf8c34f061fa64e52a7ebd5e4c6c713709f696ae7d7b7d`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:54:24 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Tue, 04 Nov 2025 02:54:24 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 02:54:24 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Tue, 04 Nov 2025 02:54:24 GMT
WORKDIR /usr/local/apache2
# Tue, 04 Nov 2025 02:55:15 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:55:15 GMT
ENV HTTPD_VERSION=2.4.65
# Tue, 04 Nov 2025 02:55:15 GMT
ENV HTTPD_SHA256=58b8be97d9940ec17f7656c0c6b9f41b618aac468b894b534148e3296c53b8b3
# Tue, 04 Nov 2025 02:55:15 GMT
ENV HTTPD_PATCHES=
# Tue, 04 Nov 2025 03:18:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Tue, 04 Nov 2025 03:18:06 GMT
STOPSIGNAL SIGWINCH
# Tue, 04 Nov 2025 03:18:07 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:18:07 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 03:18:07 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca84493726f5168dd3b3a4308713587f33020b48dd781d3795f5bddb21964e3`  
		Last Modified: Tue, 04 Nov 2025 04:01:40 GMT  
		Size: 144.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f75a9c9c5fda878ccc47a33d36894cd50f9fbb52d365b0eca79678d4e8b8c64`  
		Last Modified: Tue, 04 Nov 2025 04:01:41 GMT  
		Size: 2.0 MB (1956311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7f3080d48adc8ed691434a8e66cb7dc17ace8f487fc64ef2efe12dd2c6e685`  
		Last Modified: Tue, 04 Nov 2025 05:39:08 GMT  
		Size: 13.1 MB (13138204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:792dd117ae29badd8d57394a36654bd1d2efc5556aa7b63d3c85310f4e8697dc`  
		Last Modified: Tue, 04 Nov 2025 04:01:51 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:1c5e49f532b790dd3e528e1db2978d951dfc92464dba36fb70c547324ec8570c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2323953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0a0412443fb92b1c43d4db1118ab3f5aed8b36637e95d753778891a6715382a`

```dockerfile
```

-	Layers:
	-	`sha256:fde81d27b291031765e5b326e0511e7b2a9a1af494095ad9f81fd904f94e1f80`  
		Last Modified: Tue, 04 Nov 2025 06:52:37 GMT  
		Size: 2.3 MB (2286273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98c011c8aef0e428ffeb846d1a7e1ccacaf76dafb010031fbf9022719ed43bd8`  
		Last Modified: Tue, 04 Nov 2025 06:52:38 GMT  
		Size: 37.7 KB (37680 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:trixie` - linux; s390x

```console
$ docker pull httpd@sha256:1dad5b450c22b159d4adcec12f50486e3d124fdb7424b8fc999134473906c662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45480531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf0f4dc61b27e90fc8b079bb59e20f50cec8d36d41bcd6bf30152d919436e5f`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 06:54:25 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Tue, 04 Nov 2025 06:54:25 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 06:54:25 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Tue, 04 Nov 2025 06:54:25 GMT
WORKDIR /usr/local/apache2
# Tue, 04 Nov 2025 06:54:30 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 06:54:30 GMT
ENV HTTPD_VERSION=2.4.65
# Tue, 04 Nov 2025 06:54:30 GMT
ENV HTTPD_SHA256=58b8be97d9940ec17f7656c0c6b9f41b618aac468b894b534148e3296c53b8b3
# Tue, 04 Nov 2025 06:54:30 GMT
ENV HTTPD_PATCHES=
# Tue, 04 Nov 2025 06:56:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Tue, 04 Nov 2025 06:56:29 GMT
STOPSIGNAL SIGWINCH
# Tue, 04 Nov 2025 06:56:30 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 06:56:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 04 Nov 2025 06:56:30 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b68fce4b7d02e51e6b384182c7d4d8400c5991a24b4303b96d32dd62477444`  
		Last Modified: Tue, 04 Nov 2025 06:56:47 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d85c9d0545d528da96e3ae16815803f8122ca99cbe6cd0b424f152ecd152a49`  
		Last Modified: Tue, 04 Nov 2025 06:56:48 GMT  
		Size: 2.0 MB (2036080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98eaf45f11f10e79bc24f541a7e460bc9ee0a87cde517f26c7e99156d2bd33e1`  
		Last Modified: Tue, 04 Nov 2025 06:56:50 GMT  
		Size: 13.6 MB (13606591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a034da17c55645b48b33cf860c6f5d13a25246b8b9370142be75cdc1638f44`  
		Last Modified: Tue, 04 Nov 2025 06:56:48 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:052ecb1c1c1dd6ac06a051454ff7dcf086d71c9549310c5ddf7837faf6601f5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2331195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85667fa36617065029bd6bc6599246d73c0598f6ec0f374b840def5e540134d`

```dockerfile
```

-	Layers:
	-	`sha256:3c015edafba01e78dfd3daf36c5b4eeba185f8577ac5aaf0cd4279efcae6f154`  
		Last Modified: Tue, 04 Nov 2025 09:53:03 GMT  
		Size: 2.3 MB (2293584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b5d2a5d12ee09acd36223179b5db2b11c9cdf9f33432faca0cdcb4243fbb00c`  
		Last Modified: Tue, 04 Nov 2025 09:53:04 GMT  
		Size: 37.6 KB (37611 bytes)  
		MIME: application/vnd.in-toto+json
