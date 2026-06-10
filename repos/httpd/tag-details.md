<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `httpd`

-	[`httpd:2`](#httpd2)
-	[`httpd:2-alpine`](#httpd2-alpine)
-	[`httpd:2-alpine3.24`](#httpd2-alpine324)
-	[`httpd:2-trixie`](#httpd2-trixie)
-	[`httpd:2.4`](#httpd24)
-	[`httpd:2.4-alpine`](#httpd24-alpine)
-	[`httpd:2.4-alpine3.24`](#httpd24-alpine324)
-	[`httpd:2.4-trixie`](#httpd24-trixie)
-	[`httpd:2.4.68`](#httpd2468)
-	[`httpd:2.4.68-alpine`](#httpd2468-alpine)
-	[`httpd:2.4.68-alpine3.24`](#httpd2468-alpine324)
-	[`httpd:2.4.68-trixie`](#httpd2468-trixie)
-	[`httpd:alpine`](#httpdalpine)
-	[`httpd:alpine3.24`](#httpdalpine324)
-	[`httpd:latest`](#httpdlatest)
-	[`httpd:trixie`](#httpdtrixie)

## `httpd:2`

```console
$ docker pull httpd@sha256:bda12def1dc3b718a5314b4b26ca84927fdb3905091f11200d581186f240e4f6
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

### `httpd:2` - linux; amd64

```console
$ docker pull httpd@sha256:2b7d8a7992076bf5ceb8bb363b4c8f2b8c655072e7478f45c5e537af28f6c167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45230035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb74261f37ff6970ccb87626c9783304249efaad9f4e8cd32de4e9a3423b787d`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:48 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:48 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:48 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:53 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:30:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:30:55 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:30:55 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:30:55 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:30:55 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51757aae13a97369966a219edcf9e0f9b8cc8eaec050732a5d6fa25aa92e453`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c211dc8965131703cc3952b6267904624b637fc549d23e2e6bc0cc49b4222c`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 2.0 MB (1997894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc6b5038f865e4e495fc8fe09d6f11876069a408d170c40399b49126c800041`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 13.5 MB (13451745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9e979b34b8fed3ce647410b3644cc8cc46ef92761363f08fe8802169d5f76f`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2` - unknown; unknown

```console
$ docker pull httpd@sha256:fce1019bd8cc87b008a72778b2a2736ddff548e62baa27c4cc983db009cb5111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597fd853705160154b2bcd70d98acc6933b1b6dcf3f31cb013b0abcf1068d207`

```dockerfile
```

-	Layers:
	-	`sha256:e2025809a7e3749824decea45c53ede352d4aa58d75ace93dd07000d2b6c08a6`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 2.3 MB (2292510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:492c10869e234a6f6ccfabd1a0dfc280cec64fa0e207fc564413cc8da21c9610`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 37.6 KB (37611 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2` - linux; arm variant v5

```console
$ docker pull httpd@sha256:f361c4b24b78e1239dfeacd9d9dab2c93ea638455fd3c3b70dbbda6ab00a15f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42857065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ab2c2872db9a8045fa1ab91711e556824fe075bbaca19941f6e9bd8271bc48`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:48 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:48 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:48 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:58 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:58 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:58 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:58 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:31:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:31:48 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:31:48 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:31:48 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:31:48 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8741492638bd207b4038604a6e65e467c0a410df6afca31a4821aee832c662ab`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c069dc93d7fb7eba3c5388a00541788a95bc11398d69b0c81da9efc258d2c8d`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 1.9 MB (1912804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6002f904e7facf1cc93c7790b09f0609b922e15005a489e32e61b6fbc4316ad8`  
		Last Modified: Mon, 08 Jun 2026 18:31:57 GMT  
		Size: 13.0 MB (12989920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8efcbe4a582c8775afea0836d968f1f184bea5c26e21fe0fcbb5a0e7ebd3ff05`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2` - unknown; unknown

```console
$ docker pull httpd@sha256:f2ce1a9cefdbe977111087f3b75c7be0784ea835d0007b5a145ed2f6bfa0c95b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dfbb9b9cb8c42912b42a91046224acc7dc556f1e7d8097a01121fd91f76b72`

```dockerfile
```

-	Layers:
	-	`sha256:80fc7202154b749a8075c448c7e7a9a60d1d4f341914b54da5153b7ee3c03f5f`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 2.3 MB (2295542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27e7b847f32a118618968bc07cffc9a5d6d0c0692dee15129ee923129b35c1b4`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 37.7 KB (37749 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2` - linux; arm variant v7

```console
$ docker pull httpd@sha256:5236d5c6a10645ecac76238b7ca6f921ca8eb5ea92ab6fb293bdadae95b10ae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40548022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b12f00662f2acddd392078f235516594259077bf34e4c06e06e8288f24df443`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:54 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:54 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:54 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:54 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:29:01 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:29:01 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:29:01 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:29:01 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:31:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:31:27 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:31:27 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:31:27 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:31:27 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7617084195012707e889cdef4236f6627014b19baf5baa53b8e432880268bc`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada685e6861770db8d1c2090eecdecab5e8ae6dec8c9abc23fb86d844f8bb442`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 1.8 MB (1823341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a919558fd039a1b681fc7341aeb407767fa365ac621427a2d7bf5470f9eecc9`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 12.5 MB (12518379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a44ce25dab735595c229a5d37494e00da9b3a541edbcdd85d4f3e488c4175fd`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2` - unknown; unknown

```console
$ docker pull httpd@sha256:9db1b877234f01aa36272fba11532263d7a52f145aec8d4364b98deaca6fa87b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2331805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f897acfbf506ea853c77e9a461c832030fe5a6a95cb3bf116d12f565be924b5d`

```dockerfile
```

-	Layers:
	-	`sha256:1b5b5d4bbe67bc086194dd58eb01ec30a9bf78e7498afd570946311fcc5bbb5a`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 2.3 MB (2294057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d14fc4d73d1b623729ae4e87803dc741f0309a1a9e8d3661bd235890bb441fa`  
		Last Modified: Mon, 08 Jun 2026 18:31:35 GMT  
		Size: 37.7 KB (37748 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:05f92a0b3df99246bd094967c40d5f00311b04b74e91386ab37f3879d5b6398f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45500798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab09468e72a3fd55b26758d03ba2f8a094a6de075771c949ee820cd22f4efd4`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:48 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:48 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:48 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:53 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:30:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:30:55 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:30:55 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:30:55 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:30:55 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51757aae13a97369966a219edcf9e0f9b8cc8eaec050732a5d6fa25aa92e453`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbc1d9c94781b6fb204e9f2dd48fa707b639991a0ed9e6832bc627ee78eb793`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 2.0 MB (1971344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1897ad34a45ba49cd3bd04d81eb169b2fa80642c8bdeb1783ba8067376d69911`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 13.4 MB (13387063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8048fc63017cda60558664fdef734dbe334a9ef8bb646c61060a28ea79cc2c73`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2` - unknown; unknown

```console
$ docker pull httpd@sha256:77551cd106fe5e6dba8ab22968dcc1c2157130fb9d1ce1f165884126ef2ff11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e103ca667e4eca8f7df1a1a1760fe83de402a3064636034eca87b9551b8abeac`

```dockerfile
```

-	Layers:
	-	`sha256:9983bb17dc86db43f7ba9dfb576ff96e6213f15e4868de93bd9ac8b5b38533a0`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 2.3 MB (2292847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d696410da2eb0504c27136882e9ac61fe5c021897524d3583611c2d09de3a6ca`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 37.8 KB (37793 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2` - linux; 386

```console
$ docker pull httpd@sha256:d212f60d1de6a98f8ac5666c0f08cfb2f8d7e69c007bba602a46c8f59d8c4346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46572612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a675fd0fcf287e70a1c2a01d7ad90a4f9db4df857ba19faf767c6dd59fc412`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:49 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:49 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:49 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:49 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:55 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:55 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:55 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:55 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:31:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:31:06 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:31:06 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:31:06 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:31:06 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3f98973d06c4dd876d5ba79c06211d3cd1cea32db869157acf4434836e75b5`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82349a6b654d1e29b5f624fa403272758a3418fe2d7860fc0f98cecee1da801b`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 2.1 MB (2055642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d9f1f37b024e8db99b29e69ec67af1bc894362b189a8cce9327b62ba4c0ff8`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 13.2 MB (13221163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6acaba897604b124ab0b4b16b6083da00590bfa6de43cb198468a35afbc076`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2` - unknown; unknown

```console
$ docker pull httpd@sha256:af18d97787c89c98c8fc110c23887ed1e760fb3f9207c6089ead4f50f78ceba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2327164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a81fe9a487688b93159da3a042732411446e801c6adf453f8f6a9878133adf`

```dockerfile
```

-	Layers:
	-	`sha256:fafa740c092dc2c2d150c0a3988c531e569690a6361dd41d57a1faec9324d3e4`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 2.3 MB (2289609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c62eb654a7ce8c3c1529835aa36c0de0488098dd817dd2b7968f541c9be78d7b`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 37.6 KB (37555 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2` - linux; ppc64le

```console
$ docker pull httpd@sha256:23250993ffdf8415ee5424cdeff8f5dff52a26bff21436f6567a702b755c8cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50163250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e58559fc8be957d33533107f22829d2774b9656a856245cd16510b077a31578`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:27:34 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:27:34 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:27:34 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:27:34 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:27:48 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:27:48 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:27:48 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:27:48 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:32:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:32:03 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:32:03 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:32:03 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:32:03 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095b49d3ed9c5bd684106ef2762c8c8d6c733b6154e0f88da03b1e1966cd01df`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc91076ec4b38e804c65780f529812ce414a153e095f9380d5804984cbd9f76`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 2.1 MB (2138540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164efcce54726bc397834f6038e70f0f535de3989d1fae4a14d3ce829e318c63`  
		Last Modified: Mon, 08 Jun 2026 18:32:18 GMT  
		Size: 14.4 MB (14423785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965f08e1a921c3b4cbb9f84c6b9999ea0cc8c5df7c7ccac77ea6fd7ee24189af`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2` - unknown; unknown

```console
$ docker pull httpd@sha256:7984379d541bad6433c6840f03d5a6bf3717cc96a23a6494d8edf4f56ff068c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fdcdd51ba0de4af51f758f1a67800b27772d0b16fc1acac13a6aa87399a87e`

```dockerfile
```

-	Layers:
	-	`sha256:8a0d0e0c231ec528ec3d98a2c72ca9b7759110af04cd9392138cbfeaf1d67dc9`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 2.3 MB (2296360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa23dd30e1d59efae1e2d867d4f568fe9d993722b873f57fa8d68feb138933c7`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 37.7 KB (37682 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2` - linux; riscv64

```console
$ docker pull httpd@sha256:71876f06ab63bc1cf873ca7c7087faea82688f408c32b0224b7cb29aab33e4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43402754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75069b5306a498c987ffa1263618f82a1a44ddc86f83c3e6bde1350c1a246af6`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:27:50 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:27:50 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:27:50 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:27:50 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:42 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:42 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:42 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:42 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:51:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:51:09 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:51:09 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:51:09 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:51:09 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcb14ecded12a6ddea9368e3e0a89b321a0babb977a900740f77d9b2749c881`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6acad9c2eb5d55c394bbd6a1a2e6dc884a8bd713db7c37cd33e0deeaab271b`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 2.0 MB (1956437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691748d99998bcadae01e53818c1a0ba95d0e2ba99b846f20043d5e854281021`  
		Last Modified: Mon, 08 Jun 2026 18:52:16 GMT  
		Size: 13.2 MB (13168247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1562e123a42b9956e7d39d32f9976df80d047f431caf3c4862e78d656b7e2b7e`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2` - unknown; unknown

```console
$ docker pull httpd@sha256:fa7de91aad897f1d9eaccd4e5213a25fb802222959c9f6c423886b4fb608fa8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2324290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e51d58413798f790228b33455088967cc44329474f1c5a0c94252c4d78a9a3`

```dockerfile
```

-	Layers:
	-	`sha256:9e13f24a27b58524719240f6484550131917ee8131886a36995d67d99f36a8cc`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 2.3 MB (2286607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30c4e22ef528cabad294d53b578ccf49631760a5a1caf405303bb050958ad5df`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 37.7 KB (37683 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2` - linux; s390x

```console
$ docker pull httpd@sha256:2fa1944efe68dc19bf36d54e72ec18be919399545609955907759c62eef32556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45520012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6084b5dadfb37c1564dd4b7e44b3a1e4a405039e5715c0f39c241c50aaf0367b`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:27:38 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:27:38 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:27:38 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:27:38 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:27:44 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:27:44 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:27:44 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:27:44 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:29:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:29:45 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:29:45 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:29:45 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:29:45 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a516c95daee50c3e7a6296f522dd4fb560f14d2ca73476e1dafa47cde6b081b3`  
		Last Modified: Mon, 08 Jun 2026 18:29:57 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ffc60f849aa2b0a9016137736b47502e247d91bf7d8bdb0af208d49a528576`  
		Last Modified: Mon, 08 Jun 2026 18:29:58 GMT  
		Size: 2.0 MB (2036546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f468bbb1ef751e92d67c77000d3af1de92fc265b1a2b4e1cbb62ada60425a6`  
		Last Modified: Mon, 08 Jun 2026 18:29:58 GMT  
		Size: 13.6 MB (13637070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30130f264687b48d7a0583772d74472381b1bddbf747faebcfad8fb79fec2160`  
		Last Modified: Mon, 08 Jun 2026 18:29:57 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2` - unknown; unknown

```console
$ docker pull httpd@sha256:a2f39309c230b1b17f2d4ddc53dd8c639603464ac50ea2a0b5e711225deaa4d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2331529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e8052bca557af655c176e8eec1e6ba8355618d3fa1333efab780db0eba9e1a`

```dockerfile
```

-	Layers:
	-	`sha256:0ec2b032ffb696485fe5fd2a728ef8da7d25712bb8327e496cd8643a40c8d333`  
		Last Modified: Mon, 08 Jun 2026 18:29:58 GMT  
		Size: 2.3 MB (2293918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18e3f08e0e7176d1ce05b52cfd66efa801891a3146c7bafe1e0a1034b73df332`  
		Last Modified: Mon, 08 Jun 2026 18:29:58 GMT  
		Size: 37.6 KB (37611 bytes)  
		MIME: application/vnd.in-toto+json

## `httpd:2-alpine`

```console
$ docker pull httpd@sha256:4a15e9c73f25334bc03cfb3c692c9adfc103bb46ca89cee1f0b9a5fcbc7b21f6
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

### `httpd:2-alpine` - linux; amd64

```console
$ docker pull httpd@sha256:bf087a7b1abe6bed280d6a69dcc3c8f17055bff4d86e8b52423c7ca52dbf1103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20742245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bdbd06577ba009805166768103f9a62685d9f97a9884b54388b1fa4bea9ecdd`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 18:31:25 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Jun 2026 18:31:25 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:31:25 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:31:25 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:31:25 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:31:26 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 08 Jun 2026 18:31:26 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:31:26 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:31:26 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:32:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:32:30 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:32:30 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:32:30 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:32:30 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce5804151ace48b62ad76238cde0765d43efa9396f491d9ec2d59b41a4fa8e1`  
		Last Modified: Mon, 08 Jun 2026 18:32:37 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db356f236e7a97cfe205045ad2895819d2fe9beecb1a8bd65fae6929cc6115a1`  
		Last Modified: Mon, 08 Jun 2026 18:32:37 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc5e0e38d81ae69af4435b5d5a5be213645e9c40200ddab1281a71efec26d94`  
		Last Modified: Mon, 08 Jun 2026 18:32:37 GMT  
		Size: 11.1 MB (11066958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af2e4b44c0574322eab72595901d051fdfd3dee1524b5d0f9177ecd7953cdc0`  
		Last Modified: Mon, 08 Jun 2026 18:32:37 GMT  
		Size: 5.8 MB (5809700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86856eeef9e12dbdc8ff4c7baebbd5cdefe872848eaf6ef2aef50eced2e7bd0e`  
		Last Modified: Mon, 08 Jun 2026 18:32:38 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:70c3c56d3d003dfac3b02abe58445b9d05b65eb48d2caf76a2aae4f16d351c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1239812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2a862ab34194b98abe1ad90fb1158234040d57fa2471ca197496507a8194920`

```dockerfile
```

-	Layers:
	-	`sha256:84e23f6554b8259dbd70956df3da92e26511e07ad4412a2a0a648cc51f4f4e78`  
		Last Modified: Mon, 08 Jun 2026 18:32:37 GMT  
		Size: 1.2 MB (1201606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc8b38586c1d8780912c3f004220df6b7649ed5c47efa43fa068ee9662f47caa`  
		Last Modified: Mon, 08 Jun 2026 18:32:36 GMT  
		Size: 38.2 KB (38206 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-alpine` - linux; arm variant v6

```console
$ docker pull httpd@sha256:024536b397c6ad22fa335218e0fb10fd1206c9fdb71dd7448c4f4f7fe16a8bc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19530438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979e382592d01f76ea45774429a342ecc5edef3ae3f0cdb9f569403603dd1cda`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 18:28:46 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Jun 2026 18:28:46 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:46 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:46 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:46 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:48 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:30:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:30:08 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:30:08 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:30:08 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:30:08 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8321b554dfa7c63a2afd55c8fb184b69858f457e8dfa9880f4bc448d8a39d4`  
		Last Modified: Mon, 08 Jun 2026 18:30:13 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09a332d4df7c9bee48b2d2de86966f85e36b64798eaaf67de0975e4f1555f89`  
		Last Modified: Mon, 08 Jun 2026 18:30:13 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215e98f908ff76704a82ca9d04a502bc930ce17a9047820920844edfd57fa760`  
		Last Modified: Mon, 08 Jun 2026 18:30:14 GMT  
		Size: 10.3 MB (10286319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ee63e2411212cd08a883b8c84dc993798a84b4de02db32551ee900d921c95e`  
		Last Modified: Mon, 08 Jun 2026 18:30:14 GMT  
		Size: 5.7 MB (5670856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e101d519540f8c8be21ad616e63d9f66a84ae618343405938dddad8bdeae5f6`  
		Last Modified: Mon, 08 Jun 2026 18:30:15 GMT  
		Size: 289.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:fc8f3318e4ab42107e49368c4f569a975957bd9af2efab2cec507177830cda11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb4db6d5f35a09c872dde41878646504db7ebdfdc3744e4f6986726e057c671`

```dockerfile
```

-	Layers:
	-	`sha256:6e8897e1452670de76c435a27c21f0d31afad8b78d64fa84fdaffa8c052e60a6`  
		Last Modified: Mon, 08 Jun 2026 18:30:13 GMT  
		Size: 38.1 KB (38142 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-alpine` - linux; arm variant v7

```console
$ docker pull httpd@sha256:8061dc7af76065401d58b4b0517719208ee34c8923c83d30cffdd47abc0aa401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18701347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aab2fe87d7e0e05ed925969046f55ddf1ef27740b6067ba4161f1928c96e254`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 18:30:37 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Jun 2026 18:30:37 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:30:37 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:30:37 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:30:37 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:30:39 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 08 Jun 2026 18:30:39 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:30:39 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:30:39 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:31:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:31:55 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:31:55 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:31:55 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:31:55 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ad8e36bc25e31e63d7c1a292ea9f35a3df589ad01be37b48a4ac3ae9fc0847`  
		Last Modified: Mon, 08 Jun 2026 18:32:01 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfec7351aad4a1810cd117ec6fda31c0b8b9af893f2d6755fe6e474e5edc16a`  
		Last Modified: Mon, 08 Jun 2026 18:32:01 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89db8edd72fdbfd84fe9a186dbe1fa7539829347879a957a070d49ccc276ef92`  
		Last Modified: Mon, 08 Jun 2026 18:32:02 GMT  
		Size: 10.1 MB (10062859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7c853cb79a0e47b775a4cb5ed20a4fa1f0fa54a2a4a8fc43c5e2c52e10a4dd`  
		Last Modified: Mon, 08 Jun 2026 18:32:02 GMT  
		Size: 5.4 MB (5353967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4dfbc2ff27845415d637069fa7548a00c66b9364660c093067578b62d6d650`  
		Last Modified: Mon, 08 Jun 2026 18:32:03 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:9d340e705b4d2d4d5357cabee9b78bdebcd67b0dc92a2435cc1e019af5338324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1242371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53499d0e69d22627cf589b7d2118279c706b905969b2b30fe01ebd143120c86c`

```dockerfile
```

-	Layers:
	-	`sha256:a78794fe77e35b91f4ccad718d8777e6c1c5cd52d6a272f4cd53482c4a88cdda`  
		Last Modified: Mon, 08 Jun 2026 18:32:02 GMT  
		Size: 1.2 MB (1204014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e1fe4c2a693f67e2ff7c45c79009d14ddf8c3005f4b3747c700d1530f9d7fe6`  
		Last Modified: Mon, 08 Jun 2026 18:32:01 GMT  
		Size: 38.4 KB (38357 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-alpine` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:85b4776185fbee81f2ccf80b645c10d5d2a5eadc8004a038d38784682f667ffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21163903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d2c617afd2009094a1862af906977d4bd5a6a9fcfc1ef8cb27061905000692`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 18:30:27 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Jun 2026 18:30:27 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:30:27 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:30:27 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:30:27 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:30:28 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 08 Jun 2026 18:30:28 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:30:28 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:30:28 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:31:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:31:36 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:31:36 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:31:36 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:31:36 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2733de7154d76386a001a868473ab506efdc9813265b2e519d49513c0c0ca4c4`  
		Last Modified: Mon, 08 Jun 2026 18:31:43 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a593c24a6a1b8072f379a89d7870d2df90bb18d23f56ac71aee739dfe20489ec`  
		Last Modified: Mon, 08 Jun 2026 18:31:43 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b0d2c4d83de418eef5171c3593da6a8e7caa221b1af072d6936c20d6b74a25`  
		Last Modified: Mon, 08 Jun 2026 18:31:44 GMT  
		Size: 11.0 MB (11034000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa7baf1e3c92a7533ea08f8fdd39cd5280b65628d1c6c62793565d5e1743a6f`  
		Last Modified: Mon, 08 Jun 2026 18:31:44 GMT  
		Size: 5.9 MB (5928633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3ca4765694b549352106668014c1d542f93d13adf1f177a9a956461ed5492c`  
		Last Modified: Mon, 08 Jun 2026 18:31:44 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:4af10a58bed505a14c1108a84db0aaa27d666395366e84db3677085d87d207df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1239463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0f41e9cde0dc8d8ccf71126bd2f783f7f8231c70316ba7fe767a9230fa4bb8`

```dockerfile
```

-	Layers:
	-	`sha256:13468312a748d8b51aaf3a82ad0f3271775ef5301c38d37fbd6196359c20d00a`  
		Last Modified: Mon, 08 Jun 2026 18:31:44 GMT  
		Size: 1.2 MB (1201060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1470375ebacc02386973357f8aab79e0f87c8d365f1ff6dbcdb17779e96c813b`  
		Last Modified: Mon, 08 Jun 2026 18:31:43 GMT  
		Size: 38.4 KB (38403 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-alpine` - linux; 386

```console
$ docker pull httpd@sha256:16b1c94bd801f2d8832b0683f76414905177be78ab8e40a633e7ec0890433857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (20021926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c38ed0bd74cceb6792e9d929d312d54bc80e7cde0e19948ffd46cb48f7ab757`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 18:31:21 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Jun 2026 18:31:21 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:31:21 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:31:21 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:31:21 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:31:23 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 08 Jun 2026 18:31:23 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:31:23 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:31:23 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:32:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:32:39 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:32:39 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:32:39 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:32:39 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056f17e7b6ddfb0a1da905574c6263028f20b340ff9666ae47cfa26135676670`  
		Last Modified: Mon, 08 Jun 2026 18:32:46 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21afa337e01a5d443d84b004f17c160335eb4219e04af1e9c70ceb3707efbce0`  
		Last Modified: Mon, 08 Jun 2026 18:32:46 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbfae095ca14e5295651305f917acc6f71a2fbd5f49b85a3fc2c57e03b2be3d`  
		Last Modified: Mon, 08 Jun 2026 18:32:46 GMT  
		Size: 10.6 MB (10618085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc33c24b7089af8156a61a652ed7c5fe322baa0d78dcb691295bb589a0de453`  
		Last Modified: Mon, 08 Jun 2026 18:32:46 GMT  
		Size: 5.7 MB (5711996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b50c0cd8edcb1ed19a9637f074a4770f9a6f876606cae56220092e6243e576`  
		Last Modified: Mon, 08 Jun 2026 18:32:47 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:740f2dd920cb4f5bedec74d3f44ed0b9c47bf46d2e8b0b13557276827bcdc52e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1239709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f14334929789a57deae0012f30aba319525e7ff989e36134d070c56a6dd94dc`

```dockerfile
```

-	Layers:
	-	`sha256:d0dacd457b618139c482a7d6afa2041ffd6cb707e33b66acf044aaefaa14397e`  
		Last Modified: Mon, 08 Jun 2026 18:32:46 GMT  
		Size: 1.2 MB (1201561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44183710a388aa4b94ef6d14e896b787a7e08a8f608a9c14d36001d21668c987`  
		Last Modified: Mon, 08 Jun 2026 18:32:46 GMT  
		Size: 38.1 KB (38148 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-alpine` - linux; ppc64le

```console
$ docker pull httpd@sha256:24c446eba8c10efd7206d9e55e728f1787228d1442aa6ef61ac7a0d515cce4ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21381418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a448835add6f4d91f1982c6a872fe649b29ed77425b2e9e5aa901dd5e301205f`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 18:27:34 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Jun 2026 18:27:34 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:27:34 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:27:34 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:27:35 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:27:38 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 08 Jun 2026 18:27:38 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:27:38 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:27:38 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:29:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:29:29 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:29:29 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:29:29 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:29:29 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3833350820ce2613df1f0a4261df6ce7bc4951ba5dba44ef1a833641790aaaa`  
		Last Modified: Mon, 08 Jun 2026 18:29:47 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e9193af3a9c4cd580ff4cb24c30058cbec15dd6378f5950513a68c769c281f`  
		Last Modified: Mon, 08 Jun 2026 18:29:47 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a872efdd830ec45ac7efd740e333bf2cb140e2f4b94e60dd878415304be4b613`  
		Last Modified: Mon, 08 Jun 2026 18:29:47 GMT  
		Size: 11.3 MB (11338111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7513aa3438c9c2feecadf91e523239d954d60ceddaeda0f6e6763e2235eb9d35`  
		Last Modified: Mon, 08 Jun 2026 18:29:47 GMT  
		Size: 6.2 MB (6210978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47983e84280f04dea9f420f8879dc16efab9198e05c7c6d79eae3fe957261a48`  
		Last Modified: Mon, 08 Jun 2026 18:29:48 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:17e67c7acec63724871964de2c8a364fb31631efd6f458ddd90235490b789f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1239293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77c39681778c5b28492be2b18b099ed022a8b09c86791dd235685cbc511448b`

```dockerfile
```

-	Layers:
	-	`sha256:aa63ded6d68a8c82088e414a0d5b803f2cf467747fc6fe33326dd7f4a8ff1d61`  
		Last Modified: Mon, 08 Jun 2026 18:29:47 GMT  
		Size: 1.2 MB (1201013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:772db10801a309da7fa867f9755115f0e7af393467440d9c2ba6a20824bfd7a0`  
		Last Modified: Mon, 08 Jun 2026 18:29:47 GMT  
		Size: 38.3 KB (38280 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-alpine` - linux; riscv64

```console
$ docker pull httpd@sha256:6e901fc55fc925beed4d9e227553864af8d4da401692c898b3ba5d6198aa89e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19923429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94d1b25cfd3edbe24497157b752ff6f1b0bae2216ac56a9695500c96025ef0d8`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 18:52:56 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Jun 2026 18:52:56 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:52:56 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:52:56 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:52:57 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:53:04 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 08 Jun 2026 18:53:04 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:53:04 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:53:04 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 19:03:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 08 Jun 2026 19:03:07 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 19:03:07 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 19:03:07 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 19:03:07 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19c7f0762250b0cc52b39bb993e944c7a467ccbba9e5982b3e05a892ed00e09`  
		Last Modified: Mon, 08 Jun 2026 19:03:57 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948f4b41e7172c5b397872ec12028b50e89c8b1945bcdd382f3c4354d3816a6c`  
		Last Modified: Mon, 08 Jun 2026 19:03:57 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839bf3cd8868f427bc3edaf740a5070b32162d92911d6135ad7452faf74806e2`  
		Last Modified: Mon, 08 Jun 2026 19:04:00 GMT  
		Size: 10.5 MB (10512864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0ed49d6165d488e835183bba68a905603e14ef7c9d532d89556389e587cdb6`  
		Last Modified: Mon, 08 Jun 2026 19:03:59 GMT  
		Size: 5.8 MB (5821504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9212c34deb579c5504ab192148ff204061b0646ae26b63cc9ad5ed1aad1789c`  
		Last Modified: Mon, 08 Jun 2026 19:03:59 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:536fbac1930d7f288da7460218490b036b05488c57b17e046817cfca2d991009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1239289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63060237e36817f0674dfd5a4486b1ecb06b72e44a91033e3d2fc30181462368`

```dockerfile
```

-	Layers:
	-	`sha256:106695ede26a0f693625ca363327da8a1cf3bbdf11f35f67bf2ed2a8b03aa116`  
		Last Modified: Mon, 08 Jun 2026 19:03:58 GMT  
		Size: 1.2 MB (1201009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efd7b10cf0eb8a6248093104323312312d5e4f5d818a591a147f6a252df1d07d`  
		Last Modified: Mon, 08 Jun 2026 19:03:58 GMT  
		Size: 38.3 KB (38280 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-alpine` - linux; s390x

```console
$ docker pull httpd@sha256:6283359189b28f3ca4b868bf776ceb2b692e4add8fea4a8b3269d66b7753a935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21378874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2df8884703c6d4ccc1f8733cfd8210fb8eb0924b8b0b633ac84af6641b17fbd`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 18:27:38 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Jun 2026 18:27:38 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:27:38 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:27:38 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:27:38 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:27:40 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 08 Jun 2026 18:27:40 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:27:40 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:27:40 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:28:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:28:46 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:28:46 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:28:46 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:28:46 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548235140cb8c1ab10d4692027815816cc2544f4ec8835eba3f51db5727af171`  
		Last Modified: Mon, 08 Jun 2026 18:28:59 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369bc1e79711eb6126c37a7b565cc2b0f42d4ee767040a1f8b44f857f5adef9a`  
		Last Modified: Mon, 08 Jun 2026 18:28:59 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59e8a1afdfdaee57b84923042e279cf1dc1f97d76646bf9caebc7a940d504ca`  
		Last Modified: Mon, 08 Jun 2026 18:28:59 GMT  
		Size: 11.6 MB (11649300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138c5a50960e95cfc40f091bc4080b810eb24455ad217b422125a22d86f5284d`  
		Last Modified: Mon, 08 Jun 2026 18:28:59 GMT  
		Size: 6.0 MB (6001640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c831663f14f23188df97e6b051c05bf1da28f9a4c18fc2c2cad0bdaff1429eb`  
		Last Modified: Mon, 08 Jun 2026 18:29:00 GMT  
		Size: 289.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:5cc2f04b98cd0e537a6eb5f791971f720a637c2255c7f4758ec7d5e301ba4612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1239161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8474478033f363a3cbf719bfac24a8e06adef6eccc522a4b3c2748dda664f13`

```dockerfile
```

-	Layers:
	-	`sha256:0b586450d6cc931e529e0fe9520eca240e9996721ea62991acd52c3c73de9ee9`  
		Last Modified: Mon, 08 Jun 2026 18:28:59 GMT  
		Size: 1.2 MB (1200955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d691c6da1d20a4d1e620abc97c146c35e966efbc00988d6f0d5c0941364e3a49`  
		Last Modified: Mon, 08 Jun 2026 18:28:58 GMT  
		Size: 38.2 KB (38206 bytes)  
		MIME: application/vnd.in-toto+json

## `httpd:2-alpine3.24`

**does not exist** (yet?)

## `httpd:2-trixie`

```console
$ docker pull httpd@sha256:bda12def1dc3b718a5314b4b26ca84927fdb3905091f11200d581186f240e4f6
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

### `httpd:2-trixie` - linux; amd64

```console
$ docker pull httpd@sha256:2b7d8a7992076bf5ceb8bb363b4c8f2b8c655072e7478f45c5e537af28f6c167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45230035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb74261f37ff6970ccb87626c9783304249efaad9f4e8cd32de4e9a3423b787d`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:48 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:48 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:48 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:53 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:30:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:30:55 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:30:55 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:30:55 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:30:55 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51757aae13a97369966a219edcf9e0f9b8cc8eaec050732a5d6fa25aa92e453`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c211dc8965131703cc3952b6267904624b637fc549d23e2e6bc0cc49b4222c`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 2.0 MB (1997894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc6b5038f865e4e495fc8fe09d6f11876069a408d170c40399b49126c800041`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 13.5 MB (13451745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9e979b34b8fed3ce647410b3644cc8cc46ef92761363f08fe8802169d5f76f`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:fce1019bd8cc87b008a72778b2a2736ddff548e62baa27c4cc983db009cb5111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597fd853705160154b2bcd70d98acc6933b1b6dcf3f31cb013b0abcf1068d207`

```dockerfile
```

-	Layers:
	-	`sha256:e2025809a7e3749824decea45c53ede352d4aa58d75ace93dd07000d2b6c08a6`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 2.3 MB (2292510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:492c10869e234a6f6ccfabd1a0dfc280cec64fa0e207fc564413cc8da21c9610`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 37.6 KB (37611 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-trixie` - linux; arm variant v5

```console
$ docker pull httpd@sha256:f361c4b24b78e1239dfeacd9d9dab2c93ea638455fd3c3b70dbbda6ab00a15f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42857065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ab2c2872db9a8045fa1ab91711e556824fe075bbaca19941f6e9bd8271bc48`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:48 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:48 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:48 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:58 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:58 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:58 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:58 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:31:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:31:48 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:31:48 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:31:48 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:31:48 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8741492638bd207b4038604a6e65e467c0a410df6afca31a4821aee832c662ab`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c069dc93d7fb7eba3c5388a00541788a95bc11398d69b0c81da9efc258d2c8d`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 1.9 MB (1912804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6002f904e7facf1cc93c7790b09f0609b922e15005a489e32e61b6fbc4316ad8`  
		Last Modified: Mon, 08 Jun 2026 18:31:57 GMT  
		Size: 13.0 MB (12989920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8efcbe4a582c8775afea0836d968f1f184bea5c26e21fe0fcbb5a0e7ebd3ff05`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:f2ce1a9cefdbe977111087f3b75c7be0784ea835d0007b5a145ed2f6bfa0c95b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dfbb9b9cb8c42912b42a91046224acc7dc556f1e7d8097a01121fd91f76b72`

```dockerfile
```

-	Layers:
	-	`sha256:80fc7202154b749a8075c448c7e7a9a60d1d4f341914b54da5153b7ee3c03f5f`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 2.3 MB (2295542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27e7b847f32a118618968bc07cffc9a5d6d0c0692dee15129ee923129b35c1b4`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 37.7 KB (37749 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-trixie` - linux; arm variant v7

```console
$ docker pull httpd@sha256:5236d5c6a10645ecac76238b7ca6f921ca8eb5ea92ab6fb293bdadae95b10ae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40548022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b12f00662f2acddd392078f235516594259077bf34e4c06e06e8288f24df443`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:54 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:54 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:54 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:54 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:29:01 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:29:01 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:29:01 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:29:01 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:31:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:31:27 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:31:27 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:31:27 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:31:27 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7617084195012707e889cdef4236f6627014b19baf5baa53b8e432880268bc`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada685e6861770db8d1c2090eecdecab5e8ae6dec8c9abc23fb86d844f8bb442`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 1.8 MB (1823341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a919558fd039a1b681fc7341aeb407767fa365ac621427a2d7bf5470f9eecc9`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 12.5 MB (12518379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a44ce25dab735595c229a5d37494e00da9b3a541edbcdd85d4f3e488c4175fd`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:9db1b877234f01aa36272fba11532263d7a52f145aec8d4364b98deaca6fa87b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2331805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f897acfbf506ea853c77e9a461c832030fe5a6a95cb3bf116d12f565be924b5d`

```dockerfile
```

-	Layers:
	-	`sha256:1b5b5d4bbe67bc086194dd58eb01ec30a9bf78e7498afd570946311fcc5bbb5a`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 2.3 MB (2294057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d14fc4d73d1b623729ae4e87803dc741f0309a1a9e8d3661bd235890bb441fa`  
		Last Modified: Mon, 08 Jun 2026 18:31:35 GMT  
		Size: 37.7 KB (37748 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-trixie` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:05f92a0b3df99246bd094967c40d5f00311b04b74e91386ab37f3879d5b6398f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45500798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab09468e72a3fd55b26758d03ba2f8a094a6de075771c949ee820cd22f4efd4`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:48 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:48 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:48 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:53 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:30:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:30:55 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:30:55 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:30:55 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:30:55 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51757aae13a97369966a219edcf9e0f9b8cc8eaec050732a5d6fa25aa92e453`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbc1d9c94781b6fb204e9f2dd48fa707b639991a0ed9e6832bc627ee78eb793`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 2.0 MB (1971344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1897ad34a45ba49cd3bd04d81eb169b2fa80642c8bdeb1783ba8067376d69911`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 13.4 MB (13387063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8048fc63017cda60558664fdef734dbe334a9ef8bb646c61060a28ea79cc2c73`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:77551cd106fe5e6dba8ab22968dcc1c2157130fb9d1ce1f165884126ef2ff11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e103ca667e4eca8f7df1a1a1760fe83de402a3064636034eca87b9551b8abeac`

```dockerfile
```

-	Layers:
	-	`sha256:9983bb17dc86db43f7ba9dfb576ff96e6213f15e4868de93bd9ac8b5b38533a0`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 2.3 MB (2292847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d696410da2eb0504c27136882e9ac61fe5c021897524d3583611c2d09de3a6ca`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 37.8 KB (37793 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-trixie` - linux; 386

```console
$ docker pull httpd@sha256:d212f60d1de6a98f8ac5666c0f08cfb2f8d7e69c007bba602a46c8f59d8c4346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46572612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a675fd0fcf287e70a1c2a01d7ad90a4f9db4df857ba19faf767c6dd59fc412`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:49 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:49 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:49 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:49 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:55 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:55 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:55 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:55 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:31:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:31:06 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:31:06 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:31:06 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:31:06 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3f98973d06c4dd876d5ba79c06211d3cd1cea32db869157acf4434836e75b5`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82349a6b654d1e29b5f624fa403272758a3418fe2d7860fc0f98cecee1da801b`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 2.1 MB (2055642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d9f1f37b024e8db99b29e69ec67af1bc894362b189a8cce9327b62ba4c0ff8`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 13.2 MB (13221163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6acaba897604b124ab0b4b16b6083da00590bfa6de43cb198468a35afbc076`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:af18d97787c89c98c8fc110c23887ed1e760fb3f9207c6089ead4f50f78ceba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2327164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a81fe9a487688b93159da3a042732411446e801c6adf453f8f6a9878133adf`

```dockerfile
```

-	Layers:
	-	`sha256:fafa740c092dc2c2d150c0a3988c531e569690a6361dd41d57a1faec9324d3e4`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 2.3 MB (2289609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c62eb654a7ce8c3c1529835aa36c0de0488098dd817dd2b7968f541c9be78d7b`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 37.6 KB (37555 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-trixie` - linux; ppc64le

```console
$ docker pull httpd@sha256:23250993ffdf8415ee5424cdeff8f5dff52a26bff21436f6567a702b755c8cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50163250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e58559fc8be957d33533107f22829d2774b9656a856245cd16510b077a31578`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:27:34 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:27:34 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:27:34 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:27:34 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:27:48 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:27:48 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:27:48 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:27:48 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:32:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:32:03 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:32:03 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:32:03 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:32:03 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095b49d3ed9c5bd684106ef2762c8c8d6c733b6154e0f88da03b1e1966cd01df`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc91076ec4b38e804c65780f529812ce414a153e095f9380d5804984cbd9f76`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 2.1 MB (2138540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164efcce54726bc397834f6038e70f0f535de3989d1fae4a14d3ce829e318c63`  
		Last Modified: Mon, 08 Jun 2026 18:32:18 GMT  
		Size: 14.4 MB (14423785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965f08e1a921c3b4cbb9f84c6b9999ea0cc8c5df7c7ccac77ea6fd7ee24189af`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:7984379d541bad6433c6840f03d5a6bf3717cc96a23a6494d8edf4f56ff068c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fdcdd51ba0de4af51f758f1a67800b27772d0b16fc1acac13a6aa87399a87e`

```dockerfile
```

-	Layers:
	-	`sha256:8a0d0e0c231ec528ec3d98a2c72ca9b7759110af04cd9392138cbfeaf1d67dc9`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 2.3 MB (2296360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa23dd30e1d59efae1e2d867d4f568fe9d993722b873f57fa8d68feb138933c7`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 37.7 KB (37682 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-trixie` - linux; riscv64

```console
$ docker pull httpd@sha256:71876f06ab63bc1cf873ca7c7087faea82688f408c32b0224b7cb29aab33e4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43402754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75069b5306a498c987ffa1263618f82a1a44ddc86f83c3e6bde1350c1a246af6`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:27:50 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:27:50 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:27:50 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:27:50 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:42 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:42 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:42 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:42 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:51:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:51:09 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:51:09 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:51:09 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:51:09 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcb14ecded12a6ddea9368e3e0a89b321a0babb977a900740f77d9b2749c881`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6acad9c2eb5d55c394bbd6a1a2e6dc884a8bd713db7c37cd33e0deeaab271b`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 2.0 MB (1956437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691748d99998bcadae01e53818c1a0ba95d0e2ba99b846f20043d5e854281021`  
		Last Modified: Mon, 08 Jun 2026 18:52:16 GMT  
		Size: 13.2 MB (13168247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1562e123a42b9956e7d39d32f9976df80d047f431caf3c4862e78d656b7e2b7e`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:fa7de91aad897f1d9eaccd4e5213a25fb802222959c9f6c423886b4fb608fa8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2324290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e51d58413798f790228b33455088967cc44329474f1c5a0c94252c4d78a9a3`

```dockerfile
```

-	Layers:
	-	`sha256:9e13f24a27b58524719240f6484550131917ee8131886a36995d67d99f36a8cc`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 2.3 MB (2286607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30c4e22ef528cabad294d53b578ccf49631760a5a1caf405303bb050958ad5df`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 37.7 KB (37683 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-trixie` - linux; s390x

```console
$ docker pull httpd@sha256:2fa1944efe68dc19bf36d54e72ec18be919399545609955907759c62eef32556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45520012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6084b5dadfb37c1564dd4b7e44b3a1e4a405039e5715c0f39c241c50aaf0367b`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:27:38 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:27:38 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:27:38 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:27:38 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:27:44 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:27:44 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:27:44 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:27:44 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:29:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:29:45 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:29:45 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:29:45 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:29:45 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a516c95daee50c3e7a6296f522dd4fb560f14d2ca73476e1dafa47cde6b081b3`  
		Last Modified: Mon, 08 Jun 2026 18:29:57 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ffc60f849aa2b0a9016137736b47502e247d91bf7d8bdb0af208d49a528576`  
		Last Modified: Mon, 08 Jun 2026 18:29:58 GMT  
		Size: 2.0 MB (2036546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f468bbb1ef751e92d67c77000d3af1de92fc265b1a2b4e1cbb62ada60425a6`  
		Last Modified: Mon, 08 Jun 2026 18:29:58 GMT  
		Size: 13.6 MB (13637070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30130f264687b48d7a0583772d74472381b1bddbf747faebcfad8fb79fec2160`  
		Last Modified: Mon, 08 Jun 2026 18:29:57 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:a2f39309c230b1b17f2d4ddc53dd8c639603464ac50ea2a0b5e711225deaa4d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2331529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e8052bca557af655c176e8eec1e6ba8355618d3fa1333efab780db0eba9e1a`

```dockerfile
```

-	Layers:
	-	`sha256:0ec2b032ffb696485fe5fd2a728ef8da7d25712bb8327e496cd8643a40c8d333`  
		Last Modified: Mon, 08 Jun 2026 18:29:58 GMT  
		Size: 2.3 MB (2293918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18e3f08e0e7176d1ce05b52cfd66efa801891a3146c7bafe1e0a1034b73df332`  
		Last Modified: Mon, 08 Jun 2026 18:29:58 GMT  
		Size: 37.6 KB (37611 bytes)  
		MIME: application/vnd.in-toto+json

## `httpd:2.4`

```console
$ docker pull httpd@sha256:bda12def1dc3b718a5314b4b26ca84927fdb3905091f11200d581186f240e4f6
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

### `httpd:2.4` - linux; amd64

```console
$ docker pull httpd@sha256:2b7d8a7992076bf5ceb8bb363b4c8f2b8c655072e7478f45c5e537af28f6c167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45230035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb74261f37ff6970ccb87626c9783304249efaad9f4e8cd32de4e9a3423b787d`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:48 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:48 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:48 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:53 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:30:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:30:55 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:30:55 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:30:55 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:30:55 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51757aae13a97369966a219edcf9e0f9b8cc8eaec050732a5d6fa25aa92e453`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c211dc8965131703cc3952b6267904624b637fc549d23e2e6bc0cc49b4222c`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 2.0 MB (1997894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc6b5038f865e4e495fc8fe09d6f11876069a408d170c40399b49126c800041`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 13.5 MB (13451745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9e979b34b8fed3ce647410b3644cc8cc46ef92761363f08fe8802169d5f76f`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4` - unknown; unknown

```console
$ docker pull httpd@sha256:fce1019bd8cc87b008a72778b2a2736ddff548e62baa27c4cc983db009cb5111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597fd853705160154b2bcd70d98acc6933b1b6dcf3f31cb013b0abcf1068d207`

```dockerfile
```

-	Layers:
	-	`sha256:e2025809a7e3749824decea45c53ede352d4aa58d75ace93dd07000d2b6c08a6`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 2.3 MB (2292510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:492c10869e234a6f6ccfabd1a0dfc280cec64fa0e207fc564413cc8da21c9610`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 37.6 KB (37611 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4` - linux; arm variant v5

```console
$ docker pull httpd@sha256:f361c4b24b78e1239dfeacd9d9dab2c93ea638455fd3c3b70dbbda6ab00a15f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42857065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ab2c2872db9a8045fa1ab91711e556824fe075bbaca19941f6e9bd8271bc48`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:48 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:48 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:48 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:58 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:58 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:58 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:58 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:31:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:31:48 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:31:48 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:31:48 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:31:48 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8741492638bd207b4038604a6e65e467c0a410df6afca31a4821aee832c662ab`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c069dc93d7fb7eba3c5388a00541788a95bc11398d69b0c81da9efc258d2c8d`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 1.9 MB (1912804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6002f904e7facf1cc93c7790b09f0609b922e15005a489e32e61b6fbc4316ad8`  
		Last Modified: Mon, 08 Jun 2026 18:31:57 GMT  
		Size: 13.0 MB (12989920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8efcbe4a582c8775afea0836d968f1f184bea5c26e21fe0fcbb5a0e7ebd3ff05`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4` - unknown; unknown

```console
$ docker pull httpd@sha256:f2ce1a9cefdbe977111087f3b75c7be0784ea835d0007b5a145ed2f6bfa0c95b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dfbb9b9cb8c42912b42a91046224acc7dc556f1e7d8097a01121fd91f76b72`

```dockerfile
```

-	Layers:
	-	`sha256:80fc7202154b749a8075c448c7e7a9a60d1d4f341914b54da5153b7ee3c03f5f`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 2.3 MB (2295542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27e7b847f32a118618968bc07cffc9a5d6d0c0692dee15129ee923129b35c1b4`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 37.7 KB (37749 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4` - linux; arm variant v7

```console
$ docker pull httpd@sha256:5236d5c6a10645ecac76238b7ca6f921ca8eb5ea92ab6fb293bdadae95b10ae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40548022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b12f00662f2acddd392078f235516594259077bf34e4c06e06e8288f24df443`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:54 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:54 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:54 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:54 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:29:01 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:29:01 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:29:01 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:29:01 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:31:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:31:27 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:31:27 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:31:27 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:31:27 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7617084195012707e889cdef4236f6627014b19baf5baa53b8e432880268bc`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada685e6861770db8d1c2090eecdecab5e8ae6dec8c9abc23fb86d844f8bb442`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 1.8 MB (1823341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a919558fd039a1b681fc7341aeb407767fa365ac621427a2d7bf5470f9eecc9`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 12.5 MB (12518379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a44ce25dab735595c229a5d37494e00da9b3a541edbcdd85d4f3e488c4175fd`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4` - unknown; unknown

```console
$ docker pull httpd@sha256:9db1b877234f01aa36272fba11532263d7a52f145aec8d4364b98deaca6fa87b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2331805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f897acfbf506ea853c77e9a461c832030fe5a6a95cb3bf116d12f565be924b5d`

```dockerfile
```

-	Layers:
	-	`sha256:1b5b5d4bbe67bc086194dd58eb01ec30a9bf78e7498afd570946311fcc5bbb5a`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 2.3 MB (2294057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d14fc4d73d1b623729ae4e87803dc741f0309a1a9e8d3661bd235890bb441fa`  
		Last Modified: Mon, 08 Jun 2026 18:31:35 GMT  
		Size: 37.7 KB (37748 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:05f92a0b3df99246bd094967c40d5f00311b04b74e91386ab37f3879d5b6398f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45500798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab09468e72a3fd55b26758d03ba2f8a094a6de075771c949ee820cd22f4efd4`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:48 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:48 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:48 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:53 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:30:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:30:55 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:30:55 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:30:55 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:30:55 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51757aae13a97369966a219edcf9e0f9b8cc8eaec050732a5d6fa25aa92e453`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbc1d9c94781b6fb204e9f2dd48fa707b639991a0ed9e6832bc627ee78eb793`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 2.0 MB (1971344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1897ad34a45ba49cd3bd04d81eb169b2fa80642c8bdeb1783ba8067376d69911`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 13.4 MB (13387063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8048fc63017cda60558664fdef734dbe334a9ef8bb646c61060a28ea79cc2c73`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4` - unknown; unknown

```console
$ docker pull httpd@sha256:77551cd106fe5e6dba8ab22968dcc1c2157130fb9d1ce1f165884126ef2ff11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e103ca667e4eca8f7df1a1a1760fe83de402a3064636034eca87b9551b8abeac`

```dockerfile
```

-	Layers:
	-	`sha256:9983bb17dc86db43f7ba9dfb576ff96e6213f15e4868de93bd9ac8b5b38533a0`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 2.3 MB (2292847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d696410da2eb0504c27136882e9ac61fe5c021897524d3583611c2d09de3a6ca`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 37.8 KB (37793 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4` - linux; 386

```console
$ docker pull httpd@sha256:d212f60d1de6a98f8ac5666c0f08cfb2f8d7e69c007bba602a46c8f59d8c4346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46572612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a675fd0fcf287e70a1c2a01d7ad90a4f9db4df857ba19faf767c6dd59fc412`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:49 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:49 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:49 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:49 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:55 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:55 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:55 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:55 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:31:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:31:06 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:31:06 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:31:06 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:31:06 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3f98973d06c4dd876d5ba79c06211d3cd1cea32db869157acf4434836e75b5`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82349a6b654d1e29b5f624fa403272758a3418fe2d7860fc0f98cecee1da801b`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 2.1 MB (2055642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d9f1f37b024e8db99b29e69ec67af1bc894362b189a8cce9327b62ba4c0ff8`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 13.2 MB (13221163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6acaba897604b124ab0b4b16b6083da00590bfa6de43cb198468a35afbc076`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4` - unknown; unknown

```console
$ docker pull httpd@sha256:af18d97787c89c98c8fc110c23887ed1e760fb3f9207c6089ead4f50f78ceba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2327164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a81fe9a487688b93159da3a042732411446e801c6adf453f8f6a9878133adf`

```dockerfile
```

-	Layers:
	-	`sha256:fafa740c092dc2c2d150c0a3988c531e569690a6361dd41d57a1faec9324d3e4`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 2.3 MB (2289609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c62eb654a7ce8c3c1529835aa36c0de0488098dd817dd2b7968f541c9be78d7b`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 37.6 KB (37555 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4` - linux; ppc64le

```console
$ docker pull httpd@sha256:23250993ffdf8415ee5424cdeff8f5dff52a26bff21436f6567a702b755c8cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50163250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e58559fc8be957d33533107f22829d2774b9656a856245cd16510b077a31578`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:27:34 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:27:34 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:27:34 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:27:34 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:27:48 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:27:48 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:27:48 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:27:48 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:32:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:32:03 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:32:03 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:32:03 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:32:03 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095b49d3ed9c5bd684106ef2762c8c8d6c733b6154e0f88da03b1e1966cd01df`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc91076ec4b38e804c65780f529812ce414a153e095f9380d5804984cbd9f76`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 2.1 MB (2138540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164efcce54726bc397834f6038e70f0f535de3989d1fae4a14d3ce829e318c63`  
		Last Modified: Mon, 08 Jun 2026 18:32:18 GMT  
		Size: 14.4 MB (14423785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965f08e1a921c3b4cbb9f84c6b9999ea0cc8c5df7c7ccac77ea6fd7ee24189af`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4` - unknown; unknown

```console
$ docker pull httpd@sha256:7984379d541bad6433c6840f03d5a6bf3717cc96a23a6494d8edf4f56ff068c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fdcdd51ba0de4af51f758f1a67800b27772d0b16fc1acac13a6aa87399a87e`

```dockerfile
```

-	Layers:
	-	`sha256:8a0d0e0c231ec528ec3d98a2c72ca9b7759110af04cd9392138cbfeaf1d67dc9`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 2.3 MB (2296360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa23dd30e1d59efae1e2d867d4f568fe9d993722b873f57fa8d68feb138933c7`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 37.7 KB (37682 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4` - linux; riscv64

```console
$ docker pull httpd@sha256:71876f06ab63bc1cf873ca7c7087faea82688f408c32b0224b7cb29aab33e4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43402754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75069b5306a498c987ffa1263618f82a1a44ddc86f83c3e6bde1350c1a246af6`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:27:50 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:27:50 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:27:50 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:27:50 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:42 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:42 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:42 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:42 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:51:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:51:09 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:51:09 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:51:09 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:51:09 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcb14ecded12a6ddea9368e3e0a89b321a0babb977a900740f77d9b2749c881`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6acad9c2eb5d55c394bbd6a1a2e6dc884a8bd713db7c37cd33e0deeaab271b`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 2.0 MB (1956437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691748d99998bcadae01e53818c1a0ba95d0e2ba99b846f20043d5e854281021`  
		Last Modified: Mon, 08 Jun 2026 18:52:16 GMT  
		Size: 13.2 MB (13168247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1562e123a42b9956e7d39d32f9976df80d047f431caf3c4862e78d656b7e2b7e`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4` - unknown; unknown

```console
$ docker pull httpd@sha256:fa7de91aad897f1d9eaccd4e5213a25fb802222959c9f6c423886b4fb608fa8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2324290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e51d58413798f790228b33455088967cc44329474f1c5a0c94252c4d78a9a3`

```dockerfile
```

-	Layers:
	-	`sha256:9e13f24a27b58524719240f6484550131917ee8131886a36995d67d99f36a8cc`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 2.3 MB (2286607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30c4e22ef528cabad294d53b578ccf49631760a5a1caf405303bb050958ad5df`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 37.7 KB (37683 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4` - linux; s390x

```console
$ docker pull httpd@sha256:2fa1944efe68dc19bf36d54e72ec18be919399545609955907759c62eef32556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45520012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6084b5dadfb37c1564dd4b7e44b3a1e4a405039e5715c0f39c241c50aaf0367b`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:27:38 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:27:38 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:27:38 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:27:38 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:27:44 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:27:44 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:27:44 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:27:44 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:29:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:29:45 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:29:45 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:29:45 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:29:45 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a516c95daee50c3e7a6296f522dd4fb560f14d2ca73476e1dafa47cde6b081b3`  
		Last Modified: Mon, 08 Jun 2026 18:29:57 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ffc60f849aa2b0a9016137736b47502e247d91bf7d8bdb0af208d49a528576`  
		Last Modified: Mon, 08 Jun 2026 18:29:58 GMT  
		Size: 2.0 MB (2036546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f468bbb1ef751e92d67c77000d3af1de92fc265b1a2b4e1cbb62ada60425a6`  
		Last Modified: Mon, 08 Jun 2026 18:29:58 GMT  
		Size: 13.6 MB (13637070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30130f264687b48d7a0583772d74472381b1bddbf747faebcfad8fb79fec2160`  
		Last Modified: Mon, 08 Jun 2026 18:29:57 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4` - unknown; unknown

```console
$ docker pull httpd@sha256:a2f39309c230b1b17f2d4ddc53dd8c639603464ac50ea2a0b5e711225deaa4d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2331529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e8052bca557af655c176e8eec1e6ba8355618d3fa1333efab780db0eba9e1a`

```dockerfile
```

-	Layers:
	-	`sha256:0ec2b032ffb696485fe5fd2a728ef8da7d25712bb8327e496cd8643a40c8d333`  
		Last Modified: Mon, 08 Jun 2026 18:29:58 GMT  
		Size: 2.3 MB (2293918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18e3f08e0e7176d1ce05b52cfd66efa801891a3146c7bafe1e0a1034b73df332`  
		Last Modified: Mon, 08 Jun 2026 18:29:58 GMT  
		Size: 37.6 KB (37611 bytes)  
		MIME: application/vnd.in-toto+json

## `httpd:2.4-alpine`

```console
$ docker pull httpd@sha256:4a15e9c73f25334bc03cfb3c692c9adfc103bb46ca89cee1f0b9a5fcbc7b21f6
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

### `httpd:2.4-alpine` - linux; amd64

```console
$ docker pull httpd@sha256:bf087a7b1abe6bed280d6a69dcc3c8f17055bff4d86e8b52423c7ca52dbf1103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20742245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bdbd06577ba009805166768103f9a62685d9f97a9884b54388b1fa4bea9ecdd`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 18:31:25 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Jun 2026 18:31:25 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:31:25 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:31:25 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:31:25 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:31:26 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 08 Jun 2026 18:31:26 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:31:26 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:31:26 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:32:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:32:30 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:32:30 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:32:30 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:32:30 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce5804151ace48b62ad76238cde0765d43efa9396f491d9ec2d59b41a4fa8e1`  
		Last Modified: Mon, 08 Jun 2026 18:32:37 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db356f236e7a97cfe205045ad2895819d2fe9beecb1a8bd65fae6929cc6115a1`  
		Last Modified: Mon, 08 Jun 2026 18:32:37 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc5e0e38d81ae69af4435b5d5a5be213645e9c40200ddab1281a71efec26d94`  
		Last Modified: Mon, 08 Jun 2026 18:32:37 GMT  
		Size: 11.1 MB (11066958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af2e4b44c0574322eab72595901d051fdfd3dee1524b5d0f9177ecd7953cdc0`  
		Last Modified: Mon, 08 Jun 2026 18:32:37 GMT  
		Size: 5.8 MB (5809700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86856eeef9e12dbdc8ff4c7baebbd5cdefe872848eaf6ef2aef50eced2e7bd0e`  
		Last Modified: Mon, 08 Jun 2026 18:32:38 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:70c3c56d3d003dfac3b02abe58445b9d05b65eb48d2caf76a2aae4f16d351c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1239812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2a862ab34194b98abe1ad90fb1158234040d57fa2471ca197496507a8194920`

```dockerfile
```

-	Layers:
	-	`sha256:84e23f6554b8259dbd70956df3da92e26511e07ad4412a2a0a648cc51f4f4e78`  
		Last Modified: Mon, 08 Jun 2026 18:32:37 GMT  
		Size: 1.2 MB (1201606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc8b38586c1d8780912c3f004220df6b7649ed5c47efa43fa068ee9662f47caa`  
		Last Modified: Mon, 08 Jun 2026 18:32:36 GMT  
		Size: 38.2 KB (38206 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-alpine` - linux; arm variant v6

```console
$ docker pull httpd@sha256:024536b397c6ad22fa335218e0fb10fd1206c9fdb71dd7448c4f4f7fe16a8bc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19530438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979e382592d01f76ea45774429a342ecc5edef3ae3f0cdb9f569403603dd1cda`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 18:28:46 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Jun 2026 18:28:46 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:46 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:46 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:46 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:48 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:30:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:30:08 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:30:08 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:30:08 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:30:08 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8321b554dfa7c63a2afd55c8fb184b69858f457e8dfa9880f4bc448d8a39d4`  
		Last Modified: Mon, 08 Jun 2026 18:30:13 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09a332d4df7c9bee48b2d2de86966f85e36b64798eaaf67de0975e4f1555f89`  
		Last Modified: Mon, 08 Jun 2026 18:30:13 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215e98f908ff76704a82ca9d04a502bc930ce17a9047820920844edfd57fa760`  
		Last Modified: Mon, 08 Jun 2026 18:30:14 GMT  
		Size: 10.3 MB (10286319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ee63e2411212cd08a883b8c84dc993798a84b4de02db32551ee900d921c95e`  
		Last Modified: Mon, 08 Jun 2026 18:30:14 GMT  
		Size: 5.7 MB (5670856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e101d519540f8c8be21ad616e63d9f66a84ae618343405938dddad8bdeae5f6`  
		Last Modified: Mon, 08 Jun 2026 18:30:15 GMT  
		Size: 289.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:fc8f3318e4ab42107e49368c4f569a975957bd9af2efab2cec507177830cda11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb4db6d5f35a09c872dde41878646504db7ebdfdc3744e4f6986726e057c671`

```dockerfile
```

-	Layers:
	-	`sha256:6e8897e1452670de76c435a27c21f0d31afad8b78d64fa84fdaffa8c052e60a6`  
		Last Modified: Mon, 08 Jun 2026 18:30:13 GMT  
		Size: 38.1 KB (38142 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-alpine` - linux; arm variant v7

```console
$ docker pull httpd@sha256:8061dc7af76065401d58b4b0517719208ee34c8923c83d30cffdd47abc0aa401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18701347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aab2fe87d7e0e05ed925969046f55ddf1ef27740b6067ba4161f1928c96e254`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 18:30:37 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Jun 2026 18:30:37 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:30:37 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:30:37 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:30:37 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:30:39 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 08 Jun 2026 18:30:39 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:30:39 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:30:39 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:31:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:31:55 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:31:55 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:31:55 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:31:55 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ad8e36bc25e31e63d7c1a292ea9f35a3df589ad01be37b48a4ac3ae9fc0847`  
		Last Modified: Mon, 08 Jun 2026 18:32:01 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfec7351aad4a1810cd117ec6fda31c0b8b9af893f2d6755fe6e474e5edc16a`  
		Last Modified: Mon, 08 Jun 2026 18:32:01 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89db8edd72fdbfd84fe9a186dbe1fa7539829347879a957a070d49ccc276ef92`  
		Last Modified: Mon, 08 Jun 2026 18:32:02 GMT  
		Size: 10.1 MB (10062859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7c853cb79a0e47b775a4cb5ed20a4fa1f0fa54a2a4a8fc43c5e2c52e10a4dd`  
		Last Modified: Mon, 08 Jun 2026 18:32:02 GMT  
		Size: 5.4 MB (5353967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4dfbc2ff27845415d637069fa7548a00c66b9364660c093067578b62d6d650`  
		Last Modified: Mon, 08 Jun 2026 18:32:03 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:9d340e705b4d2d4d5357cabee9b78bdebcd67b0dc92a2435cc1e019af5338324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1242371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53499d0e69d22627cf589b7d2118279c706b905969b2b30fe01ebd143120c86c`

```dockerfile
```

-	Layers:
	-	`sha256:a78794fe77e35b91f4ccad718d8777e6c1c5cd52d6a272f4cd53482c4a88cdda`  
		Last Modified: Mon, 08 Jun 2026 18:32:02 GMT  
		Size: 1.2 MB (1204014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e1fe4c2a693f67e2ff7c45c79009d14ddf8c3005f4b3747c700d1530f9d7fe6`  
		Last Modified: Mon, 08 Jun 2026 18:32:01 GMT  
		Size: 38.4 KB (38357 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-alpine` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:85b4776185fbee81f2ccf80b645c10d5d2a5eadc8004a038d38784682f667ffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21163903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d2c617afd2009094a1862af906977d4bd5a6a9fcfc1ef8cb27061905000692`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 18:30:27 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Jun 2026 18:30:27 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:30:27 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:30:27 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:30:27 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:30:28 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 08 Jun 2026 18:30:28 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:30:28 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:30:28 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:31:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:31:36 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:31:36 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:31:36 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:31:36 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2733de7154d76386a001a868473ab506efdc9813265b2e519d49513c0c0ca4c4`  
		Last Modified: Mon, 08 Jun 2026 18:31:43 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a593c24a6a1b8072f379a89d7870d2df90bb18d23f56ac71aee739dfe20489ec`  
		Last Modified: Mon, 08 Jun 2026 18:31:43 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b0d2c4d83de418eef5171c3593da6a8e7caa221b1af072d6936c20d6b74a25`  
		Last Modified: Mon, 08 Jun 2026 18:31:44 GMT  
		Size: 11.0 MB (11034000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa7baf1e3c92a7533ea08f8fdd39cd5280b65628d1c6c62793565d5e1743a6f`  
		Last Modified: Mon, 08 Jun 2026 18:31:44 GMT  
		Size: 5.9 MB (5928633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3ca4765694b549352106668014c1d542f93d13adf1f177a9a956461ed5492c`  
		Last Modified: Mon, 08 Jun 2026 18:31:44 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:4af10a58bed505a14c1108a84db0aaa27d666395366e84db3677085d87d207df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1239463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0f41e9cde0dc8d8ccf71126bd2f783f7f8231c70316ba7fe767a9230fa4bb8`

```dockerfile
```

-	Layers:
	-	`sha256:13468312a748d8b51aaf3a82ad0f3271775ef5301c38d37fbd6196359c20d00a`  
		Last Modified: Mon, 08 Jun 2026 18:31:44 GMT  
		Size: 1.2 MB (1201060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1470375ebacc02386973357f8aab79e0f87c8d365f1ff6dbcdb17779e96c813b`  
		Last Modified: Mon, 08 Jun 2026 18:31:43 GMT  
		Size: 38.4 KB (38403 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-alpine` - linux; 386

```console
$ docker pull httpd@sha256:16b1c94bd801f2d8832b0683f76414905177be78ab8e40a633e7ec0890433857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (20021926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c38ed0bd74cceb6792e9d929d312d54bc80e7cde0e19948ffd46cb48f7ab757`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 18:31:21 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Jun 2026 18:31:21 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:31:21 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:31:21 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:31:21 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:31:23 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 08 Jun 2026 18:31:23 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:31:23 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:31:23 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:32:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:32:39 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:32:39 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:32:39 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:32:39 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056f17e7b6ddfb0a1da905574c6263028f20b340ff9666ae47cfa26135676670`  
		Last Modified: Mon, 08 Jun 2026 18:32:46 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21afa337e01a5d443d84b004f17c160335eb4219e04af1e9c70ceb3707efbce0`  
		Last Modified: Mon, 08 Jun 2026 18:32:46 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbfae095ca14e5295651305f917acc6f71a2fbd5f49b85a3fc2c57e03b2be3d`  
		Last Modified: Mon, 08 Jun 2026 18:32:46 GMT  
		Size: 10.6 MB (10618085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc33c24b7089af8156a61a652ed7c5fe322baa0d78dcb691295bb589a0de453`  
		Last Modified: Mon, 08 Jun 2026 18:32:46 GMT  
		Size: 5.7 MB (5711996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b50c0cd8edcb1ed19a9637f074a4770f9a6f876606cae56220092e6243e576`  
		Last Modified: Mon, 08 Jun 2026 18:32:47 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:740f2dd920cb4f5bedec74d3f44ed0b9c47bf46d2e8b0b13557276827bcdc52e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1239709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f14334929789a57deae0012f30aba319525e7ff989e36134d070c56a6dd94dc`

```dockerfile
```

-	Layers:
	-	`sha256:d0dacd457b618139c482a7d6afa2041ffd6cb707e33b66acf044aaefaa14397e`  
		Last Modified: Mon, 08 Jun 2026 18:32:46 GMT  
		Size: 1.2 MB (1201561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44183710a388aa4b94ef6d14e896b787a7e08a8f608a9c14d36001d21668c987`  
		Last Modified: Mon, 08 Jun 2026 18:32:46 GMT  
		Size: 38.1 KB (38148 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-alpine` - linux; ppc64le

```console
$ docker pull httpd@sha256:24c446eba8c10efd7206d9e55e728f1787228d1442aa6ef61ac7a0d515cce4ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21381418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a448835add6f4d91f1982c6a872fe649b29ed77425b2e9e5aa901dd5e301205f`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 18:27:34 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Jun 2026 18:27:34 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:27:34 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:27:34 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:27:35 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:27:38 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 08 Jun 2026 18:27:38 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:27:38 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:27:38 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:29:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:29:29 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:29:29 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:29:29 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:29:29 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3833350820ce2613df1f0a4261df6ce7bc4951ba5dba44ef1a833641790aaaa`  
		Last Modified: Mon, 08 Jun 2026 18:29:47 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e9193af3a9c4cd580ff4cb24c30058cbec15dd6378f5950513a68c769c281f`  
		Last Modified: Mon, 08 Jun 2026 18:29:47 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a872efdd830ec45ac7efd740e333bf2cb140e2f4b94e60dd878415304be4b613`  
		Last Modified: Mon, 08 Jun 2026 18:29:47 GMT  
		Size: 11.3 MB (11338111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7513aa3438c9c2feecadf91e523239d954d60ceddaeda0f6e6763e2235eb9d35`  
		Last Modified: Mon, 08 Jun 2026 18:29:47 GMT  
		Size: 6.2 MB (6210978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47983e84280f04dea9f420f8879dc16efab9198e05c7c6d79eae3fe957261a48`  
		Last Modified: Mon, 08 Jun 2026 18:29:48 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:17e67c7acec63724871964de2c8a364fb31631efd6f458ddd90235490b789f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1239293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77c39681778c5b28492be2b18b099ed022a8b09c86791dd235685cbc511448b`

```dockerfile
```

-	Layers:
	-	`sha256:aa63ded6d68a8c82088e414a0d5b803f2cf467747fc6fe33326dd7f4a8ff1d61`  
		Last Modified: Mon, 08 Jun 2026 18:29:47 GMT  
		Size: 1.2 MB (1201013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:772db10801a309da7fa867f9755115f0e7af393467440d9c2ba6a20824bfd7a0`  
		Last Modified: Mon, 08 Jun 2026 18:29:47 GMT  
		Size: 38.3 KB (38280 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-alpine` - linux; riscv64

```console
$ docker pull httpd@sha256:6e901fc55fc925beed4d9e227553864af8d4da401692c898b3ba5d6198aa89e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19923429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94d1b25cfd3edbe24497157b752ff6f1b0bae2216ac56a9695500c96025ef0d8`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 18:52:56 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Jun 2026 18:52:56 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:52:56 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:52:56 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:52:57 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:53:04 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 08 Jun 2026 18:53:04 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:53:04 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:53:04 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 19:03:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 08 Jun 2026 19:03:07 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 19:03:07 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 19:03:07 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 19:03:07 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19c7f0762250b0cc52b39bb993e944c7a467ccbba9e5982b3e05a892ed00e09`  
		Last Modified: Mon, 08 Jun 2026 19:03:57 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948f4b41e7172c5b397872ec12028b50e89c8b1945bcdd382f3c4354d3816a6c`  
		Last Modified: Mon, 08 Jun 2026 19:03:57 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839bf3cd8868f427bc3edaf740a5070b32162d92911d6135ad7452faf74806e2`  
		Last Modified: Mon, 08 Jun 2026 19:04:00 GMT  
		Size: 10.5 MB (10512864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0ed49d6165d488e835183bba68a905603e14ef7c9d532d89556389e587cdb6`  
		Last Modified: Mon, 08 Jun 2026 19:03:59 GMT  
		Size: 5.8 MB (5821504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9212c34deb579c5504ab192148ff204061b0646ae26b63cc9ad5ed1aad1789c`  
		Last Modified: Mon, 08 Jun 2026 19:03:59 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:536fbac1930d7f288da7460218490b036b05488c57b17e046817cfca2d991009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1239289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63060237e36817f0674dfd5a4486b1ecb06b72e44a91033e3d2fc30181462368`

```dockerfile
```

-	Layers:
	-	`sha256:106695ede26a0f693625ca363327da8a1cf3bbdf11f35f67bf2ed2a8b03aa116`  
		Last Modified: Mon, 08 Jun 2026 19:03:58 GMT  
		Size: 1.2 MB (1201009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efd7b10cf0eb8a6248093104323312312d5e4f5d818a591a147f6a252df1d07d`  
		Last Modified: Mon, 08 Jun 2026 19:03:58 GMT  
		Size: 38.3 KB (38280 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-alpine` - linux; s390x

```console
$ docker pull httpd@sha256:6283359189b28f3ca4b868bf776ceb2b692e4add8fea4a8b3269d66b7753a935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21378874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2df8884703c6d4ccc1f8733cfd8210fb8eb0924b8b0b633ac84af6641b17fbd`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 18:27:38 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Jun 2026 18:27:38 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:27:38 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:27:38 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:27:38 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:27:40 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 08 Jun 2026 18:27:40 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:27:40 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:27:40 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:28:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:28:46 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:28:46 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:28:46 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:28:46 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548235140cb8c1ab10d4692027815816cc2544f4ec8835eba3f51db5727af171`  
		Last Modified: Mon, 08 Jun 2026 18:28:59 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369bc1e79711eb6126c37a7b565cc2b0f42d4ee767040a1f8b44f857f5adef9a`  
		Last Modified: Mon, 08 Jun 2026 18:28:59 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59e8a1afdfdaee57b84923042e279cf1dc1f97d76646bf9caebc7a940d504ca`  
		Last Modified: Mon, 08 Jun 2026 18:28:59 GMT  
		Size: 11.6 MB (11649300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138c5a50960e95cfc40f091bc4080b810eb24455ad217b422125a22d86f5284d`  
		Last Modified: Mon, 08 Jun 2026 18:28:59 GMT  
		Size: 6.0 MB (6001640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c831663f14f23188df97e6b051c05bf1da28f9a4c18fc2c2cad0bdaff1429eb`  
		Last Modified: Mon, 08 Jun 2026 18:29:00 GMT  
		Size: 289.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:5cc2f04b98cd0e537a6eb5f791971f720a637c2255c7f4758ec7d5e301ba4612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1239161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8474478033f363a3cbf719bfac24a8e06adef6eccc522a4b3c2748dda664f13`

```dockerfile
```

-	Layers:
	-	`sha256:0b586450d6cc931e529e0fe9520eca240e9996721ea62991acd52c3c73de9ee9`  
		Last Modified: Mon, 08 Jun 2026 18:28:59 GMT  
		Size: 1.2 MB (1200955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d691c6da1d20a4d1e620abc97c146c35e966efbc00988d6f0d5c0941364e3a49`  
		Last Modified: Mon, 08 Jun 2026 18:28:58 GMT  
		Size: 38.2 KB (38206 bytes)  
		MIME: application/vnd.in-toto+json

## `httpd:2.4-alpine3.24`

**does not exist** (yet?)

## `httpd:2.4-trixie`

```console
$ docker pull httpd@sha256:bda12def1dc3b718a5314b4b26ca84927fdb3905091f11200d581186f240e4f6
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

### `httpd:2.4-trixie` - linux; amd64

```console
$ docker pull httpd@sha256:2b7d8a7992076bf5ceb8bb363b4c8f2b8c655072e7478f45c5e537af28f6c167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45230035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb74261f37ff6970ccb87626c9783304249efaad9f4e8cd32de4e9a3423b787d`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:48 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:48 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:48 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:53 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:30:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:30:55 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:30:55 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:30:55 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:30:55 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51757aae13a97369966a219edcf9e0f9b8cc8eaec050732a5d6fa25aa92e453`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c211dc8965131703cc3952b6267904624b637fc549d23e2e6bc0cc49b4222c`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 2.0 MB (1997894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc6b5038f865e4e495fc8fe09d6f11876069a408d170c40399b49126c800041`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 13.5 MB (13451745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9e979b34b8fed3ce647410b3644cc8cc46ef92761363f08fe8802169d5f76f`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:fce1019bd8cc87b008a72778b2a2736ddff548e62baa27c4cc983db009cb5111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597fd853705160154b2bcd70d98acc6933b1b6dcf3f31cb013b0abcf1068d207`

```dockerfile
```

-	Layers:
	-	`sha256:e2025809a7e3749824decea45c53ede352d4aa58d75ace93dd07000d2b6c08a6`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 2.3 MB (2292510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:492c10869e234a6f6ccfabd1a0dfc280cec64fa0e207fc564413cc8da21c9610`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 37.6 KB (37611 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-trixie` - linux; arm variant v5

```console
$ docker pull httpd@sha256:f361c4b24b78e1239dfeacd9d9dab2c93ea638455fd3c3b70dbbda6ab00a15f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42857065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ab2c2872db9a8045fa1ab91711e556824fe075bbaca19941f6e9bd8271bc48`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:48 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:48 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:48 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:58 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:58 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:58 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:58 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:31:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:31:48 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:31:48 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:31:48 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:31:48 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8741492638bd207b4038604a6e65e467c0a410df6afca31a4821aee832c662ab`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c069dc93d7fb7eba3c5388a00541788a95bc11398d69b0c81da9efc258d2c8d`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 1.9 MB (1912804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6002f904e7facf1cc93c7790b09f0609b922e15005a489e32e61b6fbc4316ad8`  
		Last Modified: Mon, 08 Jun 2026 18:31:57 GMT  
		Size: 13.0 MB (12989920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8efcbe4a582c8775afea0836d968f1f184bea5c26e21fe0fcbb5a0e7ebd3ff05`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:f2ce1a9cefdbe977111087f3b75c7be0784ea835d0007b5a145ed2f6bfa0c95b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dfbb9b9cb8c42912b42a91046224acc7dc556f1e7d8097a01121fd91f76b72`

```dockerfile
```

-	Layers:
	-	`sha256:80fc7202154b749a8075c448c7e7a9a60d1d4f341914b54da5153b7ee3c03f5f`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 2.3 MB (2295542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27e7b847f32a118618968bc07cffc9a5d6d0c0692dee15129ee923129b35c1b4`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 37.7 KB (37749 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-trixie` - linux; arm variant v7

```console
$ docker pull httpd@sha256:5236d5c6a10645ecac76238b7ca6f921ca8eb5ea92ab6fb293bdadae95b10ae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40548022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b12f00662f2acddd392078f235516594259077bf34e4c06e06e8288f24df443`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:54 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:54 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:54 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:54 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:29:01 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:29:01 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:29:01 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:29:01 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:31:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:31:27 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:31:27 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:31:27 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:31:27 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7617084195012707e889cdef4236f6627014b19baf5baa53b8e432880268bc`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada685e6861770db8d1c2090eecdecab5e8ae6dec8c9abc23fb86d844f8bb442`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 1.8 MB (1823341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a919558fd039a1b681fc7341aeb407767fa365ac621427a2d7bf5470f9eecc9`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 12.5 MB (12518379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a44ce25dab735595c229a5d37494e00da9b3a541edbcdd85d4f3e488c4175fd`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:9db1b877234f01aa36272fba11532263d7a52f145aec8d4364b98deaca6fa87b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2331805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f897acfbf506ea853c77e9a461c832030fe5a6a95cb3bf116d12f565be924b5d`

```dockerfile
```

-	Layers:
	-	`sha256:1b5b5d4bbe67bc086194dd58eb01ec30a9bf78e7498afd570946311fcc5bbb5a`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 2.3 MB (2294057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d14fc4d73d1b623729ae4e87803dc741f0309a1a9e8d3661bd235890bb441fa`  
		Last Modified: Mon, 08 Jun 2026 18:31:35 GMT  
		Size: 37.7 KB (37748 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-trixie` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:05f92a0b3df99246bd094967c40d5f00311b04b74e91386ab37f3879d5b6398f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45500798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab09468e72a3fd55b26758d03ba2f8a094a6de075771c949ee820cd22f4efd4`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:48 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:48 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:48 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:53 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:30:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:30:55 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:30:55 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:30:55 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:30:55 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51757aae13a97369966a219edcf9e0f9b8cc8eaec050732a5d6fa25aa92e453`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbc1d9c94781b6fb204e9f2dd48fa707b639991a0ed9e6832bc627ee78eb793`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 2.0 MB (1971344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1897ad34a45ba49cd3bd04d81eb169b2fa80642c8bdeb1783ba8067376d69911`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 13.4 MB (13387063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8048fc63017cda60558664fdef734dbe334a9ef8bb646c61060a28ea79cc2c73`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:77551cd106fe5e6dba8ab22968dcc1c2157130fb9d1ce1f165884126ef2ff11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e103ca667e4eca8f7df1a1a1760fe83de402a3064636034eca87b9551b8abeac`

```dockerfile
```

-	Layers:
	-	`sha256:9983bb17dc86db43f7ba9dfb576ff96e6213f15e4868de93bd9ac8b5b38533a0`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 2.3 MB (2292847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d696410da2eb0504c27136882e9ac61fe5c021897524d3583611c2d09de3a6ca`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 37.8 KB (37793 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-trixie` - linux; 386

```console
$ docker pull httpd@sha256:d212f60d1de6a98f8ac5666c0f08cfb2f8d7e69c007bba602a46c8f59d8c4346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46572612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a675fd0fcf287e70a1c2a01d7ad90a4f9db4df857ba19faf767c6dd59fc412`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:49 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:49 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:49 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:49 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:55 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:55 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:55 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:55 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:31:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:31:06 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:31:06 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:31:06 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:31:06 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3f98973d06c4dd876d5ba79c06211d3cd1cea32db869157acf4434836e75b5`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82349a6b654d1e29b5f624fa403272758a3418fe2d7860fc0f98cecee1da801b`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 2.1 MB (2055642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d9f1f37b024e8db99b29e69ec67af1bc894362b189a8cce9327b62ba4c0ff8`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 13.2 MB (13221163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6acaba897604b124ab0b4b16b6083da00590bfa6de43cb198468a35afbc076`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:af18d97787c89c98c8fc110c23887ed1e760fb3f9207c6089ead4f50f78ceba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2327164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a81fe9a487688b93159da3a042732411446e801c6adf453f8f6a9878133adf`

```dockerfile
```

-	Layers:
	-	`sha256:fafa740c092dc2c2d150c0a3988c531e569690a6361dd41d57a1faec9324d3e4`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 2.3 MB (2289609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c62eb654a7ce8c3c1529835aa36c0de0488098dd817dd2b7968f541c9be78d7b`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 37.6 KB (37555 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-trixie` - linux; ppc64le

```console
$ docker pull httpd@sha256:23250993ffdf8415ee5424cdeff8f5dff52a26bff21436f6567a702b755c8cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50163250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e58559fc8be957d33533107f22829d2774b9656a856245cd16510b077a31578`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:27:34 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:27:34 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:27:34 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:27:34 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:27:48 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:27:48 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:27:48 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:27:48 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:32:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:32:03 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:32:03 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:32:03 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:32:03 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095b49d3ed9c5bd684106ef2762c8c8d6c733b6154e0f88da03b1e1966cd01df`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc91076ec4b38e804c65780f529812ce414a153e095f9380d5804984cbd9f76`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 2.1 MB (2138540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164efcce54726bc397834f6038e70f0f535de3989d1fae4a14d3ce829e318c63`  
		Last Modified: Mon, 08 Jun 2026 18:32:18 GMT  
		Size: 14.4 MB (14423785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965f08e1a921c3b4cbb9f84c6b9999ea0cc8c5df7c7ccac77ea6fd7ee24189af`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:7984379d541bad6433c6840f03d5a6bf3717cc96a23a6494d8edf4f56ff068c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fdcdd51ba0de4af51f758f1a67800b27772d0b16fc1acac13a6aa87399a87e`

```dockerfile
```

-	Layers:
	-	`sha256:8a0d0e0c231ec528ec3d98a2c72ca9b7759110af04cd9392138cbfeaf1d67dc9`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 2.3 MB (2296360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa23dd30e1d59efae1e2d867d4f568fe9d993722b873f57fa8d68feb138933c7`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 37.7 KB (37682 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-trixie` - linux; riscv64

```console
$ docker pull httpd@sha256:71876f06ab63bc1cf873ca7c7087faea82688f408c32b0224b7cb29aab33e4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43402754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75069b5306a498c987ffa1263618f82a1a44ddc86f83c3e6bde1350c1a246af6`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:27:50 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:27:50 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:27:50 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:27:50 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:42 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:42 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:42 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:42 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:51:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:51:09 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:51:09 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:51:09 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:51:09 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcb14ecded12a6ddea9368e3e0a89b321a0babb977a900740f77d9b2749c881`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6acad9c2eb5d55c394bbd6a1a2e6dc884a8bd713db7c37cd33e0deeaab271b`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 2.0 MB (1956437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691748d99998bcadae01e53818c1a0ba95d0e2ba99b846f20043d5e854281021`  
		Last Modified: Mon, 08 Jun 2026 18:52:16 GMT  
		Size: 13.2 MB (13168247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1562e123a42b9956e7d39d32f9976df80d047f431caf3c4862e78d656b7e2b7e`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:fa7de91aad897f1d9eaccd4e5213a25fb802222959c9f6c423886b4fb608fa8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2324290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e51d58413798f790228b33455088967cc44329474f1c5a0c94252c4d78a9a3`

```dockerfile
```

-	Layers:
	-	`sha256:9e13f24a27b58524719240f6484550131917ee8131886a36995d67d99f36a8cc`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 2.3 MB (2286607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30c4e22ef528cabad294d53b578ccf49631760a5a1caf405303bb050958ad5df`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 37.7 KB (37683 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-trixie` - linux; s390x

```console
$ docker pull httpd@sha256:2fa1944efe68dc19bf36d54e72ec18be919399545609955907759c62eef32556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45520012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6084b5dadfb37c1564dd4b7e44b3a1e4a405039e5715c0f39c241c50aaf0367b`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:27:38 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:27:38 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:27:38 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:27:38 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:27:44 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:27:44 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:27:44 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:27:44 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:29:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:29:45 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:29:45 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:29:45 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:29:45 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a516c95daee50c3e7a6296f522dd4fb560f14d2ca73476e1dafa47cde6b081b3`  
		Last Modified: Mon, 08 Jun 2026 18:29:57 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ffc60f849aa2b0a9016137736b47502e247d91bf7d8bdb0af208d49a528576`  
		Last Modified: Mon, 08 Jun 2026 18:29:58 GMT  
		Size: 2.0 MB (2036546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f468bbb1ef751e92d67c77000d3af1de92fc265b1a2b4e1cbb62ada60425a6`  
		Last Modified: Mon, 08 Jun 2026 18:29:58 GMT  
		Size: 13.6 MB (13637070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30130f264687b48d7a0583772d74472381b1bddbf747faebcfad8fb79fec2160`  
		Last Modified: Mon, 08 Jun 2026 18:29:57 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:a2f39309c230b1b17f2d4ddc53dd8c639603464ac50ea2a0b5e711225deaa4d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2331529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e8052bca557af655c176e8eec1e6ba8355618d3fa1333efab780db0eba9e1a`

```dockerfile
```

-	Layers:
	-	`sha256:0ec2b032ffb696485fe5fd2a728ef8da7d25712bb8327e496cd8643a40c8d333`  
		Last Modified: Mon, 08 Jun 2026 18:29:58 GMT  
		Size: 2.3 MB (2293918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18e3f08e0e7176d1ce05b52cfd66efa801891a3146c7bafe1e0a1034b73df332`  
		Last Modified: Mon, 08 Jun 2026 18:29:58 GMT  
		Size: 37.6 KB (37611 bytes)  
		MIME: application/vnd.in-toto+json

## `httpd:2.4.68`

```console
$ docker pull httpd@sha256:bda12def1dc3b718a5314b4b26ca84927fdb3905091f11200d581186f240e4f6
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

### `httpd:2.4.68` - linux; amd64

```console
$ docker pull httpd@sha256:2b7d8a7992076bf5ceb8bb363b4c8f2b8c655072e7478f45c5e537af28f6c167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45230035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb74261f37ff6970ccb87626c9783304249efaad9f4e8cd32de4e9a3423b787d`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:48 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:48 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:48 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:53 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:30:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:30:55 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:30:55 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:30:55 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:30:55 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51757aae13a97369966a219edcf9e0f9b8cc8eaec050732a5d6fa25aa92e453`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c211dc8965131703cc3952b6267904624b637fc549d23e2e6bc0cc49b4222c`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 2.0 MB (1997894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc6b5038f865e4e495fc8fe09d6f11876069a408d170c40399b49126c800041`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 13.5 MB (13451745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9e979b34b8fed3ce647410b3644cc8cc46ef92761363f08fe8802169d5f76f`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.68` - unknown; unknown

```console
$ docker pull httpd@sha256:fce1019bd8cc87b008a72778b2a2736ddff548e62baa27c4cc983db009cb5111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597fd853705160154b2bcd70d98acc6933b1b6dcf3f31cb013b0abcf1068d207`

```dockerfile
```

-	Layers:
	-	`sha256:e2025809a7e3749824decea45c53ede352d4aa58d75ace93dd07000d2b6c08a6`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 2.3 MB (2292510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:492c10869e234a6f6ccfabd1a0dfc280cec64fa0e207fc564413cc8da21c9610`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 37.6 KB (37611 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.68` - linux; arm variant v5

```console
$ docker pull httpd@sha256:f361c4b24b78e1239dfeacd9d9dab2c93ea638455fd3c3b70dbbda6ab00a15f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42857065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ab2c2872db9a8045fa1ab91711e556824fe075bbaca19941f6e9bd8271bc48`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:48 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:48 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:48 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:58 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:58 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:58 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:58 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:31:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:31:48 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:31:48 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:31:48 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:31:48 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8741492638bd207b4038604a6e65e467c0a410df6afca31a4821aee832c662ab`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c069dc93d7fb7eba3c5388a00541788a95bc11398d69b0c81da9efc258d2c8d`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 1.9 MB (1912804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6002f904e7facf1cc93c7790b09f0609b922e15005a489e32e61b6fbc4316ad8`  
		Last Modified: Mon, 08 Jun 2026 18:31:57 GMT  
		Size: 13.0 MB (12989920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8efcbe4a582c8775afea0836d968f1f184bea5c26e21fe0fcbb5a0e7ebd3ff05`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.68` - unknown; unknown

```console
$ docker pull httpd@sha256:f2ce1a9cefdbe977111087f3b75c7be0784ea835d0007b5a145ed2f6bfa0c95b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dfbb9b9cb8c42912b42a91046224acc7dc556f1e7d8097a01121fd91f76b72`

```dockerfile
```

-	Layers:
	-	`sha256:80fc7202154b749a8075c448c7e7a9a60d1d4f341914b54da5153b7ee3c03f5f`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 2.3 MB (2295542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27e7b847f32a118618968bc07cffc9a5d6d0c0692dee15129ee923129b35c1b4`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 37.7 KB (37749 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.68` - linux; arm variant v7

```console
$ docker pull httpd@sha256:5236d5c6a10645ecac76238b7ca6f921ca8eb5ea92ab6fb293bdadae95b10ae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40548022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b12f00662f2acddd392078f235516594259077bf34e4c06e06e8288f24df443`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:54 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:54 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:54 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:54 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:29:01 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:29:01 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:29:01 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:29:01 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:31:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:31:27 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:31:27 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:31:27 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:31:27 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7617084195012707e889cdef4236f6627014b19baf5baa53b8e432880268bc`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada685e6861770db8d1c2090eecdecab5e8ae6dec8c9abc23fb86d844f8bb442`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 1.8 MB (1823341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a919558fd039a1b681fc7341aeb407767fa365ac621427a2d7bf5470f9eecc9`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 12.5 MB (12518379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a44ce25dab735595c229a5d37494e00da9b3a541edbcdd85d4f3e488c4175fd`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.68` - unknown; unknown

```console
$ docker pull httpd@sha256:9db1b877234f01aa36272fba11532263d7a52f145aec8d4364b98deaca6fa87b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2331805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f897acfbf506ea853c77e9a461c832030fe5a6a95cb3bf116d12f565be924b5d`

```dockerfile
```

-	Layers:
	-	`sha256:1b5b5d4bbe67bc086194dd58eb01ec30a9bf78e7498afd570946311fcc5bbb5a`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 2.3 MB (2294057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d14fc4d73d1b623729ae4e87803dc741f0309a1a9e8d3661bd235890bb441fa`  
		Last Modified: Mon, 08 Jun 2026 18:31:35 GMT  
		Size: 37.7 KB (37748 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.68` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:05f92a0b3df99246bd094967c40d5f00311b04b74e91386ab37f3879d5b6398f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45500798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab09468e72a3fd55b26758d03ba2f8a094a6de075771c949ee820cd22f4efd4`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:48 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:48 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:48 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:53 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:30:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:30:55 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:30:55 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:30:55 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:30:55 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51757aae13a97369966a219edcf9e0f9b8cc8eaec050732a5d6fa25aa92e453`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbc1d9c94781b6fb204e9f2dd48fa707b639991a0ed9e6832bc627ee78eb793`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 2.0 MB (1971344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1897ad34a45ba49cd3bd04d81eb169b2fa80642c8bdeb1783ba8067376d69911`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 13.4 MB (13387063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8048fc63017cda60558664fdef734dbe334a9ef8bb646c61060a28ea79cc2c73`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.68` - unknown; unknown

```console
$ docker pull httpd@sha256:77551cd106fe5e6dba8ab22968dcc1c2157130fb9d1ce1f165884126ef2ff11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e103ca667e4eca8f7df1a1a1760fe83de402a3064636034eca87b9551b8abeac`

```dockerfile
```

-	Layers:
	-	`sha256:9983bb17dc86db43f7ba9dfb576ff96e6213f15e4868de93bd9ac8b5b38533a0`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 2.3 MB (2292847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d696410da2eb0504c27136882e9ac61fe5c021897524d3583611c2d09de3a6ca`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 37.8 KB (37793 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.68` - linux; 386

```console
$ docker pull httpd@sha256:d212f60d1de6a98f8ac5666c0f08cfb2f8d7e69c007bba602a46c8f59d8c4346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46572612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a675fd0fcf287e70a1c2a01d7ad90a4f9db4df857ba19faf767c6dd59fc412`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:49 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:49 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:49 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:49 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:55 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:55 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:55 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:55 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:31:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:31:06 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:31:06 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:31:06 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:31:06 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3f98973d06c4dd876d5ba79c06211d3cd1cea32db869157acf4434836e75b5`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82349a6b654d1e29b5f624fa403272758a3418fe2d7860fc0f98cecee1da801b`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 2.1 MB (2055642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d9f1f37b024e8db99b29e69ec67af1bc894362b189a8cce9327b62ba4c0ff8`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 13.2 MB (13221163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6acaba897604b124ab0b4b16b6083da00590bfa6de43cb198468a35afbc076`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.68` - unknown; unknown

```console
$ docker pull httpd@sha256:af18d97787c89c98c8fc110c23887ed1e760fb3f9207c6089ead4f50f78ceba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2327164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a81fe9a487688b93159da3a042732411446e801c6adf453f8f6a9878133adf`

```dockerfile
```

-	Layers:
	-	`sha256:fafa740c092dc2c2d150c0a3988c531e569690a6361dd41d57a1faec9324d3e4`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 2.3 MB (2289609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c62eb654a7ce8c3c1529835aa36c0de0488098dd817dd2b7968f541c9be78d7b`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 37.6 KB (37555 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.68` - linux; ppc64le

```console
$ docker pull httpd@sha256:23250993ffdf8415ee5424cdeff8f5dff52a26bff21436f6567a702b755c8cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50163250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e58559fc8be957d33533107f22829d2774b9656a856245cd16510b077a31578`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:27:34 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:27:34 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:27:34 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:27:34 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:27:48 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:27:48 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:27:48 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:27:48 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:32:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:32:03 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:32:03 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:32:03 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:32:03 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095b49d3ed9c5bd684106ef2762c8c8d6c733b6154e0f88da03b1e1966cd01df`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc91076ec4b38e804c65780f529812ce414a153e095f9380d5804984cbd9f76`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 2.1 MB (2138540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164efcce54726bc397834f6038e70f0f535de3989d1fae4a14d3ce829e318c63`  
		Last Modified: Mon, 08 Jun 2026 18:32:18 GMT  
		Size: 14.4 MB (14423785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965f08e1a921c3b4cbb9f84c6b9999ea0cc8c5df7c7ccac77ea6fd7ee24189af`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.68` - unknown; unknown

```console
$ docker pull httpd@sha256:7984379d541bad6433c6840f03d5a6bf3717cc96a23a6494d8edf4f56ff068c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fdcdd51ba0de4af51f758f1a67800b27772d0b16fc1acac13a6aa87399a87e`

```dockerfile
```

-	Layers:
	-	`sha256:8a0d0e0c231ec528ec3d98a2c72ca9b7759110af04cd9392138cbfeaf1d67dc9`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 2.3 MB (2296360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa23dd30e1d59efae1e2d867d4f568fe9d993722b873f57fa8d68feb138933c7`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 37.7 KB (37682 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.68` - linux; riscv64

```console
$ docker pull httpd@sha256:71876f06ab63bc1cf873ca7c7087faea82688f408c32b0224b7cb29aab33e4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43402754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75069b5306a498c987ffa1263618f82a1a44ddc86f83c3e6bde1350c1a246af6`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:27:50 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:27:50 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:27:50 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:27:50 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:42 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:42 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:42 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:42 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:51:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:51:09 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:51:09 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:51:09 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:51:09 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcb14ecded12a6ddea9368e3e0a89b321a0babb977a900740f77d9b2749c881`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6acad9c2eb5d55c394bbd6a1a2e6dc884a8bd713db7c37cd33e0deeaab271b`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 2.0 MB (1956437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691748d99998bcadae01e53818c1a0ba95d0e2ba99b846f20043d5e854281021`  
		Last Modified: Mon, 08 Jun 2026 18:52:16 GMT  
		Size: 13.2 MB (13168247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1562e123a42b9956e7d39d32f9976df80d047f431caf3c4862e78d656b7e2b7e`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.68` - unknown; unknown

```console
$ docker pull httpd@sha256:fa7de91aad897f1d9eaccd4e5213a25fb802222959c9f6c423886b4fb608fa8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2324290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e51d58413798f790228b33455088967cc44329474f1c5a0c94252c4d78a9a3`

```dockerfile
```

-	Layers:
	-	`sha256:9e13f24a27b58524719240f6484550131917ee8131886a36995d67d99f36a8cc`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 2.3 MB (2286607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30c4e22ef528cabad294d53b578ccf49631760a5a1caf405303bb050958ad5df`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 37.7 KB (37683 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.68` - linux; s390x

```console
$ docker pull httpd@sha256:2fa1944efe68dc19bf36d54e72ec18be919399545609955907759c62eef32556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45520012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6084b5dadfb37c1564dd4b7e44b3a1e4a405039e5715c0f39c241c50aaf0367b`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:27:38 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:27:38 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:27:38 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:27:38 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:27:44 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:27:44 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:27:44 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:27:44 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:29:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:29:45 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:29:45 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:29:45 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:29:45 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a516c95daee50c3e7a6296f522dd4fb560f14d2ca73476e1dafa47cde6b081b3`  
		Last Modified: Mon, 08 Jun 2026 18:29:57 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ffc60f849aa2b0a9016137736b47502e247d91bf7d8bdb0af208d49a528576`  
		Last Modified: Mon, 08 Jun 2026 18:29:58 GMT  
		Size: 2.0 MB (2036546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f468bbb1ef751e92d67c77000d3af1de92fc265b1a2b4e1cbb62ada60425a6`  
		Last Modified: Mon, 08 Jun 2026 18:29:58 GMT  
		Size: 13.6 MB (13637070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30130f264687b48d7a0583772d74472381b1bddbf747faebcfad8fb79fec2160`  
		Last Modified: Mon, 08 Jun 2026 18:29:57 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.68` - unknown; unknown

```console
$ docker pull httpd@sha256:a2f39309c230b1b17f2d4ddc53dd8c639603464ac50ea2a0b5e711225deaa4d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2331529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e8052bca557af655c176e8eec1e6ba8355618d3fa1333efab780db0eba9e1a`

```dockerfile
```

-	Layers:
	-	`sha256:0ec2b032ffb696485fe5fd2a728ef8da7d25712bb8327e496cd8643a40c8d333`  
		Last Modified: Mon, 08 Jun 2026 18:29:58 GMT  
		Size: 2.3 MB (2293918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18e3f08e0e7176d1ce05b52cfd66efa801891a3146c7bafe1e0a1034b73df332`  
		Last Modified: Mon, 08 Jun 2026 18:29:58 GMT  
		Size: 37.6 KB (37611 bytes)  
		MIME: application/vnd.in-toto+json

## `httpd:2.4.68-alpine`

```console
$ docker pull httpd@sha256:4a15e9c73f25334bc03cfb3c692c9adfc103bb46ca89cee1f0b9a5fcbc7b21f6
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

### `httpd:2.4.68-alpine` - linux; amd64

```console
$ docker pull httpd@sha256:bf087a7b1abe6bed280d6a69dcc3c8f17055bff4d86e8b52423c7ca52dbf1103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20742245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bdbd06577ba009805166768103f9a62685d9f97a9884b54388b1fa4bea9ecdd`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 18:31:25 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Jun 2026 18:31:25 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:31:25 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:31:25 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:31:25 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:31:26 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 08 Jun 2026 18:31:26 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:31:26 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:31:26 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:32:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:32:30 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:32:30 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:32:30 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:32:30 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce5804151ace48b62ad76238cde0765d43efa9396f491d9ec2d59b41a4fa8e1`  
		Last Modified: Mon, 08 Jun 2026 18:32:37 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db356f236e7a97cfe205045ad2895819d2fe9beecb1a8bd65fae6929cc6115a1`  
		Last Modified: Mon, 08 Jun 2026 18:32:37 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc5e0e38d81ae69af4435b5d5a5be213645e9c40200ddab1281a71efec26d94`  
		Last Modified: Mon, 08 Jun 2026 18:32:37 GMT  
		Size: 11.1 MB (11066958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af2e4b44c0574322eab72595901d051fdfd3dee1524b5d0f9177ecd7953cdc0`  
		Last Modified: Mon, 08 Jun 2026 18:32:37 GMT  
		Size: 5.8 MB (5809700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86856eeef9e12dbdc8ff4c7baebbd5cdefe872848eaf6ef2aef50eced2e7bd0e`  
		Last Modified: Mon, 08 Jun 2026 18:32:38 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.68-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:70c3c56d3d003dfac3b02abe58445b9d05b65eb48d2caf76a2aae4f16d351c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1239812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2a862ab34194b98abe1ad90fb1158234040d57fa2471ca197496507a8194920`

```dockerfile
```

-	Layers:
	-	`sha256:84e23f6554b8259dbd70956df3da92e26511e07ad4412a2a0a648cc51f4f4e78`  
		Last Modified: Mon, 08 Jun 2026 18:32:37 GMT  
		Size: 1.2 MB (1201606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc8b38586c1d8780912c3f004220df6b7649ed5c47efa43fa068ee9662f47caa`  
		Last Modified: Mon, 08 Jun 2026 18:32:36 GMT  
		Size: 38.2 KB (38206 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.68-alpine` - linux; arm variant v6

```console
$ docker pull httpd@sha256:024536b397c6ad22fa335218e0fb10fd1206c9fdb71dd7448c4f4f7fe16a8bc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19530438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979e382592d01f76ea45774429a342ecc5edef3ae3f0cdb9f569403603dd1cda`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 18:28:46 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Jun 2026 18:28:46 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:46 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:46 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:46 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:48 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:30:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:30:08 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:30:08 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:30:08 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:30:08 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8321b554dfa7c63a2afd55c8fb184b69858f457e8dfa9880f4bc448d8a39d4`  
		Last Modified: Mon, 08 Jun 2026 18:30:13 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09a332d4df7c9bee48b2d2de86966f85e36b64798eaaf67de0975e4f1555f89`  
		Last Modified: Mon, 08 Jun 2026 18:30:13 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215e98f908ff76704a82ca9d04a502bc930ce17a9047820920844edfd57fa760`  
		Last Modified: Mon, 08 Jun 2026 18:30:14 GMT  
		Size: 10.3 MB (10286319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ee63e2411212cd08a883b8c84dc993798a84b4de02db32551ee900d921c95e`  
		Last Modified: Mon, 08 Jun 2026 18:30:14 GMT  
		Size: 5.7 MB (5670856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e101d519540f8c8be21ad616e63d9f66a84ae618343405938dddad8bdeae5f6`  
		Last Modified: Mon, 08 Jun 2026 18:30:15 GMT  
		Size: 289.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.68-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:fc8f3318e4ab42107e49368c4f569a975957bd9af2efab2cec507177830cda11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb4db6d5f35a09c872dde41878646504db7ebdfdc3744e4f6986726e057c671`

```dockerfile
```

-	Layers:
	-	`sha256:6e8897e1452670de76c435a27c21f0d31afad8b78d64fa84fdaffa8c052e60a6`  
		Last Modified: Mon, 08 Jun 2026 18:30:13 GMT  
		Size: 38.1 KB (38142 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.68-alpine` - linux; arm variant v7

```console
$ docker pull httpd@sha256:8061dc7af76065401d58b4b0517719208ee34c8923c83d30cffdd47abc0aa401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18701347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aab2fe87d7e0e05ed925969046f55ddf1ef27740b6067ba4161f1928c96e254`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 18:30:37 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Jun 2026 18:30:37 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:30:37 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:30:37 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:30:37 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:30:39 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 08 Jun 2026 18:30:39 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:30:39 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:30:39 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:31:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:31:55 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:31:55 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:31:55 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:31:55 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ad8e36bc25e31e63d7c1a292ea9f35a3df589ad01be37b48a4ac3ae9fc0847`  
		Last Modified: Mon, 08 Jun 2026 18:32:01 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfec7351aad4a1810cd117ec6fda31c0b8b9af893f2d6755fe6e474e5edc16a`  
		Last Modified: Mon, 08 Jun 2026 18:32:01 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89db8edd72fdbfd84fe9a186dbe1fa7539829347879a957a070d49ccc276ef92`  
		Last Modified: Mon, 08 Jun 2026 18:32:02 GMT  
		Size: 10.1 MB (10062859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7c853cb79a0e47b775a4cb5ed20a4fa1f0fa54a2a4a8fc43c5e2c52e10a4dd`  
		Last Modified: Mon, 08 Jun 2026 18:32:02 GMT  
		Size: 5.4 MB (5353967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4dfbc2ff27845415d637069fa7548a00c66b9364660c093067578b62d6d650`  
		Last Modified: Mon, 08 Jun 2026 18:32:03 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.68-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:9d340e705b4d2d4d5357cabee9b78bdebcd67b0dc92a2435cc1e019af5338324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1242371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53499d0e69d22627cf589b7d2118279c706b905969b2b30fe01ebd143120c86c`

```dockerfile
```

-	Layers:
	-	`sha256:a78794fe77e35b91f4ccad718d8777e6c1c5cd52d6a272f4cd53482c4a88cdda`  
		Last Modified: Mon, 08 Jun 2026 18:32:02 GMT  
		Size: 1.2 MB (1204014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e1fe4c2a693f67e2ff7c45c79009d14ddf8c3005f4b3747c700d1530f9d7fe6`  
		Last Modified: Mon, 08 Jun 2026 18:32:01 GMT  
		Size: 38.4 KB (38357 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.68-alpine` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:85b4776185fbee81f2ccf80b645c10d5d2a5eadc8004a038d38784682f667ffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21163903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d2c617afd2009094a1862af906977d4bd5a6a9fcfc1ef8cb27061905000692`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 18:30:27 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Jun 2026 18:30:27 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:30:27 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:30:27 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:30:27 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:30:28 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 08 Jun 2026 18:30:28 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:30:28 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:30:28 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:31:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:31:36 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:31:36 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:31:36 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:31:36 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2733de7154d76386a001a868473ab506efdc9813265b2e519d49513c0c0ca4c4`  
		Last Modified: Mon, 08 Jun 2026 18:31:43 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a593c24a6a1b8072f379a89d7870d2df90bb18d23f56ac71aee739dfe20489ec`  
		Last Modified: Mon, 08 Jun 2026 18:31:43 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b0d2c4d83de418eef5171c3593da6a8e7caa221b1af072d6936c20d6b74a25`  
		Last Modified: Mon, 08 Jun 2026 18:31:44 GMT  
		Size: 11.0 MB (11034000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa7baf1e3c92a7533ea08f8fdd39cd5280b65628d1c6c62793565d5e1743a6f`  
		Last Modified: Mon, 08 Jun 2026 18:31:44 GMT  
		Size: 5.9 MB (5928633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3ca4765694b549352106668014c1d542f93d13adf1f177a9a956461ed5492c`  
		Last Modified: Mon, 08 Jun 2026 18:31:44 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.68-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:4af10a58bed505a14c1108a84db0aaa27d666395366e84db3677085d87d207df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1239463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0f41e9cde0dc8d8ccf71126bd2f783f7f8231c70316ba7fe767a9230fa4bb8`

```dockerfile
```

-	Layers:
	-	`sha256:13468312a748d8b51aaf3a82ad0f3271775ef5301c38d37fbd6196359c20d00a`  
		Last Modified: Mon, 08 Jun 2026 18:31:44 GMT  
		Size: 1.2 MB (1201060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1470375ebacc02386973357f8aab79e0f87c8d365f1ff6dbcdb17779e96c813b`  
		Last Modified: Mon, 08 Jun 2026 18:31:43 GMT  
		Size: 38.4 KB (38403 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.68-alpine` - linux; 386

```console
$ docker pull httpd@sha256:16b1c94bd801f2d8832b0683f76414905177be78ab8e40a633e7ec0890433857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (20021926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c38ed0bd74cceb6792e9d929d312d54bc80e7cde0e19948ffd46cb48f7ab757`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 18:31:21 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Jun 2026 18:31:21 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:31:21 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:31:21 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:31:21 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:31:23 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 08 Jun 2026 18:31:23 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:31:23 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:31:23 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:32:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:32:39 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:32:39 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:32:39 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:32:39 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056f17e7b6ddfb0a1da905574c6263028f20b340ff9666ae47cfa26135676670`  
		Last Modified: Mon, 08 Jun 2026 18:32:46 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21afa337e01a5d443d84b004f17c160335eb4219e04af1e9c70ceb3707efbce0`  
		Last Modified: Mon, 08 Jun 2026 18:32:46 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbfae095ca14e5295651305f917acc6f71a2fbd5f49b85a3fc2c57e03b2be3d`  
		Last Modified: Mon, 08 Jun 2026 18:32:46 GMT  
		Size: 10.6 MB (10618085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc33c24b7089af8156a61a652ed7c5fe322baa0d78dcb691295bb589a0de453`  
		Last Modified: Mon, 08 Jun 2026 18:32:46 GMT  
		Size: 5.7 MB (5711996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b50c0cd8edcb1ed19a9637f074a4770f9a6f876606cae56220092e6243e576`  
		Last Modified: Mon, 08 Jun 2026 18:32:47 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.68-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:740f2dd920cb4f5bedec74d3f44ed0b9c47bf46d2e8b0b13557276827bcdc52e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1239709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f14334929789a57deae0012f30aba319525e7ff989e36134d070c56a6dd94dc`

```dockerfile
```

-	Layers:
	-	`sha256:d0dacd457b618139c482a7d6afa2041ffd6cb707e33b66acf044aaefaa14397e`  
		Last Modified: Mon, 08 Jun 2026 18:32:46 GMT  
		Size: 1.2 MB (1201561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44183710a388aa4b94ef6d14e896b787a7e08a8f608a9c14d36001d21668c987`  
		Last Modified: Mon, 08 Jun 2026 18:32:46 GMT  
		Size: 38.1 KB (38148 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.68-alpine` - linux; ppc64le

```console
$ docker pull httpd@sha256:24c446eba8c10efd7206d9e55e728f1787228d1442aa6ef61ac7a0d515cce4ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21381418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a448835add6f4d91f1982c6a872fe649b29ed77425b2e9e5aa901dd5e301205f`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 18:27:34 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Jun 2026 18:27:34 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:27:34 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:27:34 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:27:35 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:27:38 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 08 Jun 2026 18:27:38 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:27:38 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:27:38 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:29:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:29:29 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:29:29 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:29:29 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:29:29 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3833350820ce2613df1f0a4261df6ce7bc4951ba5dba44ef1a833641790aaaa`  
		Last Modified: Mon, 08 Jun 2026 18:29:47 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e9193af3a9c4cd580ff4cb24c30058cbec15dd6378f5950513a68c769c281f`  
		Last Modified: Mon, 08 Jun 2026 18:29:47 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a872efdd830ec45ac7efd740e333bf2cb140e2f4b94e60dd878415304be4b613`  
		Last Modified: Mon, 08 Jun 2026 18:29:47 GMT  
		Size: 11.3 MB (11338111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7513aa3438c9c2feecadf91e523239d954d60ceddaeda0f6e6763e2235eb9d35`  
		Last Modified: Mon, 08 Jun 2026 18:29:47 GMT  
		Size: 6.2 MB (6210978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47983e84280f04dea9f420f8879dc16efab9198e05c7c6d79eae3fe957261a48`  
		Last Modified: Mon, 08 Jun 2026 18:29:48 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.68-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:17e67c7acec63724871964de2c8a364fb31631efd6f458ddd90235490b789f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1239293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77c39681778c5b28492be2b18b099ed022a8b09c86791dd235685cbc511448b`

```dockerfile
```

-	Layers:
	-	`sha256:aa63ded6d68a8c82088e414a0d5b803f2cf467747fc6fe33326dd7f4a8ff1d61`  
		Last Modified: Mon, 08 Jun 2026 18:29:47 GMT  
		Size: 1.2 MB (1201013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:772db10801a309da7fa867f9755115f0e7af393467440d9c2ba6a20824bfd7a0`  
		Last Modified: Mon, 08 Jun 2026 18:29:47 GMT  
		Size: 38.3 KB (38280 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.68-alpine` - linux; riscv64

```console
$ docker pull httpd@sha256:6e901fc55fc925beed4d9e227553864af8d4da401692c898b3ba5d6198aa89e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19923429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94d1b25cfd3edbe24497157b752ff6f1b0bae2216ac56a9695500c96025ef0d8`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 18:52:56 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Jun 2026 18:52:56 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:52:56 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:52:56 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:52:57 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:53:04 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 08 Jun 2026 18:53:04 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:53:04 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:53:04 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 19:03:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 08 Jun 2026 19:03:07 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 19:03:07 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 19:03:07 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 19:03:07 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19c7f0762250b0cc52b39bb993e944c7a467ccbba9e5982b3e05a892ed00e09`  
		Last Modified: Mon, 08 Jun 2026 19:03:57 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948f4b41e7172c5b397872ec12028b50e89c8b1945bcdd382f3c4354d3816a6c`  
		Last Modified: Mon, 08 Jun 2026 19:03:57 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839bf3cd8868f427bc3edaf740a5070b32162d92911d6135ad7452faf74806e2`  
		Last Modified: Mon, 08 Jun 2026 19:04:00 GMT  
		Size: 10.5 MB (10512864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0ed49d6165d488e835183bba68a905603e14ef7c9d532d89556389e587cdb6`  
		Last Modified: Mon, 08 Jun 2026 19:03:59 GMT  
		Size: 5.8 MB (5821504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9212c34deb579c5504ab192148ff204061b0646ae26b63cc9ad5ed1aad1789c`  
		Last Modified: Mon, 08 Jun 2026 19:03:59 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.68-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:536fbac1930d7f288da7460218490b036b05488c57b17e046817cfca2d991009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1239289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63060237e36817f0674dfd5a4486b1ecb06b72e44a91033e3d2fc30181462368`

```dockerfile
```

-	Layers:
	-	`sha256:106695ede26a0f693625ca363327da8a1cf3bbdf11f35f67bf2ed2a8b03aa116`  
		Last Modified: Mon, 08 Jun 2026 19:03:58 GMT  
		Size: 1.2 MB (1201009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efd7b10cf0eb8a6248093104323312312d5e4f5d818a591a147f6a252df1d07d`  
		Last Modified: Mon, 08 Jun 2026 19:03:58 GMT  
		Size: 38.3 KB (38280 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.68-alpine` - linux; s390x

```console
$ docker pull httpd@sha256:6283359189b28f3ca4b868bf776ceb2b692e4add8fea4a8b3269d66b7753a935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21378874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2df8884703c6d4ccc1f8733cfd8210fb8eb0924b8b0b633ac84af6641b17fbd`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 18:27:38 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Jun 2026 18:27:38 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:27:38 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:27:38 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:27:38 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:27:40 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 08 Jun 2026 18:27:40 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:27:40 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:27:40 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:28:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:28:46 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:28:46 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:28:46 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:28:46 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548235140cb8c1ab10d4692027815816cc2544f4ec8835eba3f51db5727af171`  
		Last Modified: Mon, 08 Jun 2026 18:28:59 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369bc1e79711eb6126c37a7b565cc2b0f42d4ee767040a1f8b44f857f5adef9a`  
		Last Modified: Mon, 08 Jun 2026 18:28:59 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59e8a1afdfdaee57b84923042e279cf1dc1f97d76646bf9caebc7a940d504ca`  
		Last Modified: Mon, 08 Jun 2026 18:28:59 GMT  
		Size: 11.6 MB (11649300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138c5a50960e95cfc40f091bc4080b810eb24455ad217b422125a22d86f5284d`  
		Last Modified: Mon, 08 Jun 2026 18:28:59 GMT  
		Size: 6.0 MB (6001640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c831663f14f23188df97e6b051c05bf1da28f9a4c18fc2c2cad0bdaff1429eb`  
		Last Modified: Mon, 08 Jun 2026 18:29:00 GMT  
		Size: 289.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.68-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:5cc2f04b98cd0e537a6eb5f791971f720a637c2255c7f4758ec7d5e301ba4612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1239161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8474478033f363a3cbf719bfac24a8e06adef6eccc522a4b3c2748dda664f13`

```dockerfile
```

-	Layers:
	-	`sha256:0b586450d6cc931e529e0fe9520eca240e9996721ea62991acd52c3c73de9ee9`  
		Last Modified: Mon, 08 Jun 2026 18:28:59 GMT  
		Size: 1.2 MB (1200955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d691c6da1d20a4d1e620abc97c146c35e966efbc00988d6f0d5c0941364e3a49`  
		Last Modified: Mon, 08 Jun 2026 18:28:58 GMT  
		Size: 38.2 KB (38206 bytes)  
		MIME: application/vnd.in-toto+json

## `httpd:2.4.68-alpine3.24`

**does not exist** (yet?)

## `httpd:2.4.68-trixie`

```console
$ docker pull httpd@sha256:bda12def1dc3b718a5314b4b26ca84927fdb3905091f11200d581186f240e4f6
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

### `httpd:2.4.68-trixie` - linux; amd64

```console
$ docker pull httpd@sha256:2b7d8a7992076bf5ceb8bb363b4c8f2b8c655072e7478f45c5e537af28f6c167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45230035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb74261f37ff6970ccb87626c9783304249efaad9f4e8cd32de4e9a3423b787d`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:48 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:48 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:48 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:53 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:30:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:30:55 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:30:55 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:30:55 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:30:55 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51757aae13a97369966a219edcf9e0f9b8cc8eaec050732a5d6fa25aa92e453`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c211dc8965131703cc3952b6267904624b637fc549d23e2e6bc0cc49b4222c`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 2.0 MB (1997894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc6b5038f865e4e495fc8fe09d6f11876069a408d170c40399b49126c800041`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 13.5 MB (13451745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9e979b34b8fed3ce647410b3644cc8cc46ef92761363f08fe8802169d5f76f`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.68-trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:fce1019bd8cc87b008a72778b2a2736ddff548e62baa27c4cc983db009cb5111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597fd853705160154b2bcd70d98acc6933b1b6dcf3f31cb013b0abcf1068d207`

```dockerfile
```

-	Layers:
	-	`sha256:e2025809a7e3749824decea45c53ede352d4aa58d75ace93dd07000d2b6c08a6`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 2.3 MB (2292510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:492c10869e234a6f6ccfabd1a0dfc280cec64fa0e207fc564413cc8da21c9610`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 37.6 KB (37611 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.68-trixie` - linux; arm variant v5

```console
$ docker pull httpd@sha256:f361c4b24b78e1239dfeacd9d9dab2c93ea638455fd3c3b70dbbda6ab00a15f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42857065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ab2c2872db9a8045fa1ab91711e556824fe075bbaca19941f6e9bd8271bc48`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:48 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:48 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:48 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:58 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:58 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:58 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:58 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:31:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:31:48 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:31:48 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:31:48 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:31:48 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8741492638bd207b4038604a6e65e467c0a410df6afca31a4821aee832c662ab`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c069dc93d7fb7eba3c5388a00541788a95bc11398d69b0c81da9efc258d2c8d`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 1.9 MB (1912804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6002f904e7facf1cc93c7790b09f0609b922e15005a489e32e61b6fbc4316ad8`  
		Last Modified: Mon, 08 Jun 2026 18:31:57 GMT  
		Size: 13.0 MB (12989920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8efcbe4a582c8775afea0836d968f1f184bea5c26e21fe0fcbb5a0e7ebd3ff05`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.68-trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:f2ce1a9cefdbe977111087f3b75c7be0784ea835d0007b5a145ed2f6bfa0c95b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dfbb9b9cb8c42912b42a91046224acc7dc556f1e7d8097a01121fd91f76b72`

```dockerfile
```

-	Layers:
	-	`sha256:80fc7202154b749a8075c448c7e7a9a60d1d4f341914b54da5153b7ee3c03f5f`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 2.3 MB (2295542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27e7b847f32a118618968bc07cffc9a5d6d0c0692dee15129ee923129b35c1b4`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 37.7 KB (37749 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.68-trixie` - linux; arm variant v7

```console
$ docker pull httpd@sha256:5236d5c6a10645ecac76238b7ca6f921ca8eb5ea92ab6fb293bdadae95b10ae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40548022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b12f00662f2acddd392078f235516594259077bf34e4c06e06e8288f24df443`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:54 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:54 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:54 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:54 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:29:01 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:29:01 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:29:01 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:29:01 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:31:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:31:27 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:31:27 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:31:27 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:31:27 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7617084195012707e889cdef4236f6627014b19baf5baa53b8e432880268bc`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada685e6861770db8d1c2090eecdecab5e8ae6dec8c9abc23fb86d844f8bb442`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 1.8 MB (1823341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a919558fd039a1b681fc7341aeb407767fa365ac621427a2d7bf5470f9eecc9`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 12.5 MB (12518379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a44ce25dab735595c229a5d37494e00da9b3a541edbcdd85d4f3e488c4175fd`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.68-trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:9db1b877234f01aa36272fba11532263d7a52f145aec8d4364b98deaca6fa87b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2331805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f897acfbf506ea853c77e9a461c832030fe5a6a95cb3bf116d12f565be924b5d`

```dockerfile
```

-	Layers:
	-	`sha256:1b5b5d4bbe67bc086194dd58eb01ec30a9bf78e7498afd570946311fcc5bbb5a`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 2.3 MB (2294057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d14fc4d73d1b623729ae4e87803dc741f0309a1a9e8d3661bd235890bb441fa`  
		Last Modified: Mon, 08 Jun 2026 18:31:35 GMT  
		Size: 37.7 KB (37748 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.68-trixie` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:05f92a0b3df99246bd094967c40d5f00311b04b74e91386ab37f3879d5b6398f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45500798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab09468e72a3fd55b26758d03ba2f8a094a6de075771c949ee820cd22f4efd4`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:48 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:48 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:48 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:53 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:30:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:30:55 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:30:55 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:30:55 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:30:55 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51757aae13a97369966a219edcf9e0f9b8cc8eaec050732a5d6fa25aa92e453`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbc1d9c94781b6fb204e9f2dd48fa707b639991a0ed9e6832bc627ee78eb793`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 2.0 MB (1971344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1897ad34a45ba49cd3bd04d81eb169b2fa80642c8bdeb1783ba8067376d69911`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 13.4 MB (13387063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8048fc63017cda60558664fdef734dbe334a9ef8bb646c61060a28ea79cc2c73`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.68-trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:77551cd106fe5e6dba8ab22968dcc1c2157130fb9d1ce1f165884126ef2ff11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e103ca667e4eca8f7df1a1a1760fe83de402a3064636034eca87b9551b8abeac`

```dockerfile
```

-	Layers:
	-	`sha256:9983bb17dc86db43f7ba9dfb576ff96e6213f15e4868de93bd9ac8b5b38533a0`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 2.3 MB (2292847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d696410da2eb0504c27136882e9ac61fe5c021897524d3583611c2d09de3a6ca`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 37.8 KB (37793 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.68-trixie` - linux; 386

```console
$ docker pull httpd@sha256:d212f60d1de6a98f8ac5666c0f08cfb2f8d7e69c007bba602a46c8f59d8c4346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46572612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a675fd0fcf287e70a1c2a01d7ad90a4f9db4df857ba19faf767c6dd59fc412`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:49 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:49 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:49 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:49 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:55 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:55 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:55 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:55 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:31:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:31:06 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:31:06 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:31:06 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:31:06 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3f98973d06c4dd876d5ba79c06211d3cd1cea32db869157acf4434836e75b5`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82349a6b654d1e29b5f624fa403272758a3418fe2d7860fc0f98cecee1da801b`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 2.1 MB (2055642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d9f1f37b024e8db99b29e69ec67af1bc894362b189a8cce9327b62ba4c0ff8`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 13.2 MB (13221163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6acaba897604b124ab0b4b16b6083da00590bfa6de43cb198468a35afbc076`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.68-trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:af18d97787c89c98c8fc110c23887ed1e760fb3f9207c6089ead4f50f78ceba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2327164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a81fe9a487688b93159da3a042732411446e801c6adf453f8f6a9878133adf`

```dockerfile
```

-	Layers:
	-	`sha256:fafa740c092dc2c2d150c0a3988c531e569690a6361dd41d57a1faec9324d3e4`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 2.3 MB (2289609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c62eb654a7ce8c3c1529835aa36c0de0488098dd817dd2b7968f541c9be78d7b`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 37.6 KB (37555 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.68-trixie` - linux; ppc64le

```console
$ docker pull httpd@sha256:23250993ffdf8415ee5424cdeff8f5dff52a26bff21436f6567a702b755c8cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50163250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e58559fc8be957d33533107f22829d2774b9656a856245cd16510b077a31578`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:27:34 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:27:34 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:27:34 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:27:34 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:27:48 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:27:48 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:27:48 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:27:48 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:32:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:32:03 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:32:03 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:32:03 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:32:03 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095b49d3ed9c5bd684106ef2762c8c8d6c733b6154e0f88da03b1e1966cd01df`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc91076ec4b38e804c65780f529812ce414a153e095f9380d5804984cbd9f76`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 2.1 MB (2138540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164efcce54726bc397834f6038e70f0f535de3989d1fae4a14d3ce829e318c63`  
		Last Modified: Mon, 08 Jun 2026 18:32:18 GMT  
		Size: 14.4 MB (14423785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965f08e1a921c3b4cbb9f84c6b9999ea0cc8c5df7c7ccac77ea6fd7ee24189af`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.68-trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:7984379d541bad6433c6840f03d5a6bf3717cc96a23a6494d8edf4f56ff068c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fdcdd51ba0de4af51f758f1a67800b27772d0b16fc1acac13a6aa87399a87e`

```dockerfile
```

-	Layers:
	-	`sha256:8a0d0e0c231ec528ec3d98a2c72ca9b7759110af04cd9392138cbfeaf1d67dc9`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 2.3 MB (2296360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa23dd30e1d59efae1e2d867d4f568fe9d993722b873f57fa8d68feb138933c7`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 37.7 KB (37682 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.68-trixie` - linux; riscv64

```console
$ docker pull httpd@sha256:71876f06ab63bc1cf873ca7c7087faea82688f408c32b0224b7cb29aab33e4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43402754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75069b5306a498c987ffa1263618f82a1a44ddc86f83c3e6bde1350c1a246af6`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:27:50 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:27:50 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:27:50 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:27:50 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:42 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:42 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:42 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:42 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:51:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:51:09 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:51:09 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:51:09 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:51:09 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcb14ecded12a6ddea9368e3e0a89b321a0babb977a900740f77d9b2749c881`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6acad9c2eb5d55c394bbd6a1a2e6dc884a8bd713db7c37cd33e0deeaab271b`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 2.0 MB (1956437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691748d99998bcadae01e53818c1a0ba95d0e2ba99b846f20043d5e854281021`  
		Last Modified: Mon, 08 Jun 2026 18:52:16 GMT  
		Size: 13.2 MB (13168247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1562e123a42b9956e7d39d32f9976df80d047f431caf3c4862e78d656b7e2b7e`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.68-trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:fa7de91aad897f1d9eaccd4e5213a25fb802222959c9f6c423886b4fb608fa8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2324290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e51d58413798f790228b33455088967cc44329474f1c5a0c94252c4d78a9a3`

```dockerfile
```

-	Layers:
	-	`sha256:9e13f24a27b58524719240f6484550131917ee8131886a36995d67d99f36a8cc`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 2.3 MB (2286607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30c4e22ef528cabad294d53b578ccf49631760a5a1caf405303bb050958ad5df`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 37.7 KB (37683 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.68-trixie` - linux; s390x

```console
$ docker pull httpd@sha256:2fa1944efe68dc19bf36d54e72ec18be919399545609955907759c62eef32556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45520012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6084b5dadfb37c1564dd4b7e44b3a1e4a405039e5715c0f39c241c50aaf0367b`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:27:38 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:27:38 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:27:38 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:27:38 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:27:44 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:27:44 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:27:44 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:27:44 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:29:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:29:45 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:29:45 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:29:45 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:29:45 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a516c95daee50c3e7a6296f522dd4fb560f14d2ca73476e1dafa47cde6b081b3`  
		Last Modified: Mon, 08 Jun 2026 18:29:57 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ffc60f849aa2b0a9016137736b47502e247d91bf7d8bdb0af208d49a528576`  
		Last Modified: Mon, 08 Jun 2026 18:29:58 GMT  
		Size: 2.0 MB (2036546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f468bbb1ef751e92d67c77000d3af1de92fc265b1a2b4e1cbb62ada60425a6`  
		Last Modified: Mon, 08 Jun 2026 18:29:58 GMT  
		Size: 13.6 MB (13637070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30130f264687b48d7a0583772d74472381b1bddbf747faebcfad8fb79fec2160`  
		Last Modified: Mon, 08 Jun 2026 18:29:57 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.68-trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:a2f39309c230b1b17f2d4ddc53dd8c639603464ac50ea2a0b5e711225deaa4d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2331529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e8052bca557af655c176e8eec1e6ba8355618d3fa1333efab780db0eba9e1a`

```dockerfile
```

-	Layers:
	-	`sha256:0ec2b032ffb696485fe5fd2a728ef8da7d25712bb8327e496cd8643a40c8d333`  
		Last Modified: Mon, 08 Jun 2026 18:29:58 GMT  
		Size: 2.3 MB (2293918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18e3f08e0e7176d1ce05b52cfd66efa801891a3146c7bafe1e0a1034b73df332`  
		Last Modified: Mon, 08 Jun 2026 18:29:58 GMT  
		Size: 37.6 KB (37611 bytes)  
		MIME: application/vnd.in-toto+json

## `httpd:alpine`

```console
$ docker pull httpd@sha256:4a15e9c73f25334bc03cfb3c692c9adfc103bb46ca89cee1f0b9a5fcbc7b21f6
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

### `httpd:alpine` - linux; amd64

```console
$ docker pull httpd@sha256:bf087a7b1abe6bed280d6a69dcc3c8f17055bff4d86e8b52423c7ca52dbf1103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20742245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bdbd06577ba009805166768103f9a62685d9f97a9884b54388b1fa4bea9ecdd`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 18:31:25 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Jun 2026 18:31:25 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:31:25 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:31:25 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:31:25 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:31:26 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 08 Jun 2026 18:31:26 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:31:26 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:31:26 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:32:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:32:30 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:32:30 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:32:30 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:32:30 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce5804151ace48b62ad76238cde0765d43efa9396f491d9ec2d59b41a4fa8e1`  
		Last Modified: Mon, 08 Jun 2026 18:32:37 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db356f236e7a97cfe205045ad2895819d2fe9beecb1a8bd65fae6929cc6115a1`  
		Last Modified: Mon, 08 Jun 2026 18:32:37 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc5e0e38d81ae69af4435b5d5a5be213645e9c40200ddab1281a71efec26d94`  
		Last Modified: Mon, 08 Jun 2026 18:32:37 GMT  
		Size: 11.1 MB (11066958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af2e4b44c0574322eab72595901d051fdfd3dee1524b5d0f9177ecd7953cdc0`  
		Last Modified: Mon, 08 Jun 2026 18:32:37 GMT  
		Size: 5.8 MB (5809700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86856eeef9e12dbdc8ff4c7baebbd5cdefe872848eaf6ef2aef50eced2e7bd0e`  
		Last Modified: Mon, 08 Jun 2026 18:32:38 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:70c3c56d3d003dfac3b02abe58445b9d05b65eb48d2caf76a2aae4f16d351c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1239812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2a862ab34194b98abe1ad90fb1158234040d57fa2471ca197496507a8194920`

```dockerfile
```

-	Layers:
	-	`sha256:84e23f6554b8259dbd70956df3da92e26511e07ad4412a2a0a648cc51f4f4e78`  
		Last Modified: Mon, 08 Jun 2026 18:32:37 GMT  
		Size: 1.2 MB (1201606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc8b38586c1d8780912c3f004220df6b7649ed5c47efa43fa068ee9662f47caa`  
		Last Modified: Mon, 08 Jun 2026 18:32:36 GMT  
		Size: 38.2 KB (38206 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine` - linux; arm variant v6

```console
$ docker pull httpd@sha256:024536b397c6ad22fa335218e0fb10fd1206c9fdb71dd7448c4f4f7fe16a8bc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19530438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979e382592d01f76ea45774429a342ecc5edef3ae3f0cdb9f569403603dd1cda`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 18:28:46 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Jun 2026 18:28:46 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:46 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:46 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:46 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:48 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:30:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:30:08 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:30:08 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:30:08 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:30:08 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8321b554dfa7c63a2afd55c8fb184b69858f457e8dfa9880f4bc448d8a39d4`  
		Last Modified: Mon, 08 Jun 2026 18:30:13 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09a332d4df7c9bee48b2d2de86966f85e36b64798eaaf67de0975e4f1555f89`  
		Last Modified: Mon, 08 Jun 2026 18:30:13 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:215e98f908ff76704a82ca9d04a502bc930ce17a9047820920844edfd57fa760`  
		Last Modified: Mon, 08 Jun 2026 18:30:14 GMT  
		Size: 10.3 MB (10286319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ee63e2411212cd08a883b8c84dc993798a84b4de02db32551ee900d921c95e`  
		Last Modified: Mon, 08 Jun 2026 18:30:14 GMT  
		Size: 5.7 MB (5670856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e101d519540f8c8be21ad616e63d9f66a84ae618343405938dddad8bdeae5f6`  
		Last Modified: Mon, 08 Jun 2026 18:30:15 GMT  
		Size: 289.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:fc8f3318e4ab42107e49368c4f569a975957bd9af2efab2cec507177830cda11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.1 KB (38142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbb4db6d5f35a09c872dde41878646504db7ebdfdc3744e4f6986726e057c671`

```dockerfile
```

-	Layers:
	-	`sha256:6e8897e1452670de76c435a27c21f0d31afad8b78d64fa84fdaffa8c052e60a6`  
		Last Modified: Mon, 08 Jun 2026 18:30:13 GMT  
		Size: 38.1 KB (38142 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine` - linux; arm variant v7

```console
$ docker pull httpd@sha256:8061dc7af76065401d58b4b0517719208ee34c8923c83d30cffdd47abc0aa401
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18701347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aab2fe87d7e0e05ed925969046f55ddf1ef27740b6067ba4161f1928c96e254`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 18:30:37 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Jun 2026 18:30:37 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:30:37 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:30:37 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:30:37 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:30:39 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 08 Jun 2026 18:30:39 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:30:39 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:30:39 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:31:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:31:55 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:31:55 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:31:55 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:31:55 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ad8e36bc25e31e63d7c1a292ea9f35a3df589ad01be37b48a4ac3ae9fc0847`  
		Last Modified: Mon, 08 Jun 2026 18:32:01 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfec7351aad4a1810cd117ec6fda31c0b8b9af893f2d6755fe6e474e5edc16a`  
		Last Modified: Mon, 08 Jun 2026 18:32:01 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89db8edd72fdbfd84fe9a186dbe1fa7539829347879a957a070d49ccc276ef92`  
		Last Modified: Mon, 08 Jun 2026 18:32:02 GMT  
		Size: 10.1 MB (10062859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7c853cb79a0e47b775a4cb5ed20a4fa1f0fa54a2a4a8fc43c5e2c52e10a4dd`  
		Last Modified: Mon, 08 Jun 2026 18:32:02 GMT  
		Size: 5.4 MB (5353967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4dfbc2ff27845415d637069fa7548a00c66b9364660c093067578b62d6d650`  
		Last Modified: Mon, 08 Jun 2026 18:32:03 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:9d340e705b4d2d4d5357cabee9b78bdebcd67b0dc92a2435cc1e019af5338324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1242371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53499d0e69d22627cf589b7d2118279c706b905969b2b30fe01ebd143120c86c`

```dockerfile
```

-	Layers:
	-	`sha256:a78794fe77e35b91f4ccad718d8777e6c1c5cd52d6a272f4cd53482c4a88cdda`  
		Last Modified: Mon, 08 Jun 2026 18:32:02 GMT  
		Size: 1.2 MB (1204014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e1fe4c2a693f67e2ff7c45c79009d14ddf8c3005f4b3747c700d1530f9d7fe6`  
		Last Modified: Mon, 08 Jun 2026 18:32:01 GMT  
		Size: 38.4 KB (38357 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:85b4776185fbee81f2ccf80b645c10d5d2a5eadc8004a038d38784682f667ffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21163903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d2c617afd2009094a1862af906977d4bd5a6a9fcfc1ef8cb27061905000692`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 18:30:27 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Jun 2026 18:30:27 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:30:27 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:30:27 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:30:27 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:30:28 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 08 Jun 2026 18:30:28 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:30:28 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:30:28 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:31:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:31:36 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:31:36 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:31:36 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:31:36 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2733de7154d76386a001a868473ab506efdc9813265b2e519d49513c0c0ca4c4`  
		Last Modified: Mon, 08 Jun 2026 18:31:43 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a593c24a6a1b8072f379a89d7870d2df90bb18d23f56ac71aee739dfe20489ec`  
		Last Modified: Mon, 08 Jun 2026 18:31:43 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b0d2c4d83de418eef5171c3593da6a8e7caa221b1af072d6936c20d6b74a25`  
		Last Modified: Mon, 08 Jun 2026 18:31:44 GMT  
		Size: 11.0 MB (11034000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa7baf1e3c92a7533ea08f8fdd39cd5280b65628d1c6c62793565d5e1743a6f`  
		Last Modified: Mon, 08 Jun 2026 18:31:44 GMT  
		Size: 5.9 MB (5928633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3ca4765694b549352106668014c1d542f93d13adf1f177a9a956461ed5492c`  
		Last Modified: Mon, 08 Jun 2026 18:31:44 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:4af10a58bed505a14c1108a84db0aaa27d666395366e84db3677085d87d207df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1239463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0f41e9cde0dc8d8ccf71126bd2f783f7f8231c70316ba7fe767a9230fa4bb8`

```dockerfile
```

-	Layers:
	-	`sha256:13468312a748d8b51aaf3a82ad0f3271775ef5301c38d37fbd6196359c20d00a`  
		Last Modified: Mon, 08 Jun 2026 18:31:44 GMT  
		Size: 1.2 MB (1201060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1470375ebacc02386973357f8aab79e0f87c8d365f1ff6dbcdb17779e96c813b`  
		Last Modified: Mon, 08 Jun 2026 18:31:43 GMT  
		Size: 38.4 KB (38403 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine` - linux; 386

```console
$ docker pull httpd@sha256:16b1c94bd801f2d8832b0683f76414905177be78ab8e40a633e7ec0890433857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (20021926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c38ed0bd74cceb6792e9d929d312d54bc80e7cde0e19948ffd46cb48f7ab757`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 18:31:21 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Jun 2026 18:31:21 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:31:21 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:31:21 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:31:21 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:31:23 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 08 Jun 2026 18:31:23 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:31:23 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:31:23 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:32:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:32:39 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:32:39 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:32:39 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:32:39 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056f17e7b6ddfb0a1da905574c6263028f20b340ff9666ae47cfa26135676670`  
		Last Modified: Mon, 08 Jun 2026 18:32:46 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21afa337e01a5d443d84b004f17c160335eb4219e04af1e9c70ceb3707efbce0`  
		Last Modified: Mon, 08 Jun 2026 18:32:46 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbfae095ca14e5295651305f917acc6f71a2fbd5f49b85a3fc2c57e03b2be3d`  
		Last Modified: Mon, 08 Jun 2026 18:32:46 GMT  
		Size: 10.6 MB (10618085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc33c24b7089af8156a61a652ed7c5fe322baa0d78dcb691295bb589a0de453`  
		Last Modified: Mon, 08 Jun 2026 18:32:46 GMT  
		Size: 5.7 MB (5711996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b50c0cd8edcb1ed19a9637f074a4770f9a6f876606cae56220092e6243e576`  
		Last Modified: Mon, 08 Jun 2026 18:32:47 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:740f2dd920cb4f5bedec74d3f44ed0b9c47bf46d2e8b0b13557276827bcdc52e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1239709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f14334929789a57deae0012f30aba319525e7ff989e36134d070c56a6dd94dc`

```dockerfile
```

-	Layers:
	-	`sha256:d0dacd457b618139c482a7d6afa2041ffd6cb707e33b66acf044aaefaa14397e`  
		Last Modified: Mon, 08 Jun 2026 18:32:46 GMT  
		Size: 1.2 MB (1201561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44183710a388aa4b94ef6d14e896b787a7e08a8f608a9c14d36001d21668c987`  
		Last Modified: Mon, 08 Jun 2026 18:32:46 GMT  
		Size: 38.1 KB (38148 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine` - linux; ppc64le

```console
$ docker pull httpd@sha256:24c446eba8c10efd7206d9e55e728f1787228d1442aa6ef61ac7a0d515cce4ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21381418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a448835add6f4d91f1982c6a872fe649b29ed77425b2e9e5aa901dd5e301205f`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 18:27:34 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Jun 2026 18:27:34 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:27:34 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:27:34 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:27:35 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:27:38 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 08 Jun 2026 18:27:38 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:27:38 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:27:38 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:29:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:29:29 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:29:29 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:29:29 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:29:29 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3833350820ce2613df1f0a4261df6ce7bc4951ba5dba44ef1a833641790aaaa`  
		Last Modified: Mon, 08 Jun 2026 18:29:47 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e9193af3a9c4cd580ff4cb24c30058cbec15dd6378f5950513a68c769c281f`  
		Last Modified: Mon, 08 Jun 2026 18:29:47 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a872efdd830ec45ac7efd740e333bf2cb140e2f4b94e60dd878415304be4b613`  
		Last Modified: Mon, 08 Jun 2026 18:29:47 GMT  
		Size: 11.3 MB (11338111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7513aa3438c9c2feecadf91e523239d954d60ceddaeda0f6e6763e2235eb9d35`  
		Last Modified: Mon, 08 Jun 2026 18:29:47 GMT  
		Size: 6.2 MB (6210978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47983e84280f04dea9f420f8879dc16efab9198e05c7c6d79eae3fe957261a48`  
		Last Modified: Mon, 08 Jun 2026 18:29:48 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:17e67c7acec63724871964de2c8a364fb31631efd6f458ddd90235490b789f24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1239293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77c39681778c5b28492be2b18b099ed022a8b09c86791dd235685cbc511448b`

```dockerfile
```

-	Layers:
	-	`sha256:aa63ded6d68a8c82088e414a0d5b803f2cf467747fc6fe33326dd7f4a8ff1d61`  
		Last Modified: Mon, 08 Jun 2026 18:29:47 GMT  
		Size: 1.2 MB (1201013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:772db10801a309da7fa867f9755115f0e7af393467440d9c2ba6a20824bfd7a0`  
		Last Modified: Mon, 08 Jun 2026 18:29:47 GMT  
		Size: 38.3 KB (38280 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine` - linux; riscv64

```console
$ docker pull httpd@sha256:6e901fc55fc925beed4d9e227553864af8d4da401692c898b3ba5d6198aa89e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.9 MB (19923429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94d1b25cfd3edbe24497157b752ff6f1b0bae2216ac56a9695500c96025ef0d8`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 18:52:56 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Jun 2026 18:52:56 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:52:56 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:52:56 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:52:57 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:53:04 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 08 Jun 2026 18:53:04 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:53:04 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:53:04 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 19:03:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 08 Jun 2026 19:03:07 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 19:03:07 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 19:03:07 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 19:03:07 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b19c7f0762250b0cc52b39bb993e944c7a467ccbba9e5982b3e05a892ed00e09`  
		Last Modified: Mon, 08 Jun 2026 19:03:57 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948f4b41e7172c5b397872ec12028b50e89c8b1945bcdd382f3c4354d3816a6c`  
		Last Modified: Mon, 08 Jun 2026 19:03:57 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839bf3cd8868f427bc3edaf740a5070b32162d92911d6135ad7452faf74806e2`  
		Last Modified: Mon, 08 Jun 2026 19:04:00 GMT  
		Size: 10.5 MB (10512864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0ed49d6165d488e835183bba68a905603e14ef7c9d532d89556389e587cdb6`  
		Last Modified: Mon, 08 Jun 2026 19:03:59 GMT  
		Size: 5.8 MB (5821504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9212c34deb579c5504ab192148ff204061b0646ae26b63cc9ad5ed1aad1789c`  
		Last Modified: Mon, 08 Jun 2026 19:03:59 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:536fbac1930d7f288da7460218490b036b05488c57b17e046817cfca2d991009
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1239289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63060237e36817f0674dfd5a4486b1ecb06b72e44a91033e3d2fc30181462368`

```dockerfile
```

-	Layers:
	-	`sha256:106695ede26a0f693625ca363327da8a1cf3bbdf11f35f67bf2ed2a8b03aa116`  
		Last Modified: Mon, 08 Jun 2026 19:03:58 GMT  
		Size: 1.2 MB (1201009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efd7b10cf0eb8a6248093104323312312d5e4f5d818a591a147f6a252df1d07d`  
		Last Modified: Mon, 08 Jun 2026 19:03:58 GMT  
		Size: 38.3 KB (38280 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine` - linux; s390x

```console
$ docker pull httpd@sha256:6283359189b28f3ca4b868bf776ceb2b692e4add8fea4a8b3269d66b7753a935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21378874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2df8884703c6d4ccc1f8733cfd8210fb8eb0924b8b0b633ac84af6641b17fbd`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Mon, 08 Jun 2026 18:27:38 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 08 Jun 2026 18:27:38 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:27:38 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:27:38 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:27:38 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:27:40 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Mon, 08 Jun 2026 18:27:40 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:27:40 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:27:40 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:28:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:28:46 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:28:46 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:28:46 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:28:46 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548235140cb8c1ab10d4692027815816cc2544f4ec8835eba3f51db5727af171`  
		Last Modified: Mon, 08 Jun 2026 18:28:59 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369bc1e79711eb6126c37a7b565cc2b0f42d4ee767040a1f8b44f857f5adef9a`  
		Last Modified: Mon, 08 Jun 2026 18:28:59 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59e8a1afdfdaee57b84923042e279cf1dc1f97d76646bf9caebc7a940d504ca`  
		Last Modified: Mon, 08 Jun 2026 18:28:59 GMT  
		Size: 11.6 MB (11649300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138c5a50960e95cfc40f091bc4080b810eb24455ad217b422125a22d86f5284d`  
		Last Modified: Mon, 08 Jun 2026 18:28:59 GMT  
		Size: 6.0 MB (6001640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c831663f14f23188df97e6b051c05bf1da28f9a4c18fc2c2cad0bdaff1429eb`  
		Last Modified: Mon, 08 Jun 2026 18:29:00 GMT  
		Size: 289.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:5cc2f04b98cd0e537a6eb5f791971f720a637c2255c7f4758ec7d5e301ba4612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1239161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8474478033f363a3cbf719bfac24a8e06adef6eccc522a4b3c2748dda664f13`

```dockerfile
```

-	Layers:
	-	`sha256:0b586450d6cc931e529e0fe9520eca240e9996721ea62991acd52c3c73de9ee9`  
		Last Modified: Mon, 08 Jun 2026 18:28:59 GMT  
		Size: 1.2 MB (1200955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d691c6da1d20a4d1e620abc97c146c35e966efbc00988d6f0d5c0941364e3a49`  
		Last Modified: Mon, 08 Jun 2026 18:28:58 GMT  
		Size: 38.2 KB (38206 bytes)  
		MIME: application/vnd.in-toto+json

## `httpd:alpine3.24`

**does not exist** (yet?)

## `httpd:latest`

```console
$ docker pull httpd@sha256:bda12def1dc3b718a5314b4b26ca84927fdb3905091f11200d581186f240e4f6
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

### `httpd:latest` - linux; amd64

```console
$ docker pull httpd@sha256:2b7d8a7992076bf5ceb8bb363b4c8f2b8c655072e7478f45c5e537af28f6c167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45230035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb74261f37ff6970ccb87626c9783304249efaad9f4e8cd32de4e9a3423b787d`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:48 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:48 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:48 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:53 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:30:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:30:55 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:30:55 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:30:55 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:30:55 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51757aae13a97369966a219edcf9e0f9b8cc8eaec050732a5d6fa25aa92e453`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c211dc8965131703cc3952b6267904624b637fc549d23e2e6bc0cc49b4222c`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 2.0 MB (1997894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc6b5038f865e4e495fc8fe09d6f11876069a408d170c40399b49126c800041`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 13.5 MB (13451745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9e979b34b8fed3ce647410b3644cc8cc46ef92761363f08fe8802169d5f76f`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:latest` - unknown; unknown

```console
$ docker pull httpd@sha256:fce1019bd8cc87b008a72778b2a2736ddff548e62baa27c4cc983db009cb5111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597fd853705160154b2bcd70d98acc6933b1b6dcf3f31cb013b0abcf1068d207`

```dockerfile
```

-	Layers:
	-	`sha256:e2025809a7e3749824decea45c53ede352d4aa58d75ace93dd07000d2b6c08a6`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 2.3 MB (2292510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:492c10869e234a6f6ccfabd1a0dfc280cec64fa0e207fc564413cc8da21c9610`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 37.6 KB (37611 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:latest` - linux; arm variant v5

```console
$ docker pull httpd@sha256:f361c4b24b78e1239dfeacd9d9dab2c93ea638455fd3c3b70dbbda6ab00a15f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42857065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ab2c2872db9a8045fa1ab91711e556824fe075bbaca19941f6e9bd8271bc48`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:48 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:48 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:48 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:58 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:58 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:58 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:58 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:31:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:31:48 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:31:48 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:31:48 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:31:48 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8741492638bd207b4038604a6e65e467c0a410df6afca31a4821aee832c662ab`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c069dc93d7fb7eba3c5388a00541788a95bc11398d69b0c81da9efc258d2c8d`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 1.9 MB (1912804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6002f904e7facf1cc93c7790b09f0609b922e15005a489e32e61b6fbc4316ad8`  
		Last Modified: Mon, 08 Jun 2026 18:31:57 GMT  
		Size: 13.0 MB (12989920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8efcbe4a582c8775afea0836d968f1f184bea5c26e21fe0fcbb5a0e7ebd3ff05`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:latest` - unknown; unknown

```console
$ docker pull httpd@sha256:f2ce1a9cefdbe977111087f3b75c7be0784ea835d0007b5a145ed2f6bfa0c95b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dfbb9b9cb8c42912b42a91046224acc7dc556f1e7d8097a01121fd91f76b72`

```dockerfile
```

-	Layers:
	-	`sha256:80fc7202154b749a8075c448c7e7a9a60d1d4f341914b54da5153b7ee3c03f5f`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 2.3 MB (2295542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27e7b847f32a118618968bc07cffc9a5d6d0c0692dee15129ee923129b35c1b4`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 37.7 KB (37749 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:latest` - linux; arm variant v7

```console
$ docker pull httpd@sha256:5236d5c6a10645ecac76238b7ca6f921ca8eb5ea92ab6fb293bdadae95b10ae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40548022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b12f00662f2acddd392078f235516594259077bf34e4c06e06e8288f24df443`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:54 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:54 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:54 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:54 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:29:01 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:29:01 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:29:01 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:29:01 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:31:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:31:27 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:31:27 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:31:27 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:31:27 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7617084195012707e889cdef4236f6627014b19baf5baa53b8e432880268bc`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada685e6861770db8d1c2090eecdecab5e8ae6dec8c9abc23fb86d844f8bb442`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 1.8 MB (1823341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a919558fd039a1b681fc7341aeb407767fa365ac621427a2d7bf5470f9eecc9`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 12.5 MB (12518379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a44ce25dab735595c229a5d37494e00da9b3a541edbcdd85d4f3e488c4175fd`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:latest` - unknown; unknown

```console
$ docker pull httpd@sha256:9db1b877234f01aa36272fba11532263d7a52f145aec8d4364b98deaca6fa87b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2331805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f897acfbf506ea853c77e9a461c832030fe5a6a95cb3bf116d12f565be924b5d`

```dockerfile
```

-	Layers:
	-	`sha256:1b5b5d4bbe67bc086194dd58eb01ec30a9bf78e7498afd570946311fcc5bbb5a`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 2.3 MB (2294057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d14fc4d73d1b623729ae4e87803dc741f0309a1a9e8d3661bd235890bb441fa`  
		Last Modified: Mon, 08 Jun 2026 18:31:35 GMT  
		Size: 37.7 KB (37748 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:latest` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:05f92a0b3df99246bd094967c40d5f00311b04b74e91386ab37f3879d5b6398f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45500798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab09468e72a3fd55b26758d03ba2f8a094a6de075771c949ee820cd22f4efd4`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:48 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:48 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:48 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:53 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:30:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:30:55 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:30:55 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:30:55 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:30:55 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51757aae13a97369966a219edcf9e0f9b8cc8eaec050732a5d6fa25aa92e453`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbc1d9c94781b6fb204e9f2dd48fa707b639991a0ed9e6832bc627ee78eb793`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 2.0 MB (1971344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1897ad34a45ba49cd3bd04d81eb169b2fa80642c8bdeb1783ba8067376d69911`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 13.4 MB (13387063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8048fc63017cda60558664fdef734dbe334a9ef8bb646c61060a28ea79cc2c73`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:latest` - unknown; unknown

```console
$ docker pull httpd@sha256:77551cd106fe5e6dba8ab22968dcc1c2157130fb9d1ce1f165884126ef2ff11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e103ca667e4eca8f7df1a1a1760fe83de402a3064636034eca87b9551b8abeac`

```dockerfile
```

-	Layers:
	-	`sha256:9983bb17dc86db43f7ba9dfb576ff96e6213f15e4868de93bd9ac8b5b38533a0`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 2.3 MB (2292847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d696410da2eb0504c27136882e9ac61fe5c021897524d3583611c2d09de3a6ca`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 37.8 KB (37793 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:latest` - linux; 386

```console
$ docker pull httpd@sha256:d212f60d1de6a98f8ac5666c0f08cfb2f8d7e69c007bba602a46c8f59d8c4346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46572612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a675fd0fcf287e70a1c2a01d7ad90a4f9db4df857ba19faf767c6dd59fc412`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:49 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:49 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:49 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:49 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:55 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:55 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:55 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:55 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:31:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:31:06 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:31:06 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:31:06 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:31:06 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3f98973d06c4dd876d5ba79c06211d3cd1cea32db869157acf4434836e75b5`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82349a6b654d1e29b5f624fa403272758a3418fe2d7860fc0f98cecee1da801b`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 2.1 MB (2055642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d9f1f37b024e8db99b29e69ec67af1bc894362b189a8cce9327b62ba4c0ff8`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 13.2 MB (13221163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6acaba897604b124ab0b4b16b6083da00590bfa6de43cb198468a35afbc076`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:latest` - unknown; unknown

```console
$ docker pull httpd@sha256:af18d97787c89c98c8fc110c23887ed1e760fb3f9207c6089ead4f50f78ceba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2327164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a81fe9a487688b93159da3a042732411446e801c6adf453f8f6a9878133adf`

```dockerfile
```

-	Layers:
	-	`sha256:fafa740c092dc2c2d150c0a3988c531e569690a6361dd41d57a1faec9324d3e4`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 2.3 MB (2289609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c62eb654a7ce8c3c1529835aa36c0de0488098dd817dd2b7968f541c9be78d7b`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 37.6 KB (37555 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:latest` - linux; ppc64le

```console
$ docker pull httpd@sha256:23250993ffdf8415ee5424cdeff8f5dff52a26bff21436f6567a702b755c8cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50163250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e58559fc8be957d33533107f22829d2774b9656a856245cd16510b077a31578`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:27:34 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:27:34 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:27:34 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:27:34 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:27:48 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:27:48 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:27:48 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:27:48 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:32:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:32:03 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:32:03 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:32:03 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:32:03 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095b49d3ed9c5bd684106ef2762c8c8d6c733b6154e0f88da03b1e1966cd01df`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc91076ec4b38e804c65780f529812ce414a153e095f9380d5804984cbd9f76`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 2.1 MB (2138540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164efcce54726bc397834f6038e70f0f535de3989d1fae4a14d3ce829e318c63`  
		Last Modified: Mon, 08 Jun 2026 18:32:18 GMT  
		Size: 14.4 MB (14423785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965f08e1a921c3b4cbb9f84c6b9999ea0cc8c5df7c7ccac77ea6fd7ee24189af`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:latest` - unknown; unknown

```console
$ docker pull httpd@sha256:7984379d541bad6433c6840f03d5a6bf3717cc96a23a6494d8edf4f56ff068c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fdcdd51ba0de4af51f758f1a67800b27772d0b16fc1acac13a6aa87399a87e`

```dockerfile
```

-	Layers:
	-	`sha256:8a0d0e0c231ec528ec3d98a2c72ca9b7759110af04cd9392138cbfeaf1d67dc9`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 2.3 MB (2296360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa23dd30e1d59efae1e2d867d4f568fe9d993722b873f57fa8d68feb138933c7`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 37.7 KB (37682 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:latest` - linux; riscv64

```console
$ docker pull httpd@sha256:71876f06ab63bc1cf873ca7c7087faea82688f408c32b0224b7cb29aab33e4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43402754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75069b5306a498c987ffa1263618f82a1a44ddc86f83c3e6bde1350c1a246af6`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:27:50 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:27:50 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:27:50 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:27:50 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:42 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:42 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:42 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:42 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:51:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:51:09 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:51:09 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:51:09 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:51:09 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcb14ecded12a6ddea9368e3e0a89b321a0babb977a900740f77d9b2749c881`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6acad9c2eb5d55c394bbd6a1a2e6dc884a8bd713db7c37cd33e0deeaab271b`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 2.0 MB (1956437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691748d99998bcadae01e53818c1a0ba95d0e2ba99b846f20043d5e854281021`  
		Last Modified: Mon, 08 Jun 2026 18:52:16 GMT  
		Size: 13.2 MB (13168247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1562e123a42b9956e7d39d32f9976df80d047f431caf3c4862e78d656b7e2b7e`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:latest` - unknown; unknown

```console
$ docker pull httpd@sha256:fa7de91aad897f1d9eaccd4e5213a25fb802222959c9f6c423886b4fb608fa8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2324290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e51d58413798f790228b33455088967cc44329474f1c5a0c94252c4d78a9a3`

```dockerfile
```

-	Layers:
	-	`sha256:9e13f24a27b58524719240f6484550131917ee8131886a36995d67d99f36a8cc`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 2.3 MB (2286607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30c4e22ef528cabad294d53b578ccf49631760a5a1caf405303bb050958ad5df`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 37.7 KB (37683 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:latest` - linux; s390x

```console
$ docker pull httpd@sha256:2fa1944efe68dc19bf36d54e72ec18be919399545609955907759c62eef32556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45520012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6084b5dadfb37c1564dd4b7e44b3a1e4a405039e5715c0f39c241c50aaf0367b`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:27:38 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:27:38 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:27:38 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:27:38 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:27:44 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:27:44 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:27:44 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:27:44 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:29:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:29:45 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:29:45 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:29:45 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:29:45 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a516c95daee50c3e7a6296f522dd4fb560f14d2ca73476e1dafa47cde6b081b3`  
		Last Modified: Mon, 08 Jun 2026 18:29:57 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ffc60f849aa2b0a9016137736b47502e247d91bf7d8bdb0af208d49a528576`  
		Last Modified: Mon, 08 Jun 2026 18:29:58 GMT  
		Size: 2.0 MB (2036546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f468bbb1ef751e92d67c77000d3af1de92fc265b1a2b4e1cbb62ada60425a6`  
		Last Modified: Mon, 08 Jun 2026 18:29:58 GMT  
		Size: 13.6 MB (13637070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30130f264687b48d7a0583772d74472381b1bddbf747faebcfad8fb79fec2160`  
		Last Modified: Mon, 08 Jun 2026 18:29:57 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:latest` - unknown; unknown

```console
$ docker pull httpd@sha256:a2f39309c230b1b17f2d4ddc53dd8c639603464ac50ea2a0b5e711225deaa4d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2331529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e8052bca557af655c176e8eec1e6ba8355618d3fa1333efab780db0eba9e1a`

```dockerfile
```

-	Layers:
	-	`sha256:0ec2b032ffb696485fe5fd2a728ef8da7d25712bb8327e496cd8643a40c8d333`  
		Last Modified: Mon, 08 Jun 2026 18:29:58 GMT  
		Size: 2.3 MB (2293918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18e3f08e0e7176d1ce05b52cfd66efa801891a3146c7bafe1e0a1034b73df332`  
		Last Modified: Mon, 08 Jun 2026 18:29:58 GMT  
		Size: 37.6 KB (37611 bytes)  
		MIME: application/vnd.in-toto+json

## `httpd:trixie`

```console
$ docker pull httpd@sha256:bda12def1dc3b718a5314b4b26ca84927fdb3905091f11200d581186f240e4f6
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
$ docker pull httpd@sha256:2b7d8a7992076bf5ceb8bb363b4c8f2b8c655072e7478f45c5e537af28f6c167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45230035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb74261f37ff6970ccb87626c9783304249efaad9f4e8cd32de4e9a3423b787d`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:48 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:48 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:48 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:53 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:30:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:30:55 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:30:55 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:30:55 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:30:55 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51757aae13a97369966a219edcf9e0f9b8cc8eaec050732a5d6fa25aa92e453`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c211dc8965131703cc3952b6267904624b637fc549d23e2e6bc0cc49b4222c`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 2.0 MB (1997894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fc6b5038f865e4e495fc8fe09d6f11876069a408d170c40399b49126c800041`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 13.5 MB (13451745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9e979b34b8fed3ce647410b3644cc8cc46ef92761363f08fe8802169d5f76f`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:fce1019bd8cc87b008a72778b2a2736ddff548e62baa27c4cc983db009cb5111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:597fd853705160154b2bcd70d98acc6933b1b6dcf3f31cb013b0abcf1068d207`

```dockerfile
```

-	Layers:
	-	`sha256:e2025809a7e3749824decea45c53ede352d4aa58d75ace93dd07000d2b6c08a6`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 2.3 MB (2292510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:492c10869e234a6f6ccfabd1a0dfc280cec64fa0e207fc564413cc8da21c9610`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 37.6 KB (37611 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:trixie` - linux; arm variant v5

```console
$ docker pull httpd@sha256:f361c4b24b78e1239dfeacd9d9dab2c93ea638455fd3c3b70dbbda6ab00a15f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42857065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ab2c2872db9a8045fa1ab91711e556824fe075bbaca19941f6e9bd8271bc48`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:48 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:48 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:48 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:58 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:58 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:58 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:58 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:31:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:31:48 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:31:48 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:31:48 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:31:48 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8741492638bd207b4038604a6e65e467c0a410df6afca31a4821aee832c662ab`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c069dc93d7fb7eba3c5388a00541788a95bc11398d69b0c81da9efc258d2c8d`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 1.9 MB (1912804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6002f904e7facf1cc93c7790b09f0609b922e15005a489e32e61b6fbc4316ad8`  
		Last Modified: Mon, 08 Jun 2026 18:31:57 GMT  
		Size: 13.0 MB (12989920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8efcbe4a582c8775afea0836d968f1f184bea5c26e21fe0fcbb5a0e7ebd3ff05`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:f2ce1a9cefdbe977111087f3b75c7be0784ea835d0007b5a145ed2f6bfa0c95b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2333291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dfbb9b9cb8c42912b42a91046224acc7dc556f1e7d8097a01121fd91f76b72`

```dockerfile
```

-	Layers:
	-	`sha256:80fc7202154b749a8075c448c7e7a9a60d1d4f341914b54da5153b7ee3c03f5f`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 2.3 MB (2295542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27e7b847f32a118618968bc07cffc9a5d6d0c0692dee15129ee923129b35c1b4`  
		Last Modified: Mon, 08 Jun 2026 18:31:56 GMT  
		Size: 37.7 KB (37749 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:trixie` - linux; arm variant v7

```console
$ docker pull httpd@sha256:5236d5c6a10645ecac76238b7ca6f921ca8eb5ea92ab6fb293bdadae95b10ae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40548022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b12f00662f2acddd392078f235516594259077bf34e4c06e06e8288f24df443`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:54 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:54 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:54 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:54 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:29:01 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:29:01 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:29:01 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:29:01 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:31:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:31:27 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:31:27 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:31:27 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:31:27 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7617084195012707e889cdef4236f6627014b19baf5baa53b8e432880268bc`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada685e6861770db8d1c2090eecdecab5e8ae6dec8c9abc23fb86d844f8bb442`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 1.8 MB (1823341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a919558fd039a1b681fc7341aeb407767fa365ac621427a2d7bf5470f9eecc9`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 12.5 MB (12518379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a44ce25dab735595c229a5d37494e00da9b3a541edbcdd85d4f3e488c4175fd`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:9db1b877234f01aa36272fba11532263d7a52f145aec8d4364b98deaca6fa87b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2331805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f897acfbf506ea853c77e9a461c832030fe5a6a95cb3bf116d12f565be924b5d`

```dockerfile
```

-	Layers:
	-	`sha256:1b5b5d4bbe67bc086194dd58eb01ec30a9bf78e7498afd570946311fcc5bbb5a`  
		Last Modified: Mon, 08 Jun 2026 18:31:36 GMT  
		Size: 2.3 MB (2294057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d14fc4d73d1b623729ae4e87803dc741f0309a1a9e8d3661bd235890bb441fa`  
		Last Modified: Mon, 08 Jun 2026 18:31:35 GMT  
		Size: 37.7 KB (37748 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:trixie` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:05f92a0b3df99246bd094967c40d5f00311b04b74e91386ab37f3879d5b6398f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45500798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab09468e72a3fd55b26758d03ba2f8a094a6de075771c949ee820cd22f4efd4`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:48 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:48 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:48 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:48 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:53 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:53 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:30:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:30:55 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:30:55 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:30:55 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:30:55 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51757aae13a97369966a219edcf9e0f9b8cc8eaec050732a5d6fa25aa92e453`  
		Last Modified: Mon, 08 Jun 2026 18:31:03 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbc1d9c94781b6fb204e9f2dd48fa707b639991a0ed9e6832bc627ee78eb793`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 2.0 MB (1971344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1897ad34a45ba49cd3bd04d81eb169b2fa80642c8bdeb1783ba8067376d69911`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 13.4 MB (13387063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8048fc63017cda60558664fdef734dbe334a9ef8bb646c61060a28ea79cc2c73`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:77551cd106fe5e6dba8ab22968dcc1c2157130fb9d1ce1f165884126ef2ff11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2330640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e103ca667e4eca8f7df1a1a1760fe83de402a3064636034eca87b9551b8abeac`

```dockerfile
```

-	Layers:
	-	`sha256:9983bb17dc86db43f7ba9dfb576ff96e6213f15e4868de93bd9ac8b5b38533a0`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 2.3 MB (2292847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d696410da2eb0504c27136882e9ac61fe5c021897524d3583611c2d09de3a6ca`  
		Last Modified: Mon, 08 Jun 2026 18:31:04 GMT  
		Size: 37.8 KB (37793 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:trixie` - linux; 386

```console
$ docker pull httpd@sha256:d212f60d1de6a98f8ac5666c0f08cfb2f8d7e69c007bba602a46c8f59d8c4346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46572612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a675fd0fcf287e70a1c2a01d7ad90a4f9db4df857ba19faf767c6dd59fc412`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:28:49 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:28:49 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:28:49 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:28:49 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:55 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:55 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:55 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:55 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:31:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:31:06 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:31:06 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:31:06 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:31:06 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3f98973d06c4dd876d5ba79c06211d3cd1cea32db869157acf4434836e75b5`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82349a6b654d1e29b5f624fa403272758a3418fe2d7860fc0f98cecee1da801b`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 2.1 MB (2055642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d9f1f37b024e8db99b29e69ec67af1bc894362b189a8cce9327b62ba4c0ff8`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 13.2 MB (13221163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6acaba897604b124ab0b4b16b6083da00590bfa6de43cb198468a35afbc076`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:af18d97787c89c98c8fc110c23887ed1e760fb3f9207c6089ead4f50f78ceba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2327164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5a81fe9a487688b93159da3a042732411446e801c6adf453f8f6a9878133adf`

```dockerfile
```

-	Layers:
	-	`sha256:fafa740c092dc2c2d150c0a3988c531e569690a6361dd41d57a1faec9324d3e4`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 2.3 MB (2289609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c62eb654a7ce8c3c1529835aa36c0de0488098dd817dd2b7968f541c9be78d7b`  
		Last Modified: Mon, 08 Jun 2026 18:31:14 GMT  
		Size: 37.6 KB (37555 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:trixie` - linux; ppc64le

```console
$ docker pull httpd@sha256:23250993ffdf8415ee5424cdeff8f5dff52a26bff21436f6567a702b755c8cb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50163250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e58559fc8be957d33533107f22829d2774b9656a856245cd16510b077a31578`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:27:34 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:27:34 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:27:34 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:27:34 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:27:48 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:27:48 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:27:48 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:27:48 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:32:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:32:03 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:32:03 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:32:03 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:32:03 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095b49d3ed9c5bd684106ef2762c8c8d6c733b6154e0f88da03b1e1966cd01df`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc91076ec4b38e804c65780f529812ce414a153e095f9380d5804984cbd9f76`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 2.1 MB (2138540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164efcce54726bc397834f6038e70f0f535de3989d1fae4a14d3ce829e318c63`  
		Last Modified: Mon, 08 Jun 2026 18:32:18 GMT  
		Size: 14.4 MB (14423785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965f08e1a921c3b4cbb9f84c6b9999ea0cc8c5df7c7ccac77ea6fd7ee24189af`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:7984379d541bad6433c6840f03d5a6bf3717cc96a23a6494d8edf4f56ff068c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2334042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84fdcdd51ba0de4af51f758f1a67800b27772d0b16fc1acac13a6aa87399a87e`

```dockerfile
```

-	Layers:
	-	`sha256:8a0d0e0c231ec528ec3d98a2c72ca9b7759110af04cd9392138cbfeaf1d67dc9`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 2.3 MB (2296360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa23dd30e1d59efae1e2d867d4f568fe9d993722b873f57fa8d68feb138933c7`  
		Last Modified: Mon, 08 Jun 2026 18:32:17 GMT  
		Size: 37.7 KB (37682 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:trixie` - linux; riscv64

```console
$ docker pull httpd@sha256:71876f06ab63bc1cf873ca7c7087faea82688f408c32b0224b7cb29aab33e4a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43402754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75069b5306a498c987ffa1263618f82a1a44ddc86f83c3e6bde1350c1a246af6`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:27:50 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:27:50 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:27:50 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:27:50 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:28:42 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:28:42 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:28:42 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:28:42 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:51:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:51:09 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:51:09 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:51:09 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:51:09 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcb14ecded12a6ddea9368e3e0a89b321a0babb977a900740f77d9b2749c881`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6acad9c2eb5d55c394bbd6a1a2e6dc884a8bd713db7c37cd33e0deeaab271b`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 2.0 MB (1956437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691748d99998bcadae01e53818c1a0ba95d0e2ba99b846f20043d5e854281021`  
		Last Modified: Mon, 08 Jun 2026 18:52:16 GMT  
		Size: 13.2 MB (13168247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1562e123a42b9956e7d39d32f9976df80d047f431caf3c4862e78d656b7e2b7e`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:fa7de91aad897f1d9eaccd4e5213a25fb802222959c9f6c423886b4fb608fa8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2324290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e51d58413798f790228b33455088967cc44329474f1c5a0c94252c4d78a9a3`

```dockerfile
```

-	Layers:
	-	`sha256:9e13f24a27b58524719240f6484550131917ee8131886a36995d67d99f36a8cc`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 2.3 MB (2286607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30c4e22ef528cabad294d53b578ccf49631760a5a1caf405303bb050958ad5df`  
		Last Modified: Mon, 08 Jun 2026 18:52:14 GMT  
		Size: 37.7 KB (37683 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:trixie` - linux; s390x

```console
$ docker pull httpd@sha256:2fa1944efe68dc19bf36d54e72ec18be919399545609955907759c62eef32556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45520012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6084b5dadfb37c1564dd4b7e44b3a1e4a405039e5715c0f39c241c50aaf0367b`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Mon, 08 Jun 2026 18:27:38 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Mon, 08 Jun 2026 18:27:38 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Jun 2026 18:27:38 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Mon, 08 Jun 2026 18:27:38 GMT
WORKDIR /usr/local/apache2
# Mon, 08 Jun 2026 18:27:44 GMT
RUN set -eux; 	apt-get install --update -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	apt-get dist-clean # buildkit
# Mon, 08 Jun 2026 18:27:44 GMT
ENV HTTPD_VERSION=2.4.68
# Mon, 08 Jun 2026 18:27:44 GMT
ENV HTTPD_SHA256=68c74d4df38c26bed4dfbdb8f3baf1eb532f3872357becc1bba5d136f6b63c06
# Mon, 08 Jun 2026 18:27:44 GMT
ENV HTTPD_PATCHES=
# Mon, 08 Jun 2026 18:29:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get install --update -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre2-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		httpd -v # buildkit
# Mon, 08 Jun 2026 18:29:45 GMT
STOPSIGNAL SIGWINCH
# Mon, 08 Jun 2026 18:29:45 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Mon, 08 Jun 2026 18:29:45 GMT
EXPOSE map[80/tcp:{}]
# Mon, 08 Jun 2026 18:29:45 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a516c95daee50c3e7a6296f522dd4fb560f14d2ca73476e1dafa47cde6b081b3`  
		Last Modified: Mon, 08 Jun 2026 18:29:57 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ffc60f849aa2b0a9016137736b47502e247d91bf7d8bdb0af208d49a528576`  
		Last Modified: Mon, 08 Jun 2026 18:29:58 GMT  
		Size: 2.0 MB (2036546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f468bbb1ef751e92d67c77000d3af1de92fc265b1a2b4e1cbb62ada60425a6`  
		Last Modified: Mon, 08 Jun 2026 18:29:58 GMT  
		Size: 13.6 MB (13637070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30130f264687b48d7a0583772d74472381b1bddbf747faebcfad8fb79fec2160`  
		Last Modified: Mon, 08 Jun 2026 18:29:57 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:trixie` - unknown; unknown

```console
$ docker pull httpd@sha256:a2f39309c230b1b17f2d4ddc53dd8c639603464ac50ea2a0b5e711225deaa4d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2331529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e8052bca557af655c176e8eec1e6ba8355618d3fa1333efab780db0eba9e1a`

```dockerfile
```

-	Layers:
	-	`sha256:0ec2b032ffb696485fe5fd2a728ef8da7d25712bb8327e496cd8643a40c8d333`  
		Last Modified: Mon, 08 Jun 2026 18:29:58 GMT  
		Size: 2.3 MB (2293918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18e3f08e0e7176d1ce05b52cfd66efa801891a3146c7bafe1e0a1034b73df332`  
		Last Modified: Mon, 08 Jun 2026 18:29:58 GMT  
		Size: 37.6 KB (37611 bytes)  
		MIME: application/vnd.in-toto+json
