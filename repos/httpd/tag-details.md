<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `httpd`

-	[`httpd:2`](#httpd2)
-	[`httpd:2-alpine`](#httpd2-alpine)
-	[`httpd:2-alpine3.19`](#httpd2-alpine319)
-	[`httpd:2-bookworm`](#httpd2-bookworm)
-	[`httpd:2.4`](#httpd24)
-	[`httpd:2.4-alpine`](#httpd24-alpine)
-	[`httpd:2.4-alpine3.19`](#httpd24-alpine319)
-	[`httpd:2.4-bookworm`](#httpd24-bookworm)
-	[`httpd:2.4.59`](#httpd2459)
-	[`httpd:2.4.59-alpine`](#httpd2459-alpine)
-	[`httpd:2.4.59-alpine3.19`](#httpd2459-alpine319)
-	[`httpd:2.4.59-bookworm`](#httpd2459-bookworm)
-	[`httpd:alpine`](#httpdalpine)
-	[`httpd:alpine3.19`](#httpdalpine319)
-	[`httpd:bookworm`](#httpdbookworm)
-	[`httpd:latest`](#httpdlatest)

## `httpd:2`

```console
$ docker pull httpd@sha256:36c8c79f900108f0f09fd4148ad35ade57cba0dc19d13f3d15be24ce94e6a639
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

### `httpd:2` - linux; amd64

```console
$ docker pull httpd@sha256:518e9447a236de47cc2fb4f2dbf06466b6cd5cf50f9951742f9a20af76e8118d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59185382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c2fc9e3d849b21a35b4c96f5ad8ec4dc9b73ca44c56537039e8c6f3054db0a`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851c52adaa9bf680b2eaa45164baa37665418fb02666fb36c268002edd853994`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d9f60535a61833df2e57cc08221031d3ae50f3955a6d6b0153214619d357fb`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 4.0 MB (4006988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943a2b3cf551375517593790b58407ffc7028b4b34bca6c0756b76708ea4b3ce`  
		Last Modified: Wed, 24 Apr 2024 04:57:24 GMT  
		Size: 26.0 MB (26027444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea83e81966d64f34a57ffcc118b75ad19bc9321f9809cf9b0df25548a2fa695e`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2` - unknown; unknown

```console
$ docker pull httpd@sha256:e31d2d75b317933ed59c3503fcfd00357545f4e60e60d87368674365eed990bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc7b98024523f6963a92b3a8edb71945171fff164f1da1e3bc9296d404a1da2`

```dockerfile
```

-	Layers:
	-	`sha256:1a0e348c51fd80864d852c8a1b3dbe89c1cbf088a8d4fe204b4f9a2106b65425`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 2.5 MB (2475971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea347276a3b2b4390cbb875d979ac18e828399022ce83785af6a6e19535cf238`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 37.8 KB (37766 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2` - linux; arm variant v5

```console
$ docker pull httpd@sha256:6ac6acfaf36b492c8ee0271b5c1745e5d5173186838066fb55416fe1bad7f84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55660337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594aaef0a91e898dfb26ab368782f59da9b9f69c9ad0d9a155208b535102d8e8`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfdcc496dd931564ad13b4c74e84a37bd3e8fe4d3e8eef76531c007b4918eb3`  
		Last Modified: Wed, 24 Apr 2024 17:19:02 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7797397d89aa986596ae17907e8812fb696c601b77e453f8cfff70c5282bb68`  
		Last Modified: Wed, 24 Apr 2024 17:19:03 GMT  
		Size: 3.5 MB (3511113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabda791a3820471d4af8b4b5339e9e5ade214d951432d16dcf09a30dfc07788`  
		Last Modified: Wed, 24 Apr 2024 17:19:04 GMT  
		Size: 25.2 MB (25238724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7b73f2fae9dae743b3751fc794fe838ccfee7359899fe2ef291db96f774025`  
		Last Modified: Wed, 24 Apr 2024 17:19:03 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2` - unknown; unknown

```console
$ docker pull httpd@sha256:0559103a0db87f5edf6e70a2fce9af410a68e8207c18d62b1a99fa7d6081320a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2517016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5eb9364b67ec513d9aa9dab74264a7e94017611ae8f167c5e716aad4b7680e`

```dockerfile
```

-	Layers:
	-	`sha256:0fd0fb4e581c468abde2999045c163e01f5f465436e7aa62ce734436862f9eac`  
		Last Modified: Wed, 24 Apr 2024 17:19:03 GMT  
		Size: 2.5 MB (2479288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38cc0fcc6c1dede08c15c91c4bc214763cd7fb9e515bc4f8b07ba05cdc9cd387`  
		Last Modified: Wed, 24 Apr 2024 17:19:03 GMT  
		Size: 37.7 KB (37728 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2` - linux; arm variant v7

```console
$ docker pull httpd@sha256:e49897ae28bb259a5a1b205a464098038e49ea2bb4985187e84baac47edda986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52738179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9fefb7a703a9d947d489c78f23271b57b138126899b22193b569f3d5ceb0d2`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063593c7931b25f55a01b9bb0f7156d7398c702900d7c6c5a10ac3cb9b111eeb`  
		Last Modified: Wed, 24 Apr 2024 16:30:49 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60dd6c2df475ede40fbebdd310c9770f5c85d86278fe66bcfb34015f9975b80`  
		Last Modified: Wed, 24 Apr 2024 16:30:50 GMT  
		Size: 3.3 MB (3286910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5afe70e80d3c8da2e79abd6e84a95f7bb9516fe79ffc1e06abcb55d3af394429`  
		Last Modified: Wed, 24 Apr 2024 16:30:51 GMT  
		Size: 24.7 MB (24710357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e43b819248841764c8eaee46258c16341b869c3cd10e29c5fe19a7ad57d3ea0`  
		Last Modified: Wed, 24 Apr 2024 16:30:50 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2` - unknown; unknown

```console
$ docker pull httpd@sha256:daa1d3562f002200d97c8042f5fb9e5cce9d3a91b979ab3bae79daa3f5a6f0a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2516068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beda48825ccb307edac52c5e75efd8fc86548bb74670c0558d03c6057104e328`

```dockerfile
```

-	Layers:
	-	`sha256:6656cffeaa9a2613f22ecf4356afe7a1fd612ffb7430d4e7e2ab9004ece5d051`  
		Last Modified: Wed, 24 Apr 2024 16:30:50 GMT  
		Size: 2.5 MB (2478340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1efca153bd1cf7ed5e26102ed35722aa4aec61d831e71818bba3175e03866560`  
		Last Modified: Wed, 24 Apr 2024 16:30:50 GMT  
		Size: 37.7 KB (37728 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:b2670b51810a49855b0b59ed87dd064b3ec3ecf95e77d9dd6f6d13bab7467dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58997314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73acb239a8eb7a9ef5b6848a5b01bb26cc03d2262056705876bf7ac6ad781f02`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855b568ab02c3fee1362d51176f966517b1e03ca0c8efde55eddace90835f300`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c521cc2c4e8a439951003122cdab841fe1b1350db864e2cf9dea69298513f711`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 3.8 MB (3824128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c8bced82bd1d3557a49d39ea03bb8090bf3abc8154ab65388d9f9728f3ce02`  
		Last Modified: Thu, 25 Apr 2024 07:23:09 GMT  
		Size: 26.0 MB (25992782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae159c85a0b3662b8e9d58344f7da1b84836a7338c8ddf6b88360cea400929f`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2` - unknown; unknown

```console
$ docker pull httpd@sha256:307bc20593c828b3894250dd4e16b149c046b98c033453278fca94efd8bd0454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70026eb22d8bfc08dc60be7e7dcdce118be2390abe04aa90c7f27e6245767782`

```dockerfile
```

-	Layers:
	-	`sha256:77720a2aab607f8a1c40306899700597640ec9696bb65c714e6131dd481171b1`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 2.5 MB (2476229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd136e58015bf40bdc568f33b0d261e3140c11eee1769fbfb67f4ad2b93284f8`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 37.6 KB (37618 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2` - linux; 386

```console
$ docker pull httpd@sha256:34359f60b5aa39dfe4a6da81d319693f6ca6155e12e91b50e5d6da3ae7db89b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60223958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457768b202e686803b86961428bc138b1e4c6f0a08bec510257bba9b2d7e4486`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2941e842a389d5a4c34aa8e7f83e761d6a0deb0ed5c5bc01838c71d23659ac77`  
		Last Modified: Wed, 24 Apr 2024 04:57:41 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f800dd9ec1f906ac5c081169392c9dd10d32921d3e52e601c8c7ca7bcda3c600`  
		Last Modified: Wed, 24 Apr 2024 04:57:42 GMT  
		Size: 4.1 MB (4063511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494266189a0019f5cc3fec9ab5a55a1ea0fc3c8cc6a3ab1c1faeedbdc0fbaa5e`  
		Last Modified: Wed, 24 Apr 2024 04:57:42 GMT  
		Size: 26.0 MB (25996792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed1b4c9db903ab4981ddd506901a8ead9ae515c81f307dc7e52ed0256e73eec`  
		Last Modified: Wed, 24 Apr 2024 04:57:41 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2` - unknown; unknown

```console
$ docker pull httpd@sha256:928d95daa4cdcfd2c1395f60c62ed85d871764fdbfd6b1dbcf750c4f906d1eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2510705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8144c9b91841f94cfaea34892b458353406e2daa257e7e97e80ce41341381322`

```dockerfile
```

-	Layers:
	-	`sha256:637adc441596f6bc7ae557cdd4ef0de555b3e1b8aaa69a88adf26ea73e04a753`  
		Last Modified: Wed, 24 Apr 2024 04:57:42 GMT  
		Size: 2.5 MB (2472991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c57120021da5fb478f2b39b4540d36f1ba9bfa1efbe1c0616a07fe2a81d1e746`  
		Last Modified: Wed, 24 Apr 2024 04:57:41 GMT  
		Size: 37.7 KB (37714 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2` - linux; mips64le

```console
$ docker pull httpd@sha256:4512a76c673f11979d9f2ea96a56c59db662c5e8258c7128258245d18bb9292d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58678876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f7e1281eca6101e477c1cb3af32334cd551c69acc34839c3a8f8e3b3be6e80`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28233217e5e2c53a42bce8370d4462ed742672e46ec0e3acc021494964a6c4e`  
		Last Modified: Wed, 24 Apr 2024 23:51:19 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98af3a5736d8674d724399887f435760548973f8720121002efb9766f6892bb1`  
		Last Modified: Wed, 24 Apr 2024 23:51:20 GMT  
		Size: 3.4 MB (3373290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d3af7336bf3047ff58c8fc60fcce4943c107ecf04bb449d43849ce851d53aa`  
		Last Modified: Wed, 24 Apr 2024 23:51:22 GMT  
		Size: 26.2 MB (26160940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ed9c80633a9c8a938fb64f3eddb5677882265446491ddb3fce480647719cf5`  
		Last Modified: Wed, 24 Apr 2024 23:51:20 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2` - unknown; unknown

```console
$ docker pull httpd@sha256:b80ddb9178f5c7b1fb405cdad5a1ca2b55ae93147230041eb0b0e958dd6bd2b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f0b12a55ecb5a0fb2dc015ef1bebad8c2d781a197cd3a665b0b585ef134715`

```dockerfile
```

-	Layers:
	-	`sha256:e03a7d994013fb85dd187518a518143a7a11bc11a02be3fe21ac1bcc6c2bad8c`  
		Last Modified: Wed, 24 Apr 2024 23:51:20 GMT  
		Size: 37.5 KB (37480 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2` - linux; ppc64le

```console
$ docker pull httpd@sha256:f367b8c823d8e9650e4d0f3576cb4cb56931fb2a9abc5cf933fbc3e5e2d03eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64781656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5b1ab6010140721a568d9027ba17353616269ed57d0407e63a20a9db866d83`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8779f7411971984d8a264462c07b9383e455edbfa3945c3a7c3c0f0da6281405`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df41593893685df2f819e89678437a7190515d7cc02ecf4d3826f45e94594a6`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 4.3 MB (4329567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5fc79508ca1591a5607565a2c2fd383aaea639b5a8777f026f5767404f73eb`  
		Last Modified: Thu, 25 Apr 2024 03:19:08 GMT  
		Size: 27.3 MB (27310418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3bf3ad211e2e210d10318ae48cfccfdefd6adae953aa2a10ca77880dd921ac`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2` - unknown; unknown

```console
$ docker pull httpd@sha256:f5fdb59224d04f59d5f80ba98a242d519237e7fe401672f767a98c516fbb17b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2518193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3109624aa7219e37cb7b867bf5926f24b5e9b4eb3d6e31536b83f1751b0c42cf`

```dockerfile
```

-	Layers:
	-	`sha256:5553f9b984d60f0b17ff79178b8bd6943ed3c6a28b511fee1a71f4df9b281e63`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 2.5 MB (2480527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49e0858fd1c6faa9c04410e63c7d7bf0b572ae75294b281ff9ce3ba69ca201b3`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 37.7 KB (37666 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2` - linux; s390x

```console
$ docker pull httpd@sha256:ae3341db428440ab15b07058d2bab822247b8aa06035c19edea03f2a675e3b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56864928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed5070ae0d9687d8b499eae1be4caf30616eea45630f52af89bff9348d1cc474`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076f4d06a50ca8b3bcf6951ac8efa98b499598a608155af2bc4e4c0283e315e6`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8054bd786718ad21214203f377432a693d561157449486d1ea16ee3530d793e1`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 3.7 MB (3654647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c39e346caebedca77c0054fa938878774f458b3b88e05f7099ff4b70345256a`  
		Last Modified: Thu, 25 Apr 2024 02:28:32 GMT  
		Size: 25.7 MB (25697456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb3dcd087010aa65e19ef6e7ae889206220840a38cc7d973cd3b0e635895072`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2` - unknown; unknown

```console
$ docker pull httpd@sha256:779ecac6b7d7547b09bf644ce963543f48bac336bfe174dbd0583d7d06e3b0c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d2597d4c0c4788030bfe3a20a2ddf9842323ed2e486b682e1a863ae138ad89`

```dockerfile
```

-	Layers:
	-	`sha256:d42e15caceec6e5f15ccf873f46289eb1dc452e23ab53a076d905630a09e58e5`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 2.5 MB (2475763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28db97fd901916835b62fdb1cece860a44f5b2888ae52a2ea94026e65e136df5`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 37.6 KB (37600 bytes)  
		MIME: application/vnd.in-toto+json

## `httpd:2-alpine`

```console
$ docker pull httpd@sha256:68f6714169b70ca33126c46f60cc802eb602c6435f4ebf08349d871d500d3e70
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

### `httpd:2-alpine` - linux; amd64

```console
$ docker pull httpd@sha256:b48b48dcfff1407638908b8a1782480df0ad8bac7f5fc579496357864f97e60c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18905522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b6bf3450e2114fc55779cd878fa1a176a851a4de5a38f79ffb779639c455a2`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e13f4f5374dc8e6fd59fc8dc82c77d2dfc85ffd1136f5edbc4a9054ba955927`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333c1d8ec87c0966bd88d1293586bce65663a901c08af2a85ffe369897d7fd9e`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58593e44a54df297fb6195ac992fbda56ab083ee57a934ba5de6c49c8c6cff4a`  
		Last Modified: Fri, 05 Apr 2024 17:53:06 GMT  
		Size: 10.4 MB (10384953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608381599c688e98facb252c7e8313379b6d1f574bba1b49262a39145764d4d9`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 5.1 MB (5110138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e5ce613b310458e6aad12ed911fae7e33b9d59232a0a816ae8829774a7c351`  
		Last Modified: Fri, 05 Apr 2024 17:53:06 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:933e4cc35d564b7e6b37b9da44ff4c3a1c961ee5a115addfc4348458b9584a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1105171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32930164a83ab310294ec129967dfa6b0e208133bcd30d31b8bdaae148384c8c`

```dockerfile
```

-	Layers:
	-	`sha256:4ce2b7d308346544402cfbaecf8b70c4dfbb6d6385f79028bfeb7b9df16b2b23`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 1.1 MB (1067018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f7979b59e4c92069c8731802e0b918cc1668ed3cbc3448ac9f5863488762eec`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 38.2 KB (38153 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-alpine` - linux; arm variant v6

```console
$ docker pull httpd@sha256:3536bda1cb1b0f3581896c7acafa8426a67ac185711f3af26cffb991a76d08fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17774769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1732292898ef3f1fb223e062d5aa76bcf8087c9c7978a357ea964a0f9e6e2a4d`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8c07a4a93f0faf2d460b21b916e9f8d52550da29882704b17b06201a89e118`  
		Last Modified: Fri, 05 Apr 2024 18:11:18 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001db4688f33e38d27d733b6d51f6a9edf395f4fd76749cf91ebb32f1fd25483`  
		Last Modified: Fri, 05 Apr 2024 18:11:18 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f8fe9e9d09c4f2074ab547012fee140749069dd339f3cc87dc71e347884d92`  
		Last Modified: Fri, 05 Apr 2024 18:11:19 GMT  
		Size: 9.6 MB (9577820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c092ec8ebe549b81d3f7c2f8f6830bfc42142f090d8fe5cd5b52f296d516310`  
		Last Modified: Fri, 05 Apr 2024 18:11:19 GMT  
		Size: 5.0 MB (5029848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346b9e25e64782fa95573e9eb07893339f472741823a4062737052da7391dfd5`  
		Last Modified: Fri, 05 Apr 2024 18:11:20 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:2790d9e49f2d98ffc37ada24de30725d9196ac28a61fd2ef576263287c58aec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d270ac30275fb727064cc5d2eeeb08a7ffc7305c12f93e19d03d209ebc2d6f58`

```dockerfile
```

-	Layers:
	-	`sha256:57b3e792cca6cdd007c318692afa6ccc61834b2e257e11c1832e8403dd37032e`  
		Last Modified: Fri, 05 Apr 2024 18:11:18 GMT  
		Size: 37.9 KB (37910 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-alpine` - linux; arm variant v7

```console
$ docker pull httpd@sha256:09dd424663b1d2540476d34b124fb25360411dff64f69cc71fa3cf02381fb9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16993127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad0e3a5244891745dcd5889901c7a0101e398b81de79ff65cb7270e482bbbbb`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74aa637d7bf59fca068dcb5b7dd86513aa9ad3282aad69b3e9039cc2f6f18bcc`  
		Last Modified: Sat, 16 Mar 2024 16:04:22 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fc40e56afb70a5d1bf79dc4bf9118f2b993e3687626ab036513d862a1a286e`  
		Last Modified: Sat, 16 Mar 2024 16:04:22 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7015ed48724aa34bf3e29ddfa9b1058e3c374c383a17cc3ba6b943f7de0cf1`  
		Last Modified: Sat, 16 Mar 2024 16:04:23 GMT  
		Size: 9.3 MB (9334751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5553e605c52a438be1d61a267e9cbc342a533ce3966d9c82b03dfe7e0f1777c8`  
		Last Modified: Fri, 05 Apr 2024 17:57:38 GMT  
		Size: 4.7 MB (4737771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a356346eae4cb6bddf85f93948a3f0df8845d93176937fef76aec99cb50faef2`  
		Last Modified: Fri, 05 Apr 2024 17:57:37 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:28d8f38fd78210cba28d51dc8d470fc5068b2d90a3fd9cb0a9f14a622ff89577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1102820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3348381822a72f52b9575c5d5d34c4da16730f59ef5128ebdedb089cd1d48819`

```dockerfile
```

-	Layers:
	-	`sha256:9e5deb95007dd7e44d0a6f9d0c0ccf2ee83e76cb545b6c4691007c75be1c6498`  
		Last Modified: Fri, 05 Apr 2024 17:57:38 GMT  
		Size: 1.1 MB (1064695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a16e23262169a2b30cd14de32d5acde981fcd5bf7179967f584df46c44b1b10`  
		Last Modified: Fri, 05 Apr 2024 17:57:37 GMT  
		Size: 38.1 KB (38125 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-alpine` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:91756bbcc9b8283d49fdf66189881d39576f12c012dad8796b97948636e0b40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (18989141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d3d050f8abbaa153d704cae494aeeca773a0f24ba35600711e356083a79a66`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68b5c4e3f3b827d8933253d337cf55bf3ace2d75070b8ea7655a893c325569f`  
		Last Modified: Sat, 16 Mar 2024 15:13:13 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba68aab08183c67e796b91cc96b7c1629e35f98048a721cd67997edb83a202e2`  
		Last Modified: Sat, 16 Mar 2024 15:13:13 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1e2b5044558ea2188f9ba4d34df06cc7109e01f5caefe6c2bc5ecd11b6ced0`  
		Last Modified: Sat, 16 Mar 2024 15:13:14 GMT  
		Size: 10.4 MB (10388804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6beaeaed29f48ef5f4141a8b7e76a8e550f88775f81d464c5944634479d8ed7a`  
		Last Modified: Fri, 05 Apr 2024 17:55:14 GMT  
		Size: 5.3 MB (5250912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8742eb1c1f87645540c4e75db0e19ba29d77c28e18927d3310670a72b85ec82`  
		Last Modified: Fri, 05 Apr 2024 17:55:13 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:b266b0cecec670e48d25423f3f218b28b7745ec04fa2be113bca803f25a89f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1100073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a241afe2d5ab26a07a1794465d326a6827b70fbef1de59a250d03605dac1ded`

```dockerfile
```

-	Layers:
	-	`sha256:43abc3efae9947304de80f9a75aa23117ac15a382c784b355816810199ecbf7e`  
		Last Modified: Fri, 05 Apr 2024 17:55:13 GMT  
		Size: 1.1 MB (1062068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dcf770b26d2bae0707f3d339ee48b6778855e725144a0d1384402416186c295`  
		Last Modified: Fri, 05 Apr 2024 17:55:13 GMT  
		Size: 38.0 KB (38005 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-alpine` - linux; 386

```console
$ docker pull httpd@sha256:40a391f6e52f9fa6d56741b455cbffde4d9104948f1078da5bd6c248b3318f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18161726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa32e51497f1ebc9739fe8b3d915e5fecd520dd4959266c76adf910b71fd4ea`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740e52eababa89f531e99d9609ea4df66e75527cb8a97aa3feba95f64f8d19c1`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9d066a768f0f31e823ea143de9180c7e2b5b51ee3f0267272b2122353c5530`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320efa4f4b1525ce8d8dc283fe9bce7bf23e031d3349b59957067c1ad3f22eeb`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 9.9 MB (9862040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b89437c703e9c702702c5eb0432f2efcb16ae506d611336abbf81b083b7fbd`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 5.1 MB (5053894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1099f38eb4d16ee148b32677e9f70da2535bef69261361e1247b719b03f5a2c4`  
		Last Modified: Fri, 05 Apr 2024 17:53:13 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:52a1c8f1cdb4a7057132a6bc0f6f82528ee10ccffedf7bb17d1108bf94d8ac6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1105068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946eef1c61b246af219f7ef605bfd198e004722dc6d7fafdaa0a35c5504965e7`

```dockerfile
```

-	Layers:
	-	`sha256:56b910d095946bc43dbafed2e0f13360d62f86b726feba74f5670cb07cd93f3d`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 1.1 MB (1066973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37abeadc160510b3cfd3b1a3d82f05e600fcbb1c92c9b5e2c0a20b0c8e865bc7`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 38.1 KB (38095 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-alpine` - linux; ppc64le

```console
$ docker pull httpd@sha256:447d4eca233b95a1aebdb73d93c024d8226d6a608568aa2c9505f96a3b8f19bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19410079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bed7414a71a37df5ac42b1637107b9e12f08cc3e63e5d9ecd84556d26489d9b`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca1e90415bffcf574224c85fef296c0f849237fe22a0b5065a26673f7cbba51`  
		Last Modified: Sat, 16 Mar 2024 10:26:53 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b746962fe11d53bb9b19dfe7990c4658ac0472cccbd8daa5794e5f3a22cfda51`  
		Last Modified: Sat, 16 Mar 2024 10:26:53 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68b51060f0a52e914490ae4eeb10af1258ec331a68f78f4944118a1ca9911bd`  
		Last Modified: Sat, 16 Mar 2024 10:26:54 GMT  
		Size: 10.6 MB (10627211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f73e01f2b7ec6f92d901b09901b77c8dec59f0535633de6f26cc281f9452954`  
		Last Modified: Fri, 05 Apr 2024 17:59:16 GMT  
		Size: 5.4 MB (5422810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13941787572cd155aec58f453b55fcb5e882b928cf4aa65c8ede53e07d15a45`  
		Last Modified: Fri, 05 Apr 2024 17:59:16 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:6591d53cc91652e76f1529af4696e990fe459184e928ac7371b55488a2f3b7c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1098208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d59400ec49b3e236a314b42b69e345faf3cdcfbf0bd553b5d16dfc66d548bdd`

```dockerfile
```

-	Layers:
	-	`sha256:630456dcd802b6d23b26b5dc5b782789bc8969758ecdeca80d33ca2ef97be7bb`  
		Last Modified: Fri, 05 Apr 2024 17:59:16 GMT  
		Size: 1.1 MB (1060153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49cbad644a03a7cf5127a55a38cc827f068240cd3ce64261f61e48708941076d`  
		Last Modified: Fri, 05 Apr 2024 17:59:16 GMT  
		Size: 38.1 KB (38055 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-alpine` - linux; s390x

```console
$ docker pull httpd@sha256:8ddf2e0f8ccad02de20eaba4fa2f2e046b0032e4e17e481667d6226b3ec82061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19505364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b21662b1d3ba291b541e6898e9870c8f17fc32fc1542e8cd26321d995ed654`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d37ece6c30e22e249589d6aeda58cf29c409948f056a8037f657691f333031`  
		Last Modified: Sun, 17 Mar 2024 22:03:24 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de6b96fd2b7588019fbfc72d5afede300a4d0ef5ea65a7a99fb9715b40b506a`  
		Last Modified: Sun, 17 Mar 2024 22:03:24 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e00979af0d93fc259d0c067c3acf72e2d19ee3e48b840e26b9838a1882a12b`  
		Last Modified: Sun, 17 Mar 2024 22:03:25 GMT  
		Size: 11.0 MB (10985997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fdd3af6a86a6153ff1589309d30e18935c2aacf45522556151835153652514`  
		Last Modified: Sat, 06 Apr 2024 15:46:55 GMT  
		Size: 5.3 MB (5275029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6015f889334ad064a637db08b112726bb85893466a14f46b4034fa7edfa031b0`  
		Last Modified: Sat, 06 Apr 2024 15:46:55 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:f6d2ea0678751c8928910a6156f560c2dde868a32d09c26c484866d783af994d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1098082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd8c653038d8341ffbc2492c22b6e5888612cf77dba81bac930256963bfb5d4`

```dockerfile
```

-	Layers:
	-	`sha256:a9f0621638da42ab83a8b188d1b0e79887b581ba27e779272a93e6bd57ffc94a`  
		Last Modified: Sat, 06 Apr 2024 15:46:55 GMT  
		Size: 1.1 MB (1060095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1f2fc0d9673de65aa6403e6d5aff61166189f0445f2df8c80cea6225a259da`  
		Last Modified: Sat, 06 Apr 2024 15:46:55 GMT  
		Size: 38.0 KB (37987 bytes)  
		MIME: application/vnd.in-toto+json

## `httpd:2-alpine3.19`

```console
$ docker pull httpd@sha256:68f6714169b70ca33126c46f60cc802eb602c6435f4ebf08349d871d500d3e70
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
$ docker pull httpd@sha256:b48b48dcfff1407638908b8a1782480df0ad8bac7f5fc579496357864f97e60c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18905522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b6bf3450e2114fc55779cd878fa1a176a851a4de5a38f79ffb779639c455a2`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e13f4f5374dc8e6fd59fc8dc82c77d2dfc85ffd1136f5edbc4a9054ba955927`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333c1d8ec87c0966bd88d1293586bce65663a901c08af2a85ffe369897d7fd9e`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58593e44a54df297fb6195ac992fbda56ab083ee57a934ba5de6c49c8c6cff4a`  
		Last Modified: Fri, 05 Apr 2024 17:53:06 GMT  
		Size: 10.4 MB (10384953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608381599c688e98facb252c7e8313379b6d1f574bba1b49262a39145764d4d9`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 5.1 MB (5110138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e5ce613b310458e6aad12ed911fae7e33b9d59232a0a816ae8829774a7c351`  
		Last Modified: Fri, 05 Apr 2024 17:53:06 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:933e4cc35d564b7e6b37b9da44ff4c3a1c961ee5a115addfc4348458b9584a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1105171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32930164a83ab310294ec129967dfa6b0e208133bcd30d31b8bdaae148384c8c`

```dockerfile
```

-	Layers:
	-	`sha256:4ce2b7d308346544402cfbaecf8b70c4dfbb6d6385f79028bfeb7b9df16b2b23`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 1.1 MB (1067018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f7979b59e4c92069c8731802e0b918cc1668ed3cbc3448ac9f5863488762eec`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 38.2 KB (38153 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-alpine3.19` - linux; arm variant v6

```console
$ docker pull httpd@sha256:3536bda1cb1b0f3581896c7acafa8426a67ac185711f3af26cffb991a76d08fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17774769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1732292898ef3f1fb223e062d5aa76bcf8087c9c7978a357ea964a0f9e6e2a4d`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8c07a4a93f0faf2d460b21b916e9f8d52550da29882704b17b06201a89e118`  
		Last Modified: Fri, 05 Apr 2024 18:11:18 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001db4688f33e38d27d733b6d51f6a9edf395f4fd76749cf91ebb32f1fd25483`  
		Last Modified: Fri, 05 Apr 2024 18:11:18 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f8fe9e9d09c4f2074ab547012fee140749069dd339f3cc87dc71e347884d92`  
		Last Modified: Fri, 05 Apr 2024 18:11:19 GMT  
		Size: 9.6 MB (9577820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c092ec8ebe549b81d3f7c2f8f6830bfc42142f090d8fe5cd5b52f296d516310`  
		Last Modified: Fri, 05 Apr 2024 18:11:19 GMT  
		Size: 5.0 MB (5029848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346b9e25e64782fa95573e9eb07893339f472741823a4062737052da7391dfd5`  
		Last Modified: Fri, 05 Apr 2024 18:11:20 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:2790d9e49f2d98ffc37ada24de30725d9196ac28a61fd2ef576263287c58aec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d270ac30275fb727064cc5d2eeeb08a7ffc7305c12f93e19d03d209ebc2d6f58`

```dockerfile
```

-	Layers:
	-	`sha256:57b3e792cca6cdd007c318692afa6ccc61834b2e257e11c1832e8403dd37032e`  
		Last Modified: Fri, 05 Apr 2024 18:11:18 GMT  
		Size: 37.9 KB (37910 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-alpine3.19` - linux; arm variant v7

```console
$ docker pull httpd@sha256:09dd424663b1d2540476d34b124fb25360411dff64f69cc71fa3cf02381fb9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16993127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad0e3a5244891745dcd5889901c7a0101e398b81de79ff65cb7270e482bbbbb`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74aa637d7bf59fca068dcb5b7dd86513aa9ad3282aad69b3e9039cc2f6f18bcc`  
		Last Modified: Sat, 16 Mar 2024 16:04:22 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fc40e56afb70a5d1bf79dc4bf9118f2b993e3687626ab036513d862a1a286e`  
		Last Modified: Sat, 16 Mar 2024 16:04:22 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7015ed48724aa34bf3e29ddfa9b1058e3c374c383a17cc3ba6b943f7de0cf1`  
		Last Modified: Sat, 16 Mar 2024 16:04:23 GMT  
		Size: 9.3 MB (9334751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5553e605c52a438be1d61a267e9cbc342a533ce3966d9c82b03dfe7e0f1777c8`  
		Last Modified: Fri, 05 Apr 2024 17:57:38 GMT  
		Size: 4.7 MB (4737771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a356346eae4cb6bddf85f93948a3f0df8845d93176937fef76aec99cb50faef2`  
		Last Modified: Fri, 05 Apr 2024 17:57:37 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:28d8f38fd78210cba28d51dc8d470fc5068b2d90a3fd9cb0a9f14a622ff89577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1102820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3348381822a72f52b9575c5d5d34c4da16730f59ef5128ebdedb089cd1d48819`

```dockerfile
```

-	Layers:
	-	`sha256:9e5deb95007dd7e44d0a6f9d0c0ccf2ee83e76cb545b6c4691007c75be1c6498`  
		Last Modified: Fri, 05 Apr 2024 17:57:38 GMT  
		Size: 1.1 MB (1064695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a16e23262169a2b30cd14de32d5acde981fcd5bf7179967f584df46c44b1b10`  
		Last Modified: Fri, 05 Apr 2024 17:57:37 GMT  
		Size: 38.1 KB (38125 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:91756bbcc9b8283d49fdf66189881d39576f12c012dad8796b97948636e0b40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (18989141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d3d050f8abbaa153d704cae494aeeca773a0f24ba35600711e356083a79a66`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68b5c4e3f3b827d8933253d337cf55bf3ace2d75070b8ea7655a893c325569f`  
		Last Modified: Sat, 16 Mar 2024 15:13:13 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba68aab08183c67e796b91cc96b7c1629e35f98048a721cd67997edb83a202e2`  
		Last Modified: Sat, 16 Mar 2024 15:13:13 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1e2b5044558ea2188f9ba4d34df06cc7109e01f5caefe6c2bc5ecd11b6ced0`  
		Last Modified: Sat, 16 Mar 2024 15:13:14 GMT  
		Size: 10.4 MB (10388804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6beaeaed29f48ef5f4141a8b7e76a8e550f88775f81d464c5944634479d8ed7a`  
		Last Modified: Fri, 05 Apr 2024 17:55:14 GMT  
		Size: 5.3 MB (5250912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8742eb1c1f87645540c4e75db0e19ba29d77c28e18927d3310670a72b85ec82`  
		Last Modified: Fri, 05 Apr 2024 17:55:13 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:b266b0cecec670e48d25423f3f218b28b7745ec04fa2be113bca803f25a89f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1100073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a241afe2d5ab26a07a1794465d326a6827b70fbef1de59a250d03605dac1ded`

```dockerfile
```

-	Layers:
	-	`sha256:43abc3efae9947304de80f9a75aa23117ac15a382c784b355816810199ecbf7e`  
		Last Modified: Fri, 05 Apr 2024 17:55:13 GMT  
		Size: 1.1 MB (1062068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dcf770b26d2bae0707f3d339ee48b6778855e725144a0d1384402416186c295`  
		Last Modified: Fri, 05 Apr 2024 17:55:13 GMT  
		Size: 38.0 KB (38005 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-alpine3.19` - linux; 386

```console
$ docker pull httpd@sha256:40a391f6e52f9fa6d56741b455cbffde4d9104948f1078da5bd6c248b3318f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18161726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa32e51497f1ebc9739fe8b3d915e5fecd520dd4959266c76adf910b71fd4ea`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740e52eababa89f531e99d9609ea4df66e75527cb8a97aa3feba95f64f8d19c1`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9d066a768f0f31e823ea143de9180c7e2b5b51ee3f0267272b2122353c5530`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320efa4f4b1525ce8d8dc283fe9bce7bf23e031d3349b59957067c1ad3f22eeb`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 9.9 MB (9862040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b89437c703e9c702702c5eb0432f2efcb16ae506d611336abbf81b083b7fbd`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 5.1 MB (5053894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1099f38eb4d16ee148b32677e9f70da2535bef69261361e1247b719b03f5a2c4`  
		Last Modified: Fri, 05 Apr 2024 17:53:13 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:52a1c8f1cdb4a7057132a6bc0f6f82528ee10ccffedf7bb17d1108bf94d8ac6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1105068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946eef1c61b246af219f7ef605bfd198e004722dc6d7fafdaa0a35c5504965e7`

```dockerfile
```

-	Layers:
	-	`sha256:56b910d095946bc43dbafed2e0f13360d62f86b726feba74f5670cb07cd93f3d`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 1.1 MB (1066973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37abeadc160510b3cfd3b1a3d82f05e600fcbb1c92c9b5e2c0a20b0c8e865bc7`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 38.1 KB (38095 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-alpine3.19` - linux; ppc64le

```console
$ docker pull httpd@sha256:447d4eca233b95a1aebdb73d93c024d8226d6a608568aa2c9505f96a3b8f19bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19410079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bed7414a71a37df5ac42b1637107b9e12f08cc3e63e5d9ecd84556d26489d9b`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca1e90415bffcf574224c85fef296c0f849237fe22a0b5065a26673f7cbba51`  
		Last Modified: Sat, 16 Mar 2024 10:26:53 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b746962fe11d53bb9b19dfe7990c4658ac0472cccbd8daa5794e5f3a22cfda51`  
		Last Modified: Sat, 16 Mar 2024 10:26:53 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68b51060f0a52e914490ae4eeb10af1258ec331a68f78f4944118a1ca9911bd`  
		Last Modified: Sat, 16 Mar 2024 10:26:54 GMT  
		Size: 10.6 MB (10627211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f73e01f2b7ec6f92d901b09901b77c8dec59f0535633de6f26cc281f9452954`  
		Last Modified: Fri, 05 Apr 2024 17:59:16 GMT  
		Size: 5.4 MB (5422810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13941787572cd155aec58f453b55fcb5e882b928cf4aa65c8ede53e07d15a45`  
		Last Modified: Fri, 05 Apr 2024 17:59:16 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:6591d53cc91652e76f1529af4696e990fe459184e928ac7371b55488a2f3b7c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1098208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d59400ec49b3e236a314b42b69e345faf3cdcfbf0bd553b5d16dfc66d548bdd`

```dockerfile
```

-	Layers:
	-	`sha256:630456dcd802b6d23b26b5dc5b782789bc8969758ecdeca80d33ca2ef97be7bb`  
		Last Modified: Fri, 05 Apr 2024 17:59:16 GMT  
		Size: 1.1 MB (1060153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49cbad644a03a7cf5127a55a38cc827f068240cd3ce64261f61e48708941076d`  
		Last Modified: Fri, 05 Apr 2024 17:59:16 GMT  
		Size: 38.1 KB (38055 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-alpine3.19` - linux; s390x

```console
$ docker pull httpd@sha256:8ddf2e0f8ccad02de20eaba4fa2f2e046b0032e4e17e481667d6226b3ec82061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19505364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b21662b1d3ba291b541e6898e9870c8f17fc32fc1542e8cd26321d995ed654`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d37ece6c30e22e249589d6aeda58cf29c409948f056a8037f657691f333031`  
		Last Modified: Sun, 17 Mar 2024 22:03:24 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de6b96fd2b7588019fbfc72d5afede300a4d0ef5ea65a7a99fb9715b40b506a`  
		Last Modified: Sun, 17 Mar 2024 22:03:24 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e00979af0d93fc259d0c067c3acf72e2d19ee3e48b840e26b9838a1882a12b`  
		Last Modified: Sun, 17 Mar 2024 22:03:25 GMT  
		Size: 11.0 MB (10985997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fdd3af6a86a6153ff1589309d30e18935c2aacf45522556151835153652514`  
		Last Modified: Sat, 06 Apr 2024 15:46:55 GMT  
		Size: 5.3 MB (5275029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6015f889334ad064a637db08b112726bb85893466a14f46b4034fa7edfa031b0`  
		Last Modified: Sat, 06 Apr 2024 15:46:55 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:f6d2ea0678751c8928910a6156f560c2dde868a32d09c26c484866d783af994d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1098082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd8c653038d8341ffbc2492c22b6e5888612cf77dba81bac930256963bfb5d4`

```dockerfile
```

-	Layers:
	-	`sha256:a9f0621638da42ab83a8b188d1b0e79887b581ba27e779272a93e6bd57ffc94a`  
		Last Modified: Sat, 06 Apr 2024 15:46:55 GMT  
		Size: 1.1 MB (1060095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1f2fc0d9673de65aa6403e6d5aff61166189f0445f2df8c80cea6225a259da`  
		Last Modified: Sat, 06 Apr 2024 15:46:55 GMT  
		Size: 38.0 KB (37987 bytes)  
		MIME: application/vnd.in-toto+json

## `httpd:2-bookworm`

```console
$ docker pull httpd@sha256:36c8c79f900108f0f09fd4148ad35ade57cba0dc19d13f3d15be24ce94e6a639
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

### `httpd:2-bookworm` - linux; amd64

```console
$ docker pull httpd@sha256:518e9447a236de47cc2fb4f2dbf06466b6cd5cf50f9951742f9a20af76e8118d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59185382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c2fc9e3d849b21a35b4c96f5ad8ec4dc9b73ca44c56537039e8c6f3054db0a`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851c52adaa9bf680b2eaa45164baa37665418fb02666fb36c268002edd853994`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d9f60535a61833df2e57cc08221031d3ae50f3955a6d6b0153214619d357fb`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 4.0 MB (4006988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943a2b3cf551375517593790b58407ffc7028b4b34bca6c0756b76708ea4b3ce`  
		Last Modified: Wed, 24 Apr 2024 04:57:24 GMT  
		Size: 26.0 MB (26027444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea83e81966d64f34a57ffcc118b75ad19bc9321f9809cf9b0df25548a2fa695e`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-bookworm` - unknown; unknown

```console
$ docker pull httpd@sha256:e31d2d75b317933ed59c3503fcfd00357545f4e60e60d87368674365eed990bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc7b98024523f6963a92b3a8edb71945171fff164f1da1e3bc9296d404a1da2`

```dockerfile
```

-	Layers:
	-	`sha256:1a0e348c51fd80864d852c8a1b3dbe89c1cbf088a8d4fe204b4f9a2106b65425`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 2.5 MB (2475971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea347276a3b2b4390cbb875d979ac18e828399022ce83785af6a6e19535cf238`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 37.8 KB (37766 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-bookworm` - linux; arm variant v5

```console
$ docker pull httpd@sha256:6ac6acfaf36b492c8ee0271b5c1745e5d5173186838066fb55416fe1bad7f84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55660337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594aaef0a91e898dfb26ab368782f59da9b9f69c9ad0d9a155208b535102d8e8`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfdcc496dd931564ad13b4c74e84a37bd3e8fe4d3e8eef76531c007b4918eb3`  
		Last Modified: Wed, 24 Apr 2024 17:19:02 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7797397d89aa986596ae17907e8812fb696c601b77e453f8cfff70c5282bb68`  
		Last Modified: Wed, 24 Apr 2024 17:19:03 GMT  
		Size: 3.5 MB (3511113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabda791a3820471d4af8b4b5339e9e5ade214d951432d16dcf09a30dfc07788`  
		Last Modified: Wed, 24 Apr 2024 17:19:04 GMT  
		Size: 25.2 MB (25238724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7b73f2fae9dae743b3751fc794fe838ccfee7359899fe2ef291db96f774025`  
		Last Modified: Wed, 24 Apr 2024 17:19:03 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-bookworm` - unknown; unknown

```console
$ docker pull httpd@sha256:0559103a0db87f5edf6e70a2fce9af410a68e8207c18d62b1a99fa7d6081320a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2517016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5eb9364b67ec513d9aa9dab74264a7e94017611ae8f167c5e716aad4b7680e`

```dockerfile
```

-	Layers:
	-	`sha256:0fd0fb4e581c468abde2999045c163e01f5f465436e7aa62ce734436862f9eac`  
		Last Modified: Wed, 24 Apr 2024 17:19:03 GMT  
		Size: 2.5 MB (2479288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38cc0fcc6c1dede08c15c91c4bc214763cd7fb9e515bc4f8b07ba05cdc9cd387`  
		Last Modified: Wed, 24 Apr 2024 17:19:03 GMT  
		Size: 37.7 KB (37728 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-bookworm` - linux; arm variant v7

```console
$ docker pull httpd@sha256:e49897ae28bb259a5a1b205a464098038e49ea2bb4985187e84baac47edda986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52738179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9fefb7a703a9d947d489c78f23271b57b138126899b22193b569f3d5ceb0d2`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063593c7931b25f55a01b9bb0f7156d7398c702900d7c6c5a10ac3cb9b111eeb`  
		Last Modified: Wed, 24 Apr 2024 16:30:49 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60dd6c2df475ede40fbebdd310c9770f5c85d86278fe66bcfb34015f9975b80`  
		Last Modified: Wed, 24 Apr 2024 16:30:50 GMT  
		Size: 3.3 MB (3286910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5afe70e80d3c8da2e79abd6e84a95f7bb9516fe79ffc1e06abcb55d3af394429`  
		Last Modified: Wed, 24 Apr 2024 16:30:51 GMT  
		Size: 24.7 MB (24710357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e43b819248841764c8eaee46258c16341b869c3cd10e29c5fe19a7ad57d3ea0`  
		Last Modified: Wed, 24 Apr 2024 16:30:50 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-bookworm` - unknown; unknown

```console
$ docker pull httpd@sha256:daa1d3562f002200d97c8042f5fb9e5cce9d3a91b979ab3bae79daa3f5a6f0a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2516068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beda48825ccb307edac52c5e75efd8fc86548bb74670c0558d03c6057104e328`

```dockerfile
```

-	Layers:
	-	`sha256:6656cffeaa9a2613f22ecf4356afe7a1fd612ffb7430d4e7e2ab9004ece5d051`  
		Last Modified: Wed, 24 Apr 2024 16:30:50 GMT  
		Size: 2.5 MB (2478340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1efca153bd1cf7ed5e26102ed35722aa4aec61d831e71818bba3175e03866560`  
		Last Modified: Wed, 24 Apr 2024 16:30:50 GMT  
		Size: 37.7 KB (37728 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-bookworm` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:b2670b51810a49855b0b59ed87dd064b3ec3ecf95e77d9dd6f6d13bab7467dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58997314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73acb239a8eb7a9ef5b6848a5b01bb26cc03d2262056705876bf7ac6ad781f02`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855b568ab02c3fee1362d51176f966517b1e03ca0c8efde55eddace90835f300`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c521cc2c4e8a439951003122cdab841fe1b1350db864e2cf9dea69298513f711`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 3.8 MB (3824128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c8bced82bd1d3557a49d39ea03bb8090bf3abc8154ab65388d9f9728f3ce02`  
		Last Modified: Thu, 25 Apr 2024 07:23:09 GMT  
		Size: 26.0 MB (25992782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae159c85a0b3662b8e9d58344f7da1b84836a7338c8ddf6b88360cea400929f`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-bookworm` - unknown; unknown

```console
$ docker pull httpd@sha256:307bc20593c828b3894250dd4e16b149c046b98c033453278fca94efd8bd0454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70026eb22d8bfc08dc60be7e7dcdce118be2390abe04aa90c7f27e6245767782`

```dockerfile
```

-	Layers:
	-	`sha256:77720a2aab607f8a1c40306899700597640ec9696bb65c714e6131dd481171b1`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 2.5 MB (2476229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd136e58015bf40bdc568f33b0d261e3140c11eee1769fbfb67f4ad2b93284f8`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 37.6 KB (37618 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-bookworm` - linux; 386

```console
$ docker pull httpd@sha256:34359f60b5aa39dfe4a6da81d319693f6ca6155e12e91b50e5d6da3ae7db89b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60223958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457768b202e686803b86961428bc138b1e4c6f0a08bec510257bba9b2d7e4486`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2941e842a389d5a4c34aa8e7f83e761d6a0deb0ed5c5bc01838c71d23659ac77`  
		Last Modified: Wed, 24 Apr 2024 04:57:41 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f800dd9ec1f906ac5c081169392c9dd10d32921d3e52e601c8c7ca7bcda3c600`  
		Last Modified: Wed, 24 Apr 2024 04:57:42 GMT  
		Size: 4.1 MB (4063511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494266189a0019f5cc3fec9ab5a55a1ea0fc3c8cc6a3ab1c1faeedbdc0fbaa5e`  
		Last Modified: Wed, 24 Apr 2024 04:57:42 GMT  
		Size: 26.0 MB (25996792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed1b4c9db903ab4981ddd506901a8ead9ae515c81f307dc7e52ed0256e73eec`  
		Last Modified: Wed, 24 Apr 2024 04:57:41 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-bookworm` - unknown; unknown

```console
$ docker pull httpd@sha256:928d95daa4cdcfd2c1395f60c62ed85d871764fdbfd6b1dbcf750c4f906d1eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2510705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8144c9b91841f94cfaea34892b458353406e2daa257e7e97e80ce41341381322`

```dockerfile
```

-	Layers:
	-	`sha256:637adc441596f6bc7ae557cdd4ef0de555b3e1b8aaa69a88adf26ea73e04a753`  
		Last Modified: Wed, 24 Apr 2024 04:57:42 GMT  
		Size: 2.5 MB (2472991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c57120021da5fb478f2b39b4540d36f1ba9bfa1efbe1c0616a07fe2a81d1e746`  
		Last Modified: Wed, 24 Apr 2024 04:57:41 GMT  
		Size: 37.7 KB (37714 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-bookworm` - linux; mips64le

```console
$ docker pull httpd@sha256:4512a76c673f11979d9f2ea96a56c59db662c5e8258c7128258245d18bb9292d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58678876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f7e1281eca6101e477c1cb3af32334cd551c69acc34839c3a8f8e3b3be6e80`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28233217e5e2c53a42bce8370d4462ed742672e46ec0e3acc021494964a6c4e`  
		Last Modified: Wed, 24 Apr 2024 23:51:19 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98af3a5736d8674d724399887f435760548973f8720121002efb9766f6892bb1`  
		Last Modified: Wed, 24 Apr 2024 23:51:20 GMT  
		Size: 3.4 MB (3373290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d3af7336bf3047ff58c8fc60fcce4943c107ecf04bb449d43849ce851d53aa`  
		Last Modified: Wed, 24 Apr 2024 23:51:22 GMT  
		Size: 26.2 MB (26160940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ed9c80633a9c8a938fb64f3eddb5677882265446491ddb3fce480647719cf5`  
		Last Modified: Wed, 24 Apr 2024 23:51:20 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-bookworm` - unknown; unknown

```console
$ docker pull httpd@sha256:b80ddb9178f5c7b1fb405cdad5a1ca2b55ae93147230041eb0b0e958dd6bd2b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f0b12a55ecb5a0fb2dc015ef1bebad8c2d781a197cd3a665b0b585ef134715`

```dockerfile
```

-	Layers:
	-	`sha256:e03a7d994013fb85dd187518a518143a7a11bc11a02be3fe21ac1bcc6c2bad8c`  
		Last Modified: Wed, 24 Apr 2024 23:51:20 GMT  
		Size: 37.5 KB (37480 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-bookworm` - linux; ppc64le

```console
$ docker pull httpd@sha256:f367b8c823d8e9650e4d0f3576cb4cb56931fb2a9abc5cf933fbc3e5e2d03eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64781656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5b1ab6010140721a568d9027ba17353616269ed57d0407e63a20a9db866d83`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8779f7411971984d8a264462c07b9383e455edbfa3945c3a7c3c0f0da6281405`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df41593893685df2f819e89678437a7190515d7cc02ecf4d3826f45e94594a6`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 4.3 MB (4329567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5fc79508ca1591a5607565a2c2fd383aaea639b5a8777f026f5767404f73eb`  
		Last Modified: Thu, 25 Apr 2024 03:19:08 GMT  
		Size: 27.3 MB (27310418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3bf3ad211e2e210d10318ae48cfccfdefd6adae953aa2a10ca77880dd921ac`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-bookworm` - unknown; unknown

```console
$ docker pull httpd@sha256:f5fdb59224d04f59d5f80ba98a242d519237e7fe401672f767a98c516fbb17b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2518193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3109624aa7219e37cb7b867bf5926f24b5e9b4eb3d6e31536b83f1751b0c42cf`

```dockerfile
```

-	Layers:
	-	`sha256:5553f9b984d60f0b17ff79178b8bd6943ed3c6a28b511fee1a71f4df9b281e63`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 2.5 MB (2480527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49e0858fd1c6faa9c04410e63c7d7bf0b572ae75294b281ff9ce3ba69ca201b3`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 37.7 KB (37666 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2-bookworm` - linux; s390x

```console
$ docker pull httpd@sha256:ae3341db428440ab15b07058d2bab822247b8aa06035c19edea03f2a675e3b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56864928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed5070ae0d9687d8b499eae1be4caf30616eea45630f52af89bff9348d1cc474`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076f4d06a50ca8b3bcf6951ac8efa98b499598a608155af2bc4e4c0283e315e6`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8054bd786718ad21214203f377432a693d561157449486d1ea16ee3530d793e1`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 3.7 MB (3654647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c39e346caebedca77c0054fa938878774f458b3b88e05f7099ff4b70345256a`  
		Last Modified: Thu, 25 Apr 2024 02:28:32 GMT  
		Size: 25.7 MB (25697456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb3dcd087010aa65e19ef6e7ae889206220840a38cc7d973cd3b0e635895072`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2-bookworm` - unknown; unknown

```console
$ docker pull httpd@sha256:779ecac6b7d7547b09bf644ce963543f48bac336bfe174dbd0583d7d06e3b0c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d2597d4c0c4788030bfe3a20a2ddf9842323ed2e486b682e1a863ae138ad89`

```dockerfile
```

-	Layers:
	-	`sha256:d42e15caceec6e5f15ccf873f46289eb1dc452e23ab53a076d905630a09e58e5`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 2.5 MB (2475763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28db97fd901916835b62fdb1cece860a44f5b2888ae52a2ea94026e65e136df5`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 37.6 KB (37600 bytes)  
		MIME: application/vnd.in-toto+json

## `httpd:2.4`

```console
$ docker pull httpd@sha256:36c8c79f900108f0f09fd4148ad35ade57cba0dc19d13f3d15be24ce94e6a639
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

### `httpd:2.4` - linux; amd64

```console
$ docker pull httpd@sha256:518e9447a236de47cc2fb4f2dbf06466b6cd5cf50f9951742f9a20af76e8118d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59185382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c2fc9e3d849b21a35b4c96f5ad8ec4dc9b73ca44c56537039e8c6f3054db0a`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851c52adaa9bf680b2eaa45164baa37665418fb02666fb36c268002edd853994`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d9f60535a61833df2e57cc08221031d3ae50f3955a6d6b0153214619d357fb`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 4.0 MB (4006988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943a2b3cf551375517593790b58407ffc7028b4b34bca6c0756b76708ea4b3ce`  
		Last Modified: Wed, 24 Apr 2024 04:57:24 GMT  
		Size: 26.0 MB (26027444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea83e81966d64f34a57ffcc118b75ad19bc9321f9809cf9b0df25548a2fa695e`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4` - unknown; unknown

```console
$ docker pull httpd@sha256:e31d2d75b317933ed59c3503fcfd00357545f4e60e60d87368674365eed990bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc7b98024523f6963a92b3a8edb71945171fff164f1da1e3bc9296d404a1da2`

```dockerfile
```

-	Layers:
	-	`sha256:1a0e348c51fd80864d852c8a1b3dbe89c1cbf088a8d4fe204b4f9a2106b65425`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 2.5 MB (2475971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea347276a3b2b4390cbb875d979ac18e828399022ce83785af6a6e19535cf238`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 37.8 KB (37766 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4` - linux; arm variant v5

```console
$ docker pull httpd@sha256:6ac6acfaf36b492c8ee0271b5c1745e5d5173186838066fb55416fe1bad7f84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55660337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594aaef0a91e898dfb26ab368782f59da9b9f69c9ad0d9a155208b535102d8e8`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfdcc496dd931564ad13b4c74e84a37bd3e8fe4d3e8eef76531c007b4918eb3`  
		Last Modified: Wed, 24 Apr 2024 17:19:02 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7797397d89aa986596ae17907e8812fb696c601b77e453f8cfff70c5282bb68`  
		Last Modified: Wed, 24 Apr 2024 17:19:03 GMT  
		Size: 3.5 MB (3511113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabda791a3820471d4af8b4b5339e9e5ade214d951432d16dcf09a30dfc07788`  
		Last Modified: Wed, 24 Apr 2024 17:19:04 GMT  
		Size: 25.2 MB (25238724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7b73f2fae9dae743b3751fc794fe838ccfee7359899fe2ef291db96f774025`  
		Last Modified: Wed, 24 Apr 2024 17:19:03 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4` - unknown; unknown

```console
$ docker pull httpd@sha256:0559103a0db87f5edf6e70a2fce9af410a68e8207c18d62b1a99fa7d6081320a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2517016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5eb9364b67ec513d9aa9dab74264a7e94017611ae8f167c5e716aad4b7680e`

```dockerfile
```

-	Layers:
	-	`sha256:0fd0fb4e581c468abde2999045c163e01f5f465436e7aa62ce734436862f9eac`  
		Last Modified: Wed, 24 Apr 2024 17:19:03 GMT  
		Size: 2.5 MB (2479288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38cc0fcc6c1dede08c15c91c4bc214763cd7fb9e515bc4f8b07ba05cdc9cd387`  
		Last Modified: Wed, 24 Apr 2024 17:19:03 GMT  
		Size: 37.7 KB (37728 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4` - linux; arm variant v7

```console
$ docker pull httpd@sha256:e49897ae28bb259a5a1b205a464098038e49ea2bb4985187e84baac47edda986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52738179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9fefb7a703a9d947d489c78f23271b57b138126899b22193b569f3d5ceb0d2`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063593c7931b25f55a01b9bb0f7156d7398c702900d7c6c5a10ac3cb9b111eeb`  
		Last Modified: Wed, 24 Apr 2024 16:30:49 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60dd6c2df475ede40fbebdd310c9770f5c85d86278fe66bcfb34015f9975b80`  
		Last Modified: Wed, 24 Apr 2024 16:30:50 GMT  
		Size: 3.3 MB (3286910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5afe70e80d3c8da2e79abd6e84a95f7bb9516fe79ffc1e06abcb55d3af394429`  
		Last Modified: Wed, 24 Apr 2024 16:30:51 GMT  
		Size: 24.7 MB (24710357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e43b819248841764c8eaee46258c16341b869c3cd10e29c5fe19a7ad57d3ea0`  
		Last Modified: Wed, 24 Apr 2024 16:30:50 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4` - unknown; unknown

```console
$ docker pull httpd@sha256:daa1d3562f002200d97c8042f5fb9e5cce9d3a91b979ab3bae79daa3f5a6f0a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2516068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beda48825ccb307edac52c5e75efd8fc86548bb74670c0558d03c6057104e328`

```dockerfile
```

-	Layers:
	-	`sha256:6656cffeaa9a2613f22ecf4356afe7a1fd612ffb7430d4e7e2ab9004ece5d051`  
		Last Modified: Wed, 24 Apr 2024 16:30:50 GMT  
		Size: 2.5 MB (2478340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1efca153bd1cf7ed5e26102ed35722aa4aec61d831e71818bba3175e03866560`  
		Last Modified: Wed, 24 Apr 2024 16:30:50 GMT  
		Size: 37.7 KB (37728 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:b2670b51810a49855b0b59ed87dd064b3ec3ecf95e77d9dd6f6d13bab7467dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58997314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73acb239a8eb7a9ef5b6848a5b01bb26cc03d2262056705876bf7ac6ad781f02`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855b568ab02c3fee1362d51176f966517b1e03ca0c8efde55eddace90835f300`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c521cc2c4e8a439951003122cdab841fe1b1350db864e2cf9dea69298513f711`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 3.8 MB (3824128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c8bced82bd1d3557a49d39ea03bb8090bf3abc8154ab65388d9f9728f3ce02`  
		Last Modified: Thu, 25 Apr 2024 07:23:09 GMT  
		Size: 26.0 MB (25992782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae159c85a0b3662b8e9d58344f7da1b84836a7338c8ddf6b88360cea400929f`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4` - unknown; unknown

```console
$ docker pull httpd@sha256:307bc20593c828b3894250dd4e16b149c046b98c033453278fca94efd8bd0454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70026eb22d8bfc08dc60be7e7dcdce118be2390abe04aa90c7f27e6245767782`

```dockerfile
```

-	Layers:
	-	`sha256:77720a2aab607f8a1c40306899700597640ec9696bb65c714e6131dd481171b1`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 2.5 MB (2476229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd136e58015bf40bdc568f33b0d261e3140c11eee1769fbfb67f4ad2b93284f8`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 37.6 KB (37618 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4` - linux; 386

```console
$ docker pull httpd@sha256:34359f60b5aa39dfe4a6da81d319693f6ca6155e12e91b50e5d6da3ae7db89b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60223958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457768b202e686803b86961428bc138b1e4c6f0a08bec510257bba9b2d7e4486`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2941e842a389d5a4c34aa8e7f83e761d6a0deb0ed5c5bc01838c71d23659ac77`  
		Last Modified: Wed, 24 Apr 2024 04:57:41 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f800dd9ec1f906ac5c081169392c9dd10d32921d3e52e601c8c7ca7bcda3c600`  
		Last Modified: Wed, 24 Apr 2024 04:57:42 GMT  
		Size: 4.1 MB (4063511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494266189a0019f5cc3fec9ab5a55a1ea0fc3c8cc6a3ab1c1faeedbdc0fbaa5e`  
		Last Modified: Wed, 24 Apr 2024 04:57:42 GMT  
		Size: 26.0 MB (25996792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed1b4c9db903ab4981ddd506901a8ead9ae515c81f307dc7e52ed0256e73eec`  
		Last Modified: Wed, 24 Apr 2024 04:57:41 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4` - unknown; unknown

```console
$ docker pull httpd@sha256:928d95daa4cdcfd2c1395f60c62ed85d871764fdbfd6b1dbcf750c4f906d1eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2510705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8144c9b91841f94cfaea34892b458353406e2daa257e7e97e80ce41341381322`

```dockerfile
```

-	Layers:
	-	`sha256:637adc441596f6bc7ae557cdd4ef0de555b3e1b8aaa69a88adf26ea73e04a753`  
		Last Modified: Wed, 24 Apr 2024 04:57:42 GMT  
		Size: 2.5 MB (2472991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c57120021da5fb478f2b39b4540d36f1ba9bfa1efbe1c0616a07fe2a81d1e746`  
		Last Modified: Wed, 24 Apr 2024 04:57:41 GMT  
		Size: 37.7 KB (37714 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4` - linux; mips64le

```console
$ docker pull httpd@sha256:4512a76c673f11979d9f2ea96a56c59db662c5e8258c7128258245d18bb9292d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58678876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f7e1281eca6101e477c1cb3af32334cd551c69acc34839c3a8f8e3b3be6e80`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28233217e5e2c53a42bce8370d4462ed742672e46ec0e3acc021494964a6c4e`  
		Last Modified: Wed, 24 Apr 2024 23:51:19 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98af3a5736d8674d724399887f435760548973f8720121002efb9766f6892bb1`  
		Last Modified: Wed, 24 Apr 2024 23:51:20 GMT  
		Size: 3.4 MB (3373290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d3af7336bf3047ff58c8fc60fcce4943c107ecf04bb449d43849ce851d53aa`  
		Last Modified: Wed, 24 Apr 2024 23:51:22 GMT  
		Size: 26.2 MB (26160940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ed9c80633a9c8a938fb64f3eddb5677882265446491ddb3fce480647719cf5`  
		Last Modified: Wed, 24 Apr 2024 23:51:20 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4` - unknown; unknown

```console
$ docker pull httpd@sha256:b80ddb9178f5c7b1fb405cdad5a1ca2b55ae93147230041eb0b0e958dd6bd2b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f0b12a55ecb5a0fb2dc015ef1bebad8c2d781a197cd3a665b0b585ef134715`

```dockerfile
```

-	Layers:
	-	`sha256:e03a7d994013fb85dd187518a518143a7a11bc11a02be3fe21ac1bcc6c2bad8c`  
		Last Modified: Wed, 24 Apr 2024 23:51:20 GMT  
		Size: 37.5 KB (37480 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4` - linux; ppc64le

```console
$ docker pull httpd@sha256:f367b8c823d8e9650e4d0f3576cb4cb56931fb2a9abc5cf933fbc3e5e2d03eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64781656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5b1ab6010140721a568d9027ba17353616269ed57d0407e63a20a9db866d83`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8779f7411971984d8a264462c07b9383e455edbfa3945c3a7c3c0f0da6281405`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df41593893685df2f819e89678437a7190515d7cc02ecf4d3826f45e94594a6`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 4.3 MB (4329567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5fc79508ca1591a5607565a2c2fd383aaea639b5a8777f026f5767404f73eb`  
		Last Modified: Thu, 25 Apr 2024 03:19:08 GMT  
		Size: 27.3 MB (27310418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3bf3ad211e2e210d10318ae48cfccfdefd6adae953aa2a10ca77880dd921ac`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4` - unknown; unknown

```console
$ docker pull httpd@sha256:f5fdb59224d04f59d5f80ba98a242d519237e7fe401672f767a98c516fbb17b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2518193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3109624aa7219e37cb7b867bf5926f24b5e9b4eb3d6e31536b83f1751b0c42cf`

```dockerfile
```

-	Layers:
	-	`sha256:5553f9b984d60f0b17ff79178b8bd6943ed3c6a28b511fee1a71f4df9b281e63`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 2.5 MB (2480527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49e0858fd1c6faa9c04410e63c7d7bf0b572ae75294b281ff9ce3ba69ca201b3`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 37.7 KB (37666 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4` - linux; s390x

```console
$ docker pull httpd@sha256:ae3341db428440ab15b07058d2bab822247b8aa06035c19edea03f2a675e3b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56864928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed5070ae0d9687d8b499eae1be4caf30616eea45630f52af89bff9348d1cc474`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076f4d06a50ca8b3bcf6951ac8efa98b499598a608155af2bc4e4c0283e315e6`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8054bd786718ad21214203f377432a693d561157449486d1ea16ee3530d793e1`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 3.7 MB (3654647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c39e346caebedca77c0054fa938878774f458b3b88e05f7099ff4b70345256a`  
		Last Modified: Thu, 25 Apr 2024 02:28:32 GMT  
		Size: 25.7 MB (25697456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb3dcd087010aa65e19ef6e7ae889206220840a38cc7d973cd3b0e635895072`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4` - unknown; unknown

```console
$ docker pull httpd@sha256:779ecac6b7d7547b09bf644ce963543f48bac336bfe174dbd0583d7d06e3b0c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d2597d4c0c4788030bfe3a20a2ddf9842323ed2e486b682e1a863ae138ad89`

```dockerfile
```

-	Layers:
	-	`sha256:d42e15caceec6e5f15ccf873f46289eb1dc452e23ab53a076d905630a09e58e5`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 2.5 MB (2475763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28db97fd901916835b62fdb1cece860a44f5b2888ae52a2ea94026e65e136df5`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 37.6 KB (37600 bytes)  
		MIME: application/vnd.in-toto+json

## `httpd:2.4-alpine`

```console
$ docker pull httpd@sha256:68f6714169b70ca33126c46f60cc802eb602c6435f4ebf08349d871d500d3e70
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

### `httpd:2.4-alpine` - linux; amd64

```console
$ docker pull httpd@sha256:b48b48dcfff1407638908b8a1782480df0ad8bac7f5fc579496357864f97e60c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18905522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b6bf3450e2114fc55779cd878fa1a176a851a4de5a38f79ffb779639c455a2`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e13f4f5374dc8e6fd59fc8dc82c77d2dfc85ffd1136f5edbc4a9054ba955927`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333c1d8ec87c0966bd88d1293586bce65663a901c08af2a85ffe369897d7fd9e`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58593e44a54df297fb6195ac992fbda56ab083ee57a934ba5de6c49c8c6cff4a`  
		Last Modified: Fri, 05 Apr 2024 17:53:06 GMT  
		Size: 10.4 MB (10384953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608381599c688e98facb252c7e8313379b6d1f574bba1b49262a39145764d4d9`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 5.1 MB (5110138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e5ce613b310458e6aad12ed911fae7e33b9d59232a0a816ae8829774a7c351`  
		Last Modified: Fri, 05 Apr 2024 17:53:06 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:933e4cc35d564b7e6b37b9da44ff4c3a1c961ee5a115addfc4348458b9584a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1105171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32930164a83ab310294ec129967dfa6b0e208133bcd30d31b8bdaae148384c8c`

```dockerfile
```

-	Layers:
	-	`sha256:4ce2b7d308346544402cfbaecf8b70c4dfbb6d6385f79028bfeb7b9df16b2b23`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 1.1 MB (1067018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f7979b59e4c92069c8731802e0b918cc1668ed3cbc3448ac9f5863488762eec`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 38.2 KB (38153 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-alpine` - linux; arm variant v6

```console
$ docker pull httpd@sha256:3536bda1cb1b0f3581896c7acafa8426a67ac185711f3af26cffb991a76d08fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17774769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1732292898ef3f1fb223e062d5aa76bcf8087c9c7978a357ea964a0f9e6e2a4d`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8c07a4a93f0faf2d460b21b916e9f8d52550da29882704b17b06201a89e118`  
		Last Modified: Fri, 05 Apr 2024 18:11:18 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001db4688f33e38d27d733b6d51f6a9edf395f4fd76749cf91ebb32f1fd25483`  
		Last Modified: Fri, 05 Apr 2024 18:11:18 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f8fe9e9d09c4f2074ab547012fee140749069dd339f3cc87dc71e347884d92`  
		Last Modified: Fri, 05 Apr 2024 18:11:19 GMT  
		Size: 9.6 MB (9577820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c092ec8ebe549b81d3f7c2f8f6830bfc42142f090d8fe5cd5b52f296d516310`  
		Last Modified: Fri, 05 Apr 2024 18:11:19 GMT  
		Size: 5.0 MB (5029848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346b9e25e64782fa95573e9eb07893339f472741823a4062737052da7391dfd5`  
		Last Modified: Fri, 05 Apr 2024 18:11:20 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:2790d9e49f2d98ffc37ada24de30725d9196ac28a61fd2ef576263287c58aec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d270ac30275fb727064cc5d2eeeb08a7ffc7305c12f93e19d03d209ebc2d6f58`

```dockerfile
```

-	Layers:
	-	`sha256:57b3e792cca6cdd007c318692afa6ccc61834b2e257e11c1832e8403dd37032e`  
		Last Modified: Fri, 05 Apr 2024 18:11:18 GMT  
		Size: 37.9 KB (37910 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-alpine` - linux; arm variant v7

```console
$ docker pull httpd@sha256:09dd424663b1d2540476d34b124fb25360411dff64f69cc71fa3cf02381fb9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16993127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad0e3a5244891745dcd5889901c7a0101e398b81de79ff65cb7270e482bbbbb`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74aa637d7bf59fca068dcb5b7dd86513aa9ad3282aad69b3e9039cc2f6f18bcc`  
		Last Modified: Sat, 16 Mar 2024 16:04:22 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fc40e56afb70a5d1bf79dc4bf9118f2b993e3687626ab036513d862a1a286e`  
		Last Modified: Sat, 16 Mar 2024 16:04:22 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7015ed48724aa34bf3e29ddfa9b1058e3c374c383a17cc3ba6b943f7de0cf1`  
		Last Modified: Sat, 16 Mar 2024 16:04:23 GMT  
		Size: 9.3 MB (9334751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5553e605c52a438be1d61a267e9cbc342a533ce3966d9c82b03dfe7e0f1777c8`  
		Last Modified: Fri, 05 Apr 2024 17:57:38 GMT  
		Size: 4.7 MB (4737771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a356346eae4cb6bddf85f93948a3f0df8845d93176937fef76aec99cb50faef2`  
		Last Modified: Fri, 05 Apr 2024 17:57:37 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:28d8f38fd78210cba28d51dc8d470fc5068b2d90a3fd9cb0a9f14a622ff89577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1102820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3348381822a72f52b9575c5d5d34c4da16730f59ef5128ebdedb089cd1d48819`

```dockerfile
```

-	Layers:
	-	`sha256:9e5deb95007dd7e44d0a6f9d0c0ccf2ee83e76cb545b6c4691007c75be1c6498`  
		Last Modified: Fri, 05 Apr 2024 17:57:38 GMT  
		Size: 1.1 MB (1064695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a16e23262169a2b30cd14de32d5acde981fcd5bf7179967f584df46c44b1b10`  
		Last Modified: Fri, 05 Apr 2024 17:57:37 GMT  
		Size: 38.1 KB (38125 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-alpine` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:91756bbcc9b8283d49fdf66189881d39576f12c012dad8796b97948636e0b40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (18989141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d3d050f8abbaa153d704cae494aeeca773a0f24ba35600711e356083a79a66`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68b5c4e3f3b827d8933253d337cf55bf3ace2d75070b8ea7655a893c325569f`  
		Last Modified: Sat, 16 Mar 2024 15:13:13 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba68aab08183c67e796b91cc96b7c1629e35f98048a721cd67997edb83a202e2`  
		Last Modified: Sat, 16 Mar 2024 15:13:13 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1e2b5044558ea2188f9ba4d34df06cc7109e01f5caefe6c2bc5ecd11b6ced0`  
		Last Modified: Sat, 16 Mar 2024 15:13:14 GMT  
		Size: 10.4 MB (10388804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6beaeaed29f48ef5f4141a8b7e76a8e550f88775f81d464c5944634479d8ed7a`  
		Last Modified: Fri, 05 Apr 2024 17:55:14 GMT  
		Size: 5.3 MB (5250912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8742eb1c1f87645540c4e75db0e19ba29d77c28e18927d3310670a72b85ec82`  
		Last Modified: Fri, 05 Apr 2024 17:55:13 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:b266b0cecec670e48d25423f3f218b28b7745ec04fa2be113bca803f25a89f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1100073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a241afe2d5ab26a07a1794465d326a6827b70fbef1de59a250d03605dac1ded`

```dockerfile
```

-	Layers:
	-	`sha256:43abc3efae9947304de80f9a75aa23117ac15a382c784b355816810199ecbf7e`  
		Last Modified: Fri, 05 Apr 2024 17:55:13 GMT  
		Size: 1.1 MB (1062068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dcf770b26d2bae0707f3d339ee48b6778855e725144a0d1384402416186c295`  
		Last Modified: Fri, 05 Apr 2024 17:55:13 GMT  
		Size: 38.0 KB (38005 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-alpine` - linux; 386

```console
$ docker pull httpd@sha256:40a391f6e52f9fa6d56741b455cbffde4d9104948f1078da5bd6c248b3318f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18161726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa32e51497f1ebc9739fe8b3d915e5fecd520dd4959266c76adf910b71fd4ea`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740e52eababa89f531e99d9609ea4df66e75527cb8a97aa3feba95f64f8d19c1`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9d066a768f0f31e823ea143de9180c7e2b5b51ee3f0267272b2122353c5530`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320efa4f4b1525ce8d8dc283fe9bce7bf23e031d3349b59957067c1ad3f22eeb`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 9.9 MB (9862040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b89437c703e9c702702c5eb0432f2efcb16ae506d611336abbf81b083b7fbd`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 5.1 MB (5053894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1099f38eb4d16ee148b32677e9f70da2535bef69261361e1247b719b03f5a2c4`  
		Last Modified: Fri, 05 Apr 2024 17:53:13 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:52a1c8f1cdb4a7057132a6bc0f6f82528ee10ccffedf7bb17d1108bf94d8ac6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1105068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946eef1c61b246af219f7ef605bfd198e004722dc6d7fafdaa0a35c5504965e7`

```dockerfile
```

-	Layers:
	-	`sha256:56b910d095946bc43dbafed2e0f13360d62f86b726feba74f5670cb07cd93f3d`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 1.1 MB (1066973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37abeadc160510b3cfd3b1a3d82f05e600fcbb1c92c9b5e2c0a20b0c8e865bc7`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 38.1 KB (38095 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-alpine` - linux; ppc64le

```console
$ docker pull httpd@sha256:447d4eca233b95a1aebdb73d93c024d8226d6a608568aa2c9505f96a3b8f19bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19410079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bed7414a71a37df5ac42b1637107b9e12f08cc3e63e5d9ecd84556d26489d9b`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca1e90415bffcf574224c85fef296c0f849237fe22a0b5065a26673f7cbba51`  
		Last Modified: Sat, 16 Mar 2024 10:26:53 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b746962fe11d53bb9b19dfe7990c4658ac0472cccbd8daa5794e5f3a22cfda51`  
		Last Modified: Sat, 16 Mar 2024 10:26:53 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68b51060f0a52e914490ae4eeb10af1258ec331a68f78f4944118a1ca9911bd`  
		Last Modified: Sat, 16 Mar 2024 10:26:54 GMT  
		Size: 10.6 MB (10627211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f73e01f2b7ec6f92d901b09901b77c8dec59f0535633de6f26cc281f9452954`  
		Last Modified: Fri, 05 Apr 2024 17:59:16 GMT  
		Size: 5.4 MB (5422810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13941787572cd155aec58f453b55fcb5e882b928cf4aa65c8ede53e07d15a45`  
		Last Modified: Fri, 05 Apr 2024 17:59:16 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:6591d53cc91652e76f1529af4696e990fe459184e928ac7371b55488a2f3b7c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1098208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d59400ec49b3e236a314b42b69e345faf3cdcfbf0bd553b5d16dfc66d548bdd`

```dockerfile
```

-	Layers:
	-	`sha256:630456dcd802b6d23b26b5dc5b782789bc8969758ecdeca80d33ca2ef97be7bb`  
		Last Modified: Fri, 05 Apr 2024 17:59:16 GMT  
		Size: 1.1 MB (1060153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49cbad644a03a7cf5127a55a38cc827f068240cd3ce64261f61e48708941076d`  
		Last Modified: Fri, 05 Apr 2024 17:59:16 GMT  
		Size: 38.1 KB (38055 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-alpine` - linux; s390x

```console
$ docker pull httpd@sha256:8ddf2e0f8ccad02de20eaba4fa2f2e046b0032e4e17e481667d6226b3ec82061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19505364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b21662b1d3ba291b541e6898e9870c8f17fc32fc1542e8cd26321d995ed654`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d37ece6c30e22e249589d6aeda58cf29c409948f056a8037f657691f333031`  
		Last Modified: Sun, 17 Mar 2024 22:03:24 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de6b96fd2b7588019fbfc72d5afede300a4d0ef5ea65a7a99fb9715b40b506a`  
		Last Modified: Sun, 17 Mar 2024 22:03:24 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e00979af0d93fc259d0c067c3acf72e2d19ee3e48b840e26b9838a1882a12b`  
		Last Modified: Sun, 17 Mar 2024 22:03:25 GMT  
		Size: 11.0 MB (10985997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fdd3af6a86a6153ff1589309d30e18935c2aacf45522556151835153652514`  
		Last Modified: Sat, 06 Apr 2024 15:46:55 GMT  
		Size: 5.3 MB (5275029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6015f889334ad064a637db08b112726bb85893466a14f46b4034fa7edfa031b0`  
		Last Modified: Sat, 06 Apr 2024 15:46:55 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:f6d2ea0678751c8928910a6156f560c2dde868a32d09c26c484866d783af994d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1098082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd8c653038d8341ffbc2492c22b6e5888612cf77dba81bac930256963bfb5d4`

```dockerfile
```

-	Layers:
	-	`sha256:a9f0621638da42ab83a8b188d1b0e79887b581ba27e779272a93e6bd57ffc94a`  
		Last Modified: Sat, 06 Apr 2024 15:46:55 GMT  
		Size: 1.1 MB (1060095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1f2fc0d9673de65aa6403e6d5aff61166189f0445f2df8c80cea6225a259da`  
		Last Modified: Sat, 06 Apr 2024 15:46:55 GMT  
		Size: 38.0 KB (37987 bytes)  
		MIME: application/vnd.in-toto+json

## `httpd:2.4-alpine3.19`

```console
$ docker pull httpd@sha256:68f6714169b70ca33126c46f60cc802eb602c6435f4ebf08349d871d500d3e70
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

### `httpd:2.4-alpine3.19` - linux; amd64

```console
$ docker pull httpd@sha256:b48b48dcfff1407638908b8a1782480df0ad8bac7f5fc579496357864f97e60c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18905522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b6bf3450e2114fc55779cd878fa1a176a851a4de5a38f79ffb779639c455a2`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e13f4f5374dc8e6fd59fc8dc82c77d2dfc85ffd1136f5edbc4a9054ba955927`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333c1d8ec87c0966bd88d1293586bce65663a901c08af2a85ffe369897d7fd9e`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58593e44a54df297fb6195ac992fbda56ab083ee57a934ba5de6c49c8c6cff4a`  
		Last Modified: Fri, 05 Apr 2024 17:53:06 GMT  
		Size: 10.4 MB (10384953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608381599c688e98facb252c7e8313379b6d1f574bba1b49262a39145764d4d9`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 5.1 MB (5110138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e5ce613b310458e6aad12ed911fae7e33b9d59232a0a816ae8829774a7c351`  
		Last Modified: Fri, 05 Apr 2024 17:53:06 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:933e4cc35d564b7e6b37b9da44ff4c3a1c961ee5a115addfc4348458b9584a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1105171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32930164a83ab310294ec129967dfa6b0e208133bcd30d31b8bdaae148384c8c`

```dockerfile
```

-	Layers:
	-	`sha256:4ce2b7d308346544402cfbaecf8b70c4dfbb6d6385f79028bfeb7b9df16b2b23`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 1.1 MB (1067018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f7979b59e4c92069c8731802e0b918cc1668ed3cbc3448ac9f5863488762eec`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 38.2 KB (38153 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-alpine3.19` - linux; arm variant v6

```console
$ docker pull httpd@sha256:3536bda1cb1b0f3581896c7acafa8426a67ac185711f3af26cffb991a76d08fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17774769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1732292898ef3f1fb223e062d5aa76bcf8087c9c7978a357ea964a0f9e6e2a4d`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8c07a4a93f0faf2d460b21b916e9f8d52550da29882704b17b06201a89e118`  
		Last Modified: Fri, 05 Apr 2024 18:11:18 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001db4688f33e38d27d733b6d51f6a9edf395f4fd76749cf91ebb32f1fd25483`  
		Last Modified: Fri, 05 Apr 2024 18:11:18 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f8fe9e9d09c4f2074ab547012fee140749069dd339f3cc87dc71e347884d92`  
		Last Modified: Fri, 05 Apr 2024 18:11:19 GMT  
		Size: 9.6 MB (9577820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c092ec8ebe549b81d3f7c2f8f6830bfc42142f090d8fe5cd5b52f296d516310`  
		Last Modified: Fri, 05 Apr 2024 18:11:19 GMT  
		Size: 5.0 MB (5029848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346b9e25e64782fa95573e9eb07893339f472741823a4062737052da7391dfd5`  
		Last Modified: Fri, 05 Apr 2024 18:11:20 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:2790d9e49f2d98ffc37ada24de30725d9196ac28a61fd2ef576263287c58aec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d270ac30275fb727064cc5d2eeeb08a7ffc7305c12f93e19d03d209ebc2d6f58`

```dockerfile
```

-	Layers:
	-	`sha256:57b3e792cca6cdd007c318692afa6ccc61834b2e257e11c1832e8403dd37032e`  
		Last Modified: Fri, 05 Apr 2024 18:11:18 GMT  
		Size: 37.9 KB (37910 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-alpine3.19` - linux; arm variant v7

```console
$ docker pull httpd@sha256:09dd424663b1d2540476d34b124fb25360411dff64f69cc71fa3cf02381fb9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16993127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad0e3a5244891745dcd5889901c7a0101e398b81de79ff65cb7270e482bbbbb`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74aa637d7bf59fca068dcb5b7dd86513aa9ad3282aad69b3e9039cc2f6f18bcc`  
		Last Modified: Sat, 16 Mar 2024 16:04:22 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fc40e56afb70a5d1bf79dc4bf9118f2b993e3687626ab036513d862a1a286e`  
		Last Modified: Sat, 16 Mar 2024 16:04:22 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7015ed48724aa34bf3e29ddfa9b1058e3c374c383a17cc3ba6b943f7de0cf1`  
		Last Modified: Sat, 16 Mar 2024 16:04:23 GMT  
		Size: 9.3 MB (9334751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5553e605c52a438be1d61a267e9cbc342a533ce3966d9c82b03dfe7e0f1777c8`  
		Last Modified: Fri, 05 Apr 2024 17:57:38 GMT  
		Size: 4.7 MB (4737771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a356346eae4cb6bddf85f93948a3f0df8845d93176937fef76aec99cb50faef2`  
		Last Modified: Fri, 05 Apr 2024 17:57:37 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:28d8f38fd78210cba28d51dc8d470fc5068b2d90a3fd9cb0a9f14a622ff89577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1102820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3348381822a72f52b9575c5d5d34c4da16730f59ef5128ebdedb089cd1d48819`

```dockerfile
```

-	Layers:
	-	`sha256:9e5deb95007dd7e44d0a6f9d0c0ccf2ee83e76cb545b6c4691007c75be1c6498`  
		Last Modified: Fri, 05 Apr 2024 17:57:38 GMT  
		Size: 1.1 MB (1064695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a16e23262169a2b30cd14de32d5acde981fcd5bf7179967f584df46c44b1b10`  
		Last Modified: Fri, 05 Apr 2024 17:57:37 GMT  
		Size: 38.1 KB (38125 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:91756bbcc9b8283d49fdf66189881d39576f12c012dad8796b97948636e0b40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (18989141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d3d050f8abbaa153d704cae494aeeca773a0f24ba35600711e356083a79a66`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68b5c4e3f3b827d8933253d337cf55bf3ace2d75070b8ea7655a893c325569f`  
		Last Modified: Sat, 16 Mar 2024 15:13:13 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba68aab08183c67e796b91cc96b7c1629e35f98048a721cd67997edb83a202e2`  
		Last Modified: Sat, 16 Mar 2024 15:13:13 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1e2b5044558ea2188f9ba4d34df06cc7109e01f5caefe6c2bc5ecd11b6ced0`  
		Last Modified: Sat, 16 Mar 2024 15:13:14 GMT  
		Size: 10.4 MB (10388804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6beaeaed29f48ef5f4141a8b7e76a8e550f88775f81d464c5944634479d8ed7a`  
		Last Modified: Fri, 05 Apr 2024 17:55:14 GMT  
		Size: 5.3 MB (5250912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8742eb1c1f87645540c4e75db0e19ba29d77c28e18927d3310670a72b85ec82`  
		Last Modified: Fri, 05 Apr 2024 17:55:13 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:b266b0cecec670e48d25423f3f218b28b7745ec04fa2be113bca803f25a89f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1100073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a241afe2d5ab26a07a1794465d326a6827b70fbef1de59a250d03605dac1ded`

```dockerfile
```

-	Layers:
	-	`sha256:43abc3efae9947304de80f9a75aa23117ac15a382c784b355816810199ecbf7e`  
		Last Modified: Fri, 05 Apr 2024 17:55:13 GMT  
		Size: 1.1 MB (1062068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dcf770b26d2bae0707f3d339ee48b6778855e725144a0d1384402416186c295`  
		Last Modified: Fri, 05 Apr 2024 17:55:13 GMT  
		Size: 38.0 KB (38005 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-alpine3.19` - linux; 386

```console
$ docker pull httpd@sha256:40a391f6e52f9fa6d56741b455cbffde4d9104948f1078da5bd6c248b3318f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18161726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa32e51497f1ebc9739fe8b3d915e5fecd520dd4959266c76adf910b71fd4ea`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740e52eababa89f531e99d9609ea4df66e75527cb8a97aa3feba95f64f8d19c1`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9d066a768f0f31e823ea143de9180c7e2b5b51ee3f0267272b2122353c5530`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320efa4f4b1525ce8d8dc283fe9bce7bf23e031d3349b59957067c1ad3f22eeb`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 9.9 MB (9862040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b89437c703e9c702702c5eb0432f2efcb16ae506d611336abbf81b083b7fbd`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 5.1 MB (5053894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1099f38eb4d16ee148b32677e9f70da2535bef69261361e1247b719b03f5a2c4`  
		Last Modified: Fri, 05 Apr 2024 17:53:13 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:52a1c8f1cdb4a7057132a6bc0f6f82528ee10ccffedf7bb17d1108bf94d8ac6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1105068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946eef1c61b246af219f7ef605bfd198e004722dc6d7fafdaa0a35c5504965e7`

```dockerfile
```

-	Layers:
	-	`sha256:56b910d095946bc43dbafed2e0f13360d62f86b726feba74f5670cb07cd93f3d`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 1.1 MB (1066973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37abeadc160510b3cfd3b1a3d82f05e600fcbb1c92c9b5e2c0a20b0c8e865bc7`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 38.1 KB (38095 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-alpine3.19` - linux; ppc64le

```console
$ docker pull httpd@sha256:447d4eca233b95a1aebdb73d93c024d8226d6a608568aa2c9505f96a3b8f19bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19410079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bed7414a71a37df5ac42b1637107b9e12f08cc3e63e5d9ecd84556d26489d9b`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca1e90415bffcf574224c85fef296c0f849237fe22a0b5065a26673f7cbba51`  
		Last Modified: Sat, 16 Mar 2024 10:26:53 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b746962fe11d53bb9b19dfe7990c4658ac0472cccbd8daa5794e5f3a22cfda51`  
		Last Modified: Sat, 16 Mar 2024 10:26:53 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68b51060f0a52e914490ae4eeb10af1258ec331a68f78f4944118a1ca9911bd`  
		Last Modified: Sat, 16 Mar 2024 10:26:54 GMT  
		Size: 10.6 MB (10627211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f73e01f2b7ec6f92d901b09901b77c8dec59f0535633de6f26cc281f9452954`  
		Last Modified: Fri, 05 Apr 2024 17:59:16 GMT  
		Size: 5.4 MB (5422810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13941787572cd155aec58f453b55fcb5e882b928cf4aa65c8ede53e07d15a45`  
		Last Modified: Fri, 05 Apr 2024 17:59:16 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:6591d53cc91652e76f1529af4696e990fe459184e928ac7371b55488a2f3b7c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1098208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d59400ec49b3e236a314b42b69e345faf3cdcfbf0bd553b5d16dfc66d548bdd`

```dockerfile
```

-	Layers:
	-	`sha256:630456dcd802b6d23b26b5dc5b782789bc8969758ecdeca80d33ca2ef97be7bb`  
		Last Modified: Fri, 05 Apr 2024 17:59:16 GMT  
		Size: 1.1 MB (1060153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49cbad644a03a7cf5127a55a38cc827f068240cd3ce64261f61e48708941076d`  
		Last Modified: Fri, 05 Apr 2024 17:59:16 GMT  
		Size: 38.1 KB (38055 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-alpine3.19` - linux; s390x

```console
$ docker pull httpd@sha256:8ddf2e0f8ccad02de20eaba4fa2f2e046b0032e4e17e481667d6226b3ec82061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19505364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b21662b1d3ba291b541e6898e9870c8f17fc32fc1542e8cd26321d995ed654`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d37ece6c30e22e249589d6aeda58cf29c409948f056a8037f657691f333031`  
		Last Modified: Sun, 17 Mar 2024 22:03:24 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de6b96fd2b7588019fbfc72d5afede300a4d0ef5ea65a7a99fb9715b40b506a`  
		Last Modified: Sun, 17 Mar 2024 22:03:24 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e00979af0d93fc259d0c067c3acf72e2d19ee3e48b840e26b9838a1882a12b`  
		Last Modified: Sun, 17 Mar 2024 22:03:25 GMT  
		Size: 11.0 MB (10985997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fdd3af6a86a6153ff1589309d30e18935c2aacf45522556151835153652514`  
		Last Modified: Sat, 06 Apr 2024 15:46:55 GMT  
		Size: 5.3 MB (5275029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6015f889334ad064a637db08b112726bb85893466a14f46b4034fa7edfa031b0`  
		Last Modified: Sat, 06 Apr 2024 15:46:55 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:f6d2ea0678751c8928910a6156f560c2dde868a32d09c26c484866d783af994d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1098082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd8c653038d8341ffbc2492c22b6e5888612cf77dba81bac930256963bfb5d4`

```dockerfile
```

-	Layers:
	-	`sha256:a9f0621638da42ab83a8b188d1b0e79887b581ba27e779272a93e6bd57ffc94a`  
		Last Modified: Sat, 06 Apr 2024 15:46:55 GMT  
		Size: 1.1 MB (1060095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1f2fc0d9673de65aa6403e6d5aff61166189f0445f2df8c80cea6225a259da`  
		Last Modified: Sat, 06 Apr 2024 15:46:55 GMT  
		Size: 38.0 KB (37987 bytes)  
		MIME: application/vnd.in-toto+json

## `httpd:2.4-bookworm`

```console
$ docker pull httpd@sha256:36c8c79f900108f0f09fd4148ad35ade57cba0dc19d13f3d15be24ce94e6a639
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

### `httpd:2.4-bookworm` - linux; amd64

```console
$ docker pull httpd@sha256:518e9447a236de47cc2fb4f2dbf06466b6cd5cf50f9951742f9a20af76e8118d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59185382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c2fc9e3d849b21a35b4c96f5ad8ec4dc9b73ca44c56537039e8c6f3054db0a`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851c52adaa9bf680b2eaa45164baa37665418fb02666fb36c268002edd853994`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d9f60535a61833df2e57cc08221031d3ae50f3955a6d6b0153214619d357fb`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 4.0 MB (4006988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943a2b3cf551375517593790b58407ffc7028b4b34bca6c0756b76708ea4b3ce`  
		Last Modified: Wed, 24 Apr 2024 04:57:24 GMT  
		Size: 26.0 MB (26027444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea83e81966d64f34a57ffcc118b75ad19bc9321f9809cf9b0df25548a2fa695e`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-bookworm` - unknown; unknown

```console
$ docker pull httpd@sha256:e31d2d75b317933ed59c3503fcfd00357545f4e60e60d87368674365eed990bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc7b98024523f6963a92b3a8edb71945171fff164f1da1e3bc9296d404a1da2`

```dockerfile
```

-	Layers:
	-	`sha256:1a0e348c51fd80864d852c8a1b3dbe89c1cbf088a8d4fe204b4f9a2106b65425`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 2.5 MB (2475971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea347276a3b2b4390cbb875d979ac18e828399022ce83785af6a6e19535cf238`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 37.8 KB (37766 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-bookworm` - linux; arm variant v5

```console
$ docker pull httpd@sha256:6ac6acfaf36b492c8ee0271b5c1745e5d5173186838066fb55416fe1bad7f84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55660337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594aaef0a91e898dfb26ab368782f59da9b9f69c9ad0d9a155208b535102d8e8`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfdcc496dd931564ad13b4c74e84a37bd3e8fe4d3e8eef76531c007b4918eb3`  
		Last Modified: Wed, 24 Apr 2024 17:19:02 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7797397d89aa986596ae17907e8812fb696c601b77e453f8cfff70c5282bb68`  
		Last Modified: Wed, 24 Apr 2024 17:19:03 GMT  
		Size: 3.5 MB (3511113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabda791a3820471d4af8b4b5339e9e5ade214d951432d16dcf09a30dfc07788`  
		Last Modified: Wed, 24 Apr 2024 17:19:04 GMT  
		Size: 25.2 MB (25238724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7b73f2fae9dae743b3751fc794fe838ccfee7359899fe2ef291db96f774025`  
		Last Modified: Wed, 24 Apr 2024 17:19:03 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-bookworm` - unknown; unknown

```console
$ docker pull httpd@sha256:0559103a0db87f5edf6e70a2fce9af410a68e8207c18d62b1a99fa7d6081320a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2517016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5eb9364b67ec513d9aa9dab74264a7e94017611ae8f167c5e716aad4b7680e`

```dockerfile
```

-	Layers:
	-	`sha256:0fd0fb4e581c468abde2999045c163e01f5f465436e7aa62ce734436862f9eac`  
		Last Modified: Wed, 24 Apr 2024 17:19:03 GMT  
		Size: 2.5 MB (2479288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38cc0fcc6c1dede08c15c91c4bc214763cd7fb9e515bc4f8b07ba05cdc9cd387`  
		Last Modified: Wed, 24 Apr 2024 17:19:03 GMT  
		Size: 37.7 KB (37728 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-bookworm` - linux; arm variant v7

```console
$ docker pull httpd@sha256:e49897ae28bb259a5a1b205a464098038e49ea2bb4985187e84baac47edda986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52738179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9fefb7a703a9d947d489c78f23271b57b138126899b22193b569f3d5ceb0d2`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063593c7931b25f55a01b9bb0f7156d7398c702900d7c6c5a10ac3cb9b111eeb`  
		Last Modified: Wed, 24 Apr 2024 16:30:49 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60dd6c2df475ede40fbebdd310c9770f5c85d86278fe66bcfb34015f9975b80`  
		Last Modified: Wed, 24 Apr 2024 16:30:50 GMT  
		Size: 3.3 MB (3286910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5afe70e80d3c8da2e79abd6e84a95f7bb9516fe79ffc1e06abcb55d3af394429`  
		Last Modified: Wed, 24 Apr 2024 16:30:51 GMT  
		Size: 24.7 MB (24710357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e43b819248841764c8eaee46258c16341b869c3cd10e29c5fe19a7ad57d3ea0`  
		Last Modified: Wed, 24 Apr 2024 16:30:50 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-bookworm` - unknown; unknown

```console
$ docker pull httpd@sha256:daa1d3562f002200d97c8042f5fb9e5cce9d3a91b979ab3bae79daa3f5a6f0a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2516068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beda48825ccb307edac52c5e75efd8fc86548bb74670c0558d03c6057104e328`

```dockerfile
```

-	Layers:
	-	`sha256:6656cffeaa9a2613f22ecf4356afe7a1fd612ffb7430d4e7e2ab9004ece5d051`  
		Last Modified: Wed, 24 Apr 2024 16:30:50 GMT  
		Size: 2.5 MB (2478340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1efca153bd1cf7ed5e26102ed35722aa4aec61d831e71818bba3175e03866560`  
		Last Modified: Wed, 24 Apr 2024 16:30:50 GMT  
		Size: 37.7 KB (37728 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-bookworm` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:b2670b51810a49855b0b59ed87dd064b3ec3ecf95e77d9dd6f6d13bab7467dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58997314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73acb239a8eb7a9ef5b6848a5b01bb26cc03d2262056705876bf7ac6ad781f02`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855b568ab02c3fee1362d51176f966517b1e03ca0c8efde55eddace90835f300`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c521cc2c4e8a439951003122cdab841fe1b1350db864e2cf9dea69298513f711`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 3.8 MB (3824128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c8bced82bd1d3557a49d39ea03bb8090bf3abc8154ab65388d9f9728f3ce02`  
		Last Modified: Thu, 25 Apr 2024 07:23:09 GMT  
		Size: 26.0 MB (25992782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae159c85a0b3662b8e9d58344f7da1b84836a7338c8ddf6b88360cea400929f`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-bookworm` - unknown; unknown

```console
$ docker pull httpd@sha256:307bc20593c828b3894250dd4e16b149c046b98c033453278fca94efd8bd0454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70026eb22d8bfc08dc60be7e7dcdce118be2390abe04aa90c7f27e6245767782`

```dockerfile
```

-	Layers:
	-	`sha256:77720a2aab607f8a1c40306899700597640ec9696bb65c714e6131dd481171b1`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 2.5 MB (2476229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd136e58015bf40bdc568f33b0d261e3140c11eee1769fbfb67f4ad2b93284f8`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 37.6 KB (37618 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-bookworm` - linux; 386

```console
$ docker pull httpd@sha256:34359f60b5aa39dfe4a6da81d319693f6ca6155e12e91b50e5d6da3ae7db89b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60223958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457768b202e686803b86961428bc138b1e4c6f0a08bec510257bba9b2d7e4486`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2941e842a389d5a4c34aa8e7f83e761d6a0deb0ed5c5bc01838c71d23659ac77`  
		Last Modified: Wed, 24 Apr 2024 04:57:41 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f800dd9ec1f906ac5c081169392c9dd10d32921d3e52e601c8c7ca7bcda3c600`  
		Last Modified: Wed, 24 Apr 2024 04:57:42 GMT  
		Size: 4.1 MB (4063511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494266189a0019f5cc3fec9ab5a55a1ea0fc3c8cc6a3ab1c1faeedbdc0fbaa5e`  
		Last Modified: Wed, 24 Apr 2024 04:57:42 GMT  
		Size: 26.0 MB (25996792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed1b4c9db903ab4981ddd506901a8ead9ae515c81f307dc7e52ed0256e73eec`  
		Last Modified: Wed, 24 Apr 2024 04:57:41 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-bookworm` - unknown; unknown

```console
$ docker pull httpd@sha256:928d95daa4cdcfd2c1395f60c62ed85d871764fdbfd6b1dbcf750c4f906d1eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2510705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8144c9b91841f94cfaea34892b458353406e2daa257e7e97e80ce41341381322`

```dockerfile
```

-	Layers:
	-	`sha256:637adc441596f6bc7ae557cdd4ef0de555b3e1b8aaa69a88adf26ea73e04a753`  
		Last Modified: Wed, 24 Apr 2024 04:57:42 GMT  
		Size: 2.5 MB (2472991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c57120021da5fb478f2b39b4540d36f1ba9bfa1efbe1c0616a07fe2a81d1e746`  
		Last Modified: Wed, 24 Apr 2024 04:57:41 GMT  
		Size: 37.7 KB (37714 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-bookworm` - linux; mips64le

```console
$ docker pull httpd@sha256:4512a76c673f11979d9f2ea96a56c59db662c5e8258c7128258245d18bb9292d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58678876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f7e1281eca6101e477c1cb3af32334cd551c69acc34839c3a8f8e3b3be6e80`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28233217e5e2c53a42bce8370d4462ed742672e46ec0e3acc021494964a6c4e`  
		Last Modified: Wed, 24 Apr 2024 23:51:19 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98af3a5736d8674d724399887f435760548973f8720121002efb9766f6892bb1`  
		Last Modified: Wed, 24 Apr 2024 23:51:20 GMT  
		Size: 3.4 MB (3373290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d3af7336bf3047ff58c8fc60fcce4943c107ecf04bb449d43849ce851d53aa`  
		Last Modified: Wed, 24 Apr 2024 23:51:22 GMT  
		Size: 26.2 MB (26160940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ed9c80633a9c8a938fb64f3eddb5677882265446491ddb3fce480647719cf5`  
		Last Modified: Wed, 24 Apr 2024 23:51:20 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-bookworm` - unknown; unknown

```console
$ docker pull httpd@sha256:b80ddb9178f5c7b1fb405cdad5a1ca2b55ae93147230041eb0b0e958dd6bd2b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f0b12a55ecb5a0fb2dc015ef1bebad8c2d781a197cd3a665b0b585ef134715`

```dockerfile
```

-	Layers:
	-	`sha256:e03a7d994013fb85dd187518a518143a7a11bc11a02be3fe21ac1bcc6c2bad8c`  
		Last Modified: Wed, 24 Apr 2024 23:51:20 GMT  
		Size: 37.5 KB (37480 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-bookworm` - linux; ppc64le

```console
$ docker pull httpd@sha256:f367b8c823d8e9650e4d0f3576cb4cb56931fb2a9abc5cf933fbc3e5e2d03eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64781656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5b1ab6010140721a568d9027ba17353616269ed57d0407e63a20a9db866d83`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8779f7411971984d8a264462c07b9383e455edbfa3945c3a7c3c0f0da6281405`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df41593893685df2f819e89678437a7190515d7cc02ecf4d3826f45e94594a6`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 4.3 MB (4329567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5fc79508ca1591a5607565a2c2fd383aaea639b5a8777f026f5767404f73eb`  
		Last Modified: Thu, 25 Apr 2024 03:19:08 GMT  
		Size: 27.3 MB (27310418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3bf3ad211e2e210d10318ae48cfccfdefd6adae953aa2a10ca77880dd921ac`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-bookworm` - unknown; unknown

```console
$ docker pull httpd@sha256:f5fdb59224d04f59d5f80ba98a242d519237e7fe401672f767a98c516fbb17b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2518193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3109624aa7219e37cb7b867bf5926f24b5e9b4eb3d6e31536b83f1751b0c42cf`

```dockerfile
```

-	Layers:
	-	`sha256:5553f9b984d60f0b17ff79178b8bd6943ed3c6a28b511fee1a71f4df9b281e63`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 2.5 MB (2480527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49e0858fd1c6faa9c04410e63c7d7bf0b572ae75294b281ff9ce3ba69ca201b3`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 37.7 KB (37666 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4-bookworm` - linux; s390x

```console
$ docker pull httpd@sha256:ae3341db428440ab15b07058d2bab822247b8aa06035c19edea03f2a675e3b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56864928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed5070ae0d9687d8b499eae1be4caf30616eea45630f52af89bff9348d1cc474`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076f4d06a50ca8b3bcf6951ac8efa98b499598a608155af2bc4e4c0283e315e6`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8054bd786718ad21214203f377432a693d561157449486d1ea16ee3530d793e1`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 3.7 MB (3654647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c39e346caebedca77c0054fa938878774f458b3b88e05f7099ff4b70345256a`  
		Last Modified: Thu, 25 Apr 2024 02:28:32 GMT  
		Size: 25.7 MB (25697456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb3dcd087010aa65e19ef6e7ae889206220840a38cc7d973cd3b0e635895072`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4-bookworm` - unknown; unknown

```console
$ docker pull httpd@sha256:779ecac6b7d7547b09bf644ce963543f48bac336bfe174dbd0583d7d06e3b0c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d2597d4c0c4788030bfe3a20a2ddf9842323ed2e486b682e1a863ae138ad89`

```dockerfile
```

-	Layers:
	-	`sha256:d42e15caceec6e5f15ccf873f46289eb1dc452e23ab53a076d905630a09e58e5`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 2.5 MB (2475763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28db97fd901916835b62fdb1cece860a44f5b2888ae52a2ea94026e65e136df5`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 37.6 KB (37600 bytes)  
		MIME: application/vnd.in-toto+json

## `httpd:2.4.59`

```console
$ docker pull httpd@sha256:36c8c79f900108f0f09fd4148ad35ade57cba0dc19d13f3d15be24ce94e6a639
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

### `httpd:2.4.59` - linux; amd64

```console
$ docker pull httpd@sha256:518e9447a236de47cc2fb4f2dbf06466b6cd5cf50f9951742f9a20af76e8118d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59185382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c2fc9e3d849b21a35b4c96f5ad8ec4dc9b73ca44c56537039e8c6f3054db0a`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851c52adaa9bf680b2eaa45164baa37665418fb02666fb36c268002edd853994`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d9f60535a61833df2e57cc08221031d3ae50f3955a6d6b0153214619d357fb`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 4.0 MB (4006988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943a2b3cf551375517593790b58407ffc7028b4b34bca6c0756b76708ea4b3ce`  
		Last Modified: Wed, 24 Apr 2024 04:57:24 GMT  
		Size: 26.0 MB (26027444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea83e81966d64f34a57ffcc118b75ad19bc9321f9809cf9b0df25548a2fa695e`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.59` - unknown; unknown

```console
$ docker pull httpd@sha256:e31d2d75b317933ed59c3503fcfd00357545f4e60e60d87368674365eed990bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc7b98024523f6963a92b3a8edb71945171fff164f1da1e3bc9296d404a1da2`

```dockerfile
```

-	Layers:
	-	`sha256:1a0e348c51fd80864d852c8a1b3dbe89c1cbf088a8d4fe204b4f9a2106b65425`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 2.5 MB (2475971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea347276a3b2b4390cbb875d979ac18e828399022ce83785af6a6e19535cf238`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 37.8 KB (37766 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.59` - linux; arm variant v5

```console
$ docker pull httpd@sha256:6ac6acfaf36b492c8ee0271b5c1745e5d5173186838066fb55416fe1bad7f84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55660337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594aaef0a91e898dfb26ab368782f59da9b9f69c9ad0d9a155208b535102d8e8`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfdcc496dd931564ad13b4c74e84a37bd3e8fe4d3e8eef76531c007b4918eb3`  
		Last Modified: Wed, 24 Apr 2024 17:19:02 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7797397d89aa986596ae17907e8812fb696c601b77e453f8cfff70c5282bb68`  
		Last Modified: Wed, 24 Apr 2024 17:19:03 GMT  
		Size: 3.5 MB (3511113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabda791a3820471d4af8b4b5339e9e5ade214d951432d16dcf09a30dfc07788`  
		Last Modified: Wed, 24 Apr 2024 17:19:04 GMT  
		Size: 25.2 MB (25238724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7b73f2fae9dae743b3751fc794fe838ccfee7359899fe2ef291db96f774025`  
		Last Modified: Wed, 24 Apr 2024 17:19:03 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.59` - unknown; unknown

```console
$ docker pull httpd@sha256:0559103a0db87f5edf6e70a2fce9af410a68e8207c18d62b1a99fa7d6081320a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2517016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5eb9364b67ec513d9aa9dab74264a7e94017611ae8f167c5e716aad4b7680e`

```dockerfile
```

-	Layers:
	-	`sha256:0fd0fb4e581c468abde2999045c163e01f5f465436e7aa62ce734436862f9eac`  
		Last Modified: Wed, 24 Apr 2024 17:19:03 GMT  
		Size: 2.5 MB (2479288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38cc0fcc6c1dede08c15c91c4bc214763cd7fb9e515bc4f8b07ba05cdc9cd387`  
		Last Modified: Wed, 24 Apr 2024 17:19:03 GMT  
		Size: 37.7 KB (37728 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.59` - linux; arm variant v7

```console
$ docker pull httpd@sha256:e49897ae28bb259a5a1b205a464098038e49ea2bb4985187e84baac47edda986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52738179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9fefb7a703a9d947d489c78f23271b57b138126899b22193b569f3d5ceb0d2`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063593c7931b25f55a01b9bb0f7156d7398c702900d7c6c5a10ac3cb9b111eeb`  
		Last Modified: Wed, 24 Apr 2024 16:30:49 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60dd6c2df475ede40fbebdd310c9770f5c85d86278fe66bcfb34015f9975b80`  
		Last Modified: Wed, 24 Apr 2024 16:30:50 GMT  
		Size: 3.3 MB (3286910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5afe70e80d3c8da2e79abd6e84a95f7bb9516fe79ffc1e06abcb55d3af394429`  
		Last Modified: Wed, 24 Apr 2024 16:30:51 GMT  
		Size: 24.7 MB (24710357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e43b819248841764c8eaee46258c16341b869c3cd10e29c5fe19a7ad57d3ea0`  
		Last Modified: Wed, 24 Apr 2024 16:30:50 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.59` - unknown; unknown

```console
$ docker pull httpd@sha256:daa1d3562f002200d97c8042f5fb9e5cce9d3a91b979ab3bae79daa3f5a6f0a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2516068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beda48825ccb307edac52c5e75efd8fc86548bb74670c0558d03c6057104e328`

```dockerfile
```

-	Layers:
	-	`sha256:6656cffeaa9a2613f22ecf4356afe7a1fd612ffb7430d4e7e2ab9004ece5d051`  
		Last Modified: Wed, 24 Apr 2024 16:30:50 GMT  
		Size: 2.5 MB (2478340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1efca153bd1cf7ed5e26102ed35722aa4aec61d831e71818bba3175e03866560`  
		Last Modified: Wed, 24 Apr 2024 16:30:50 GMT  
		Size: 37.7 KB (37728 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.59` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:b2670b51810a49855b0b59ed87dd064b3ec3ecf95e77d9dd6f6d13bab7467dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58997314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73acb239a8eb7a9ef5b6848a5b01bb26cc03d2262056705876bf7ac6ad781f02`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855b568ab02c3fee1362d51176f966517b1e03ca0c8efde55eddace90835f300`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c521cc2c4e8a439951003122cdab841fe1b1350db864e2cf9dea69298513f711`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 3.8 MB (3824128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c8bced82bd1d3557a49d39ea03bb8090bf3abc8154ab65388d9f9728f3ce02`  
		Last Modified: Thu, 25 Apr 2024 07:23:09 GMT  
		Size: 26.0 MB (25992782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae159c85a0b3662b8e9d58344f7da1b84836a7338c8ddf6b88360cea400929f`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.59` - unknown; unknown

```console
$ docker pull httpd@sha256:307bc20593c828b3894250dd4e16b149c046b98c033453278fca94efd8bd0454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70026eb22d8bfc08dc60be7e7dcdce118be2390abe04aa90c7f27e6245767782`

```dockerfile
```

-	Layers:
	-	`sha256:77720a2aab607f8a1c40306899700597640ec9696bb65c714e6131dd481171b1`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 2.5 MB (2476229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd136e58015bf40bdc568f33b0d261e3140c11eee1769fbfb67f4ad2b93284f8`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 37.6 KB (37618 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.59` - linux; 386

```console
$ docker pull httpd@sha256:34359f60b5aa39dfe4a6da81d319693f6ca6155e12e91b50e5d6da3ae7db89b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60223958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457768b202e686803b86961428bc138b1e4c6f0a08bec510257bba9b2d7e4486`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2941e842a389d5a4c34aa8e7f83e761d6a0deb0ed5c5bc01838c71d23659ac77`  
		Last Modified: Wed, 24 Apr 2024 04:57:41 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f800dd9ec1f906ac5c081169392c9dd10d32921d3e52e601c8c7ca7bcda3c600`  
		Last Modified: Wed, 24 Apr 2024 04:57:42 GMT  
		Size: 4.1 MB (4063511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494266189a0019f5cc3fec9ab5a55a1ea0fc3c8cc6a3ab1c1faeedbdc0fbaa5e`  
		Last Modified: Wed, 24 Apr 2024 04:57:42 GMT  
		Size: 26.0 MB (25996792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed1b4c9db903ab4981ddd506901a8ead9ae515c81f307dc7e52ed0256e73eec`  
		Last Modified: Wed, 24 Apr 2024 04:57:41 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.59` - unknown; unknown

```console
$ docker pull httpd@sha256:928d95daa4cdcfd2c1395f60c62ed85d871764fdbfd6b1dbcf750c4f906d1eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2510705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8144c9b91841f94cfaea34892b458353406e2daa257e7e97e80ce41341381322`

```dockerfile
```

-	Layers:
	-	`sha256:637adc441596f6bc7ae557cdd4ef0de555b3e1b8aaa69a88adf26ea73e04a753`  
		Last Modified: Wed, 24 Apr 2024 04:57:42 GMT  
		Size: 2.5 MB (2472991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c57120021da5fb478f2b39b4540d36f1ba9bfa1efbe1c0616a07fe2a81d1e746`  
		Last Modified: Wed, 24 Apr 2024 04:57:41 GMT  
		Size: 37.7 KB (37714 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.59` - linux; mips64le

```console
$ docker pull httpd@sha256:4512a76c673f11979d9f2ea96a56c59db662c5e8258c7128258245d18bb9292d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58678876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f7e1281eca6101e477c1cb3af32334cd551c69acc34839c3a8f8e3b3be6e80`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28233217e5e2c53a42bce8370d4462ed742672e46ec0e3acc021494964a6c4e`  
		Last Modified: Wed, 24 Apr 2024 23:51:19 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98af3a5736d8674d724399887f435760548973f8720121002efb9766f6892bb1`  
		Last Modified: Wed, 24 Apr 2024 23:51:20 GMT  
		Size: 3.4 MB (3373290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d3af7336bf3047ff58c8fc60fcce4943c107ecf04bb449d43849ce851d53aa`  
		Last Modified: Wed, 24 Apr 2024 23:51:22 GMT  
		Size: 26.2 MB (26160940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ed9c80633a9c8a938fb64f3eddb5677882265446491ddb3fce480647719cf5`  
		Last Modified: Wed, 24 Apr 2024 23:51:20 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.59` - unknown; unknown

```console
$ docker pull httpd@sha256:b80ddb9178f5c7b1fb405cdad5a1ca2b55ae93147230041eb0b0e958dd6bd2b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f0b12a55ecb5a0fb2dc015ef1bebad8c2d781a197cd3a665b0b585ef134715`

```dockerfile
```

-	Layers:
	-	`sha256:e03a7d994013fb85dd187518a518143a7a11bc11a02be3fe21ac1bcc6c2bad8c`  
		Last Modified: Wed, 24 Apr 2024 23:51:20 GMT  
		Size: 37.5 KB (37480 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.59` - linux; ppc64le

```console
$ docker pull httpd@sha256:f367b8c823d8e9650e4d0f3576cb4cb56931fb2a9abc5cf933fbc3e5e2d03eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64781656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5b1ab6010140721a568d9027ba17353616269ed57d0407e63a20a9db866d83`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8779f7411971984d8a264462c07b9383e455edbfa3945c3a7c3c0f0da6281405`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df41593893685df2f819e89678437a7190515d7cc02ecf4d3826f45e94594a6`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 4.3 MB (4329567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5fc79508ca1591a5607565a2c2fd383aaea639b5a8777f026f5767404f73eb`  
		Last Modified: Thu, 25 Apr 2024 03:19:08 GMT  
		Size: 27.3 MB (27310418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3bf3ad211e2e210d10318ae48cfccfdefd6adae953aa2a10ca77880dd921ac`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.59` - unknown; unknown

```console
$ docker pull httpd@sha256:f5fdb59224d04f59d5f80ba98a242d519237e7fe401672f767a98c516fbb17b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2518193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3109624aa7219e37cb7b867bf5926f24b5e9b4eb3d6e31536b83f1751b0c42cf`

```dockerfile
```

-	Layers:
	-	`sha256:5553f9b984d60f0b17ff79178b8bd6943ed3c6a28b511fee1a71f4df9b281e63`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 2.5 MB (2480527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49e0858fd1c6faa9c04410e63c7d7bf0b572ae75294b281ff9ce3ba69ca201b3`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 37.7 KB (37666 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.59` - linux; s390x

```console
$ docker pull httpd@sha256:ae3341db428440ab15b07058d2bab822247b8aa06035c19edea03f2a675e3b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56864928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed5070ae0d9687d8b499eae1be4caf30616eea45630f52af89bff9348d1cc474`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076f4d06a50ca8b3bcf6951ac8efa98b499598a608155af2bc4e4c0283e315e6`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8054bd786718ad21214203f377432a693d561157449486d1ea16ee3530d793e1`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 3.7 MB (3654647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c39e346caebedca77c0054fa938878774f458b3b88e05f7099ff4b70345256a`  
		Last Modified: Thu, 25 Apr 2024 02:28:32 GMT  
		Size: 25.7 MB (25697456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb3dcd087010aa65e19ef6e7ae889206220840a38cc7d973cd3b0e635895072`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.59` - unknown; unknown

```console
$ docker pull httpd@sha256:779ecac6b7d7547b09bf644ce963543f48bac336bfe174dbd0583d7d06e3b0c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d2597d4c0c4788030bfe3a20a2ddf9842323ed2e486b682e1a863ae138ad89`

```dockerfile
```

-	Layers:
	-	`sha256:d42e15caceec6e5f15ccf873f46289eb1dc452e23ab53a076d905630a09e58e5`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 2.5 MB (2475763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28db97fd901916835b62fdb1cece860a44f5b2888ae52a2ea94026e65e136df5`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 37.6 KB (37600 bytes)  
		MIME: application/vnd.in-toto+json

## `httpd:2.4.59-alpine`

```console
$ docker pull httpd@sha256:68f6714169b70ca33126c46f60cc802eb602c6435f4ebf08349d871d500d3e70
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

### `httpd:2.4.59-alpine` - linux; amd64

```console
$ docker pull httpd@sha256:b48b48dcfff1407638908b8a1782480df0ad8bac7f5fc579496357864f97e60c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18905522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b6bf3450e2114fc55779cd878fa1a176a851a4de5a38f79ffb779639c455a2`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e13f4f5374dc8e6fd59fc8dc82c77d2dfc85ffd1136f5edbc4a9054ba955927`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333c1d8ec87c0966bd88d1293586bce65663a901c08af2a85ffe369897d7fd9e`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58593e44a54df297fb6195ac992fbda56ab083ee57a934ba5de6c49c8c6cff4a`  
		Last Modified: Fri, 05 Apr 2024 17:53:06 GMT  
		Size: 10.4 MB (10384953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608381599c688e98facb252c7e8313379b6d1f574bba1b49262a39145764d4d9`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 5.1 MB (5110138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e5ce613b310458e6aad12ed911fae7e33b9d59232a0a816ae8829774a7c351`  
		Last Modified: Fri, 05 Apr 2024 17:53:06 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.59-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:933e4cc35d564b7e6b37b9da44ff4c3a1c961ee5a115addfc4348458b9584a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1105171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32930164a83ab310294ec129967dfa6b0e208133bcd30d31b8bdaae148384c8c`

```dockerfile
```

-	Layers:
	-	`sha256:4ce2b7d308346544402cfbaecf8b70c4dfbb6d6385f79028bfeb7b9df16b2b23`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 1.1 MB (1067018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f7979b59e4c92069c8731802e0b918cc1668ed3cbc3448ac9f5863488762eec`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 38.2 KB (38153 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.59-alpine` - linux; arm variant v6

```console
$ docker pull httpd@sha256:3536bda1cb1b0f3581896c7acafa8426a67ac185711f3af26cffb991a76d08fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17774769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1732292898ef3f1fb223e062d5aa76bcf8087c9c7978a357ea964a0f9e6e2a4d`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8c07a4a93f0faf2d460b21b916e9f8d52550da29882704b17b06201a89e118`  
		Last Modified: Fri, 05 Apr 2024 18:11:18 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001db4688f33e38d27d733b6d51f6a9edf395f4fd76749cf91ebb32f1fd25483`  
		Last Modified: Fri, 05 Apr 2024 18:11:18 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f8fe9e9d09c4f2074ab547012fee140749069dd339f3cc87dc71e347884d92`  
		Last Modified: Fri, 05 Apr 2024 18:11:19 GMT  
		Size: 9.6 MB (9577820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c092ec8ebe549b81d3f7c2f8f6830bfc42142f090d8fe5cd5b52f296d516310`  
		Last Modified: Fri, 05 Apr 2024 18:11:19 GMT  
		Size: 5.0 MB (5029848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346b9e25e64782fa95573e9eb07893339f472741823a4062737052da7391dfd5`  
		Last Modified: Fri, 05 Apr 2024 18:11:20 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.59-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:2790d9e49f2d98ffc37ada24de30725d9196ac28a61fd2ef576263287c58aec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d270ac30275fb727064cc5d2eeeb08a7ffc7305c12f93e19d03d209ebc2d6f58`

```dockerfile
```

-	Layers:
	-	`sha256:57b3e792cca6cdd007c318692afa6ccc61834b2e257e11c1832e8403dd37032e`  
		Last Modified: Fri, 05 Apr 2024 18:11:18 GMT  
		Size: 37.9 KB (37910 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.59-alpine` - linux; arm variant v7

```console
$ docker pull httpd@sha256:09dd424663b1d2540476d34b124fb25360411dff64f69cc71fa3cf02381fb9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16993127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad0e3a5244891745dcd5889901c7a0101e398b81de79ff65cb7270e482bbbbb`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74aa637d7bf59fca068dcb5b7dd86513aa9ad3282aad69b3e9039cc2f6f18bcc`  
		Last Modified: Sat, 16 Mar 2024 16:04:22 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fc40e56afb70a5d1bf79dc4bf9118f2b993e3687626ab036513d862a1a286e`  
		Last Modified: Sat, 16 Mar 2024 16:04:22 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7015ed48724aa34bf3e29ddfa9b1058e3c374c383a17cc3ba6b943f7de0cf1`  
		Last Modified: Sat, 16 Mar 2024 16:04:23 GMT  
		Size: 9.3 MB (9334751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5553e605c52a438be1d61a267e9cbc342a533ce3966d9c82b03dfe7e0f1777c8`  
		Last Modified: Fri, 05 Apr 2024 17:57:38 GMT  
		Size: 4.7 MB (4737771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a356346eae4cb6bddf85f93948a3f0df8845d93176937fef76aec99cb50faef2`  
		Last Modified: Fri, 05 Apr 2024 17:57:37 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.59-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:28d8f38fd78210cba28d51dc8d470fc5068b2d90a3fd9cb0a9f14a622ff89577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1102820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3348381822a72f52b9575c5d5d34c4da16730f59ef5128ebdedb089cd1d48819`

```dockerfile
```

-	Layers:
	-	`sha256:9e5deb95007dd7e44d0a6f9d0c0ccf2ee83e76cb545b6c4691007c75be1c6498`  
		Last Modified: Fri, 05 Apr 2024 17:57:38 GMT  
		Size: 1.1 MB (1064695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a16e23262169a2b30cd14de32d5acde981fcd5bf7179967f584df46c44b1b10`  
		Last Modified: Fri, 05 Apr 2024 17:57:37 GMT  
		Size: 38.1 KB (38125 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.59-alpine` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:91756bbcc9b8283d49fdf66189881d39576f12c012dad8796b97948636e0b40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (18989141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d3d050f8abbaa153d704cae494aeeca773a0f24ba35600711e356083a79a66`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68b5c4e3f3b827d8933253d337cf55bf3ace2d75070b8ea7655a893c325569f`  
		Last Modified: Sat, 16 Mar 2024 15:13:13 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba68aab08183c67e796b91cc96b7c1629e35f98048a721cd67997edb83a202e2`  
		Last Modified: Sat, 16 Mar 2024 15:13:13 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1e2b5044558ea2188f9ba4d34df06cc7109e01f5caefe6c2bc5ecd11b6ced0`  
		Last Modified: Sat, 16 Mar 2024 15:13:14 GMT  
		Size: 10.4 MB (10388804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6beaeaed29f48ef5f4141a8b7e76a8e550f88775f81d464c5944634479d8ed7a`  
		Last Modified: Fri, 05 Apr 2024 17:55:14 GMT  
		Size: 5.3 MB (5250912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8742eb1c1f87645540c4e75db0e19ba29d77c28e18927d3310670a72b85ec82`  
		Last Modified: Fri, 05 Apr 2024 17:55:13 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.59-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:b266b0cecec670e48d25423f3f218b28b7745ec04fa2be113bca803f25a89f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1100073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a241afe2d5ab26a07a1794465d326a6827b70fbef1de59a250d03605dac1ded`

```dockerfile
```

-	Layers:
	-	`sha256:43abc3efae9947304de80f9a75aa23117ac15a382c784b355816810199ecbf7e`  
		Last Modified: Fri, 05 Apr 2024 17:55:13 GMT  
		Size: 1.1 MB (1062068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dcf770b26d2bae0707f3d339ee48b6778855e725144a0d1384402416186c295`  
		Last Modified: Fri, 05 Apr 2024 17:55:13 GMT  
		Size: 38.0 KB (38005 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.59-alpine` - linux; 386

```console
$ docker pull httpd@sha256:40a391f6e52f9fa6d56741b455cbffde4d9104948f1078da5bd6c248b3318f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18161726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa32e51497f1ebc9739fe8b3d915e5fecd520dd4959266c76adf910b71fd4ea`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740e52eababa89f531e99d9609ea4df66e75527cb8a97aa3feba95f64f8d19c1`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9d066a768f0f31e823ea143de9180c7e2b5b51ee3f0267272b2122353c5530`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320efa4f4b1525ce8d8dc283fe9bce7bf23e031d3349b59957067c1ad3f22eeb`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 9.9 MB (9862040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b89437c703e9c702702c5eb0432f2efcb16ae506d611336abbf81b083b7fbd`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 5.1 MB (5053894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1099f38eb4d16ee148b32677e9f70da2535bef69261361e1247b719b03f5a2c4`  
		Last Modified: Fri, 05 Apr 2024 17:53:13 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.59-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:52a1c8f1cdb4a7057132a6bc0f6f82528ee10ccffedf7bb17d1108bf94d8ac6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1105068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946eef1c61b246af219f7ef605bfd198e004722dc6d7fafdaa0a35c5504965e7`

```dockerfile
```

-	Layers:
	-	`sha256:56b910d095946bc43dbafed2e0f13360d62f86b726feba74f5670cb07cd93f3d`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 1.1 MB (1066973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37abeadc160510b3cfd3b1a3d82f05e600fcbb1c92c9b5e2c0a20b0c8e865bc7`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 38.1 KB (38095 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.59-alpine` - linux; ppc64le

```console
$ docker pull httpd@sha256:447d4eca233b95a1aebdb73d93c024d8226d6a608568aa2c9505f96a3b8f19bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19410079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bed7414a71a37df5ac42b1637107b9e12f08cc3e63e5d9ecd84556d26489d9b`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca1e90415bffcf574224c85fef296c0f849237fe22a0b5065a26673f7cbba51`  
		Last Modified: Sat, 16 Mar 2024 10:26:53 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b746962fe11d53bb9b19dfe7990c4658ac0472cccbd8daa5794e5f3a22cfda51`  
		Last Modified: Sat, 16 Mar 2024 10:26:53 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68b51060f0a52e914490ae4eeb10af1258ec331a68f78f4944118a1ca9911bd`  
		Last Modified: Sat, 16 Mar 2024 10:26:54 GMT  
		Size: 10.6 MB (10627211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f73e01f2b7ec6f92d901b09901b77c8dec59f0535633de6f26cc281f9452954`  
		Last Modified: Fri, 05 Apr 2024 17:59:16 GMT  
		Size: 5.4 MB (5422810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13941787572cd155aec58f453b55fcb5e882b928cf4aa65c8ede53e07d15a45`  
		Last Modified: Fri, 05 Apr 2024 17:59:16 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.59-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:6591d53cc91652e76f1529af4696e990fe459184e928ac7371b55488a2f3b7c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1098208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d59400ec49b3e236a314b42b69e345faf3cdcfbf0bd553b5d16dfc66d548bdd`

```dockerfile
```

-	Layers:
	-	`sha256:630456dcd802b6d23b26b5dc5b782789bc8969758ecdeca80d33ca2ef97be7bb`  
		Last Modified: Fri, 05 Apr 2024 17:59:16 GMT  
		Size: 1.1 MB (1060153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49cbad644a03a7cf5127a55a38cc827f068240cd3ce64261f61e48708941076d`  
		Last Modified: Fri, 05 Apr 2024 17:59:16 GMT  
		Size: 38.1 KB (38055 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.59-alpine` - linux; s390x

```console
$ docker pull httpd@sha256:8ddf2e0f8ccad02de20eaba4fa2f2e046b0032e4e17e481667d6226b3ec82061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19505364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b21662b1d3ba291b541e6898e9870c8f17fc32fc1542e8cd26321d995ed654`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d37ece6c30e22e249589d6aeda58cf29c409948f056a8037f657691f333031`  
		Last Modified: Sun, 17 Mar 2024 22:03:24 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de6b96fd2b7588019fbfc72d5afede300a4d0ef5ea65a7a99fb9715b40b506a`  
		Last Modified: Sun, 17 Mar 2024 22:03:24 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e00979af0d93fc259d0c067c3acf72e2d19ee3e48b840e26b9838a1882a12b`  
		Last Modified: Sun, 17 Mar 2024 22:03:25 GMT  
		Size: 11.0 MB (10985997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fdd3af6a86a6153ff1589309d30e18935c2aacf45522556151835153652514`  
		Last Modified: Sat, 06 Apr 2024 15:46:55 GMT  
		Size: 5.3 MB (5275029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6015f889334ad064a637db08b112726bb85893466a14f46b4034fa7edfa031b0`  
		Last Modified: Sat, 06 Apr 2024 15:46:55 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.59-alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:f6d2ea0678751c8928910a6156f560c2dde868a32d09c26c484866d783af994d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1098082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd8c653038d8341ffbc2492c22b6e5888612cf77dba81bac930256963bfb5d4`

```dockerfile
```

-	Layers:
	-	`sha256:a9f0621638da42ab83a8b188d1b0e79887b581ba27e779272a93e6bd57ffc94a`  
		Last Modified: Sat, 06 Apr 2024 15:46:55 GMT  
		Size: 1.1 MB (1060095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1f2fc0d9673de65aa6403e6d5aff61166189f0445f2df8c80cea6225a259da`  
		Last Modified: Sat, 06 Apr 2024 15:46:55 GMT  
		Size: 38.0 KB (37987 bytes)  
		MIME: application/vnd.in-toto+json

## `httpd:2.4.59-alpine3.19`

```console
$ docker pull httpd@sha256:68f6714169b70ca33126c46f60cc802eb602c6435f4ebf08349d871d500d3e70
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

### `httpd:2.4.59-alpine3.19` - linux; amd64

```console
$ docker pull httpd@sha256:b48b48dcfff1407638908b8a1782480df0ad8bac7f5fc579496357864f97e60c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18905522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b6bf3450e2114fc55779cd878fa1a176a851a4de5a38f79ffb779639c455a2`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e13f4f5374dc8e6fd59fc8dc82c77d2dfc85ffd1136f5edbc4a9054ba955927`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333c1d8ec87c0966bd88d1293586bce65663a901c08af2a85ffe369897d7fd9e`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58593e44a54df297fb6195ac992fbda56ab083ee57a934ba5de6c49c8c6cff4a`  
		Last Modified: Fri, 05 Apr 2024 17:53:06 GMT  
		Size: 10.4 MB (10384953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608381599c688e98facb252c7e8313379b6d1f574bba1b49262a39145764d4d9`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 5.1 MB (5110138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e5ce613b310458e6aad12ed911fae7e33b9d59232a0a816ae8829774a7c351`  
		Last Modified: Fri, 05 Apr 2024 17:53:06 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.59-alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:933e4cc35d564b7e6b37b9da44ff4c3a1c961ee5a115addfc4348458b9584a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1105171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32930164a83ab310294ec129967dfa6b0e208133bcd30d31b8bdaae148384c8c`

```dockerfile
```

-	Layers:
	-	`sha256:4ce2b7d308346544402cfbaecf8b70c4dfbb6d6385f79028bfeb7b9df16b2b23`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 1.1 MB (1067018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f7979b59e4c92069c8731802e0b918cc1668ed3cbc3448ac9f5863488762eec`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 38.2 KB (38153 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.59-alpine3.19` - linux; arm variant v6

```console
$ docker pull httpd@sha256:3536bda1cb1b0f3581896c7acafa8426a67ac185711f3af26cffb991a76d08fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17774769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1732292898ef3f1fb223e062d5aa76bcf8087c9c7978a357ea964a0f9e6e2a4d`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8c07a4a93f0faf2d460b21b916e9f8d52550da29882704b17b06201a89e118`  
		Last Modified: Fri, 05 Apr 2024 18:11:18 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001db4688f33e38d27d733b6d51f6a9edf395f4fd76749cf91ebb32f1fd25483`  
		Last Modified: Fri, 05 Apr 2024 18:11:18 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f8fe9e9d09c4f2074ab547012fee140749069dd339f3cc87dc71e347884d92`  
		Last Modified: Fri, 05 Apr 2024 18:11:19 GMT  
		Size: 9.6 MB (9577820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c092ec8ebe549b81d3f7c2f8f6830bfc42142f090d8fe5cd5b52f296d516310`  
		Last Modified: Fri, 05 Apr 2024 18:11:19 GMT  
		Size: 5.0 MB (5029848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346b9e25e64782fa95573e9eb07893339f472741823a4062737052da7391dfd5`  
		Last Modified: Fri, 05 Apr 2024 18:11:20 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.59-alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:2790d9e49f2d98ffc37ada24de30725d9196ac28a61fd2ef576263287c58aec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d270ac30275fb727064cc5d2eeeb08a7ffc7305c12f93e19d03d209ebc2d6f58`

```dockerfile
```

-	Layers:
	-	`sha256:57b3e792cca6cdd007c318692afa6ccc61834b2e257e11c1832e8403dd37032e`  
		Last Modified: Fri, 05 Apr 2024 18:11:18 GMT  
		Size: 37.9 KB (37910 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.59-alpine3.19` - linux; arm variant v7

```console
$ docker pull httpd@sha256:09dd424663b1d2540476d34b124fb25360411dff64f69cc71fa3cf02381fb9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16993127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad0e3a5244891745dcd5889901c7a0101e398b81de79ff65cb7270e482bbbbb`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74aa637d7bf59fca068dcb5b7dd86513aa9ad3282aad69b3e9039cc2f6f18bcc`  
		Last Modified: Sat, 16 Mar 2024 16:04:22 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fc40e56afb70a5d1bf79dc4bf9118f2b993e3687626ab036513d862a1a286e`  
		Last Modified: Sat, 16 Mar 2024 16:04:22 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7015ed48724aa34bf3e29ddfa9b1058e3c374c383a17cc3ba6b943f7de0cf1`  
		Last Modified: Sat, 16 Mar 2024 16:04:23 GMT  
		Size: 9.3 MB (9334751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5553e605c52a438be1d61a267e9cbc342a533ce3966d9c82b03dfe7e0f1777c8`  
		Last Modified: Fri, 05 Apr 2024 17:57:38 GMT  
		Size: 4.7 MB (4737771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a356346eae4cb6bddf85f93948a3f0df8845d93176937fef76aec99cb50faef2`  
		Last Modified: Fri, 05 Apr 2024 17:57:37 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.59-alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:28d8f38fd78210cba28d51dc8d470fc5068b2d90a3fd9cb0a9f14a622ff89577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1102820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3348381822a72f52b9575c5d5d34c4da16730f59ef5128ebdedb089cd1d48819`

```dockerfile
```

-	Layers:
	-	`sha256:9e5deb95007dd7e44d0a6f9d0c0ccf2ee83e76cb545b6c4691007c75be1c6498`  
		Last Modified: Fri, 05 Apr 2024 17:57:38 GMT  
		Size: 1.1 MB (1064695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a16e23262169a2b30cd14de32d5acde981fcd5bf7179967f584df46c44b1b10`  
		Last Modified: Fri, 05 Apr 2024 17:57:37 GMT  
		Size: 38.1 KB (38125 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.59-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:91756bbcc9b8283d49fdf66189881d39576f12c012dad8796b97948636e0b40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (18989141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d3d050f8abbaa153d704cae494aeeca773a0f24ba35600711e356083a79a66`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68b5c4e3f3b827d8933253d337cf55bf3ace2d75070b8ea7655a893c325569f`  
		Last Modified: Sat, 16 Mar 2024 15:13:13 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba68aab08183c67e796b91cc96b7c1629e35f98048a721cd67997edb83a202e2`  
		Last Modified: Sat, 16 Mar 2024 15:13:13 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1e2b5044558ea2188f9ba4d34df06cc7109e01f5caefe6c2bc5ecd11b6ced0`  
		Last Modified: Sat, 16 Mar 2024 15:13:14 GMT  
		Size: 10.4 MB (10388804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6beaeaed29f48ef5f4141a8b7e76a8e550f88775f81d464c5944634479d8ed7a`  
		Last Modified: Fri, 05 Apr 2024 17:55:14 GMT  
		Size: 5.3 MB (5250912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8742eb1c1f87645540c4e75db0e19ba29d77c28e18927d3310670a72b85ec82`  
		Last Modified: Fri, 05 Apr 2024 17:55:13 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.59-alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:b266b0cecec670e48d25423f3f218b28b7745ec04fa2be113bca803f25a89f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1100073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a241afe2d5ab26a07a1794465d326a6827b70fbef1de59a250d03605dac1ded`

```dockerfile
```

-	Layers:
	-	`sha256:43abc3efae9947304de80f9a75aa23117ac15a382c784b355816810199ecbf7e`  
		Last Modified: Fri, 05 Apr 2024 17:55:13 GMT  
		Size: 1.1 MB (1062068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dcf770b26d2bae0707f3d339ee48b6778855e725144a0d1384402416186c295`  
		Last Modified: Fri, 05 Apr 2024 17:55:13 GMT  
		Size: 38.0 KB (38005 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.59-alpine3.19` - linux; 386

```console
$ docker pull httpd@sha256:40a391f6e52f9fa6d56741b455cbffde4d9104948f1078da5bd6c248b3318f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18161726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa32e51497f1ebc9739fe8b3d915e5fecd520dd4959266c76adf910b71fd4ea`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740e52eababa89f531e99d9609ea4df66e75527cb8a97aa3feba95f64f8d19c1`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9d066a768f0f31e823ea143de9180c7e2b5b51ee3f0267272b2122353c5530`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320efa4f4b1525ce8d8dc283fe9bce7bf23e031d3349b59957067c1ad3f22eeb`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 9.9 MB (9862040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b89437c703e9c702702c5eb0432f2efcb16ae506d611336abbf81b083b7fbd`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 5.1 MB (5053894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1099f38eb4d16ee148b32677e9f70da2535bef69261361e1247b719b03f5a2c4`  
		Last Modified: Fri, 05 Apr 2024 17:53:13 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.59-alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:52a1c8f1cdb4a7057132a6bc0f6f82528ee10ccffedf7bb17d1108bf94d8ac6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1105068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946eef1c61b246af219f7ef605bfd198e004722dc6d7fafdaa0a35c5504965e7`

```dockerfile
```

-	Layers:
	-	`sha256:56b910d095946bc43dbafed2e0f13360d62f86b726feba74f5670cb07cd93f3d`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 1.1 MB (1066973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37abeadc160510b3cfd3b1a3d82f05e600fcbb1c92c9b5e2c0a20b0c8e865bc7`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 38.1 KB (38095 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.59-alpine3.19` - linux; ppc64le

```console
$ docker pull httpd@sha256:447d4eca233b95a1aebdb73d93c024d8226d6a608568aa2c9505f96a3b8f19bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19410079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bed7414a71a37df5ac42b1637107b9e12f08cc3e63e5d9ecd84556d26489d9b`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca1e90415bffcf574224c85fef296c0f849237fe22a0b5065a26673f7cbba51`  
		Last Modified: Sat, 16 Mar 2024 10:26:53 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b746962fe11d53bb9b19dfe7990c4658ac0472cccbd8daa5794e5f3a22cfda51`  
		Last Modified: Sat, 16 Mar 2024 10:26:53 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68b51060f0a52e914490ae4eeb10af1258ec331a68f78f4944118a1ca9911bd`  
		Last Modified: Sat, 16 Mar 2024 10:26:54 GMT  
		Size: 10.6 MB (10627211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f73e01f2b7ec6f92d901b09901b77c8dec59f0535633de6f26cc281f9452954`  
		Last Modified: Fri, 05 Apr 2024 17:59:16 GMT  
		Size: 5.4 MB (5422810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13941787572cd155aec58f453b55fcb5e882b928cf4aa65c8ede53e07d15a45`  
		Last Modified: Fri, 05 Apr 2024 17:59:16 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.59-alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:6591d53cc91652e76f1529af4696e990fe459184e928ac7371b55488a2f3b7c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1098208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d59400ec49b3e236a314b42b69e345faf3cdcfbf0bd553b5d16dfc66d548bdd`

```dockerfile
```

-	Layers:
	-	`sha256:630456dcd802b6d23b26b5dc5b782789bc8969758ecdeca80d33ca2ef97be7bb`  
		Last Modified: Fri, 05 Apr 2024 17:59:16 GMT  
		Size: 1.1 MB (1060153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49cbad644a03a7cf5127a55a38cc827f068240cd3ce64261f61e48708941076d`  
		Last Modified: Fri, 05 Apr 2024 17:59:16 GMT  
		Size: 38.1 KB (38055 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.59-alpine3.19` - linux; s390x

```console
$ docker pull httpd@sha256:8ddf2e0f8ccad02de20eaba4fa2f2e046b0032e4e17e481667d6226b3ec82061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19505364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b21662b1d3ba291b541e6898e9870c8f17fc32fc1542e8cd26321d995ed654`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d37ece6c30e22e249589d6aeda58cf29c409948f056a8037f657691f333031`  
		Last Modified: Sun, 17 Mar 2024 22:03:24 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de6b96fd2b7588019fbfc72d5afede300a4d0ef5ea65a7a99fb9715b40b506a`  
		Last Modified: Sun, 17 Mar 2024 22:03:24 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e00979af0d93fc259d0c067c3acf72e2d19ee3e48b840e26b9838a1882a12b`  
		Last Modified: Sun, 17 Mar 2024 22:03:25 GMT  
		Size: 11.0 MB (10985997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fdd3af6a86a6153ff1589309d30e18935c2aacf45522556151835153652514`  
		Last Modified: Sat, 06 Apr 2024 15:46:55 GMT  
		Size: 5.3 MB (5275029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6015f889334ad064a637db08b112726bb85893466a14f46b4034fa7edfa031b0`  
		Last Modified: Sat, 06 Apr 2024 15:46:55 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.59-alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:f6d2ea0678751c8928910a6156f560c2dde868a32d09c26c484866d783af994d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1098082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd8c653038d8341ffbc2492c22b6e5888612cf77dba81bac930256963bfb5d4`

```dockerfile
```

-	Layers:
	-	`sha256:a9f0621638da42ab83a8b188d1b0e79887b581ba27e779272a93e6bd57ffc94a`  
		Last Modified: Sat, 06 Apr 2024 15:46:55 GMT  
		Size: 1.1 MB (1060095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1f2fc0d9673de65aa6403e6d5aff61166189f0445f2df8c80cea6225a259da`  
		Last Modified: Sat, 06 Apr 2024 15:46:55 GMT  
		Size: 38.0 KB (37987 bytes)  
		MIME: application/vnd.in-toto+json

## `httpd:2.4.59-bookworm`

```console
$ docker pull httpd@sha256:36c8c79f900108f0f09fd4148ad35ade57cba0dc19d13f3d15be24ce94e6a639
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

### `httpd:2.4.59-bookworm` - linux; amd64

```console
$ docker pull httpd@sha256:518e9447a236de47cc2fb4f2dbf06466b6cd5cf50f9951742f9a20af76e8118d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59185382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c2fc9e3d849b21a35b4c96f5ad8ec4dc9b73ca44c56537039e8c6f3054db0a`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851c52adaa9bf680b2eaa45164baa37665418fb02666fb36c268002edd853994`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d9f60535a61833df2e57cc08221031d3ae50f3955a6d6b0153214619d357fb`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 4.0 MB (4006988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943a2b3cf551375517593790b58407ffc7028b4b34bca6c0756b76708ea4b3ce`  
		Last Modified: Wed, 24 Apr 2024 04:57:24 GMT  
		Size: 26.0 MB (26027444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea83e81966d64f34a57ffcc118b75ad19bc9321f9809cf9b0df25548a2fa695e`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.59-bookworm` - unknown; unknown

```console
$ docker pull httpd@sha256:e31d2d75b317933ed59c3503fcfd00357545f4e60e60d87368674365eed990bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc7b98024523f6963a92b3a8edb71945171fff164f1da1e3bc9296d404a1da2`

```dockerfile
```

-	Layers:
	-	`sha256:1a0e348c51fd80864d852c8a1b3dbe89c1cbf088a8d4fe204b4f9a2106b65425`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 2.5 MB (2475971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea347276a3b2b4390cbb875d979ac18e828399022ce83785af6a6e19535cf238`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 37.8 KB (37766 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.59-bookworm` - linux; arm variant v5

```console
$ docker pull httpd@sha256:6ac6acfaf36b492c8ee0271b5c1745e5d5173186838066fb55416fe1bad7f84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55660337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594aaef0a91e898dfb26ab368782f59da9b9f69c9ad0d9a155208b535102d8e8`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfdcc496dd931564ad13b4c74e84a37bd3e8fe4d3e8eef76531c007b4918eb3`  
		Last Modified: Wed, 24 Apr 2024 17:19:02 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7797397d89aa986596ae17907e8812fb696c601b77e453f8cfff70c5282bb68`  
		Last Modified: Wed, 24 Apr 2024 17:19:03 GMT  
		Size: 3.5 MB (3511113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabda791a3820471d4af8b4b5339e9e5ade214d951432d16dcf09a30dfc07788`  
		Last Modified: Wed, 24 Apr 2024 17:19:04 GMT  
		Size: 25.2 MB (25238724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7b73f2fae9dae743b3751fc794fe838ccfee7359899fe2ef291db96f774025`  
		Last Modified: Wed, 24 Apr 2024 17:19:03 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.59-bookworm` - unknown; unknown

```console
$ docker pull httpd@sha256:0559103a0db87f5edf6e70a2fce9af410a68e8207c18d62b1a99fa7d6081320a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2517016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5eb9364b67ec513d9aa9dab74264a7e94017611ae8f167c5e716aad4b7680e`

```dockerfile
```

-	Layers:
	-	`sha256:0fd0fb4e581c468abde2999045c163e01f5f465436e7aa62ce734436862f9eac`  
		Last Modified: Wed, 24 Apr 2024 17:19:03 GMT  
		Size: 2.5 MB (2479288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38cc0fcc6c1dede08c15c91c4bc214763cd7fb9e515bc4f8b07ba05cdc9cd387`  
		Last Modified: Wed, 24 Apr 2024 17:19:03 GMT  
		Size: 37.7 KB (37728 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.59-bookworm` - linux; arm variant v7

```console
$ docker pull httpd@sha256:e49897ae28bb259a5a1b205a464098038e49ea2bb4985187e84baac47edda986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52738179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9fefb7a703a9d947d489c78f23271b57b138126899b22193b569f3d5ceb0d2`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063593c7931b25f55a01b9bb0f7156d7398c702900d7c6c5a10ac3cb9b111eeb`  
		Last Modified: Wed, 24 Apr 2024 16:30:49 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60dd6c2df475ede40fbebdd310c9770f5c85d86278fe66bcfb34015f9975b80`  
		Last Modified: Wed, 24 Apr 2024 16:30:50 GMT  
		Size: 3.3 MB (3286910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5afe70e80d3c8da2e79abd6e84a95f7bb9516fe79ffc1e06abcb55d3af394429`  
		Last Modified: Wed, 24 Apr 2024 16:30:51 GMT  
		Size: 24.7 MB (24710357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e43b819248841764c8eaee46258c16341b869c3cd10e29c5fe19a7ad57d3ea0`  
		Last Modified: Wed, 24 Apr 2024 16:30:50 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.59-bookworm` - unknown; unknown

```console
$ docker pull httpd@sha256:daa1d3562f002200d97c8042f5fb9e5cce9d3a91b979ab3bae79daa3f5a6f0a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2516068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beda48825ccb307edac52c5e75efd8fc86548bb74670c0558d03c6057104e328`

```dockerfile
```

-	Layers:
	-	`sha256:6656cffeaa9a2613f22ecf4356afe7a1fd612ffb7430d4e7e2ab9004ece5d051`  
		Last Modified: Wed, 24 Apr 2024 16:30:50 GMT  
		Size: 2.5 MB (2478340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1efca153bd1cf7ed5e26102ed35722aa4aec61d831e71818bba3175e03866560`  
		Last Modified: Wed, 24 Apr 2024 16:30:50 GMT  
		Size: 37.7 KB (37728 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.59-bookworm` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:b2670b51810a49855b0b59ed87dd064b3ec3ecf95e77d9dd6f6d13bab7467dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58997314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73acb239a8eb7a9ef5b6848a5b01bb26cc03d2262056705876bf7ac6ad781f02`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855b568ab02c3fee1362d51176f966517b1e03ca0c8efde55eddace90835f300`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c521cc2c4e8a439951003122cdab841fe1b1350db864e2cf9dea69298513f711`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 3.8 MB (3824128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c8bced82bd1d3557a49d39ea03bb8090bf3abc8154ab65388d9f9728f3ce02`  
		Last Modified: Thu, 25 Apr 2024 07:23:09 GMT  
		Size: 26.0 MB (25992782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae159c85a0b3662b8e9d58344f7da1b84836a7338c8ddf6b88360cea400929f`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.59-bookworm` - unknown; unknown

```console
$ docker pull httpd@sha256:307bc20593c828b3894250dd4e16b149c046b98c033453278fca94efd8bd0454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70026eb22d8bfc08dc60be7e7dcdce118be2390abe04aa90c7f27e6245767782`

```dockerfile
```

-	Layers:
	-	`sha256:77720a2aab607f8a1c40306899700597640ec9696bb65c714e6131dd481171b1`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 2.5 MB (2476229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd136e58015bf40bdc568f33b0d261e3140c11eee1769fbfb67f4ad2b93284f8`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 37.6 KB (37618 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.59-bookworm` - linux; 386

```console
$ docker pull httpd@sha256:34359f60b5aa39dfe4a6da81d319693f6ca6155e12e91b50e5d6da3ae7db89b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60223958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457768b202e686803b86961428bc138b1e4c6f0a08bec510257bba9b2d7e4486`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2941e842a389d5a4c34aa8e7f83e761d6a0deb0ed5c5bc01838c71d23659ac77`  
		Last Modified: Wed, 24 Apr 2024 04:57:41 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f800dd9ec1f906ac5c081169392c9dd10d32921d3e52e601c8c7ca7bcda3c600`  
		Last Modified: Wed, 24 Apr 2024 04:57:42 GMT  
		Size: 4.1 MB (4063511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494266189a0019f5cc3fec9ab5a55a1ea0fc3c8cc6a3ab1c1faeedbdc0fbaa5e`  
		Last Modified: Wed, 24 Apr 2024 04:57:42 GMT  
		Size: 26.0 MB (25996792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed1b4c9db903ab4981ddd506901a8ead9ae515c81f307dc7e52ed0256e73eec`  
		Last Modified: Wed, 24 Apr 2024 04:57:41 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.59-bookworm` - unknown; unknown

```console
$ docker pull httpd@sha256:928d95daa4cdcfd2c1395f60c62ed85d871764fdbfd6b1dbcf750c4f906d1eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2510705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8144c9b91841f94cfaea34892b458353406e2daa257e7e97e80ce41341381322`

```dockerfile
```

-	Layers:
	-	`sha256:637adc441596f6bc7ae557cdd4ef0de555b3e1b8aaa69a88adf26ea73e04a753`  
		Last Modified: Wed, 24 Apr 2024 04:57:42 GMT  
		Size: 2.5 MB (2472991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c57120021da5fb478f2b39b4540d36f1ba9bfa1efbe1c0616a07fe2a81d1e746`  
		Last Modified: Wed, 24 Apr 2024 04:57:41 GMT  
		Size: 37.7 KB (37714 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.59-bookworm` - linux; mips64le

```console
$ docker pull httpd@sha256:4512a76c673f11979d9f2ea96a56c59db662c5e8258c7128258245d18bb9292d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58678876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f7e1281eca6101e477c1cb3af32334cd551c69acc34839c3a8f8e3b3be6e80`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28233217e5e2c53a42bce8370d4462ed742672e46ec0e3acc021494964a6c4e`  
		Last Modified: Wed, 24 Apr 2024 23:51:19 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98af3a5736d8674d724399887f435760548973f8720121002efb9766f6892bb1`  
		Last Modified: Wed, 24 Apr 2024 23:51:20 GMT  
		Size: 3.4 MB (3373290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d3af7336bf3047ff58c8fc60fcce4943c107ecf04bb449d43849ce851d53aa`  
		Last Modified: Wed, 24 Apr 2024 23:51:22 GMT  
		Size: 26.2 MB (26160940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ed9c80633a9c8a938fb64f3eddb5677882265446491ddb3fce480647719cf5`  
		Last Modified: Wed, 24 Apr 2024 23:51:20 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.59-bookworm` - unknown; unknown

```console
$ docker pull httpd@sha256:b80ddb9178f5c7b1fb405cdad5a1ca2b55ae93147230041eb0b0e958dd6bd2b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f0b12a55ecb5a0fb2dc015ef1bebad8c2d781a197cd3a665b0b585ef134715`

```dockerfile
```

-	Layers:
	-	`sha256:e03a7d994013fb85dd187518a518143a7a11bc11a02be3fe21ac1bcc6c2bad8c`  
		Last Modified: Wed, 24 Apr 2024 23:51:20 GMT  
		Size: 37.5 KB (37480 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.59-bookworm` - linux; ppc64le

```console
$ docker pull httpd@sha256:f367b8c823d8e9650e4d0f3576cb4cb56931fb2a9abc5cf933fbc3e5e2d03eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64781656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5b1ab6010140721a568d9027ba17353616269ed57d0407e63a20a9db866d83`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8779f7411971984d8a264462c07b9383e455edbfa3945c3a7c3c0f0da6281405`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df41593893685df2f819e89678437a7190515d7cc02ecf4d3826f45e94594a6`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 4.3 MB (4329567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5fc79508ca1591a5607565a2c2fd383aaea639b5a8777f026f5767404f73eb`  
		Last Modified: Thu, 25 Apr 2024 03:19:08 GMT  
		Size: 27.3 MB (27310418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3bf3ad211e2e210d10318ae48cfccfdefd6adae953aa2a10ca77880dd921ac`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.59-bookworm` - unknown; unknown

```console
$ docker pull httpd@sha256:f5fdb59224d04f59d5f80ba98a242d519237e7fe401672f767a98c516fbb17b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2518193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3109624aa7219e37cb7b867bf5926f24b5e9b4eb3d6e31536b83f1751b0c42cf`

```dockerfile
```

-	Layers:
	-	`sha256:5553f9b984d60f0b17ff79178b8bd6943ed3c6a28b511fee1a71f4df9b281e63`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 2.5 MB (2480527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49e0858fd1c6faa9c04410e63c7d7bf0b572ae75294b281ff9ce3ba69ca201b3`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 37.7 KB (37666 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:2.4.59-bookworm` - linux; s390x

```console
$ docker pull httpd@sha256:ae3341db428440ab15b07058d2bab822247b8aa06035c19edea03f2a675e3b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56864928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed5070ae0d9687d8b499eae1be4caf30616eea45630f52af89bff9348d1cc474`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076f4d06a50ca8b3bcf6951ac8efa98b499598a608155af2bc4e4c0283e315e6`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8054bd786718ad21214203f377432a693d561157449486d1ea16ee3530d793e1`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 3.7 MB (3654647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c39e346caebedca77c0054fa938878774f458b3b88e05f7099ff4b70345256a`  
		Last Modified: Thu, 25 Apr 2024 02:28:32 GMT  
		Size: 25.7 MB (25697456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb3dcd087010aa65e19ef6e7ae889206220840a38cc7d973cd3b0e635895072`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:2.4.59-bookworm` - unknown; unknown

```console
$ docker pull httpd@sha256:779ecac6b7d7547b09bf644ce963543f48bac336bfe174dbd0583d7d06e3b0c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d2597d4c0c4788030bfe3a20a2ddf9842323ed2e486b682e1a863ae138ad89`

```dockerfile
```

-	Layers:
	-	`sha256:d42e15caceec6e5f15ccf873f46289eb1dc452e23ab53a076d905630a09e58e5`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 2.5 MB (2475763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28db97fd901916835b62fdb1cece860a44f5b2888ae52a2ea94026e65e136df5`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 37.6 KB (37600 bytes)  
		MIME: application/vnd.in-toto+json

## `httpd:alpine`

```console
$ docker pull httpd@sha256:68f6714169b70ca33126c46f60cc802eb602c6435f4ebf08349d871d500d3e70
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

### `httpd:alpine` - linux; amd64

```console
$ docker pull httpd@sha256:b48b48dcfff1407638908b8a1782480df0ad8bac7f5fc579496357864f97e60c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18905522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b6bf3450e2114fc55779cd878fa1a176a851a4de5a38f79ffb779639c455a2`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e13f4f5374dc8e6fd59fc8dc82c77d2dfc85ffd1136f5edbc4a9054ba955927`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333c1d8ec87c0966bd88d1293586bce65663a901c08af2a85ffe369897d7fd9e`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58593e44a54df297fb6195ac992fbda56ab083ee57a934ba5de6c49c8c6cff4a`  
		Last Modified: Fri, 05 Apr 2024 17:53:06 GMT  
		Size: 10.4 MB (10384953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608381599c688e98facb252c7e8313379b6d1f574bba1b49262a39145764d4d9`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 5.1 MB (5110138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e5ce613b310458e6aad12ed911fae7e33b9d59232a0a816ae8829774a7c351`  
		Last Modified: Fri, 05 Apr 2024 17:53:06 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:933e4cc35d564b7e6b37b9da44ff4c3a1c961ee5a115addfc4348458b9584a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1105171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32930164a83ab310294ec129967dfa6b0e208133bcd30d31b8bdaae148384c8c`

```dockerfile
```

-	Layers:
	-	`sha256:4ce2b7d308346544402cfbaecf8b70c4dfbb6d6385f79028bfeb7b9df16b2b23`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 1.1 MB (1067018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f7979b59e4c92069c8731802e0b918cc1668ed3cbc3448ac9f5863488762eec`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 38.2 KB (38153 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine` - linux; arm variant v6

```console
$ docker pull httpd@sha256:3536bda1cb1b0f3581896c7acafa8426a67ac185711f3af26cffb991a76d08fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17774769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1732292898ef3f1fb223e062d5aa76bcf8087c9c7978a357ea964a0f9e6e2a4d`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8c07a4a93f0faf2d460b21b916e9f8d52550da29882704b17b06201a89e118`  
		Last Modified: Fri, 05 Apr 2024 18:11:18 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001db4688f33e38d27d733b6d51f6a9edf395f4fd76749cf91ebb32f1fd25483`  
		Last Modified: Fri, 05 Apr 2024 18:11:18 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f8fe9e9d09c4f2074ab547012fee140749069dd339f3cc87dc71e347884d92`  
		Last Modified: Fri, 05 Apr 2024 18:11:19 GMT  
		Size: 9.6 MB (9577820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c092ec8ebe549b81d3f7c2f8f6830bfc42142f090d8fe5cd5b52f296d516310`  
		Last Modified: Fri, 05 Apr 2024 18:11:19 GMT  
		Size: 5.0 MB (5029848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346b9e25e64782fa95573e9eb07893339f472741823a4062737052da7391dfd5`  
		Last Modified: Fri, 05 Apr 2024 18:11:20 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:2790d9e49f2d98ffc37ada24de30725d9196ac28a61fd2ef576263287c58aec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d270ac30275fb727064cc5d2eeeb08a7ffc7305c12f93e19d03d209ebc2d6f58`

```dockerfile
```

-	Layers:
	-	`sha256:57b3e792cca6cdd007c318692afa6ccc61834b2e257e11c1832e8403dd37032e`  
		Last Modified: Fri, 05 Apr 2024 18:11:18 GMT  
		Size: 37.9 KB (37910 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine` - linux; arm variant v7

```console
$ docker pull httpd@sha256:09dd424663b1d2540476d34b124fb25360411dff64f69cc71fa3cf02381fb9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16993127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad0e3a5244891745dcd5889901c7a0101e398b81de79ff65cb7270e482bbbbb`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74aa637d7bf59fca068dcb5b7dd86513aa9ad3282aad69b3e9039cc2f6f18bcc`  
		Last Modified: Sat, 16 Mar 2024 16:04:22 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fc40e56afb70a5d1bf79dc4bf9118f2b993e3687626ab036513d862a1a286e`  
		Last Modified: Sat, 16 Mar 2024 16:04:22 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7015ed48724aa34bf3e29ddfa9b1058e3c374c383a17cc3ba6b943f7de0cf1`  
		Last Modified: Sat, 16 Mar 2024 16:04:23 GMT  
		Size: 9.3 MB (9334751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5553e605c52a438be1d61a267e9cbc342a533ce3966d9c82b03dfe7e0f1777c8`  
		Last Modified: Fri, 05 Apr 2024 17:57:38 GMT  
		Size: 4.7 MB (4737771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a356346eae4cb6bddf85f93948a3f0df8845d93176937fef76aec99cb50faef2`  
		Last Modified: Fri, 05 Apr 2024 17:57:37 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:28d8f38fd78210cba28d51dc8d470fc5068b2d90a3fd9cb0a9f14a622ff89577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1102820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3348381822a72f52b9575c5d5d34c4da16730f59ef5128ebdedb089cd1d48819`

```dockerfile
```

-	Layers:
	-	`sha256:9e5deb95007dd7e44d0a6f9d0c0ccf2ee83e76cb545b6c4691007c75be1c6498`  
		Last Modified: Fri, 05 Apr 2024 17:57:38 GMT  
		Size: 1.1 MB (1064695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a16e23262169a2b30cd14de32d5acde981fcd5bf7179967f584df46c44b1b10`  
		Last Modified: Fri, 05 Apr 2024 17:57:37 GMT  
		Size: 38.1 KB (38125 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:91756bbcc9b8283d49fdf66189881d39576f12c012dad8796b97948636e0b40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (18989141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d3d050f8abbaa153d704cae494aeeca773a0f24ba35600711e356083a79a66`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68b5c4e3f3b827d8933253d337cf55bf3ace2d75070b8ea7655a893c325569f`  
		Last Modified: Sat, 16 Mar 2024 15:13:13 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba68aab08183c67e796b91cc96b7c1629e35f98048a721cd67997edb83a202e2`  
		Last Modified: Sat, 16 Mar 2024 15:13:13 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1e2b5044558ea2188f9ba4d34df06cc7109e01f5caefe6c2bc5ecd11b6ced0`  
		Last Modified: Sat, 16 Mar 2024 15:13:14 GMT  
		Size: 10.4 MB (10388804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6beaeaed29f48ef5f4141a8b7e76a8e550f88775f81d464c5944634479d8ed7a`  
		Last Modified: Fri, 05 Apr 2024 17:55:14 GMT  
		Size: 5.3 MB (5250912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8742eb1c1f87645540c4e75db0e19ba29d77c28e18927d3310670a72b85ec82`  
		Last Modified: Fri, 05 Apr 2024 17:55:13 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:b266b0cecec670e48d25423f3f218b28b7745ec04fa2be113bca803f25a89f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1100073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a241afe2d5ab26a07a1794465d326a6827b70fbef1de59a250d03605dac1ded`

```dockerfile
```

-	Layers:
	-	`sha256:43abc3efae9947304de80f9a75aa23117ac15a382c784b355816810199ecbf7e`  
		Last Modified: Fri, 05 Apr 2024 17:55:13 GMT  
		Size: 1.1 MB (1062068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dcf770b26d2bae0707f3d339ee48b6778855e725144a0d1384402416186c295`  
		Last Modified: Fri, 05 Apr 2024 17:55:13 GMT  
		Size: 38.0 KB (38005 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine` - linux; 386

```console
$ docker pull httpd@sha256:40a391f6e52f9fa6d56741b455cbffde4d9104948f1078da5bd6c248b3318f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18161726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa32e51497f1ebc9739fe8b3d915e5fecd520dd4959266c76adf910b71fd4ea`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740e52eababa89f531e99d9609ea4df66e75527cb8a97aa3feba95f64f8d19c1`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9d066a768f0f31e823ea143de9180c7e2b5b51ee3f0267272b2122353c5530`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320efa4f4b1525ce8d8dc283fe9bce7bf23e031d3349b59957067c1ad3f22eeb`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 9.9 MB (9862040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b89437c703e9c702702c5eb0432f2efcb16ae506d611336abbf81b083b7fbd`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 5.1 MB (5053894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1099f38eb4d16ee148b32677e9f70da2535bef69261361e1247b719b03f5a2c4`  
		Last Modified: Fri, 05 Apr 2024 17:53:13 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:52a1c8f1cdb4a7057132a6bc0f6f82528ee10ccffedf7bb17d1108bf94d8ac6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1105068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946eef1c61b246af219f7ef605bfd198e004722dc6d7fafdaa0a35c5504965e7`

```dockerfile
```

-	Layers:
	-	`sha256:56b910d095946bc43dbafed2e0f13360d62f86b726feba74f5670cb07cd93f3d`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 1.1 MB (1066973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37abeadc160510b3cfd3b1a3d82f05e600fcbb1c92c9b5e2c0a20b0c8e865bc7`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 38.1 KB (38095 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine` - linux; ppc64le

```console
$ docker pull httpd@sha256:447d4eca233b95a1aebdb73d93c024d8226d6a608568aa2c9505f96a3b8f19bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19410079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bed7414a71a37df5ac42b1637107b9e12f08cc3e63e5d9ecd84556d26489d9b`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca1e90415bffcf574224c85fef296c0f849237fe22a0b5065a26673f7cbba51`  
		Last Modified: Sat, 16 Mar 2024 10:26:53 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b746962fe11d53bb9b19dfe7990c4658ac0472cccbd8daa5794e5f3a22cfda51`  
		Last Modified: Sat, 16 Mar 2024 10:26:53 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68b51060f0a52e914490ae4eeb10af1258ec331a68f78f4944118a1ca9911bd`  
		Last Modified: Sat, 16 Mar 2024 10:26:54 GMT  
		Size: 10.6 MB (10627211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f73e01f2b7ec6f92d901b09901b77c8dec59f0535633de6f26cc281f9452954`  
		Last Modified: Fri, 05 Apr 2024 17:59:16 GMT  
		Size: 5.4 MB (5422810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13941787572cd155aec58f453b55fcb5e882b928cf4aa65c8ede53e07d15a45`  
		Last Modified: Fri, 05 Apr 2024 17:59:16 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:6591d53cc91652e76f1529af4696e990fe459184e928ac7371b55488a2f3b7c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1098208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d59400ec49b3e236a314b42b69e345faf3cdcfbf0bd553b5d16dfc66d548bdd`

```dockerfile
```

-	Layers:
	-	`sha256:630456dcd802b6d23b26b5dc5b782789bc8969758ecdeca80d33ca2ef97be7bb`  
		Last Modified: Fri, 05 Apr 2024 17:59:16 GMT  
		Size: 1.1 MB (1060153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49cbad644a03a7cf5127a55a38cc827f068240cd3ce64261f61e48708941076d`  
		Last Modified: Fri, 05 Apr 2024 17:59:16 GMT  
		Size: 38.1 KB (38055 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine` - linux; s390x

```console
$ docker pull httpd@sha256:8ddf2e0f8ccad02de20eaba4fa2f2e046b0032e4e17e481667d6226b3ec82061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19505364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b21662b1d3ba291b541e6898e9870c8f17fc32fc1542e8cd26321d995ed654`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d37ece6c30e22e249589d6aeda58cf29c409948f056a8037f657691f333031`  
		Last Modified: Sun, 17 Mar 2024 22:03:24 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de6b96fd2b7588019fbfc72d5afede300a4d0ef5ea65a7a99fb9715b40b506a`  
		Last Modified: Sun, 17 Mar 2024 22:03:24 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e00979af0d93fc259d0c067c3acf72e2d19ee3e48b840e26b9838a1882a12b`  
		Last Modified: Sun, 17 Mar 2024 22:03:25 GMT  
		Size: 11.0 MB (10985997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fdd3af6a86a6153ff1589309d30e18935c2aacf45522556151835153652514`  
		Last Modified: Sat, 06 Apr 2024 15:46:55 GMT  
		Size: 5.3 MB (5275029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6015f889334ad064a637db08b112726bb85893466a14f46b4034fa7edfa031b0`  
		Last Modified: Sat, 06 Apr 2024 15:46:55 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine` - unknown; unknown

```console
$ docker pull httpd@sha256:f6d2ea0678751c8928910a6156f560c2dde868a32d09c26c484866d783af994d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1098082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd8c653038d8341ffbc2492c22b6e5888612cf77dba81bac930256963bfb5d4`

```dockerfile
```

-	Layers:
	-	`sha256:a9f0621638da42ab83a8b188d1b0e79887b581ba27e779272a93e6bd57ffc94a`  
		Last Modified: Sat, 06 Apr 2024 15:46:55 GMT  
		Size: 1.1 MB (1060095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1f2fc0d9673de65aa6403e6d5aff61166189f0445f2df8c80cea6225a259da`  
		Last Modified: Sat, 06 Apr 2024 15:46:55 GMT  
		Size: 38.0 KB (37987 bytes)  
		MIME: application/vnd.in-toto+json

## `httpd:alpine3.19`

```console
$ docker pull httpd@sha256:68f6714169b70ca33126c46f60cc802eb602c6435f4ebf08349d871d500d3e70
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

### `httpd:alpine3.19` - linux; amd64

```console
$ docker pull httpd@sha256:b48b48dcfff1407638908b8a1782480df0ad8bac7f5fc579496357864f97e60c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.9 MB (18905522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b6bf3450e2114fc55779cd878fa1a176a851a4de5a38f79ffb779639c455a2`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e13f4f5374dc8e6fd59fc8dc82c77d2dfc85ffd1136f5edbc4a9054ba955927`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333c1d8ec87c0966bd88d1293586bce65663a901c08af2a85ffe369897d7fd9e`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58593e44a54df297fb6195ac992fbda56ab083ee57a934ba5de6c49c8c6cff4a`  
		Last Modified: Fri, 05 Apr 2024 17:53:06 GMT  
		Size: 10.4 MB (10384953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608381599c688e98facb252c7e8313379b6d1f574bba1b49262a39145764d4d9`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 5.1 MB (5110138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e5ce613b310458e6aad12ed911fae7e33b9d59232a0a816ae8829774a7c351`  
		Last Modified: Fri, 05 Apr 2024 17:53:06 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:933e4cc35d564b7e6b37b9da44ff4c3a1c961ee5a115addfc4348458b9584a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1105171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32930164a83ab310294ec129967dfa6b0e208133bcd30d31b8bdaae148384c8c`

```dockerfile
```

-	Layers:
	-	`sha256:4ce2b7d308346544402cfbaecf8b70c4dfbb6d6385f79028bfeb7b9df16b2b23`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 1.1 MB (1067018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f7979b59e4c92069c8731802e0b918cc1668ed3cbc3448ac9f5863488762eec`  
		Last Modified: Fri, 05 Apr 2024 17:53:05 GMT  
		Size: 38.2 KB (38153 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine3.19` - linux; arm variant v6

```console
$ docker pull httpd@sha256:3536bda1cb1b0f3581896c7acafa8426a67ac185711f3af26cffb991a76d08fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17774769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1732292898ef3f1fb223e062d5aa76bcf8087c9c7978a357ea964a0f9e6e2a4d`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8c07a4a93f0faf2d460b21b916e9f8d52550da29882704b17b06201a89e118`  
		Last Modified: Fri, 05 Apr 2024 18:11:18 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001db4688f33e38d27d733b6d51f6a9edf395f4fd76749cf91ebb32f1fd25483`  
		Last Modified: Fri, 05 Apr 2024 18:11:18 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f8fe9e9d09c4f2074ab547012fee140749069dd339f3cc87dc71e347884d92`  
		Last Modified: Fri, 05 Apr 2024 18:11:19 GMT  
		Size: 9.6 MB (9577820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c092ec8ebe549b81d3f7c2f8f6830bfc42142f090d8fe5cd5b52f296d516310`  
		Last Modified: Fri, 05 Apr 2024 18:11:19 GMT  
		Size: 5.0 MB (5029848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346b9e25e64782fa95573e9eb07893339f472741823a4062737052da7391dfd5`  
		Last Modified: Fri, 05 Apr 2024 18:11:20 GMT  
		Size: 288.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:2790d9e49f2d98ffc37ada24de30725d9196ac28a61fd2ef576263287c58aec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 KB (37910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d270ac30275fb727064cc5d2eeeb08a7ffc7305c12f93e19d03d209ebc2d6f58`

```dockerfile
```

-	Layers:
	-	`sha256:57b3e792cca6cdd007c318692afa6ccc61834b2e257e11c1832e8403dd37032e`  
		Last Modified: Fri, 05 Apr 2024 18:11:18 GMT  
		Size: 37.9 KB (37910 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine3.19` - linux; arm variant v7

```console
$ docker pull httpd@sha256:09dd424663b1d2540476d34b124fb25360411dff64f69cc71fa3cf02381fb9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16993127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad0e3a5244891745dcd5889901c7a0101e398b81de79ff65cb7270e482bbbbb`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74aa637d7bf59fca068dcb5b7dd86513aa9ad3282aad69b3e9039cc2f6f18bcc`  
		Last Modified: Sat, 16 Mar 2024 16:04:22 GMT  
		Size: 1.2 KB (1236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fc40e56afb70a5d1bf79dc4bf9118f2b993e3687626ab036513d862a1a286e`  
		Last Modified: Sat, 16 Mar 2024 16:04:22 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7015ed48724aa34bf3e29ddfa9b1058e3c374c383a17cc3ba6b943f7de0cf1`  
		Last Modified: Sat, 16 Mar 2024 16:04:23 GMT  
		Size: 9.3 MB (9334751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5553e605c52a438be1d61a267e9cbc342a533ce3966d9c82b03dfe7e0f1777c8`  
		Last Modified: Fri, 05 Apr 2024 17:57:38 GMT  
		Size: 4.7 MB (4737771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a356346eae4cb6bddf85f93948a3f0df8845d93176937fef76aec99cb50faef2`  
		Last Modified: Fri, 05 Apr 2024 17:57:37 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:28d8f38fd78210cba28d51dc8d470fc5068b2d90a3fd9cb0a9f14a622ff89577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1102820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3348381822a72f52b9575c5d5d34c4da16730f59ef5128ebdedb089cd1d48819`

```dockerfile
```

-	Layers:
	-	`sha256:9e5deb95007dd7e44d0a6f9d0c0ccf2ee83e76cb545b6c4691007c75be1c6498`  
		Last Modified: Fri, 05 Apr 2024 17:57:38 GMT  
		Size: 1.1 MB (1064695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a16e23262169a2b30cd14de32d5acde981fcd5bf7179967f584df46c44b1b10`  
		Last Modified: Fri, 05 Apr 2024 17:57:37 GMT  
		Size: 38.1 KB (38125 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:91756bbcc9b8283d49fdf66189881d39576f12c012dad8796b97948636e0b40a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.0 MB (18989141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d3d050f8abbaa153d704cae494aeeca773a0f24ba35600711e356083a79a66`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68b5c4e3f3b827d8933253d337cf55bf3ace2d75070b8ea7655a893c325569f`  
		Last Modified: Sat, 16 Mar 2024 15:13:13 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba68aab08183c67e796b91cc96b7c1629e35f98048a721cd67997edb83a202e2`  
		Last Modified: Sat, 16 Mar 2024 15:13:13 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1e2b5044558ea2188f9ba4d34df06cc7109e01f5caefe6c2bc5ecd11b6ced0`  
		Last Modified: Sat, 16 Mar 2024 15:13:14 GMT  
		Size: 10.4 MB (10388804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6beaeaed29f48ef5f4141a8b7e76a8e550f88775f81d464c5944634479d8ed7a`  
		Last Modified: Fri, 05 Apr 2024 17:55:14 GMT  
		Size: 5.3 MB (5250912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8742eb1c1f87645540c4e75db0e19ba29d77c28e18927d3310670a72b85ec82`  
		Last Modified: Fri, 05 Apr 2024 17:55:13 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:b266b0cecec670e48d25423f3f218b28b7745ec04fa2be113bca803f25a89f5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1100073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a241afe2d5ab26a07a1794465d326a6827b70fbef1de59a250d03605dac1ded`

```dockerfile
```

-	Layers:
	-	`sha256:43abc3efae9947304de80f9a75aa23117ac15a382c784b355816810199ecbf7e`  
		Last Modified: Fri, 05 Apr 2024 17:55:13 GMT  
		Size: 1.1 MB (1062068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dcf770b26d2bae0707f3d339ee48b6778855e725144a0d1384402416186c295`  
		Last Modified: Fri, 05 Apr 2024 17:55:13 GMT  
		Size: 38.0 KB (38005 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine3.19` - linux; 386

```console
$ docker pull httpd@sha256:40a391f6e52f9fa6d56741b455cbffde4d9104948f1078da5bd6c248b3318f26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.2 MB (18161726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa32e51497f1ebc9739fe8b3d915e5fecd520dd4959266c76adf910b71fd4ea`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740e52eababa89f531e99d9609ea4df66e75527cb8a97aa3feba95f64f8d19c1`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9d066a768f0f31e823ea143de9180c7e2b5b51ee3f0267272b2122353c5530`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320efa4f4b1525ce8d8dc283fe9bce7bf23e031d3349b59957067c1ad3f22eeb`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 9.9 MB (9862040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b89437c703e9c702702c5eb0432f2efcb16ae506d611336abbf81b083b7fbd`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 5.1 MB (5053894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1099f38eb4d16ee148b32677e9f70da2535bef69261361e1247b719b03f5a2c4`  
		Last Modified: Fri, 05 Apr 2024 17:53:13 GMT  
		Size: 287.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:52a1c8f1cdb4a7057132a6bc0f6f82528ee10ccffedf7bb17d1108bf94d8ac6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1105068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946eef1c61b246af219f7ef605bfd198e004722dc6d7fafdaa0a35c5504965e7`

```dockerfile
```

-	Layers:
	-	`sha256:56b910d095946bc43dbafed2e0f13360d62f86b726feba74f5670cb07cd93f3d`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 1.1 MB (1066973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37abeadc160510b3cfd3b1a3d82f05e600fcbb1c92c9b5e2c0a20b0c8e865bc7`  
		Last Modified: Fri, 05 Apr 2024 17:53:12 GMT  
		Size: 38.1 KB (38095 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine3.19` - linux; ppc64le

```console
$ docker pull httpd@sha256:447d4eca233b95a1aebdb73d93c024d8226d6a608568aa2c9505f96a3b8f19bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.4 MB (19410079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bed7414a71a37df5ac42b1637107b9e12f08cc3e63e5d9ecd84556d26489d9b`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca1e90415bffcf574224c85fef296c0f849237fe22a0b5065a26673f7cbba51`  
		Last Modified: Sat, 16 Mar 2024 10:26:53 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b746962fe11d53bb9b19dfe7990c4658ac0472cccbd8daa5794e5f3a22cfda51`  
		Last Modified: Sat, 16 Mar 2024 10:26:53 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68b51060f0a52e914490ae4eeb10af1258ec331a68f78f4944118a1ca9911bd`  
		Last Modified: Sat, 16 Mar 2024 10:26:54 GMT  
		Size: 10.6 MB (10627211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f73e01f2b7ec6f92d901b09901b77c8dec59f0535633de6f26cc281f9452954`  
		Last Modified: Fri, 05 Apr 2024 17:59:16 GMT  
		Size: 5.4 MB (5422810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13941787572cd155aec58f453b55fcb5e882b928cf4aa65c8ede53e07d15a45`  
		Last Modified: Fri, 05 Apr 2024 17:59:16 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:6591d53cc91652e76f1529af4696e990fe459184e928ac7371b55488a2f3b7c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1098208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d59400ec49b3e236a314b42b69e345faf3cdcfbf0bd553b5d16dfc66d548bdd`

```dockerfile
```

-	Layers:
	-	`sha256:630456dcd802b6d23b26b5dc5b782789bc8969758ecdeca80d33ca2ef97be7bb`  
		Last Modified: Fri, 05 Apr 2024 17:59:16 GMT  
		Size: 1.1 MB (1060153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49cbad644a03a7cf5127a55a38cc827f068240cd3ce64261f61e48708941076d`  
		Last Modified: Fri, 05 Apr 2024 17:59:16 GMT  
		Size: 38.1 KB (38055 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:alpine3.19` - linux; s390x

```console
$ docker pull httpd@sha256:8ddf2e0f8ccad02de20eaba4fa2f2e046b0032e4e17e481667d6226b3ec82061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.5 MB (19505364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b21662b1d3ba291b541e6898e9870c8f17fc32fc1542e8cd26321d995ed654`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -x 	&& adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Apr 2024 17:31:14 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
WORKDIR /usr/local/apache2
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 	apk add --no-cache 		apr 		apr-util 		apr-util-ldap 		ca-certificates 		perl 	; # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_VERSION=2.4.59
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Thu, 04 Apr 2024 17:31:14 GMT
ENV HTTPD_PATCHES=
# Thu, 04 Apr 2024 17:31:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		apr-dev 		apr-util-dev 		coreutils 		dpkg-dev dpkg 		gcc 		gnupg 		libc-dev 		patch 		curl-dev 		jansson-dev 		libxml2-dev 		lua-dev 		make 		nghttp2-dev 		openssl 		openssl-dev 		pcre-dev 		tar 		zlib-dev 		brotli-dev 	; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			'https://www.apache.org/dyn/closer.cgi?action=download&filename=' 			https://downloads.apache.org/ 			https://www-us.apache.org/dist/ 			https://www.apache.org/dist/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		deps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .httpd-so-deps $deps; 	apk del --no-network .build-deps; 		httpd -v # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
STOPSIGNAL SIGWINCH
# Thu, 04 Apr 2024 17:31:14 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Thu, 04 Apr 2024 17:31:14 GMT
EXPOSE map[80/tcp:{}]
# Thu, 04 Apr 2024 17:31:14 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d37ece6c30e22e249589d6aeda58cf29c409948f056a8037f657691f333031`  
		Last Modified: Sun, 17 Mar 2024 22:03:24 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de6b96fd2b7588019fbfc72d5afede300a4d0ef5ea65a7a99fb9715b40b506a`  
		Last Modified: Sun, 17 Mar 2024 22:03:24 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e00979af0d93fc259d0c067c3acf72e2d19ee3e48b840e26b9838a1882a12b`  
		Last Modified: Sun, 17 Mar 2024 22:03:25 GMT  
		Size: 11.0 MB (10985997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fdd3af6a86a6153ff1589309d30e18935c2aacf45522556151835153652514`  
		Last Modified: Sat, 06 Apr 2024 15:46:55 GMT  
		Size: 5.3 MB (5275029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6015f889334ad064a637db08b112726bb85893466a14f46b4034fa7edfa031b0`  
		Last Modified: Sat, 06 Apr 2024 15:46:55 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:alpine3.19` - unknown; unknown

```console
$ docker pull httpd@sha256:f6d2ea0678751c8928910a6156f560c2dde868a32d09c26c484866d783af994d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1098082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd8c653038d8341ffbc2492c22b6e5888612cf77dba81bac930256963bfb5d4`

```dockerfile
```

-	Layers:
	-	`sha256:a9f0621638da42ab83a8b188d1b0e79887b581ba27e779272a93e6bd57ffc94a`  
		Last Modified: Sat, 06 Apr 2024 15:46:55 GMT  
		Size: 1.1 MB (1060095 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1f2fc0d9673de65aa6403e6d5aff61166189f0445f2df8c80cea6225a259da`  
		Last Modified: Sat, 06 Apr 2024 15:46:55 GMT  
		Size: 38.0 KB (37987 bytes)  
		MIME: application/vnd.in-toto+json

## `httpd:bookworm`

```console
$ docker pull httpd@sha256:36c8c79f900108f0f09fd4148ad35ade57cba0dc19d13f3d15be24ce94e6a639
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

### `httpd:bookworm` - linux; amd64

```console
$ docker pull httpd@sha256:518e9447a236de47cc2fb4f2dbf06466b6cd5cf50f9951742f9a20af76e8118d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59185382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c2fc9e3d849b21a35b4c96f5ad8ec4dc9b73ca44c56537039e8c6f3054db0a`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851c52adaa9bf680b2eaa45164baa37665418fb02666fb36c268002edd853994`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d9f60535a61833df2e57cc08221031d3ae50f3955a6d6b0153214619d357fb`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 4.0 MB (4006988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943a2b3cf551375517593790b58407ffc7028b4b34bca6c0756b76708ea4b3ce`  
		Last Modified: Wed, 24 Apr 2024 04:57:24 GMT  
		Size: 26.0 MB (26027444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea83e81966d64f34a57ffcc118b75ad19bc9321f9809cf9b0df25548a2fa695e`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:bookworm` - unknown; unknown

```console
$ docker pull httpd@sha256:e31d2d75b317933ed59c3503fcfd00357545f4e60e60d87368674365eed990bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc7b98024523f6963a92b3a8edb71945171fff164f1da1e3bc9296d404a1da2`

```dockerfile
```

-	Layers:
	-	`sha256:1a0e348c51fd80864d852c8a1b3dbe89c1cbf088a8d4fe204b4f9a2106b65425`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 2.5 MB (2475971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea347276a3b2b4390cbb875d979ac18e828399022ce83785af6a6e19535cf238`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 37.8 KB (37766 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:bookworm` - linux; arm variant v5

```console
$ docker pull httpd@sha256:6ac6acfaf36b492c8ee0271b5c1745e5d5173186838066fb55416fe1bad7f84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55660337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594aaef0a91e898dfb26ab368782f59da9b9f69c9ad0d9a155208b535102d8e8`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfdcc496dd931564ad13b4c74e84a37bd3e8fe4d3e8eef76531c007b4918eb3`  
		Last Modified: Wed, 24 Apr 2024 17:19:02 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7797397d89aa986596ae17907e8812fb696c601b77e453f8cfff70c5282bb68`  
		Last Modified: Wed, 24 Apr 2024 17:19:03 GMT  
		Size: 3.5 MB (3511113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabda791a3820471d4af8b4b5339e9e5ade214d951432d16dcf09a30dfc07788`  
		Last Modified: Wed, 24 Apr 2024 17:19:04 GMT  
		Size: 25.2 MB (25238724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7b73f2fae9dae743b3751fc794fe838ccfee7359899fe2ef291db96f774025`  
		Last Modified: Wed, 24 Apr 2024 17:19:03 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:bookworm` - unknown; unknown

```console
$ docker pull httpd@sha256:0559103a0db87f5edf6e70a2fce9af410a68e8207c18d62b1a99fa7d6081320a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2517016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5eb9364b67ec513d9aa9dab74264a7e94017611ae8f167c5e716aad4b7680e`

```dockerfile
```

-	Layers:
	-	`sha256:0fd0fb4e581c468abde2999045c163e01f5f465436e7aa62ce734436862f9eac`  
		Last Modified: Wed, 24 Apr 2024 17:19:03 GMT  
		Size: 2.5 MB (2479288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38cc0fcc6c1dede08c15c91c4bc214763cd7fb9e515bc4f8b07ba05cdc9cd387`  
		Last Modified: Wed, 24 Apr 2024 17:19:03 GMT  
		Size: 37.7 KB (37728 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:bookworm` - linux; arm variant v7

```console
$ docker pull httpd@sha256:e49897ae28bb259a5a1b205a464098038e49ea2bb4985187e84baac47edda986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52738179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9fefb7a703a9d947d489c78f23271b57b138126899b22193b569f3d5ceb0d2`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063593c7931b25f55a01b9bb0f7156d7398c702900d7c6c5a10ac3cb9b111eeb`  
		Last Modified: Wed, 24 Apr 2024 16:30:49 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60dd6c2df475ede40fbebdd310c9770f5c85d86278fe66bcfb34015f9975b80`  
		Last Modified: Wed, 24 Apr 2024 16:30:50 GMT  
		Size: 3.3 MB (3286910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5afe70e80d3c8da2e79abd6e84a95f7bb9516fe79ffc1e06abcb55d3af394429`  
		Last Modified: Wed, 24 Apr 2024 16:30:51 GMT  
		Size: 24.7 MB (24710357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e43b819248841764c8eaee46258c16341b869c3cd10e29c5fe19a7ad57d3ea0`  
		Last Modified: Wed, 24 Apr 2024 16:30:50 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:bookworm` - unknown; unknown

```console
$ docker pull httpd@sha256:daa1d3562f002200d97c8042f5fb9e5cce9d3a91b979ab3bae79daa3f5a6f0a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2516068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beda48825ccb307edac52c5e75efd8fc86548bb74670c0558d03c6057104e328`

```dockerfile
```

-	Layers:
	-	`sha256:6656cffeaa9a2613f22ecf4356afe7a1fd612ffb7430d4e7e2ab9004ece5d051`  
		Last Modified: Wed, 24 Apr 2024 16:30:50 GMT  
		Size: 2.5 MB (2478340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1efca153bd1cf7ed5e26102ed35722aa4aec61d831e71818bba3175e03866560`  
		Last Modified: Wed, 24 Apr 2024 16:30:50 GMT  
		Size: 37.7 KB (37728 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:bookworm` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:b2670b51810a49855b0b59ed87dd064b3ec3ecf95e77d9dd6f6d13bab7467dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58997314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73acb239a8eb7a9ef5b6848a5b01bb26cc03d2262056705876bf7ac6ad781f02`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855b568ab02c3fee1362d51176f966517b1e03ca0c8efde55eddace90835f300`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c521cc2c4e8a439951003122cdab841fe1b1350db864e2cf9dea69298513f711`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 3.8 MB (3824128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c8bced82bd1d3557a49d39ea03bb8090bf3abc8154ab65388d9f9728f3ce02`  
		Last Modified: Thu, 25 Apr 2024 07:23:09 GMT  
		Size: 26.0 MB (25992782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae159c85a0b3662b8e9d58344f7da1b84836a7338c8ddf6b88360cea400929f`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:bookworm` - unknown; unknown

```console
$ docker pull httpd@sha256:307bc20593c828b3894250dd4e16b149c046b98c033453278fca94efd8bd0454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70026eb22d8bfc08dc60be7e7dcdce118be2390abe04aa90c7f27e6245767782`

```dockerfile
```

-	Layers:
	-	`sha256:77720a2aab607f8a1c40306899700597640ec9696bb65c714e6131dd481171b1`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 2.5 MB (2476229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd136e58015bf40bdc568f33b0d261e3140c11eee1769fbfb67f4ad2b93284f8`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 37.6 KB (37618 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:bookworm` - linux; 386

```console
$ docker pull httpd@sha256:34359f60b5aa39dfe4a6da81d319693f6ca6155e12e91b50e5d6da3ae7db89b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60223958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457768b202e686803b86961428bc138b1e4c6f0a08bec510257bba9b2d7e4486`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2941e842a389d5a4c34aa8e7f83e761d6a0deb0ed5c5bc01838c71d23659ac77`  
		Last Modified: Wed, 24 Apr 2024 04:57:41 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f800dd9ec1f906ac5c081169392c9dd10d32921d3e52e601c8c7ca7bcda3c600`  
		Last Modified: Wed, 24 Apr 2024 04:57:42 GMT  
		Size: 4.1 MB (4063511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494266189a0019f5cc3fec9ab5a55a1ea0fc3c8cc6a3ab1c1faeedbdc0fbaa5e`  
		Last Modified: Wed, 24 Apr 2024 04:57:42 GMT  
		Size: 26.0 MB (25996792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed1b4c9db903ab4981ddd506901a8ead9ae515c81f307dc7e52ed0256e73eec`  
		Last Modified: Wed, 24 Apr 2024 04:57:41 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:bookworm` - unknown; unknown

```console
$ docker pull httpd@sha256:928d95daa4cdcfd2c1395f60c62ed85d871764fdbfd6b1dbcf750c4f906d1eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2510705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8144c9b91841f94cfaea34892b458353406e2daa257e7e97e80ce41341381322`

```dockerfile
```

-	Layers:
	-	`sha256:637adc441596f6bc7ae557cdd4ef0de555b3e1b8aaa69a88adf26ea73e04a753`  
		Last Modified: Wed, 24 Apr 2024 04:57:42 GMT  
		Size: 2.5 MB (2472991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c57120021da5fb478f2b39b4540d36f1ba9bfa1efbe1c0616a07fe2a81d1e746`  
		Last Modified: Wed, 24 Apr 2024 04:57:41 GMT  
		Size: 37.7 KB (37714 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:bookworm` - linux; mips64le

```console
$ docker pull httpd@sha256:4512a76c673f11979d9f2ea96a56c59db662c5e8258c7128258245d18bb9292d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58678876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f7e1281eca6101e477c1cb3af32334cd551c69acc34839c3a8f8e3b3be6e80`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28233217e5e2c53a42bce8370d4462ed742672e46ec0e3acc021494964a6c4e`  
		Last Modified: Wed, 24 Apr 2024 23:51:19 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98af3a5736d8674d724399887f435760548973f8720121002efb9766f6892bb1`  
		Last Modified: Wed, 24 Apr 2024 23:51:20 GMT  
		Size: 3.4 MB (3373290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d3af7336bf3047ff58c8fc60fcce4943c107ecf04bb449d43849ce851d53aa`  
		Last Modified: Wed, 24 Apr 2024 23:51:22 GMT  
		Size: 26.2 MB (26160940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ed9c80633a9c8a938fb64f3eddb5677882265446491ddb3fce480647719cf5`  
		Last Modified: Wed, 24 Apr 2024 23:51:20 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:bookworm` - unknown; unknown

```console
$ docker pull httpd@sha256:b80ddb9178f5c7b1fb405cdad5a1ca2b55ae93147230041eb0b0e958dd6bd2b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f0b12a55ecb5a0fb2dc015ef1bebad8c2d781a197cd3a665b0b585ef134715`

```dockerfile
```

-	Layers:
	-	`sha256:e03a7d994013fb85dd187518a518143a7a11bc11a02be3fe21ac1bcc6c2bad8c`  
		Last Modified: Wed, 24 Apr 2024 23:51:20 GMT  
		Size: 37.5 KB (37480 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:bookworm` - linux; ppc64le

```console
$ docker pull httpd@sha256:f367b8c823d8e9650e4d0f3576cb4cb56931fb2a9abc5cf933fbc3e5e2d03eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64781656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5b1ab6010140721a568d9027ba17353616269ed57d0407e63a20a9db866d83`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8779f7411971984d8a264462c07b9383e455edbfa3945c3a7c3c0f0da6281405`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df41593893685df2f819e89678437a7190515d7cc02ecf4d3826f45e94594a6`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 4.3 MB (4329567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5fc79508ca1591a5607565a2c2fd383aaea639b5a8777f026f5767404f73eb`  
		Last Modified: Thu, 25 Apr 2024 03:19:08 GMT  
		Size: 27.3 MB (27310418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3bf3ad211e2e210d10318ae48cfccfdefd6adae953aa2a10ca77880dd921ac`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:bookworm` - unknown; unknown

```console
$ docker pull httpd@sha256:f5fdb59224d04f59d5f80ba98a242d519237e7fe401672f767a98c516fbb17b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2518193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3109624aa7219e37cb7b867bf5926f24b5e9b4eb3d6e31536b83f1751b0c42cf`

```dockerfile
```

-	Layers:
	-	`sha256:5553f9b984d60f0b17ff79178b8bd6943ed3c6a28b511fee1a71f4df9b281e63`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 2.5 MB (2480527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49e0858fd1c6faa9c04410e63c7d7bf0b572ae75294b281ff9ce3ba69ca201b3`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 37.7 KB (37666 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:bookworm` - linux; s390x

```console
$ docker pull httpd@sha256:ae3341db428440ab15b07058d2bab822247b8aa06035c19edea03f2a675e3b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56864928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed5070ae0d9687d8b499eae1be4caf30616eea45630f52af89bff9348d1cc474`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076f4d06a50ca8b3bcf6951ac8efa98b499598a608155af2bc4e4c0283e315e6`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8054bd786718ad21214203f377432a693d561157449486d1ea16ee3530d793e1`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 3.7 MB (3654647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c39e346caebedca77c0054fa938878774f458b3b88e05f7099ff4b70345256a`  
		Last Modified: Thu, 25 Apr 2024 02:28:32 GMT  
		Size: 25.7 MB (25697456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb3dcd087010aa65e19ef6e7ae889206220840a38cc7d973cd3b0e635895072`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:bookworm` - unknown; unknown

```console
$ docker pull httpd@sha256:779ecac6b7d7547b09bf644ce963543f48bac336bfe174dbd0583d7d06e3b0c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d2597d4c0c4788030bfe3a20a2ddf9842323ed2e486b682e1a863ae138ad89`

```dockerfile
```

-	Layers:
	-	`sha256:d42e15caceec6e5f15ccf873f46289eb1dc452e23ab53a076d905630a09e58e5`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 2.5 MB (2475763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28db97fd901916835b62fdb1cece860a44f5b2888ae52a2ea94026e65e136df5`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 37.6 KB (37600 bytes)  
		MIME: application/vnd.in-toto+json

## `httpd:latest`

```console
$ docker pull httpd@sha256:36c8c79f900108f0f09fd4148ad35ade57cba0dc19d13f3d15be24ce94e6a639
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
$ docker pull httpd@sha256:518e9447a236de47cc2fb4f2dbf06466b6cd5cf50f9951742f9a20af76e8118d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59185382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c2fc9e3d849b21a35b4c96f5ad8ec4dc9b73ca44c56537039e8c6f3054db0a`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851c52adaa9bf680b2eaa45164baa37665418fb02666fb36c268002edd853994`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d9f60535a61833df2e57cc08221031d3ae50f3955a6d6b0153214619d357fb`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 4.0 MB (4006988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943a2b3cf551375517593790b58407ffc7028b4b34bca6c0756b76708ea4b3ce`  
		Last Modified: Wed, 24 Apr 2024 04:57:24 GMT  
		Size: 26.0 MB (26027444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea83e81966d64f34a57ffcc118b75ad19bc9321f9809cf9b0df25548a2fa695e`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:latest` - unknown; unknown

```console
$ docker pull httpd@sha256:e31d2d75b317933ed59c3503fcfd00357545f4e60e60d87368674365eed990bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc7b98024523f6963a92b3a8edb71945171fff164f1da1e3bc9296d404a1da2`

```dockerfile
```

-	Layers:
	-	`sha256:1a0e348c51fd80864d852c8a1b3dbe89c1cbf088a8d4fe204b4f9a2106b65425`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 2.5 MB (2475971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea347276a3b2b4390cbb875d979ac18e828399022ce83785af6a6e19535cf238`  
		Last Modified: Wed, 24 Apr 2024 04:57:22 GMT  
		Size: 37.8 KB (37766 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:latest` - linux; arm variant v5

```console
$ docker pull httpd@sha256:6ac6acfaf36b492c8ee0271b5c1745e5d5173186838066fb55416fe1bad7f84e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55660337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594aaef0a91e898dfb26ab368782f59da9b9f69c9ad0d9a155208b535102d8e8`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:0140ab9be4171f94aae33901f189ffd8822ce6da4a052798883fd66d03b79be9 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:2c9444d4d8a989f4536a8afd8b41a3461ede5b15d490d87c3369b051095d7ae3`  
		Last Modified: Wed, 24 Apr 2024 03:56:28 GMT  
		Size: 26.9 MB (26910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfdcc496dd931564ad13b4c74e84a37bd3e8fe4d3e8eef76531c007b4918eb3`  
		Last Modified: Wed, 24 Apr 2024 17:19:02 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7797397d89aa986596ae17907e8812fb696c601b77e453f8cfff70c5282bb68`  
		Last Modified: Wed, 24 Apr 2024 17:19:03 GMT  
		Size: 3.5 MB (3511113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabda791a3820471d4af8b4b5339e9e5ade214d951432d16dcf09a30dfc07788`  
		Last Modified: Wed, 24 Apr 2024 17:19:04 GMT  
		Size: 25.2 MB (25238724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7b73f2fae9dae743b3751fc794fe838ccfee7359899fe2ef291db96f774025`  
		Last Modified: Wed, 24 Apr 2024 17:19:03 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:latest` - unknown; unknown

```console
$ docker pull httpd@sha256:0559103a0db87f5edf6e70a2fce9af410a68e8207c18d62b1a99fa7d6081320a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2517016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5eb9364b67ec513d9aa9dab74264a7e94017611ae8f167c5e716aad4b7680e`

```dockerfile
```

-	Layers:
	-	`sha256:0fd0fb4e581c468abde2999045c163e01f5f465436e7aa62ce734436862f9eac`  
		Last Modified: Wed, 24 Apr 2024 17:19:03 GMT  
		Size: 2.5 MB (2479288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38cc0fcc6c1dede08c15c91c4bc214763cd7fb9e515bc4f8b07ba05cdc9cd387`  
		Last Modified: Wed, 24 Apr 2024 17:19:03 GMT  
		Size: 37.7 KB (37728 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:latest` - linux; arm variant v7

```console
$ docker pull httpd@sha256:e49897ae28bb259a5a1b205a464098038e49ea2bb4985187e84baac47edda986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52738179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9fefb7a703a9d947d489c78f23271b57b138126899b22193b569f3d5ceb0d2`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063593c7931b25f55a01b9bb0f7156d7398c702900d7c6c5a10ac3cb9b111eeb`  
		Last Modified: Wed, 24 Apr 2024 16:30:49 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60dd6c2df475ede40fbebdd310c9770f5c85d86278fe66bcfb34015f9975b80`  
		Last Modified: Wed, 24 Apr 2024 16:30:50 GMT  
		Size: 3.3 MB (3286910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5afe70e80d3c8da2e79abd6e84a95f7bb9516fe79ffc1e06abcb55d3af394429`  
		Last Modified: Wed, 24 Apr 2024 16:30:51 GMT  
		Size: 24.7 MB (24710357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e43b819248841764c8eaee46258c16341b869c3cd10e29c5fe19a7ad57d3ea0`  
		Last Modified: Wed, 24 Apr 2024 16:30:50 GMT  
		Size: 292.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:latest` - unknown; unknown

```console
$ docker pull httpd@sha256:daa1d3562f002200d97c8042f5fb9e5cce9d3a91b979ab3bae79daa3f5a6f0a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2516068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beda48825ccb307edac52c5e75efd8fc86548bb74670c0558d03c6057104e328`

```dockerfile
```

-	Layers:
	-	`sha256:6656cffeaa9a2613f22ecf4356afe7a1fd612ffb7430d4e7e2ab9004ece5d051`  
		Last Modified: Wed, 24 Apr 2024 16:30:50 GMT  
		Size: 2.5 MB (2478340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1efca153bd1cf7ed5e26102ed35722aa4aec61d831e71818bba3175e03866560`  
		Last Modified: Wed, 24 Apr 2024 16:30:50 GMT  
		Size: 37.7 KB (37728 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:latest` - linux; arm64 variant v8

```console
$ docker pull httpd@sha256:b2670b51810a49855b0b59ed87dd064b3ec3ecf95e77d9dd6f6d13bab7467dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58997314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73acb239a8eb7a9ef5b6848a5b01bb26cc03d2262056705876bf7ac6ad781f02`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855b568ab02c3fee1362d51176f966517b1e03ca0c8efde55eddace90835f300`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c521cc2c4e8a439951003122cdab841fe1b1350db864e2cf9dea69298513f711`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 3.8 MB (3824128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c8bced82bd1d3557a49d39ea03bb8090bf3abc8154ab65388d9f9728f3ce02`  
		Last Modified: Thu, 25 Apr 2024 07:23:09 GMT  
		Size: 26.0 MB (25992782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae159c85a0b3662b8e9d58344f7da1b84836a7338c8ddf6b88360cea400929f`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:latest` - unknown; unknown

```console
$ docker pull httpd@sha256:307bc20593c828b3894250dd4e16b149c046b98c033453278fca94efd8bd0454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70026eb22d8bfc08dc60be7e7dcdce118be2390abe04aa90c7f27e6245767782`

```dockerfile
```

-	Layers:
	-	`sha256:77720a2aab607f8a1c40306899700597640ec9696bb65c714e6131dd481171b1`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 2.5 MB (2476229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd136e58015bf40bdc568f33b0d261e3140c11eee1769fbfb67f4ad2b93284f8`  
		Last Modified: Thu, 25 Apr 2024 07:23:08 GMT  
		Size: 37.6 KB (37618 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:latest` - linux; 386

```console
$ docker pull httpd@sha256:34359f60b5aa39dfe4a6da81d319693f6ca6155e12e91b50e5d6da3ae7db89b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60223958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457768b202e686803b86961428bc138b1e4c6f0a08bec510257bba9b2d7e4486`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2941e842a389d5a4c34aa8e7f83e761d6a0deb0ed5c5bc01838c71d23659ac77`  
		Last Modified: Wed, 24 Apr 2024 04:57:41 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f800dd9ec1f906ac5c081169392c9dd10d32921d3e52e601c8c7ca7bcda3c600`  
		Last Modified: Wed, 24 Apr 2024 04:57:42 GMT  
		Size: 4.1 MB (4063511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494266189a0019f5cc3fec9ab5a55a1ea0fc3c8cc6a3ab1c1faeedbdc0fbaa5e`  
		Last Modified: Wed, 24 Apr 2024 04:57:42 GMT  
		Size: 26.0 MB (25996792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed1b4c9db903ab4981ddd506901a8ead9ae515c81f307dc7e52ed0256e73eec`  
		Last Modified: Wed, 24 Apr 2024 04:57:41 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:latest` - unknown; unknown

```console
$ docker pull httpd@sha256:928d95daa4cdcfd2c1395f60c62ed85d871764fdbfd6b1dbcf750c4f906d1eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2510705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8144c9b91841f94cfaea34892b458353406e2daa257e7e97e80ce41341381322`

```dockerfile
```

-	Layers:
	-	`sha256:637adc441596f6bc7ae557cdd4ef0de555b3e1b8aaa69a88adf26ea73e04a753`  
		Last Modified: Wed, 24 Apr 2024 04:57:42 GMT  
		Size: 2.5 MB (2472991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c57120021da5fb478f2b39b4540d36f1ba9bfa1efbe1c0616a07fe2a81d1e746`  
		Last Modified: Wed, 24 Apr 2024 04:57:41 GMT  
		Size: 37.7 KB (37714 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:latest` - linux; mips64le

```console
$ docker pull httpd@sha256:4512a76c673f11979d9f2ea96a56c59db662c5e8258c7128258245d18bb9292d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.7 MB (58678876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f7e1281eca6101e477c1cb3af32334cd551c69acc34839c3a8f8e3b3be6e80`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:a3e63beab80160854bfc2d48f69e7c70a9542cdfaf3c5b50f1d6248a998b75ae in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:af25825be002e7bdd52bf28c2fbef5bae0ba9fcef8118e5591a874e7a70b2a62`  
		Last Modified: Wed, 24 Apr 2024 03:25:20 GMT  
		Size: 29.1 MB (29144174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28233217e5e2c53a42bce8370d4462ed742672e46ec0e3acc021494964a6c4e`  
		Last Modified: Wed, 24 Apr 2024 23:51:19 GMT  
		Size: 146.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98af3a5736d8674d724399887f435760548973f8720121002efb9766f6892bb1`  
		Last Modified: Wed, 24 Apr 2024 23:51:20 GMT  
		Size: 3.4 MB (3373290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d3af7336bf3047ff58c8fc60fcce4943c107ecf04bb449d43849ce851d53aa`  
		Last Modified: Wed, 24 Apr 2024 23:51:22 GMT  
		Size: 26.2 MB (26160940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ed9c80633a9c8a938fb64f3eddb5677882265446491ddb3fce480647719cf5`  
		Last Modified: Wed, 24 Apr 2024 23:51:20 GMT  
		Size: 294.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:latest` - unknown; unknown

```console
$ docker pull httpd@sha256:b80ddb9178f5c7b1fb405cdad5a1ca2b55ae93147230041eb0b0e958dd6bd2b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 KB (37480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f0b12a55ecb5a0fb2dc015ef1bebad8c2d781a197cd3a665b0b585ef134715`

```dockerfile
```

-	Layers:
	-	`sha256:e03a7d994013fb85dd187518a518143a7a11bc11a02be3fe21ac1bcc6c2bad8c`  
		Last Modified: Wed, 24 Apr 2024 23:51:20 GMT  
		Size: 37.5 KB (37480 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:latest` - linux; ppc64le

```console
$ docker pull httpd@sha256:f367b8c823d8e9650e4d0f3576cb4cb56931fb2a9abc5cf933fbc3e5e2d03eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64781656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d5b1ab6010140721a568d9027ba17353616269ed57d0407e63a20a9db866d83`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8779f7411971984d8a264462c07b9383e455edbfa3945c3a7c3c0f0da6281405`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 145.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df41593893685df2f819e89678437a7190515d7cc02ecf4d3826f45e94594a6`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 4.3 MB (4329567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5fc79508ca1591a5607565a2c2fd383aaea639b5a8777f026f5767404f73eb`  
		Last Modified: Thu, 25 Apr 2024 03:19:08 GMT  
		Size: 27.3 MB (27310418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3bf3ad211e2e210d10318ae48cfccfdefd6adae953aa2a10ca77880dd921ac`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 293.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:latest` - unknown; unknown

```console
$ docker pull httpd@sha256:f5fdb59224d04f59d5f80ba98a242d519237e7fe401672f767a98c516fbb17b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2518193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3109624aa7219e37cb7b867bf5926f24b5e9b4eb3d6e31536b83f1751b0c42cf`

```dockerfile
```

-	Layers:
	-	`sha256:5553f9b984d60f0b17ff79178b8bd6943ed3c6a28b511fee1a71f4df9b281e63`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 2.5 MB (2480527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49e0858fd1c6faa9c04410e63c7d7bf0b572ae75294b281ff9ce3ba69ca201b3`  
		Last Modified: Thu, 25 Apr 2024 03:19:07 GMT  
		Size: 37.7 KB (37666 bytes)  
		MIME: application/vnd.in-toto+json

### `httpd:latest` - linux; s390x

```console
$ docker pull httpd@sha256:ae3341db428440ab15b07058d2bab822247b8aa06035c19edea03f2a675e3b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56864928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed5070ae0d9687d8b499eae1be4caf30616eea45630f52af89bff9348d1cc474`
-	Default Command: `["httpd-foreground"]`

```dockerfile
# Fri, 05 Apr 2024 21:49:16 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PREFIX=/usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
ENV PATH=/usr/local/apache2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:49:16 GMT
RUN mkdir -p "$HTTPD_PREFIX" 	&& chown www-data:www-data "$HTTPD_PREFIX" # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
WORKDIR /usr/local/apache2
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libaprutil1-ldap 		libldap-common 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_VERSION=2.4.59
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_SHA256=ec51501ec480284ff52f637258135d333230a7d229c3afa6f6c2f9040e321323
# Fri, 05 Apr 2024 21:49:16 GMT
ENV HTTPD_PATCHES=
# Fri, 05 Apr 2024 21:49:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		dpkg-dev 		gcc 		gnupg 		libapr1-dev 		libaprutil1-dev 		libbrotli-dev 		libcurl4-openssl-dev 		libjansson-dev 		liblua5.2-dev 		libnghttp2-dev 		libpcre3-dev 		libssl-dev 		libxml2-dev 		make 		patch 		wget 		zlib1g-dev 	; 	rm -r /var/lib/apt/lists/*; 		ddist() { 		local f="$1"; shift; 		local distFile="$1"; shift; 		local success=; 		local distUrl=; 		for distUrl in 			https://dlcdn.apache.org/ 			https://archive.apache.org/dist/ 		; do 			if wget -O "$f" "$distUrl$distFile" && [ -s "$f" ]; then 				success=1; 				break; 			fi; 		done; 		[ -n "$success" ]; 	}; 		ddist 'httpd.tar.bz2' "httpd/httpd-$HTTPD_VERSION.tar.bz2"; 	echo "$HTTPD_SHA256 *httpd.tar.bz2" | sha256sum -c -; 		ddist 'httpd.tar.bz2.asc' "httpd/httpd-$HTTPD_VERSION.tar.bz2.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in 		DE29FB3971E71543FD2DC049508EAEC5302DA568 		13155B0E9E634F42BF6C163FDDBA64BA2C312D2F 		8B39757B1D8A994DF2433ED58B3A601F08C975E5 		31EE1A81B8D066548156D37B7D6DBFD1F08E012A 		A10208FEC3152DD7C0C9B59B361522D782AB7BD1 		3DE024AFDA7A4B15CB6C14410F81AA8AB0D5F771 		EB138C6AF0FC691001B16D93344A844D751D7F27 		CBA5A7C21EC143314C41393E5B968010E04F9A89 		3C016F2B764621BB549C66B516A96495E2226795 		937FB3994A242BA9BF49E93021454AF0CC8B0F7E 		EAD1359A4C0F2D37472AAF28F55DF0293A4E7AC9 		4C1EADADB4EF5007579C919C6635B6C0DE885DD3 		01E475360FCCF1D0F24B9D145D414AE1E005C9CB 		92CCEF0AA7DD46AC3A0F498BCA6939748103A37E 		D395C7573A68B9796D38C258153FA0CD75A67692 		FA39B617B61493FD283503E7EED1EA392261D073 		984FB3350C1D5C7A3282255BB31B213D208F5064 		FE7A49DAA875E890B4167F76CCB2EB46E76CF6D0 		39F6691A0ECF0C50E8BB849CF78875F642721F00 		29A2BA848177B73878277FA475CAA2A3F39B3750 		120A8667241AEDD4A78B46104C042818311A3DE5 		453510BDA6C5855624E009236D0BC73A40581837 		0DE5C55C6BF3B2352DABB89E13249B4FEC88A0BF 		7CDBED100806552182F98844E8E7E00B4DAA1988 		A8BA9617EF3BCCAC3B29B869EDB105896F9522D8 		3E6AC004854F3A7F03566B592FF06894E55B0D0E 		5B5181C2C0AB13E59DA3F7A3EC582EB639FF092C 		A93D62ECC3C8EA12DB220EC934EA76E6791485A8 		65B2D44FE74BD5E3DE3AC3F082781DE46D5954FA 		8935926745E1CE7E3ED748F6EC99EE267EB5F61A 		E3480043595621FE56105F112AB12A7ADC55C003 		93525CFCF6FDFFB3FD9700DD5A4B10AE43B56A27 		C55AB7B9139EB2263CD1AABC19B033D1760C227B 		26F51EF9A82F4ACB43F1903ED377C9E7D1944C66 	; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify httpd.tar.bz2.asc httpd.tar.bz2; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" httpd.tar.bz2.asc; 		mkdir -p src; 	tar -xf httpd.tar.bz2 -C src --strip-components=1; 	rm httpd.tar.bz2; 	cd src; 		patches() { 		while [ "$#" -gt 0 ]; do 			local patchFile="$1"; shift; 			local patchSha256="$1"; shift; 			ddist "$patchFile" "httpd/patches/apply_to_$HTTPD_VERSION/$patchFile"; 			echo "$patchSha256 *$patchFile" | sha256sum -c -; 			patch -p0 < "$patchFile"; 			rm -f "$patchFile"; 		done; 	}; 	patches $HTTPD_PATCHES; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	CPPFLAGS="$(dpkg-buildflags --get CPPFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	./configure 		--build="$gnuArch" 		--prefix="$HTTPD_PREFIX" 		--enable-mods-shared=reallyall 		--enable-mpms-shared=all 		--enable-pie 		CFLAGS="-pipe $CFLAGS" 		CPPFLAGS="$CPPFLAGS" 		LDFLAGS="-Wl,--as-needed $LDFLAGS" 	; 	make -j "$(nproc)"; 	make install; 		cd ..; 	rm -r src man manual; 		sed -ri 		-e 's!^(\s*CustomLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*ErrorLog)\s+\S+!\1 /proc/self/fd/2!g' 		-e 's!^(\s*TransferLog)\s+\S+!\1 /proc/self/fd/1!g' 		-e 's!^(\s*User)\s+daemon\s*$!\1 www-data!g' 		-e 's!^(\s*Group)\s+daemon\s*$!\1 www-data!g' 		"$HTTPD_PREFIX/conf/httpd.conf" 		"$HTTPD_PREFIX/conf/extra/httpd-ssl.conf" 	; 	grep -E '^\s*User www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 	grep -E '^\s*Group www-data$' "$HTTPD_PREFIX/conf/httpd.conf"; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		httpd -v # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 05 Apr 2024 21:49:16 GMT
COPY httpd-foreground /usr/local/bin/ # buildkit
# Fri, 05 Apr 2024 21:49:16 GMT
EXPOSE map[80/tcp:{}]
# Fri, 05 Apr 2024 21:49:16 GMT
CMD ["httpd-foreground"]
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076f4d06a50ca8b3bcf6951ac8efa98b499598a608155af2bc4e4c0283e315e6`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 147.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8054bd786718ad21214203f377432a693d561157449486d1ea16ee3530d793e1`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 3.7 MB (3654647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c39e346caebedca77c0054fa938878774f458b3b88e05f7099ff4b70345256a`  
		Last Modified: Thu, 25 Apr 2024 02:28:32 GMT  
		Size: 25.7 MB (25697456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb3dcd087010aa65e19ef6e7ae889206220840a38cc7d973cd3b0e635895072`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `httpd:latest` - unknown; unknown

```console
$ docker pull httpd@sha256:779ecac6b7d7547b09bf644ce963543f48bac336bfe174dbd0583d7d06e3b0c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d2597d4c0c4788030bfe3a20a2ddf9842323ed2e486b682e1a863ae138ad89`

```dockerfile
```

-	Layers:
	-	`sha256:d42e15caceec6e5f15ccf873f46289eb1dc452e23ab53a076d905630a09e58e5`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 2.5 MB (2475763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28db97fd901916835b62fdb1cece860a44f5b2888ae52a2ea94026e65e136df5`  
		Last Modified: Thu, 25 Apr 2024 02:28:31 GMT  
		Size: 37.6 KB (37600 bytes)  
		MIME: application/vnd.in-toto+json
