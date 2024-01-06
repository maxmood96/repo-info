## `hylang:python3.8-alpine3.19`

```console
$ docker pull hylang@sha256:998fbbc69e9a509001579096de4c53888f3f2a93d5a3723c8defaf22ba3d09b5
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

### `hylang:python3.8-alpine3.19` - linux; amd64

```console
$ docker pull hylang@sha256:a361a065033669c3aaab1fad5c16665c8fc0e954482a90a1bddc08b07d81a42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (24035495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b479f8e132a3cff46d63c39f4108e75aad307617f8f33d30f6511554c0d3d7cc`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Dec 2023 09:55:38 GMT
ENV LANG=C.UTF-8
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_VERSION=3.8.18
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cda88cd45dc00d3349d343b46e92f0d55daa059d276f3ecf860c174bbedf81`  
		Last Modified: Sat, 09 Dec 2023 01:44:02 GMT  
		Size: 621.7 KB (621692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588652b0a3bf66db4325dd3ddc19f90a42cf13c16e34e8c69999223afa60de20`  
		Last Modified: Sat, 09 Dec 2023 01:47:12 GMT  
		Size: 13.4 MB (13429913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a01b0f6dede8a9183367ce58fa1c2c7e550dc0026039f43e6be63da63b1312f0`  
		Last Modified: Sat, 09 Dec 2023 01:47:10 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668a2d5b038620e9d1461af567bf8b7ad9b481b4e03135fc6b2c0e4c053f6b63`  
		Last Modified: Sat, 09 Dec 2023 01:47:11 GMT  
		Size: 2.9 MB (2851658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5b25e47a852b21216597a97a226686f34c44814419509325f197d83e5b443e`  
		Last Modified: Fri, 05 Jan 2024 23:55:44 GMT  
		Size: 3.7 MB (3723512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:8e3cd7ee8e7e7fd689e47a0e6f4e4f7d3fb648267a2ef3a2090315f4d6e7942f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **875.0 KB (874966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12587cd12bdd7fcb7665af49042d9e88bc415cc1418a593f9ebc447704a0808a`

```dockerfile
```

-	Layers:
	-	`sha256:2f93dccd5ab6f9961ca127a77fa0dd554dbb3dfbc3d931440a75b9959401f6ce`  
		Last Modified: Fri, 05 Jan 2024 23:55:44 GMT  
		Size: 864.5 KB (864534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab121abee6cb77065957bf7bef8c3ac08ec0d765d3c9883e85edd9f9a74a5aa1`  
		Last Modified: Fri, 05 Jan 2024 23:55:44 GMT  
		Size: 10.4 KB (10432 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.19` - linux; arm variant v6

```console
$ docker pull hylang@sha256:98fec504869c630d80d38a7a65b16368a4f00ba45c5398edeefe6a25373c39d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23439002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c65dbe811e916e930453206a605e93ceefb6cc38d7e418417157ad7a71031711`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Dec 2023 09:55:38 GMT
ENV LANG=C.UTF-8
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_VERSION=3.8.18
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
CMD ["python3"]
# Tue, 12 Dec 2023 23:44:12 GMT
ENV HY_VERSION=0.27.0
# Tue, 12 Dec 2023 23:44:12 GMT
ENV HYRULE_VERSION=0.4.0
# Tue, 12 Dec 2023 23:44:12 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 12 Dec 2023 23:44:12 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42929f9f4a31e1902cdf6c4235d3aa6d6778d097653c2630af687f5e8e809d3`  
		Last Modified: Fri, 08 Dec 2023 23:46:53 GMT  
		Size: 622.9 KB (622903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f5c62bb90705e79607999bb755f524af0cf36bd6593aeba5871846be098d7e`  
		Last Modified: Fri, 08 Dec 2023 23:48:38 GMT  
		Size: 13.1 MB (13100120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e51f68601b070c0effe63888e6bbbdda621823270cc973f75c296f165fdcea65`  
		Last Modified: Fri, 08 Dec 2023 23:48:35 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da85e7cadf4b95f77a557be7b6c1d85b27414c26e1749087550d25f645e9a8a7`  
		Last Modified: Fri, 08 Dec 2023 23:48:37 GMT  
		Size: 2.9 MB (2851689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb2742cb92252fbbb00836030f5a2d1429b6d3bd3aa00267399f6103276bd71`  
		Last Modified: Wed, 20 Dec 2023 21:56:54 GMT  
		Size: 3.7 MB (3698904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:a6ce37b552e64fe23d39742051bb603dd364f1f2b77ac0a2c5a3b67340f67d4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 KB (10319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9abfafdfc3d0a6f398ebbd4799bd5a995f864480be70a4531e0692fea275174f`

```dockerfile
```

-	Layers:
	-	`sha256:88bef652b95e54f8efe111e3f264229bc800297c436af38b4cb7f805100426cc`  
		Last Modified: Wed, 20 Dec 2023 21:56:53 GMT  
		Size: 10.3 KB (10319 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.19` - linux; arm variant v7

```console
$ docker pull hylang@sha256:efeb626d88a07bccffb1dfd732047624c6cddb39acdc5bb165eae794ba908986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22830840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0065290114213d344b3ed89db974414a6faeb5df4ebf3a95e6285e46f08e7523`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Dec 2023 09:55:38 GMT
ENV LANG=C.UTF-8
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_VERSION=3.8.18
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0196bec49f2a69fdcb2616601ab1de1723d29440f95d478ab8ca13b3fa59c6`  
		Last Modified: Sat, 09 Dec 2023 02:18:07 GMT  
		Size: 621.9 KB (621916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c80ea8e00e537f80edde08d4b40df67d17e631ca4afe44c8e89e3babf7fea49a`  
		Last Modified: Sat, 09 Dec 2023 02:21:14 GMT  
		Size: 12.7 MB (12714347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc548bcece79b41aaee84d415ca0aa430391fb1f634d0986fd9eb5a4ce393926`  
		Last Modified: Sat, 09 Dec 2023 02:21:12 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63b4f7bf47090c0ad5b980555b9b0455575746dd75751359c0d17afc6fcf969`  
		Last Modified: Sat, 09 Dec 2023 02:21:13 GMT  
		Size: 2.9 MB (2851687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c61aafc7094cf47d9a16baab0c1a650cde8019f56ab41e8e38648c85071607ca`  
		Last Modified: Sat, 06 Jan 2024 04:59:52 GMT  
		Size: 3.7 MB (3723946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:f59c51f9a4d742caaf182131a5ba50f3170045a95c42a47e429e23f18d323c42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **876.8 KB (876790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5213d6495787aeb5205904e032323905da764599bf060d3d9c37da4532a90b5e`

```dockerfile
```

-	Layers:
	-	`sha256:c5b802efab9822b95b57e1ce5b7bd1376e526b055802caeb4b508a6fcd07beee`  
		Last Modified: Sat, 06 Jan 2024 04:59:52 GMT  
		Size: 867.1 KB (867074 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eab5d3818d8e1550021a9afea1146bd25caa73ae5a56c70bcd7044af78dfbda0`  
		Last Modified: Sat, 06 Jan 2024 04:59:51 GMT  
		Size: 9.7 KB (9716 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:5d03b64766bfac3e9662994654399b8c3ed5bc69422570f7d35147145e7194e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24066467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b22bb14b6a8764763ffadb7d97e39bcdb2f01190ae7248ee82d8707fcc3d531b`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Dec 2023 09:55:38 GMT
ENV LANG=C.UTF-8
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_VERSION=3.8.18
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e853c0f38ea7ee895b324be2572635fb61172c5bb439c16909ff93c5626bf9e3`  
		Last Modified: Sat, 09 Dec 2023 01:29:58 GMT  
		Size: 624.7 KB (624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a15cb4da4a424b8585532d92e4b0284de439e34f045cf1c5098fb82db760fa`  
		Last Modified: Sat, 09 Dec 2023 01:33:11 GMT  
		Size: 13.5 MB (13518338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9ad5bef1ba2feda5813a1782ef3c5928c96a6e68a1f0ad0c5dd20261eb6132`  
		Last Modified: Sat, 09 Dec 2023 01:33:09 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a92b85fa20ad8bf4b34994557d66e9eb2e89ebac00c7014cfe53a88f45a6866`  
		Last Modified: Sat, 09 Dec 2023 01:33:09 GMT  
		Size: 2.9 MB (2851673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723d0d381e47516d244e4f61c0109e561834f61ef1d7ecc80be406750a3d4112`  
		Last Modified: Sat, 06 Jan 2024 00:42:51 GMT  
		Size: 3.7 MB (3723699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:5b81171d285ee20ebd4cadc5bac4956c3f4ea9b1c22b905623d1cacdda8c23f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **874.2 KB (874185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09e9896fcbefcec13b62a578c2b16cfaf844e2d7f8bb15b7463e2f6a8edc3644`

```dockerfile
```

-	Layers:
	-	`sha256:18784d3c5ed297a5c094ac0a89b8ae2757a9474bb69cff008c020425024c6a75`  
		Last Modified: Sat, 06 Jan 2024 00:42:51 GMT  
		Size: 864.6 KB (864553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ad384be2e24c583922eb71bc446fae2dcf53794d675986aefce0e7db64db882`  
		Last Modified: Sat, 06 Jan 2024 00:42:50 GMT  
		Size: 9.6 KB (9632 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.19` - linux; 386

```console
$ docker pull hylang@sha256:7aac3b3b222400522cd5fa1b539bbaf3e629903c6a184e9c6fb6334a70120fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24096867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1afda71122d20901de262c95228e9925057492978cf3ca8c3f54ea9c93e002d`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 08 Dec 2023 01:38:25 GMT
ADD file:bd52540f209ba362654d795d7893669c819d35011a16f9f319301727a33b3bd9 in / 
# Fri, 08 Dec 2023 01:38:25 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Dec 2023 09:55:38 GMT
ENV LANG=C.UTF-8
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_VERSION=3.8.18
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9acd8b4c9d4385585f74dabb4bc6b3351888710ae37ec5dbd9ea950281b8f9bb`  
		Last Modified: Fri, 08 Dec 2023 01:38:43 GMT  
		Size: 3.2 MB (3244115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2119bf6dee75c7b7760616d3acb471ec49b73b34ea14f7bc5482840548fad5`  
		Last Modified: Sat, 09 Dec 2023 04:27:59 GMT  
		Size: 622.4 KB (622375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549dc1a2b062eb5622242450cae8cd785f6930915144828e7f0adb4594d8badb`  
		Last Modified: Sat, 09 Dec 2023 04:31:14 GMT  
		Size: 13.7 MB (13654642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c35af8f015bd1fae77516acdc123614e53c909608d6ca9b69bbacadc7b4f142`  
		Last Modified: Sat, 09 Dec 2023 04:31:11 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622861f2f18a9c662c0eb7261268cc3c0bf920c4581dc51f8484181c4b172161`  
		Last Modified: Sat, 09 Dec 2023 04:31:12 GMT  
		Size: 2.9 MB (2851714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb2e90a81c5c40587c275232273c250b4fd5740a5b438e567674a10cd9760ae8`  
		Last Modified: Fri, 05 Jan 2024 23:55:55 GMT  
		Size: 3.7 MB (3723778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:a91125e6518a08dcd602bfa59cabe588f348a696a468e98340f59de64c025f1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **874.9 KB (874872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9851ce08e6677dea5f2d7ac551da9d7eb92ca14264b7226468ae1197da5128`

```dockerfile
```

-	Layers:
	-	`sha256:a494d4f2e2123851eb017c59bc88a697487ff9b7cde77639e7d014037205050a`  
		Last Modified: Fri, 05 Jan 2024 23:55:55 GMT  
		Size: 864.5 KB (864489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:630edd67712cf4fe245d7608ee347d49461206e666b67148157921aa982c2732`  
		Last Modified: Fri, 05 Jan 2024 23:55:54 GMT  
		Size: 10.4 KB (10383 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.19` - linux; ppc64le

```console
$ docker pull hylang@sha256:0dcc934517e2a4102a4edfd09adb8739f196a45b40b0dbc96b5408447e3c9acf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 MB (24462579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6bb4df10fc80bc5de6af520ffbee66d839e27dcde14e32d39104873273bf799`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 08 Dec 2023 01:22:51 GMT
ADD file:052421189f8d269382daaaa8beb63c687e4d8ca908c421abdce53bcc627a40b4 in / 
# Fri, 08 Dec 2023 01:22:51 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Dec 2023 09:55:38 GMT
ENV LANG=C.UTF-8
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_VERSION=3.8.18
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:243ac51c334a47917a84be93e972ee6378987e9b3b917a5a8df29025e161c1f3`  
		Last Modified: Fri, 08 Dec 2023 01:23:14 GMT  
		Size: 3.4 MB (3358233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a081cf452e352600ba7e978072f652f412217d025eb9e6fdee9520f88252831c`  
		Last Modified: Sat, 09 Dec 2023 02:20:52 GMT  
		Size: 625.1 KB (625119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6687208b3ef9ba2923bea80c980292f51116a635fb30b988e16f513e3d91b3`  
		Last Modified: Sat, 09 Dec 2023 02:24:11 GMT  
		Size: 13.9 MB (13903135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11917434a1c59c138105f60e29750d6995943deb499ce273c76340f25b43bc01`  
		Last Modified: Sat, 09 Dec 2023 02:24:09 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ab62f9205cf1493d2e0f4722ba68823a9e4768d53cd9aa3cf8b8f95125c729`  
		Last Modified: Sat, 09 Dec 2023 02:24:10 GMT  
		Size: 2.9 MB (2851726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40db288f5b07c55dd1d8441f04e50dd69e275d00e43f259ce4ccc848876727e`  
		Last Modified: Sat, 06 Jan 2024 02:48:27 GMT  
		Size: 3.7 MB (3724124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:9d2d7fe9e998c04a0ba4f8e3d8f7ef3a53172626334dac6909017d32212d6219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **872.6 KB (872631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d12f694bba47f33f6185c08a2e0c5563814c34b0e12870b53eaa6e4cafe91ae7`

```dockerfile
```

-	Layers:
	-	`sha256:9bf596461f94d599d2d81c3063ebe01971472fe330885cf909735293d16021a3`  
		Last Modified: Sat, 06 Jan 2024 02:48:27 GMT  
		Size: 863.0 KB (862956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8c282dff8a5a0df14db6579e6b735a5bac30aeef4aa47e220c4e831888586f9`  
		Last Modified: Sat, 06 Jan 2024 02:48:26 GMT  
		Size: 9.7 KB (9675 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.19` - linux; s390x

```console
$ docker pull hylang@sha256:9f6800b20d8a67c9232649376c640797365276590046af099549876be97a42a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24151118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3898c4a6ce7ec8667275cfa5911d76db51853f9ea2efd6bb64f760b5683e1e9c`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Dec 2023 09:55:38 GMT
ENV LANG=C.UTF-8
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_VERSION=3.8.18
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44507c21692f6a1dfe3960dcd32b105ed10a012358912cf6e622dd984c44e76`  
		Last Modified: Sat, 09 Dec 2023 00:43:53 GMT  
		Size: 622.9 KB (622924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d06ff90596114ca28b6e93b8983311780820f89c6d8e339d7c18038496b792`  
		Last Modified: Sat, 09 Dec 2023 00:46:05 GMT  
		Size: 13.7 MB (13710066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d388b7d50ac0668ce3859d1cb9c90d4df87df5873a6188267c4d803dba5a2d0e`  
		Last Modified: Sat, 09 Dec 2023 00:46:04 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0352795e2dca9e7f2fffcc5db9547d9e8f2903f88d23ba61b941aabc7e69aa35`  
		Last Modified: Sat, 09 Dec 2023 00:46:04 GMT  
		Size: 2.9 MB (2851683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bdf93402a9a1dab2cf553a971cf850b5a819aeef4494113ba12008cc4113217`  
		Last Modified: Sat, 06 Jan 2024 00:34:39 GMT  
		Size: 3.7 MB (3723870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:44e3fd2fdde8a970b4fbc524ff1a5f4c98932373e8301c771150657220dcd62d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **872.5 KB (872512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ad2494f7e351ae99d3ca7917a77fbfbc228c141ca1a0d473ef5b509ce3ce23`

```dockerfile
```

-	Layers:
	-	`sha256:55dccf7f131de3761773d673708476a04f26e0bd102f6136b8bf005ee5996d7a`  
		Last Modified: Sat, 06 Jan 2024 00:34:39 GMT  
		Size: 862.9 KB (862898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c1db0625b4c9e0fe5086535d77ad4dacc9e84a0820aab52067266eaf93c3831`  
		Last Modified: Sat, 06 Jan 2024 00:34:39 GMT  
		Size: 9.6 KB (9614 bytes)  
		MIME: application/vnd.in-toto+json
