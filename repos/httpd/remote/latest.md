## `httpd:latest`

```console
$ docker pull httpd@sha256:21df40fe3b51739516f22b40f6332624d6d6b3db891db1874cb304c7dae8c875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `httpd:latest` - linux; amd64

```console
$ docker pull httpd@sha256:36c40ed474a8b3468df6184d8ffc9d53130ce3a2a2d2f32558516f40c39851f6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61941854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e60c8eb27a1e2a9370e6d0120008433b3f543888d3fd8636a2426b3b8b37aa`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 15 May 2020 06:28:44 GMT
ADD file:7780c81c33e6cc5b6261af4a6c611cce0f39dec3131009bb297e65f12020c150 in / 
# Fri, 15 May 2020 06:28:44 GMT
CMD ["bash"]
# Fri, 15 May 2020 19:10:32 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 15 May 2020 19:10:33 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2020 19:10:34 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX"
# Fri, 15 May 2020 19:10:35 GMT
WORKDIR /usr/local/apache2
# Fri, 15 May 2020 19:10:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libapr1-dev 		libaprutil1-dev 		libaprutil1-ldap 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 15 May 2020 19:10:46 GMT
ENV HTTPD_VERSION=2.4.43
# Fri, 15 May 2020 19:10:46 GMT
ENV HTTPD_SHA256=a497652ab3fc81318cdc2a203090a999150d86461acff97c1065dc910fe10f43
# Fri, 15 May 2020 19:10:46 GMT
ENV HTTPD_PATCHES=
# Fri, 15 May 2020 19:13:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		B9E8213AEFB861AF35A41F2C995E35221AD84DFF 	; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v
# Fri, 15 May 2020 19:13:44 GMT
STOPSIGNAL SIGWINCH
# Fri, 15 May 2020 19:13:45 GMT
COPY file:c432ff61c4993ecdef4786f48d91a96f8f0707f6179816ccb98db661bfb96b90 in /usr/local/bin/ 
# Fri, 15 May 2020 19:13:45 GMT
EXPOSE 80
# Fri, 15 May 2020 19:13:45 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:afb6ec6fdc1c3ba04f7a56db32c5ff5ff38962dc4cd0ffdef5beaa0ce2eb77e2`  
		Last Modified: Fri, 15 May 2020 06:37:39 GMT  
		Size: 27.1 MB (27098756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6b409207a35a05a9d8625b595f223b3675cc62626c69a2c9af925660a01887`  
		Last Modified: Fri, 15 May 2020 19:14:18 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e5e22239e22091482802c93141a24c0fafa82cc23c8a206ecad7c36fb75171`  
		Last Modified: Fri, 15 May 2020 19:14:27 GMT  
		Size: 10.4 MB (10374249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9829f70a6a6b9d260967a5ff0245d18cb081a90f8ce79d14791037fe3c835614`  
		Last Modified: Fri, 15 May 2020 19:14:37 GMT  
		Size: 24.5 MB (24468406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd774fea20244fabba8a25d20cb16142206be6dbcb52b9c9639dda4b36b857e`  
		Last Modified: Fri, 15 May 2020 19:14:18 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `httpd:latest` - linux; arm variant v5

```console
$ docker pull httpd@sha256:ec85394d03036c7d5ce51779915bc7880295ba356c86b151654a516314068d63
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.8 MB (56816671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46f86b6509e51f9a6ec9385074d4e4a8a4d0cd335b98e1572e72da5d50489833`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Tue, 09 Jun 2020 00:51:58 GMT
ADD file:7fde417d1c70a9ef2b4e468f6e2ee4cbd3f340fb2d5b67ede087c81520c95f4a in / 
# Tue, 09 Jun 2020 00:51:59 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:04:36 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Tue, 09 Jun 2020 02:04:37 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 02:04:40 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX"
# Tue, 09 Jun 2020 02:04:41 GMT
WORKDIR /usr/local/apache2
# Tue, 09 Jun 2020 02:05:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libapr1-dev 		libaprutil1-dev 		libaprutil1-ldap 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:05:08 GMT
ENV HTTPD_VERSION=2.4.43
# Tue, 09 Jun 2020 02:05:09 GMT
ENV HTTPD_SHA256=a497652ab3fc81318cdc2a203090a999150d86461acff97c1065dc910fe10f43
# Tue, 09 Jun 2020 02:05:10 GMT
ENV HTTPD_PATCHES=
# Tue, 09 Jun 2020 02:08:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		B9E8213AEFB861AF35A41F2C995E35221AD84DFF 	; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v
# Tue, 09 Jun 2020 02:08:43 GMT
STOPSIGNAL SIGWINCH
# Tue, 09 Jun 2020 02:08:44 GMT
COPY file:c432ff61c4993ecdef4786f48d91a96f8f0707f6179816ccb98db661bfb96b90 in /usr/local/bin/ 
# Tue, 09 Jun 2020 02:08:44 GMT
EXPOSE 80
# Tue, 09 Jun 2020 02:08:45 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:5b11fc09c1a26b11a7df7d593adf43baff53c5cdba71cf8a87ae4a6dd17eb52c`  
		Last Modified: Tue, 09 Jun 2020 00:59:24 GMT  
		Size: 24.8 MB (24837249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f7a6d0881fcf7729bb2528c220480ae99b19d247992901ed8573bcb9cdddc1`  
		Last Modified: Tue, 09 Jun 2020 02:09:01 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbf7b84ce0f57725da5007c849b52750f890cae50b2135764d7890a62912dc2`  
		Last Modified: Tue, 09 Jun 2020 02:09:06 GMT  
		Size: 8.3 MB (8325321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d83ede803fcd47a2f663cb178214a64dfee5abab1b2e50f836006b9f750612`  
		Last Modified: Tue, 09 Jun 2020 02:09:09 GMT  
		Size: 23.7 MB (23653631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfac4d0283fded8dd3f6c8d04740dfcc605a55e755f8b9c1e9b236f7ddda2f3f`  
		Last Modified: Tue, 09 Jun 2020 02:09:01 GMT  
		Size: 295.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `httpd:latest` - linux; arm variant v7

```console
$ docker pull httpd@sha256:26ba233f330df638d5b35f8d60839ba92a6180a985edfa7c444f96e566227312
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53873447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7b89ccb17426c9349697756ef38400ea988daa9f5c4ff0f3411ab7e90b4563`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Tue, 09 Jun 2020 01:01:24 GMT
ADD file:a35ca31d2a743d6a1738b1652f4f06c789abbca314d120f0e7e748311ac09ed2 in / 
# Tue, 09 Jun 2020 01:01:30 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:26:09 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Tue, 09 Jun 2020 04:26:10 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 04:26:12 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX"
# Tue, 09 Jun 2020 04:26:13 GMT
WORKDIR /usr/local/apache2
# Tue, 09 Jun 2020 04:26:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libapr1-dev 		libaprutil1-dev 		libaprutil1-ldap 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 04:26:33 GMT
ENV HTTPD_VERSION=2.4.43
# Tue, 09 Jun 2020 04:26:34 GMT
ENV HTTPD_SHA256=a497652ab3fc81318cdc2a203090a999150d86461acff97c1065dc910fe10f43
# Tue, 09 Jun 2020 04:26:35 GMT
ENV HTTPD_PATCHES=
# Tue, 09 Jun 2020 04:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		B9E8213AEFB861AF35A41F2C995E35221AD84DFF 	; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v
# Tue, 09 Jun 2020 04:29:56 GMT
STOPSIGNAL SIGWINCH
# Tue, 09 Jun 2020 04:29:57 GMT
COPY file:c432ff61c4993ecdef4786f48d91a96f8f0707f6179816ccb98db661bfb96b90 in /usr/local/bin/ 
# Tue, 09 Jun 2020 04:29:58 GMT
EXPOSE 80
# Tue, 09 Jun 2020 04:29:59 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:2dd003996c9ab82cac8112be0a4c04068e666e7a5d0cce3c65fb8f064de284e7`  
		Last Modified: Tue, 09 Jun 2020 01:10:25 GMT  
		Size: 22.7 MB (22705913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b225e9a96c3158ac154fbed742cd4a9c88c485b2f695c3142ff49677b909fd4`  
		Last Modified: Tue, 09 Jun 2020 04:30:30 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01047465ca28915396ff8954e36b50ec8b7059bf6717da44dd296da5daa9cb2`  
		Last Modified: Tue, 09 Jun 2020 04:30:33 GMT  
		Size: 8.0 MB (7953760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf077499005d7b086efb77b92dc26391029bdf4b59c7dd4344117b39ff18c69f`  
		Last Modified: Tue, 09 Jun 2020 04:30:37 GMT  
		Size: 23.2 MB (23213299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c527ac6959123ea52324d33da604a507f1cb5fc08de6e21098ffdf8f825f145`  
		Last Modified: Tue, 09 Jun 2020 04:30:29 GMT  
		Size: 298.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `httpd:latest` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:221a8a7486de7af861e2914c4464977c565f8be1ae288a84901ab6edbbc4fa59
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59278085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b598305371be81a7e36427089a5a26e98b0d88f1c08fdb5382f4b073404b3ef`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Tue, 09 Jun 2020 01:52:01 GMT
ADD file:98823648634dfc3af50862b1e2da1028b23996a37adf43b1b0c3c5b29e94b9c7 in / 
# Tue, 09 Jun 2020 01:52:04 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:52:23 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Tue, 09 Jun 2020 02:52:24 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 02:52:26 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX"
# Tue, 09 Jun 2020 02:52:26 GMT
WORKDIR /usr/local/apache2
# Tue, 09 Jun 2020 02:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libapr1-dev 		libaprutil1-dev 		libaprutil1-ldap 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:52:43 GMT
ENV HTTPD_VERSION=2.4.43
# Tue, 09 Jun 2020 02:52:43 GMT
ENV HTTPD_SHA256=a497652ab3fc81318cdc2a203090a999150d86461acff97c1065dc910fe10f43
# Tue, 09 Jun 2020 02:52:44 GMT
ENV HTTPD_PATCHES=
# Tue, 09 Jun 2020 02:55:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		B9E8213AEFB861AF35A41F2C995E35221AD84DFF 	; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v
# Tue, 09 Jun 2020 02:55:53 GMT
STOPSIGNAL SIGWINCH
# Tue, 09 Jun 2020 02:55:54 GMT
COPY file:c432ff61c4993ecdef4786f48d91a96f8f0707f6179816ccb98db661bfb96b90 in /usr/local/bin/ 
# Tue, 09 Jun 2020 02:55:55 GMT
EXPOSE 80
# Tue, 09 Jun 2020 02:55:56 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:33cc09c9b190539635d7c971301f623d94fda5b4b5647966c6c240902119009f`  
		Last Modified: Tue, 09 Jun 2020 01:58:14 GMT  
		Size: 25.9 MB (25857704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0adc4d0b81bf6df947a712496ef5fab45f3fb65bdde2df0349972dba502f154a`  
		Last Modified: Tue, 09 Jun 2020 02:56:28 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ef0544557ae8f3c9127565fbcdb118f4e23d23d82955796805b9d5b4260346`  
		Last Modified: Tue, 09 Jun 2020 02:56:31 GMT  
		Size: 9.0 MB (9040372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbd2835dd104629049c4eb35e537cb02715254e7921f7b7d424e171ecbd2979`  
		Last Modified: Tue, 09 Jun 2020 02:56:34 GMT  
		Size: 24.4 MB (24379536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a649f7fe9206a3ad6dac22fdd1fc6c26d22b6ce953a4836b1880c5ebca8e8125`  
		Last Modified: Tue, 09 Jun 2020 02:56:28 GMT  
		Size: 296.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `httpd:latest` - linux; 386

```console
$ docker pull httpd@sha256:f810e9ab70258f7d131ccddf42f7edb85f7472f9b57ec60e3a5fd7fb23d9beae
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67198196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c9cc8285086f257f297dd92b2f56b1df26c17533427d626fe97de198dc0eb7`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Tue, 09 Jun 2020 01:39:49 GMT
ADD file:9fb8fd8bf970c4134f555964fe485a3baa84f1d4c91c5aa35276c24404de9d5d in / 
# Tue, 09 Jun 2020 01:39:49 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:39:18 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Tue, 09 Jun 2020 02:39:18 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 02:39:20 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX"
# Tue, 09 Jun 2020 02:39:20 GMT
WORKDIR /usr/local/apache2
# Tue, 09 Jun 2020 02:39:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libapr1-dev 		libaprutil1-dev 		libaprutil1-ldap 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:39:35 GMT
ENV HTTPD_VERSION=2.4.43
# Tue, 09 Jun 2020 02:39:35 GMT
ENV HTTPD_SHA256=a497652ab3fc81318cdc2a203090a999150d86461acff97c1065dc910fe10f43
# Tue, 09 Jun 2020 02:39:35 GMT
ENV HTTPD_PATCHES=
# Tue, 09 Jun 2020 02:43:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		B9E8213AEFB861AF35A41F2C995E35221AD84DFF 	; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v
# Tue, 09 Jun 2020 02:43:44 GMT
STOPSIGNAL SIGWINCH
# Tue, 09 Jun 2020 02:43:44 GMT
COPY file:c432ff61c4993ecdef4786f48d91a96f8f0707f6179816ccb98db661bfb96b90 in /usr/local/bin/ 
# Tue, 09 Jun 2020 02:43:45 GMT
EXPOSE 80
# Tue, 09 Jun 2020 02:43:45 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:860f8957d8be856e2235a28e49fc4dca17254951e0eb67d760769755656f5cad`  
		Last Modified: Tue, 09 Jun 2020 01:45:01 GMT  
		Size: 27.8 MB (27754909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9279eb3796f506166bbd2253edc5a25a242897dab6691421b95b10e13d9c1fab`  
		Last Modified: Tue, 09 Jun 2020 02:43:59 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ffb9121ae62764f4d67af5849527ab401bf2d63430bd800e9a697ebb49f7a9`  
		Last Modified: Tue, 09 Jun 2020 02:44:05 GMT  
		Size: 15.0 MB (15025576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f47205bbf4b77f83a961e6b9a5d39437c87633e53dfe7812f905e1f3da4e617`  
		Last Modified: Tue, 09 Jun 2020 02:44:06 GMT  
		Size: 24.4 MB (24417267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd3ae1d6a73d6d1d2150fa9482c5f97419f3052dfd82ff36715fff486e7725a`  
		Last Modified: Tue, 09 Jun 2020 02:44:00 GMT  
		Size: 298.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `httpd:latest` - linux; mips64le

```console
$ docker pull httpd@sha256:d97db48e5025263bcdf641ccaea046fefbd8bac3aabcbe9a8463ec656bac0588
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59672338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c3cf6cd09e7490e1518c70b6aac011b4471fc5217b303ce945a06e371ea244`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Thu, 16 Apr 2020 03:30:32 GMT
ADD file:1324f1b90326c771ad3fbeba783010d46ba465c130b2b400ff60232e52bc4bbb in / 
# Thu, 16 Apr 2020 03:30:33 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 07:05:46 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 16 Apr 2020 07:05:46 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 07:05:48 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX"
# Thu, 16 Apr 2020 07:05:49 GMT
WORKDIR /usr/local/apache2
# Thu, 16 Apr 2020 07:06:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libapr1-dev 		libaprutil1-dev 		libaprutil1-ldap 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 07:06:12 GMT
ENV HTTPD_VERSION=2.4.43
# Thu, 16 Apr 2020 07:06:12 GMT
ENV HTTPD_SHA256=a497652ab3fc81318cdc2a203090a999150d86461acff97c1065dc910fe10f43
# Thu, 16 Apr 2020 07:06:13 GMT
ENV HTTPD_PATCHES=
# Thu, 16 Apr 2020 07:13:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		B9E8213AEFB861AF35A41F2C995E35221AD84DFF 	; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v
# Thu, 16 Apr 2020 07:13:10 GMT
STOPSIGNAL SIGWINCH
# Thu, 16 Apr 2020 07:13:11 GMT
COPY file:c432ff61c4993ecdef4786f48d91a96f8f0707f6179816ccb98db661bfb96b90 in /usr/local/bin/ 
# Thu, 16 Apr 2020 07:13:11 GMT
EXPOSE 80
# Thu, 16 Apr 2020 07:13:11 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:9d68bbb6bb3e325311e23872a0324580a3e32aea907701fa94bab81e80ff88c4`  
		Last Modified: Thu, 16 Apr 2020 03:56:50 GMT  
		Size: 25.8 MB (25762172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff3b49c81c40abb251d493183a8609dd5eebd474b512229e09a0966180047f7`  
		Last Modified: Thu, 16 Apr 2020 07:13:24 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17db9983aeaf0ba9e9de1cb8692b7f0643c8afaeb31327fce3af76a67332f7ab`  
		Last Modified: Thu, 16 Apr 2020 07:13:36 GMT  
		Size: 9.4 MB (9396794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2705ebf94b492a989c15b60fdea5260d324e0965b14fe887acf945b96a314062`  
		Last Modified: Thu, 16 Apr 2020 07:13:44 GMT  
		Size: 24.5 MB (24512928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f574b1db3167562c8880b4d83454f8d2702a364bb10017387b47e87067bcf39`  
		Last Modified: Thu, 16 Apr 2020 07:13:24 GMT  
		Size: 298.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `httpd:latest` - linux; ppc64le

```console
$ docker pull httpd@sha256:9994b04d712b6aaf158d59e8004873e0bf68b6feba960592dbe558076542725e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66522384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054d3259a2a32fddb2ed4de055c0e73e23f6619994c337c3655e26e8c63c4af2`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Tue, 09 Jun 2020 01:22:34 GMT
ADD file:796aad1a35ba276b8cccc19987c152a713db101b2b65e30923db753f5b7f4b0f in / 
# Tue, 09 Jun 2020 01:22:38 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 04:07:58 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Tue, 09 Jun 2020 04:08:02 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 04:08:09 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX"
# Tue, 09 Jun 2020 04:08:15 GMT
WORKDIR /usr/local/apache2
# Tue, 09 Jun 2020 04:09:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libapr1-dev 		libaprutil1-dev 		libaprutil1-ldap 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 04:09:15 GMT
ENV HTTPD_VERSION=2.4.43
# Tue, 09 Jun 2020 04:09:20 GMT
ENV HTTPD_SHA256=a497652ab3fc81318cdc2a203090a999150d86461acff97c1065dc910fe10f43
# Tue, 09 Jun 2020 04:09:23 GMT
ENV HTTPD_PATCHES=
# Tue, 09 Jun 2020 04:14:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		B9E8213AEFB861AF35A41F2C995E35221AD84DFF 	; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v
# Tue, 09 Jun 2020 04:14:40 GMT
STOPSIGNAL SIGWINCH
# Tue, 09 Jun 2020 04:14:41 GMT
COPY file:c432ff61c4993ecdef4786f48d91a96f8f0707f6179816ccb98db661bfb96b90 in /usr/local/bin/ 
# Tue, 09 Jun 2020 04:14:42 GMT
EXPOSE 80
# Tue, 09 Jun 2020 04:14:45 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:63dbb66c5119bb5086d9e6fb6b154211afc20b44ed136ab7df808f6044cfc6f1`  
		Last Modified: Tue, 09 Jun 2020 01:31:04 GMT  
		Size: 30.5 MB (30524405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670e5d9485cf668e9f874280a16ad73bd2982e0f88fdf869df2f0860b2ebec13`  
		Last Modified: Tue, 09 Jun 2020 04:15:10 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcba295953d989a7ed7e5ac31b5d5cb1943dd6e10e3f39fce8bafe663a5ce732`  
		Last Modified: Tue, 09 Jun 2020 04:15:13 GMT  
		Size: 10.4 MB (10362299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9400a7db8444a511a6fb393919041c7a22cf9641b4403e1456c0136c1e0a62bb`  
		Last Modified: Tue, 09 Jun 2020 04:15:15 GMT  
		Size: 25.6 MB (25635206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e0bc776a087dd4aaf4849df0a32260732da849d38bb1565cb2844206515cb2`  
		Last Modified: Tue, 09 Jun 2020 04:15:10 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `httpd:latest` - linux; s390x

```console
$ docker pull httpd@sha256:94676add59e99aa51d52fe3ab92b41655c5c6b40b7198c1f012f01b3baf136b7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59069751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e76ad4aa963374d39bfccaecdb41d3a1ec935d044933e4205700ff4d42f1cc1e`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Tue, 09 Jun 2020 01:42:37 GMT
ADD file:b21d426de40a194c6c76ed27593f33fb1ea470e15d4d43b00d7601472110de1a in / 
# Tue, 09 Jun 2020 01:42:38 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:33:18 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Tue, 09 Jun 2020 03:33:18 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Jun 2020 03:33:19 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX"
# Tue, 09 Jun 2020 03:33:19 GMT
WORKDIR /usr/local/apache2
# Tue, 09 Jun 2020 03:33:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		libapr1-dev 		libaprutil1-dev 		libaprutil1-ldap 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:33:27 GMT
ENV HTTPD_VERSION=2.4.43
# Tue, 09 Jun 2020 03:33:27 GMT
ENV HTTPD_SHA256=a497652ab3fc81318cdc2a203090a999150d86461acff97c1065dc910fe10f43
# Tue, 09 Jun 2020 03:33:27 GMT
ENV HTTPD_PATCHES=
# Tue, 09 Jun 2020 03:34:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		B9E8213AEFB861AF35A41F2C995E35221AD84DFF 	; do 		gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v
# Tue, 09 Jun 2020 03:34:47 GMT
STOPSIGNAL SIGWINCH
# Tue, 09 Jun 2020 03:34:47 GMT
COPY file:c432ff61c4993ecdef4786f48d91a96f8f0707f6179816ccb98db661bfb96b90 in /usr/local/bin/ 
# Tue, 09 Jun 2020 03:34:47 GMT
EXPOSE 80
# Tue, 09 Jun 2020 03:34:47 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:405e75bf6bb0104d67fcebf58e07cd21bf344589df9c1a41c00354a60ea3a604`  
		Last Modified: Tue, 09 Jun 2020 01:46:30 GMT  
		Size: 25.7 MB (25712668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97db9df7f03f17a63023f1023d3d0ca33f64cad19945b36dca3dffe4bfefa57e`  
		Last Modified: Tue, 09 Jun 2020 03:35:15 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dba20e3948c0e292051389c6c8e86ea99055606f462b833ba9a2993f1aae0933`  
		Last Modified: Tue, 09 Jun 2020 03:35:17 GMT  
		Size: 9.0 MB (9003821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c546aacb202f0a77b674bff319b016cb94f145dbc8d12e7c08e7e52d700d6731`  
		Last Modified: Tue, 09 Jun 2020 03:35:18 GMT  
		Size: 24.4 MB (24352792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33495666d1e38c57ff3614b775ab64a8c7459bc7d6e36dfdce0ba0338568ee8c`  
		Last Modified: Tue, 09 Jun 2020 03:35:21 GMT  
		Size: 295.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
