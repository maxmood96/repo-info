## `hylang:1-python3.10-alpine`

```console
$ docker pull hylang@sha256:a3730b250f7d83fa8ef7c6cdca9574b86218269d811abaddaa27f2403e510bc8
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

### `hylang:1-python3.10-alpine` - linux; amd64

```console
$ docker pull hylang@sha256:3128dab08c9edfa211ac5dbdd170372dd182ca8ec468bd75ea0365b7532c6b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24113457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0728c037c5f657c9e2615d4ae6a7c861a04bd1d68eaf2cfe04836d64756979c`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 21:49:13 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PYTHON_VERSION=3.10.18
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PYTHON_SHA256=ae665bc678abd9ab6a6e1573d2481625a53719bc517e9a634ed2b9fefae3817f
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
CMD ["python3"]
# Tue, 08 Jul 2025 16:37:15 GMT
ENV HY_VERSION=1.1.0
# Tue, 08 Jul 2025 16:37:15 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 08 Jul 2025 16:37:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Jul 2025 16:37:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec82994db298b1da04d7e196f51be502d568436adb336b8f563f68976184355`  
		Last Modified: Wed, 04 Jun 2025 17:11:17 GMT  
		Size: 460.2 KB (460220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0693031b932431257842c493b412250da3c9edc2d235b84d810c087a25d4ee`  
		Last Modified: Wed, 04 Jun 2025 17:11:19 GMT  
		Size: 15.7 MB (15661425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3cddf76546dc236c84f3d7b63f41d06281a9b6df0a37196759312cf7990208`  
		Last Modified: Wed, 04 Jun 2025 17:11:17 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf119cd9bb0c6df7dc3e563c7823e18dacf7d9b18cf70d1efe724e932dc23432`  
		Last Modified: Thu, 10 Jul 2025 00:30:25 GMT  
		Size: 4.2 MB (4194720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:09c9710da849639bea42d33b1fd93f201c32159b7c9de4f28f7a2696ebb6c6b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.1 KB (671059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d915d15166eab8bf6556be63ef135889704296b1b55f1d45a5a6b24b34b9fc`

```dockerfile
```

-	Layers:
	-	`sha256:d001a53a7e612eab743ebc5b31e642a42bd33320c2bc9bd8c199f6b5bed6b16f`  
		Last Modified: Tue, 08 Jul 2025 17:19:27 GMT  
		Size: 661.7 KB (661717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:472d3ccf1e2b6228c679157035b9c3b175cd9e56a0b503f1230b94b44cfa7d09`  
		Last Modified: Tue, 08 Jul 2025 17:19:28 GMT  
		Size: 9.3 KB (9342 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-alpine` - linux; arm variant v6

```console
$ docker pull hylang@sha256:cd80751483a0bb1861be9beebb8a563fd1998561c4c3eaa85e1d378b01d11811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23399597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b870ccea212e992b4128739b72a0a180bffde00605dc0b5fc590eaa57b6fa683`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 21:49:13 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PYTHON_VERSION=3.10.18
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PYTHON_SHA256=ae665bc678abd9ab6a6e1573d2481625a53719bc517e9a634ed2b9fefae3817f
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
CMD ["python3"]
# Tue, 08 Jul 2025 16:37:15 GMT
ENV HY_VERSION=1.1.0
# Tue, 08 Jul 2025 16:37:15 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 08 Jul 2025 16:37:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Jul 2025 16:37:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0593ef940db1a49cc8edfc4d51f6106c39000f71f3a4c1391bf4e442c5e8f96`  
		Last Modified: Tue, 03 Jun 2025 15:16:26 GMT  
		Size: 461.0 KB (460996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d82c85c3a13f14effab83e7a8c57cff6cda7e18f59bb6404d4c070fb263d71a`  
		Last Modified: Wed, 04 Jun 2025 18:09:13 GMT  
		Size: 15.2 MB (15242720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a06f8032b239c19010c307c8430ce8512f7835bc363fcc50493559027f2853b`  
		Last Modified: Wed, 04 Jun 2025 18:09:11 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e5df6d1beaf81c2301b6adb240eeb77419ee4dc182001bf825c84b6c5d8046`  
		Last Modified: Tue, 08 Jul 2025 17:20:12 GMT  
		Size: 4.2 MB (4194704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:37e3604c8463a13f44f3f92e1754f4c5753c041fa2a536f18b94abe2031e57d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834aaa7ae0efbcd5ea9cdd4600c0fe8b6b755673303ef55be364cc765254f4f1`

```dockerfile
```

-	Layers:
	-	`sha256:ea9ba0791c7c61ce587d2cd8520a7bf7aa2d814606fa25050e29131e53abe074`  
		Last Modified: Tue, 08 Jul 2025 17:19:32 GMT  
		Size: 9.2 KB (9235 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-alpine` - linux; arm variant v7

```console
$ docker pull hylang@sha256:d85e2434aaf151db1f12a020d41a6bc9b5d85b28b88a4783dec94967446de584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22715664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a2483ca4eb2ebe0e301a578f36a90a77da5719663b30c69311da4cf0808443`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 21:49:13 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PYTHON_VERSION=3.10.18
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PYTHON_SHA256=ae665bc678abd9ab6a6e1573d2481625a53719bc517e9a634ed2b9fefae3817f
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
CMD ["python3"]
# Tue, 08 Jul 2025 16:37:15 GMT
ENV HY_VERSION=1.1.0
# Tue, 08 Jul 2025 16:37:15 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 08 Jul 2025 16:37:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Jul 2025 16:37:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c74e96bfa905036c4a182345ac5e3f3cdf8045aede2f3a6bc0b97677fa3615`  
		Last Modified: Tue, 03 Jun 2025 13:53:15 GMT  
		Size: 460.2 KB (460219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563c52b348f100d8ed63045d50551ddff150c88497a32e05733f7f2b9a24a000`  
		Last Modified: Thu, 05 Jun 2025 00:10:20 GMT  
		Size: 14.8 MB (14841260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313bfc97ba7d8bfef735c1ac88d611502d7841baaeab99c3ea1888d7ed934816`  
		Last Modified: Wed, 04 Jun 2025 22:41:26 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cbf50bdfd65cd78fb23c4ac65e0aa724c5aee7d83df54753a05f6c3561257d`  
		Last Modified: Tue, 08 Jul 2025 17:06:40 GMT  
		Size: 4.2 MB (4194755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:0adf260fda07e42fe07809682873ff5e4fd3cfa26074ef7dca59618156e544d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.2 KB (674225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f485942414753b04b0a1bf9bcbd42fea82a735b95ff824470c2378e4f74314a`

```dockerfile
```

-	Layers:
	-	`sha256:1f3c54877771aad75eb04fed086167e1ae55d4f9a245d2945cde4959d7d00fe7`  
		Last Modified: Tue, 08 Jul 2025 20:18:31 GMT  
		Size: 664.8 KB (664775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2d05d0eaca6af73782df878d66f3b7c5bf39dfac74194f2095f52580b3d356c`  
		Last Modified: Tue, 08 Jul 2025 20:18:32 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-alpine` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:8595e6e1df6b1d53f06d74cee482753c2df03d9f61a98a0d708032b91f8e37e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 MB (24511330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8086bfcdbf1092e943c4739120d3f728ffc4abdc86cf0af4e1e6057b4c4e4e`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 21:49:13 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PYTHON_VERSION=3.10.18
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PYTHON_SHA256=ae665bc678abd9ab6a6e1573d2481625a53719bc517e9a634ed2b9fefae3817f
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
CMD ["python3"]
# Tue, 08 Jul 2025 16:37:15 GMT
ENV HY_VERSION=1.1.0
# Tue, 08 Jul 2025 16:37:15 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 08 Jul 2025 16:37:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Jul 2025 16:37:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0303525f5fc2078701bddff73754961e5f7f6980fdb042875c249b94fea4d72a`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 462.1 KB (462092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bdcce1b765899199c0cf1867467924f7e2c423342eea7f9f591ce8612f02910`  
		Last Modified: Wed, 04 Jun 2025 21:21:06 GMT  
		Size: 15.7 MB (15718413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2556dda7cf316ec8515a369a357ed0e780f3e1bd7f0e465c9dd65f7ccc6ee3c4`  
		Last Modified: Wed, 04 Jun 2025 21:03:20 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664d7ae1646447456d5b20c6b60c01fa524e5e9d7268d44dabb127cc36c37ca3`  
		Last Modified: Thu, 10 Jul 2025 00:30:42 GMT  
		Size: 4.2 MB (4194635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:9bac3e43390da8b50ed8dfff8396467dc6e530cda4a5bcedaf592558b380dae5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.3 KB (671314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54be3514f141a6328f3dd1ccdcb07f2b52ddc873c809b636cc3c066b707d5e1d`

```dockerfile
```

-	Layers:
	-	`sha256:80d7642963fa82f0171768fca95c9f12d676319328411019105782a92c245469`  
		Last Modified: Tue, 08 Jul 2025 20:18:37 GMT  
		Size: 661.8 KB (661821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09c57bc810f6afdaf97e1ef248a5acabcffa53701c9eb01c5b308b5af2e61e99`  
		Last Modified: Tue, 08 Jul 2025 20:18:38 GMT  
		Size: 9.5 KB (9493 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-alpine` - linux; 386

```console
$ docker pull hylang@sha256:4b920b756008fcfc6e2dc59ba0c7376586445b5f9265ab21f669fd60d61c4850
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24168594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfb9c6812a6653799265d0ea76593b2310dde430282e869dd65e3549394228f8`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 21:49:13 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PYTHON_VERSION=3.10.18
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PYTHON_SHA256=ae665bc678abd9ab6a6e1573d2481625a53719bc517e9a634ed2b9fefae3817f
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
CMD ["python3"]
# Tue, 08 Jul 2025 16:37:15 GMT
ENV HY_VERSION=1.1.0
# Tue, 08 Jul 2025 16:37:15 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 08 Jul 2025 16:37:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Jul 2025 16:37:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b9074d0ceff705d3513f997447a20d7d0be8d551cf5ab4d7a8487a2cf83643`  
		Last Modified: Wed, 04 Jun 2025 17:11:43 GMT  
		Size: 460.6 KB (460640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30029958f9bdae38a6c05bec18620e12c87b009240601516983bc97aa04adf7`  
		Last Modified: Wed, 04 Jun 2025 17:11:44 GMT  
		Size: 15.9 MB (15896967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f875d487596d69ebb9f40a0c024a6930ccbec275cc364b02136875d25a617f5`  
		Last Modified: Wed, 04 Jun 2025 17:11:42 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97e9b071523e3c3a343bf2b2bcaebe60e77ef083578e83c75e95736de1ad2e3`  
		Last Modified: Tue, 08 Jul 2025 16:58:36 GMT  
		Size: 4.2 MB (4194710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:184ad3f6539e1ab4ea722ee3b2940f845ee29e99e1f19ce523c8309b5d13c4f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.0 KB (670962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8357813bf163018fbe315b76e193d814151586c8c90f8e6aa2a04c1307023968`

```dockerfile
```

-	Layers:
	-	`sha256:b46b3ba047ff087ae8fc7153925606e9834404616364923ee3dd11dfa1402200`  
		Last Modified: Tue, 08 Jul 2025 17:19:45 GMT  
		Size: 661.7 KB (661672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e53df2c35a0fc0d73e489a326181633bf53fe58709039019625ba2738a318b7b`  
		Last Modified: Tue, 08 Jul 2025 17:19:46 GMT  
		Size: 9.3 KB (9290 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-alpine` - linux; ppc64le

```console
$ docker pull hylang@sha256:de732b473d415d34ee0b567edec49f8fdcb2e390c05bb574702f90e7f1d42143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24746937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e550f67e3996914a4ec6651238722adbbedd10c923af9767cc9661fa1308887b`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 21:49:13 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PYTHON_VERSION=3.10.18
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PYTHON_SHA256=ae665bc678abd9ab6a6e1573d2481625a53719bc517e9a634ed2b9fefae3817f
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
CMD ["python3"]
# Tue, 08 Jul 2025 16:37:15 GMT
ENV HY_VERSION=1.1.0
# Tue, 08 Jul 2025 16:37:15 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 08 Jul 2025 16:37:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Jul 2025 16:37:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582dfca0b0b8a32c3acefae6bb15487546cf2dd6873d926c6fab731b2e46b27c`  
		Last Modified: Tue, 03 Jun 2025 14:32:54 GMT  
		Size: 462.6 KB (462601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7a34127cf41af2c636ff2d27b00fc2bd2cc8bf27916777505aea8697b541bb`  
		Last Modified: Wed, 04 Jun 2025 19:50:51 GMT  
		Size: 16.4 MB (16359132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e3bdbe115ac81b55ee4dce5a9a9ba87cb34830a032b8aa4bb0db02b156b364`  
		Last Modified: Wed, 04 Jun 2025 19:50:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5efe6c80cd691f466197ea4769538b19feaa74b920364aec1de78b5abf4c782`  
		Last Modified: Tue, 08 Jul 2025 17:09:25 GMT  
		Size: 4.2 MB (4194769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:43f039932754662efac76f25e159f62d17933756c1106a6982defe65c3e97c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.2 KB (669234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992b6f7eb8a1d2d30d87703cff89c829bb767999dc5c08202162571a42945840`

```dockerfile
```

-	Layers:
	-	`sha256:3858d1e43063b536284b4585c57d07c2d924371b59cbdf6a015223f47e43a49a`  
		Last Modified: Tue, 08 Jul 2025 20:18:43 GMT  
		Size: 659.8 KB (659824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb84940cde891f88dddd3e3de37427e577df7242d0ae662c1c45fc649ee72d13`  
		Last Modified: Tue, 08 Jul 2025 20:18:44 GMT  
		Size: 9.4 KB (9410 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-alpine` - linux; riscv64

```console
$ docker pull hylang@sha256:e318880e37ac339147eb78d524226d74238449b85220e95900bdad8dde14198d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23843263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb1390570a416906d5eb48b6cb521dfbd7c059ed0c00df9886ff9ef8b00f851`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 21:49:13 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PYTHON_VERSION=3.10.18
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PYTHON_SHA256=ae665bc678abd9ab6a6e1573d2481625a53719bc517e9a634ed2b9fefae3817f
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
CMD ["python3"]
# Tue, 08 Jul 2025 16:37:15 GMT
ENV HY_VERSION=1.1.0
# Tue, 08 Jul 2025 16:37:15 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 08 Jul 2025 16:37:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Jul 2025 16:37:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce47d15047d7ecd16bc91f46bce748b363a0a590d08ce23c00ff31bf0702ffe`  
		Last Modified: Tue, 03 Jun 2025 15:16:26 GMT  
		Size: 460.6 KB (460587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d3eabececd7d3d6f6153061f8c6259e5be40d5c4594b6d4091b817eb8ab303`  
		Last Modified: Wed, 04 Jun 2025 21:19:27 GMT  
		Size: 15.7 MB (15672993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8eb979793f60b2d932af8014c567b1b179f10eb8069cc5d15e611c05c22741d`  
		Last Modified: Wed, 04 Jun 2025 21:02:52 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5bf71333c15adeb6ac4cff4573f46e360311503d87425eb03607b2cc3c82e8`  
		Last Modified: Tue, 08 Jul 2025 17:34:44 GMT  
		Size: 4.2 MB (4195623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:85643adc337cde9856301433294cf35466a2647e5fb8864d2dd31af38d3e657a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.2 KB (669230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e95406fa4c402581691d1a809e49becc3c207b6b0d7f9cb97707c57aa3ec3f`

```dockerfile
```

-	Layers:
	-	`sha256:c8383b93c4b5966a78275842d5e63a6f468cf80f2f7c7f961d09f267211fdf42`  
		Last Modified: Tue, 08 Jul 2025 20:18:48 GMT  
		Size: 659.8 KB (659820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f31fb9f80716caf317a8f4109d648678e7a4f4472a9d92adf34d0e7931d7ffe5`  
		Last Modified: Tue, 08 Jul 2025 20:18:49 GMT  
		Size: 9.4 KB (9410 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-alpine` - linux; s390x

```console
$ docker pull hylang@sha256:ed12fc589a80242b4de72fc37924c7a7c71b1871a95a5bf203b11b66feb202aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24375575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8dd38ee88cfe766a21bf23d1fcd917e018f0eb392ab609c55c4c63e836c0fb`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 21:49:13 GMT
ENV LANG=C.UTF-8
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PYTHON_VERSION=3.10.18
# Tue, 03 Jun 2025 21:49:13 GMT
ENV PYTHON_SHA256=ae665bc678abd9ab6a6e1573d2481625a53719bc517e9a634ed2b9fefae3817f
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Jun 2025 21:49:13 GMT
CMD ["python3"]
# Tue, 08 Jul 2025 16:37:15 GMT
ENV HY_VERSION=1.1.0
# Tue, 08 Jul 2025 16:37:15 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 08 Jul 2025 16:37:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Jul 2025 16:37:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dfff2032a8a185dc4fb89c227529cdce2a3e2234326610f8495964f1eaada74`  
		Last Modified: Tue, 03 Jun 2025 14:32:54 GMT  
		Size: 461.2 KB (461180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673f1ac3e4ddc9fba3d32975fba3aeca02ec7d82b4ae4c53e15a782699e9c589`  
		Last Modified: Wed, 04 Jun 2025 19:51:34 GMT  
		Size: 16.1 MB (16071958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacbbc64d29ce9fc71c93e0b3d648891b528208fb3d29ddbc3744815f8cce3ad`  
		Last Modified: Wed, 04 Jun 2025 19:51:33 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d549765cb9b4bf19411a95c6e319fe7619c03d85f18392c00c2a23e91a10cf`  
		Last Modified: Tue, 08 Jul 2025 17:07:16 GMT  
		Size: 4.2 MB (4194659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:746e6d5ebe54a31e8b66a633f6afd92086960de938f673928db5c736074b8235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.1 KB (669107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b201f2dfda37dfc9033305ec885cf1ac96d4767779979deddc3d7c04b017cddc`

```dockerfile
```

-	Layers:
	-	`sha256:6f7f7e42989fb46fdd26ca9e59034e172f58a1f27059827f99792524f8bedde9`  
		Last Modified: Tue, 08 Jul 2025 20:18:52 GMT  
		Size: 659.8 KB (659766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4102986c01ec83378c6c5ff172bb5228ad0f8bb4ccaa8312a2b9bea63b0db544`  
		Last Modified: Tue, 08 Jul 2025 20:18:53 GMT  
		Size: 9.3 KB (9341 bytes)  
		MIME: application/vnd.in-toto+json
