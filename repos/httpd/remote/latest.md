## `httpd:latest`

```console
$ docker pull httpd@sha256:4c7788695c832bf415a662dfb5160f1895e65fc65c025e85f436ee2c9e7d7f3e
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `httpd:latest` - linux; amd64

```console
$ docker pull httpd@sha256:9bcff6411877512a61746511841abee9b342c01768d0bc3abd574df7ad4cab9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 MB (58456184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f81fca8b7f7458d67b07f14dca30fb827ab36563ab98f40a222a3045d9a56b32`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 17 Jul 2024 23:31:14 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Wed, 17 Jul 2024 23:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jul 2024 23:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
WORKDIR /usr/local/apache2
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_VERSION=2.4.62
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_SHA256=674188e7bf44ced82da8db522da946849e22080d73d16c93f7f4df89e25729ec
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_PATCHES=
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
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
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1931671199d6303431c53e50082f23f763cdf78934c679250c2b0dbf956ce3b8`  
		Last Modified: Tue, 14 Jan 2025 02:21:52 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bf18aad5028d8cc85ac216c34372be4b0e0c7916fb8973b415ce59149b3e47`  
		Last Modified: Tue, 14 Jan 2025 02:21:52 GMT  
		Size: 4.2 MB (4201248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9fd325f2c7bf16219376b015d923a2602a4ac8bd9330fdf1b75830f64bc93c`  
		Last Modified: Tue, 14 Jan 2025 02:21:53 GMT  
		Size: 26.0 MB (26042049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7228b499327f71584afe2c0407f6854e2ddb2beae138fb5d1f7c10f35bbb9529`  
		Last Modified: Tue, 14 Jan 2025 02:21:52 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:latest` - unknown; unknown

```console
$ docker pull httpd@sha256:f374e79257d46b171e210a6c84730a1b71a93cc169e98c76b60acb683239645b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2549749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0349e928669ebaf5583ad3b40f7baed4a46fac39327c97db7d19d7e2593b6f2`

```dockerfile
```

-	Layers:
	-	`sha256:fbfbc269f09913bb1ddd8929cbd16aabee902fa0f19c3d68f8a6fbad7c8393b2`  
		Last Modified: Tue, 14 Jan 2025 02:21:52 GMT  
		Size: 2.5 MB (2511907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50424d2da7ca827243d87f425edbda50f93fa7f045c032fa8fdb7bd6071b92eb`  
		Last Modified: Tue, 14 Jan 2025 23:58:13 GMT  
		Size: 37.8 KB (37842 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:latest` - linux; arm variant v5

```console
$ docker pull httpd@sha256:c8b77630f58c7364b1717ed2e0b14c53d3dfaaf7aea0565b8446964bf741dbf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54701720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6888311bfcc7969931afb4c28c6884625ea360c478c9b52131f8ca5f8ab624d0`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 17 Jul 2024 23:31:14 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1736726400'
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Wed, 17 Jul 2024 23:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jul 2024 23:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
WORKDIR /usr/local/apache2
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_VERSION=2.4.62
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_SHA256=674188e7bf44ced82da8db522da946849e22080d73d16c93f7f4df89e25729ec
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_PATCHES=
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
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
	-	`sha256:7a3fc1134bc1af98e13c0b7ea743c863d5a17f830a5fbd5a7002f750500e76c2`  
		Last Modified: Tue, 14 Jan 2025 20:33:17 GMT  
		Size: 25.7 MB (25736665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a7f3cc380c2f426c23a8c2b2170b823bf0bf79d1d5862db66f9f89bc5f90cf`  
		Last Modified: Tue, 14 Jan 2025 02:29:37 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7200c14f8e2d6aaf8eebb1a931599cfb75a79b8258fb2fd30125cf798c6da3ee`  
		Last Modified: Wed, 15 Jan 2025 01:18:10 GMT  
		Size: 3.7 MB (3709285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de83702d0f64d4fe30a2e9e467dde1ca34ec78002e136d645f89dce4a1d469be`  
		Last Modified: Wed, 15 Jan 2025 01:18:22 GMT  
		Size: 25.3 MB (25255303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e786575186dd3ff6915c405a4f0d6a8d19bcfb7169e71e3c2b5c985d969635`  
		Last Modified: Tue, 14 Jan 2025 02:29:37 GMT  
		Size: 289.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:latest` - unknown; unknown

```console
$ docker pull httpd@sha256:68ecdfd6b6d57a5a79c015ad1b0b2d451559ad0b61f453079dc54254c0e10c6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2553451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a910cfb2414e6ff39c70c41b34d60e8841ba04c4a70569d77d966dd8848d078`

```dockerfile
```

-	Layers:
	-	`sha256:498b4340b85a3bd57a53cdf250a9f2c9df04a184ab7b08a1b42221fee8f74235`  
		Last Modified: Tue, 14 Jan 2025 22:00:15 GMT  
		Size: 2.5 MB (2515474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da1f24ea88829e726950a91b5a7aa5de35658f9fb1ccba52d96fc0dda5b057ec`  
		Last Modified: Tue, 14 Jan 2025 22:00:15 GMT  
		Size: 38.0 KB (37977 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:latest` - linux; arm variant v7

```console
$ docker pull httpd@sha256:e90a8d68c43fe93a03723aae898acbb87cf588702f7a0808ba8e19538fbf84ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52112073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc768d4faf581df4bbdea0c3fba1818a770ee5671ea5b12405d083c869550e5e`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 17 Jul 2024 23:31:14 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Wed, 17 Jul 2024 23:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jul 2024 23:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
WORKDIR /usr/local/apache2
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_VERSION=2.4.62
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_SHA256=674188e7bf44ced82da8db522da946849e22080d73d16c93f7f4df89e25729ec
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_PATCHES=
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
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
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 20:33:55 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc03a7a310f366ef28e29917d00e020b5b36d7fdee39535833506c90e67c7af`  
		Last Modified: Tue, 14 Jan 2025 21:37:25 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ffa272ba828b751cad2b2daaa0addab234df81ffd1c21f416de29a9e156ae1a`  
		Last Modified: Tue, 14 Jan 2025 02:33:54 GMT  
		Size: 3.5 MB (3482059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088c331bf23461caf0b2bd0c1ea9549853aa99d6ac5c4f442cecc47a07fc9994`  
		Last Modified: Tue, 14 Jan 2025 21:35:02 GMT  
		Size: 24.7 MB (24714946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d047d28d9fd1388905784773239944a18b3f48e244ea6e546232e7aabbd4980`  
		Last Modified: Tue, 14 Jan 2025 21:37:27 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:latest` - unknown; unknown

```console
$ docker pull httpd@sha256:1661106f70fbb01260ad31f089dca425150402e08a89f9533171f323d8a526e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2552254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7068d4e125de1fab8b30e27aa7c7cb0b671d44ee4513e61c9b5e65c2e2d8cb`

```dockerfile
```

-	Layers:
	-	`sha256:27a81c46cadd794340a4ecb7d42e0ce2b81d0b7e3c7761dce4ff3b97ca099e29`  
		Last Modified: Tue, 14 Jan 2025 22:00:17 GMT  
		Size: 2.5 MB (2514277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aa430c4174222c340f636fbb19faeab338d2907638381f6cb88be1276d72361`  
		Last Modified: Tue, 14 Jan 2025 02:33:53 GMT  
		Size: 38.0 KB (37977 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:latest` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:0f9b5163217dc3bae86510a29c957f28b44e990b20b83942eebf870fb40bf0ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.1 MB (58071076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062dcbdad052c7978a22e9939deb168c3a2b21e4c087ef3e902f43d8f8c3805c`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 17 Jul 2024 23:31:14 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Wed, 17 Jul 2024 23:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jul 2024 23:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
WORKDIR /usr/local/apache2
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_VERSION=2.4.62
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_SHA256=674188e7bf44ced82da8db522da946849e22080d73d16c93f7f4df89e25729ec
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_PATCHES=
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
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
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfbb68d32bc7db19f01ad8f0bbb5a6e79e5b00291eb1d84166372fa05fc8d16`  
		Last Modified: Tue, 14 Jan 2025 02:59:55 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e4ed7f50dd650b9fc5e1f834f6064f47f77036a67f8344a7e2b4367276bf7b`  
		Last Modified: Tue, 14 Jan 2025 02:59:56 GMT  
		Size: 4.0 MB (4025023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e219b11acd472f6f510be8e0d5f4dcf049ce3189f4ce9a70e4286101ac2bf823`  
		Last Modified: Tue, 14 Jan 2025 02:59:57 GMT  
		Size: 26.0 MB (26004553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dffd7e864fdcb4fa68b3d441d541532438eb25d3e30c85347a38b5ce6c084a5`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:latest` - unknown; unknown

```console
$ docker pull httpd@sha256:724eae1c77281fc802540a25ed8677794e2628f4c172023958b8d5d856ca366d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2550276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f32c485780afaae650c62ac1425331209c74b79a283ee0b9e00961da768afa0`

```dockerfile
```

-	Layers:
	-	`sha256:cc1a46321442e40d9c7882d94b8a43ae6fb4f4d0f82ff59d34af4c0ca7adb9a0`  
		Last Modified: Wed, 15 Jan 2025 01:20:53 GMT  
		Size: 2.5 MB (2512251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b76075389ae281b71eb269f3aae83b0e5db8e0493f58d03fcacebe4bea8af9a0`  
		Last Modified: Tue, 14 Jan 2025 22:00:20 GMT  
		Size: 38.0 KB (38025 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:latest` - linux; 386

```console
$ docker pull httpd@sha256:3f411b6f7d1ae32ab7bfc26f98133c8e601cdcca684a9c16e6f146463cbacb76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59464818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2eebd749c9fa5f88e68ac2ba65144d505601081e8803fe28445415625161f4`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 17 Jul 2024 23:31:14 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Wed, 17 Jul 2024 23:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jul 2024 23:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
WORKDIR /usr/local/apache2
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_VERSION=2.4.62
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_SHA256=674188e7bf44ced82da8db522da946849e22080d73d16c93f7f4df89e25729ec
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_PATCHES=
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
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
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5bda7a00109fea5329fab6d258cfa25a8130d79b3c703d6bf35bf825e66ce8`  
		Last Modified: Tue, 14 Jan 2025 23:58:37 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840809b8ee9c9c91b6203a81f1079e695265e5fc4cdd286a845805c9fce74efe`  
		Last Modified: Tue, 14 Jan 2025 02:18:27 GMT  
		Size: 4.3 MB (4261442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e4029862dd1ed1d0b8ff46bfc821b601f1e08a7a4ed8a76752d0937d18e3e8`  
		Last Modified: Tue, 14 Jan 2025 02:18:28 GMT  
		Size: 26.0 MB (26015312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3a2b90ec52b957a19d892ab34718a1cea5a13f23475e5c3d97c213822febfd`  
		Last Modified: Tue, 14 Jan 2025 23:58:42 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:latest` - unknown; unknown

```console
$ docker pull httpd@sha256:2865f853230caee8a5d0fe667f925e698c913fb6d0e3a1941c554924a4a1636c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2546713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bfb38ad936a1ee8c3c10c7f952abd72b18ac0fd8b2d8ae3b1ceaff23255fbf`

```dockerfile
```

-	Layers:
	-	`sha256:39aa8379542d63cde7ec45dd07280e2f7f3f5b44fbc959ae75adc4e83acb7695`  
		Last Modified: Tue, 14 Jan 2025 02:18:27 GMT  
		Size: 2.5 MB (2508928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55718f20b44137d52b369e60249a525cd19a7d78c8e050defc5286ae4b411fa0`  
		Last Modified: Tue, 14 Jan 2025 02:18:27 GMT  
		Size: 37.8 KB (37785 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:latest` - linux; mips64le

```console
$ docker pull httpd@sha256:d1228fb3c9c73a50ff61981b86ad009e854f629cc098eb4eaa1af57a817857ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58233576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93472bb8404ac8835204b9c250ddc36a9011b060ac46d0cc406b34b9c83464ce`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 17 Jul 2024 23:31:14 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1736726400'
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Wed, 17 Jul 2024 23:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jul 2024 23:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
WORKDIR /usr/local/apache2
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_VERSION=2.4.62
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_SHA256=674188e7bf44ced82da8db522da946849e22080d73d16c93f7f4df89e25729ec
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_PATCHES=
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
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
	-	`sha256:b08d7e697b04bda8cef97763765ebbbc16790e22945b5ab31d97d448a15c8650`  
		Last Modified: Tue, 14 Jan 2025 20:36:28 GMT  
		Size: 28.5 MB (28486647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d4b0b92faf176c5d1a3d1a3dc763f3bc2facad89ede0ac4bd7190480fadb5a`  
		Last Modified: Tue, 14 Jan 2025 03:06:47 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35574806cd933845e49d1d5eb5e67793177758174c769a4e027a7d12611715e8`  
		Last Modified: Tue, 14 Jan 2025 03:06:47 GMT  
		Size: 3.6 MB (3571205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83da26e6de1d0baabf00f87a3d746e85a539476eaa503036909aef7185deaa93`  
		Last Modified: Tue, 14 Jan 2025 23:58:50 GMT  
		Size: 26.2 MB (26175253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646c4ba5c0ddef8ca7672af4f039c1119141e4d7d05af81fe16f90590782bb28`  
		Last Modified: Wed, 15 Jan 2025 01:22:38 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:latest` - unknown; unknown

```console
$ docker pull httpd@sha256:47b68c06055e684262e6605ec2212a004738615077e40c1aea27a0d165728577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 KB (37736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:758c2cae38d4353b98d5fa50dd478a28cb6c2303c72215f841c58509ba3c80cc`

```dockerfile
```

-	Layers:
	-	`sha256:02be489781132ef55ebfd87d69499c393f0ee6c0fc02b9807bf01cddc5cce3c3`  
		Last Modified: Tue, 14 Jan 2025 03:06:47 GMT  
		Size: 37.7 KB (37736 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:latest` - linux; ppc64le

```console
$ docker pull httpd@sha256:c4bbc441ec47ccc98497a651a309f2a623fc077a3bde5ee264fcfd8f7ce1a70d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63908165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4345b44b4572c90ce96da7aa98032e5342d8b7bdaf22fa12f62c90cc886ed099`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 17 Jul 2024 23:31:14 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1736726400'
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Wed, 17 Jul 2024 23:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jul 2024 23:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
WORKDIR /usr/local/apache2
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_VERSION=2.4.62
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_SHA256=674188e7bf44ced82da8db522da946849e22080d73d16c93f7f4df89e25729ec
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_PATCHES=
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
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
	-	`sha256:70e5167c90e251fcf2a687213601657926417de61cc905425399c9fcffb3d50f`  
		Last Modified: Tue, 14 Jan 2025 20:35:46 GMT  
		Size: 32.0 MB (32044847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e77b37d3181215bdfc902b48ff9a5adfb5d329df687b156dbf4e937b20344e`  
		Last Modified: Wed, 15 Jan 2025 03:15:26 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e125e4987b77e783bd2585fb249dadf58cac10c6fa992577375bd9f5a8ec5ad`  
		Last Modified: Tue, 14 Jan 2025 02:54:32 GMT  
		Size: 4.5 MB (4530021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc74ea8bc24c59a7c716011600a728c3e01a9447279e03dc884fa926279223c6`  
		Last Modified: Wed, 15 Jan 2025 02:17:49 GMT  
		Size: 27.3 MB (27332829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c957642b0282e6ad804852f77984d49f2620f6b7f1b872e2340ebe64d21e9245`  
		Last Modified: Tue, 14 Jan 2025 02:54:32 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:latest` - unknown; unknown

```console
$ docker pull httpd@sha256:abb4e51ec6ca0d482307f70c515c8e9258f5e027357a43e524c28707d66a1ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2554379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2958b9a9fc54ab1cad310ff82f65dbb5e8abf1e9741824f4d727b0776518e77d`

```dockerfile
```

-	Layers:
	-	`sha256:c55197beb52b0b7a6694b11e7d46fd4b067410799dbf857647c782cf43556b94`  
		Last Modified: Tue, 14 Jan 2025 02:54:32 GMT  
		Size: 2.5 MB (2516464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ebfe526b1b608e18caa043ddaa5bb90125e417a78cb37711148611bba7dc337`  
		Last Modified: Tue, 14 Jan 2025 02:54:32 GMT  
		Size: 37.9 KB (37915 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:latest` - linux; s390x

```console
$ docker pull httpd@sha256:884c200157fc0e911df5c80824e2bd841e13c5a2eb1fed125db63920a3246356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.4 MB (56421831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3de59a4f9015cac052046162c3e227ca9b9edf38a963bc098a131644b8239e26`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Wed, 17 Jul 2024 23:31:14 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1736726400'
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Wed, 17 Jul 2024 23:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 17 Jul 2024 23:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
WORKDIR /usr/local/apache2
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_VERSION=2.4.62
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_SHA256=674188e7bf44ced82da8db522da946849e22080d73d16c93f7f4df89e25729ec
# Wed, 17 Jul 2024 23:31:14 GMT
ENV HTTPD_PATCHES=
# Wed, 17 Jul 2024 23:31:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
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
	-	`sha256:310acd011b0fc666229ef81942693adcf97c49991b6d41b858d0bb251bfe23d5`  
		Last Modified: Tue, 14 Jan 2025 01:34:40 GMT  
		Size: 26.9 MB (26858738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8dbfed78d9399ab483fcf541e81a3d317bc02991f2c19629faef3c657c78f4b`  
		Last Modified: Wed, 15 Jan 2025 00:57:11 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931e81dfe865535fa73828b4eed257ce58de3d4df7ffa10c984de051632eb47f`  
		Last Modified: Tue, 14 Jan 2025 02:43:44 GMT  
		Size: 3.9 MB (3853464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd31f5d560905ac5115ddf4bcc616ca93946818d36d5cd6e81004f80370fba4`  
		Last Modified: Tue, 14 Jan 2025 23:59:04 GMT  
		Size: 25.7 MB (25709161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3bf9bd99dc3474bc3efec6b8033ab48f15a9a9d2d7c498a4635397e3fa4ed1`  
		Last Modified: Tue, 14 Jan 2025 23:59:05 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:latest` - unknown; unknown

```console
$ docker pull httpd@sha256:d3906c808edcd43b3d70c22bb625820d4e8bb610ab729af91e07b168d74898ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2549435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20349a19dd6b4db1c296db0c1314ec7c296b06b69ec9906a862162e0e049e0d6`

```dockerfile
```

-	Layers:
	-	`sha256:65ed48a8a422f12457d66c911ebab1e3025ed3f21939034d68b1b5fd3bbf205a`  
		Last Modified: Tue, 14 Jan 2025 02:43:44 GMT  
		Size: 2.5 MB (2511592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15fb98e13405cf9fb9c3983803ebaff8c36f7704393a0f5d54ca9da068904954`  
		Last Modified: Tue, 14 Jan 2025 02:43:44 GMT  
		Size: 37.8 KB (37843 bytes)  
		MIME: application/vnd.in-toto+json
