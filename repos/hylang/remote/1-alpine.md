## `hylang:1-alpine`

```console
$ docker pull hylang@sha256:d70abbb7e675f685768aebcba57786a3de6f8f6f18556c150492956d7070ef14
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

### `hylang:1-alpine` - linux; amd64

```console
$ docker pull hylang@sha256:45ec95925cbb9d59187e780886490411fbcf3ee111f8cdcfab00efd7327ca4d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22281538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec0fc2a0182aad5ed8f8b4b6a180d8002a4d37c7300e795f53e248a67eca6ea`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 12:35:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jan 2025 12:35:53 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Jan 2025 12:35:53 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 17 Jan 2025 12:35:53 GMT
ENV PYTHON_VERSION=3.13.1
# Fri, 17 Jan 2025 12:35:53 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Fri, 17 Jan 2025 12:35:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	test "$gnuArch" != 'i686-linux-gnu' && EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Jan 2025 12:35:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Jan 2025 12:35:53 GMT
CMD ["python3"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HY_VERSION=1.0.0
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 22 Jan 2025 19:41:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7486ee1cd0b33ed93151ce1d3f73254a0987b484773adb31f37fe42bad78ba63`  
		Last Modified: Fri, 24 Jan 2025 19:35:39 GMT  
		Size: 458.8 KB (458769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c174cb6c8cb4276eaff5e9ebfb56eb7124be68c8fcb4518cb5eb6b18245cf5`  
		Last Modified: Fri, 24 Jan 2025 19:35:39 GMT  
		Size: 12.5 MB (12489203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2109cea89a773ab9365659a6a63a1b7d8be1f7be6031112a429533bd7ba07f68`  
		Last Modified: Fri, 24 Jan 2025 19:35:38 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f1e1e89a9da40ed07cc15a138e87a91fc5e51ad1f02b83c42b168d5a792cc4`  
		Last Modified: Fri, 24 Jan 2025 20:08:09 GMT  
		Size: 5.7 MB (5691599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:f5030930ff120a19627152f3c8c3521728a31019e8645ca99ee0c5cdf2c138c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.3 KB (643264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf5c9c3ad2b748bbc2f985e956f66a18230a93a4d55ad4c7c55ee12f0829d241`

```dockerfile
```

-	Layers:
	-	`sha256:ab216f7da2620cd99145fff9046677ea6959517ef6befd340a1d25f9a8ab0eee`  
		Last Modified: Fri, 24 Jan 2025 20:08:09 GMT  
		Size: 631.5 KB (631474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aca0e4d7bc52412b2b867165ca3dc7139e206ed8b8586cfee8357f07ccf4dc06`  
		Last Modified: Fri, 24 Jan 2025 20:08:09 GMT  
		Size: 11.8 KB (11790 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine` - linux; arm variant v6

```console
$ docker pull hylang@sha256:757b728e592b1a2f4f72e15e30dfa9d3f445373cf47afd699c4af82e78a1f1d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21594175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2db7b37017621b09f8390bd82d7e798af70cabc1500fe45bd6713fa8eff914`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 05 Dec 2024 13:19:52 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.13.1
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["python3"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HY_VERSION=1.0.0
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 22 Jan 2025 19:41:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2dec769123af1f5a0c91c72bfe4e9f0159b1fda485ecb156007cf295004a14`  
		Last Modified: Thu, 09 Jan 2025 07:15:26 GMT  
		Size: 459.6 KB (459577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f5bf6c509711888714b44725ddb8314a7cd0c8616f44120cba68ab338a871d`  
		Last Modified: Thu, 09 Jan 2025 07:33:09 GMT  
		Size: 12.1 MB (12078525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85029bcce07b09c3bca5100f3b3479f04aec178cc28f3eeeed5cbae50553fa18`  
		Last Modified: Thu, 09 Jan 2025 07:33:08 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b2cfdfb33b77be2b012415707248972589c791cb0e47d65a1ad50ac09b075e`  
		Last Modified: Thu, 23 Jan 2025 01:39:53 GMT  
		Size: 5.7 MB (5691944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:a1e9020faef47b567e0e7a1fda854708dcd475acdf78da34e8d1bb18954ee7ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 KB (11747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce852898bd0e722574cd4a73841795effc7c802d64f9812662f4c7f34f0b98f9`

```dockerfile
```

-	Layers:
	-	`sha256:1d5e87689095e06c915b6392053613ab023cf9ae588c3a289e61a705303e5e43`  
		Last Modified: Thu, 23 Jan 2025 01:39:53 GMT  
		Size: 11.7 KB (11747 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine` - linux; arm variant v7

```console
$ docker pull hylang@sha256:d267b665dc31ec4e054c54f8a87a2d55f72d27d7fc6537868077681ba204dfde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 MB (20993036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17a2b7782d6a0fca623db70ffb18261b577d0056de47eba3d09669a413cfa0a`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 05 Dec 2024 13:19:52 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.13.1
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["python3"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HY_VERSION=1.0.0
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 22 Jan 2025 19:41:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52fed4f44c67cbc108822cb67f010dfbf3a64ce27abbeff6c7c380b97b0a0f4`  
		Last Modified: Thu, 09 Jan 2025 07:50:42 GMT  
		Size: 458.7 KB (458718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b984a709735022d801995ac68ec89637537057a51258b42378ec488745c7929d`  
		Last Modified: Thu, 09 Jan 2025 08:05:32 GMT  
		Size: 11.7 MB (11745227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c170c2be395a93e07d23b21d9e135b4c56370dc1d81ccf1d79ae8dfb9a4cb0`  
		Last Modified: Thu, 09 Jan 2025 08:05:32 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e040931ec950ac77c6163c9fad58e461a1536c8c29bed062acdd8d067fbac98`  
		Last Modified: Thu, 23 Jan 2025 05:10:05 GMT  
		Size: 5.7 MB (5691730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:80420e08932675f7fc535f968541664028f89a258c5d516b2a09cfba0a8c9774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **646.4 KB (646381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc5710e8aa99a9968dd4f1611fc28255682fca4fa5b592443de3cd74eca9d8c`

```dockerfile
```

-	Layers:
	-	`sha256:6abff43cabeb230d498afc529fe353efb44ae5dd5806c9043b0757ef1dde3297`  
		Last Modified: Thu, 23 Jan 2025 05:10:09 GMT  
		Size: 634.4 KB (634419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b094bbfe7608e90da1c20c5b4fb159a2d6fef943cbd42609b4eaf1a88270d07d`  
		Last Modified: Thu, 23 Jan 2025 05:10:08 GMT  
		Size: 12.0 KB (11962 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:787d769ffa115472ad88a9fef54afa7e56a2222b1037f7fb92dd1403e1524dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22651132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:783fe63b1192ce18d04c343fc2cf9f5a1bffe2f2d3523be93ac50dfdc5bbcee2`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 12:35:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jan 2025 12:35:53 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Jan 2025 12:35:53 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 17 Jan 2025 12:35:53 GMT
ENV PYTHON_VERSION=3.13.1
# Fri, 17 Jan 2025 12:35:53 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Fri, 17 Jan 2025 12:35:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	test "$gnuArch" != 'i686-linux-gnu' && EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Jan 2025 12:35:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Jan 2025 12:35:53 GMT
CMD ["python3"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HY_VERSION=1.0.0
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 22 Jan 2025 19:41:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844e1cf46642efec467c0d66e3ca2031dea03979799a64785bcb140b5fce2a70`  
		Last Modified: Thu, 09 Jan 2025 04:15:13 GMT  
		Size: 460.8 KB (460837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7104bcbebe4088951d616b089d9b407ad30bbeb110f8d8ee4447df58e33d5f`  
		Last Modified: Fri, 24 Jan 2025 21:39:06 GMT  
		Size: 12.5 MB (12506157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646ab5f7ca64b565bae4a1b4a4180f0cbdf3ca0dd983cdabf2f6e2ca042ddc9d`  
		Last Modified: Fri, 24 Jan 2025 21:39:06 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9996afa7973b70121141531d27cc5ce41c2fe8cf3e463f5f5262cda8b4bfec93`  
		Last Modified: Fri, 24 Jan 2025 23:10:51 GMT  
		Size: 5.7 MB (5691530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:0e25423f86370eb0dc15052565790ac6ad7f650d19ec6c5162ddc9fdcee21b60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.7 KB (643712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e20825e6d4b7ed82910d6009cf41ec53fad7fbeaf02ada42e5b6712aa77995`

```dockerfile
```

-	Layers:
	-	`sha256:b3d3bf923f7582844ebdc7003db60ab6bd6a96b74387726049a0e52fc298fb49`  
		Last Modified: Fri, 24 Jan 2025 23:10:51 GMT  
		Size: 631.7 KB (631674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f171db9630f62c6eed43129bfd64bb2ca4bcb25ec6eda99d26ca445b08854e6a`  
		Last Modified: Fri, 24 Jan 2025 23:10:50 GMT  
		Size: 12.0 KB (12038 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine` - linux; 386

```console
$ docker pull hylang@sha256:8d855b512b119fb21b890d2396cac9d252478389ab766d5f73cfbd8692e7d9c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 MB (22092093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913970e672fc46fe8a0a4e7b592b9c3db346e5089611a4a292d6b678a92e8941`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 12:35:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Jan 2025 12:35:53 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Jan 2025 12:35:53 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 17 Jan 2025 12:35:53 GMT
ENV PYTHON_VERSION=3.13.1
# Fri, 17 Jan 2025 12:35:53 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Fri, 17 Jan 2025 12:35:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	test "$gnuArch" != 'i686-linux-gnu' && EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Jan 2025 12:35:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Jan 2025 12:35:53 GMT
CMD ["python3"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HY_VERSION=1.0.0
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 22 Jan 2025 19:41:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d2e7f61ec036a94d47f09a2b2a29df6168d9300f2d23ef1a976ebeda83bcbf`  
		Last Modified: Fri, 24 Jan 2025 19:36:00 GMT  
		Size: 459.2 KB (459183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1f343b1934a4de6b058fb8cc7d3187472f5d3debbf43434f18f285d726dbac`  
		Last Modified: Fri, 24 Jan 2025 19:36:00 GMT  
		Size: 12.5 MB (12477909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2f53107d59fc5f07b5dd9b7a45a294483e9744a821f829d340f022e6f864c2`  
		Last Modified: Fri, 24 Jan 2025 19:36:00 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d7ed221b959408e3088218079e28d0ada3c2ddb92c3170031d22e98d443886`  
		Last Modified: Fri, 24 Jan 2025 20:08:06 GMT  
		Size: 5.7 MB (5691626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:aac18b003bff76d4b7576b60ef8f0bcfc5c7c918b5a1fc5884688219e7b679f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.1 KB (643087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c08b2f821ab0962a4060cfd9ec12132f34f10547472c19d043840b5edfe47126`

```dockerfile
```

-	Layers:
	-	`sha256:687a7fa03732123869745b1895ec67646925f40a9df4e878dc753e815e1006d4`  
		Last Modified: Fri, 24 Jan 2025 20:08:05 GMT  
		Size: 631.4 KB (631389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee884176ae9518983c0215b42c7aae979ae83cbe7421347198f42b66e352f3b2`  
		Last Modified: Fri, 24 Jan 2025 20:08:05 GMT  
		Size: 11.7 KB (11698 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine` - linux; ppc64le

```console
$ docker pull hylang@sha256:bd219522eee90a7df08b59cbe6bb4351363c36e0b45d5d9fa38ae5247c937d60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22885853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ba71d37ae4271d48ba62c10d7618c6cf2140a99e77a090b908be3537fb285ba`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 05 Dec 2024 13:19:52 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.13.1
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["python3"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HY_VERSION=1.0.0
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 22 Jan 2025 19:41:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78682beede19196d68ea8312fad482211dddc22810f3e520b446a72a6396fc56`  
		Last Modified: Wed, 08 Jan 2025 23:06:50 GMT  
		Size: 461.3 KB (461293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61127848696fe1469fc229d4a8d9539ec5f12604118349c58cb6369079b3ce85`  
		Last Modified: Wed, 08 Jan 2025 23:23:34 GMT  
		Size: 13.2 MB (13158928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d63bf5f02ed4160f84a317b8c72d34a9a3c1d45b3a7eac06f69fddd2fead07`  
		Last Modified: Wed, 08 Jan 2025 23:23:33 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda2d99c4e0132275e154f378ed86ceedfc5f2ca31b38f82439424bea7190bcb`  
		Last Modified: Thu, 23 Jan 2025 01:29:40 GMT  
		Size: 5.7 MB (5691781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:d06dd84940303fd1f2a10e38b4c897be13567fc8aecc1d63ed067673d52e37df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.5 KB (641535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:742133cb5b4831a41c8045455859ada1114e8d8b78990b2daa792bc79f2bd2ec`

```dockerfile
```

-	Layers:
	-	`sha256:e1f0409f0ac403161c6c14287992c418230ada1b1ce6a740f19fbe790f545d87`  
		Last Modified: Thu, 23 Jan 2025 01:29:40 GMT  
		Size: 629.6 KB (629629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:003fd035be740ae6cdd6d2b01f31148cadd9da33be052496c9bed89ca639ca8f`  
		Last Modified: Thu, 23 Jan 2025 01:29:40 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-alpine` - linux; s390x

```console
$ docker pull hylang@sha256:476b446f54a458c1365de1bb16b0d59660eba2e4687e7ed6bf03948480a9fdd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22520165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f42a94f1994d71edc3fcd51df89c363425152b0514831f4f91aec02131ccbb`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 05 Dec 2024 13:19:52 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.13.1
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["python3"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HY_VERSION=1.0.0
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 22 Jan 2025 19:41:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ba53597a2004ea77723ad280fa3859e5c80d6ba286dd12179ceb5e3e7dc776`  
		Last Modified: Thu, 09 Jan 2025 05:24:30 GMT  
		Size: 459.7 KB (459691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61281a81b7ccd9118b5444aa7d5106c17f2f79abd7a99a0c75e1b77544d2e211`  
		Last Modified: Thu, 09 Jan 2025 05:39:18 GMT  
		Size: 12.9 MB (12901664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4be1fb9cb7b302c9d75dbfacbbfce53ec1a585f4cfffea4db5a45b824583d8`  
		Last Modified: Thu, 09 Jan 2025 05:39:17 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4326d533dc35e1523b5bcb809f78603047391c9d700afd16588d547110c2d75a`  
		Last Modified: Thu, 23 Jan 2025 03:02:29 GMT  
		Size: 5.7 MB (5691693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:1e2fdaf2eb836c631584e48a6f80816d8f45fe340a6367a71e83e5afb873906a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.3 KB (641313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b1217cd912bbdf59fd7c2c8b52a5c9a00786c28ee4660ded823002ccddf0086`

```dockerfile
```

-	Layers:
	-	`sha256:dc05fcfdb9a7cb148470b06b721c0d098397655aed1053653466a1cc063e2932`  
		Last Modified: Thu, 23 Jan 2025 03:02:28 GMT  
		Size: 629.5 KB (629523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a419569a9f1e881be563f009c9381f579b3cf8b46f9795b323eafb79f5e49f07`  
		Last Modified: Thu, 23 Jan 2025 03:02:28 GMT  
		Size: 11.8 KB (11790 bytes)  
		MIME: application/vnd.in-toto+json
