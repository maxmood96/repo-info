## `hylang:python3.13-alpine`

```console
$ docker pull hylang@sha256:84d3e870b9bf870a3298328626d1e7bb2cf7a9ca382fc9a24672f6eb2b1999b0
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

### `hylang:python3.13-alpine` - linux; amd64

```console
$ docker pull hylang@sha256:62dffeef5cac7be43489daa7336d4cfe7e6c63431c7019fc9f8049a4c774c910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24583561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a1874f0459a80680eb0caf76f45319398257c9966aa5b0b851ecbb3b3700b1`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.13.1
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96bad37e6db985258227bbc565a57a962989511c88872ecb51b7709c7392fd52`  
		Last Modified: Wed, 04 Dec 2024 20:36:39 GMT  
		Size: 455.1 KB (455124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91fb7730f44636edd2a991295069f180157972d8a33709674f7fb068b40192e`  
		Last Modified: Wed, 04 Dec 2024 20:36:40 GMT  
		Size: 14.8 MB (14818568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9059bd6473e26d681b3506fbba2f84a69ea09d1a583f6daf7d021c9949d9851`  
		Last Modified: Wed, 04 Dec 2024 20:36:39 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eeae46b0437d68e18637f9a1246f226cc7487647b09ff3758b15a8f680e0dc4`  
		Last Modified: Wed, 04 Dec 2024 21:10:03 GMT  
		Size: 5.7 MB (5685715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:61726ecbfa876baaf35e37f0941e53454ac33a068980ad7f65b9e41d736cab4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.0 KB (638006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecb9a04c7c054daed7a78cf6f85d710f133b9ccd59dbb671ae41a49aa03c266`

```dockerfile
```

-	Layers:
	-	`sha256:e2e2ab50a0a618c5265f6e4bd9d2a2366854e8cf8f4e8ccbe646af47990a6567`  
		Last Modified: Wed, 04 Dec 2024 21:10:03 GMT  
		Size: 626.2 KB (626216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d65752aa4bb34a6c41dfb669219232b6b600ef4025c9e02eee2ab856e978bf05`  
		Last Modified: Wed, 04 Dec 2024 21:10:03 GMT  
		Size: 11.8 KB (11790 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine` - linux; arm variant v6

```console
$ docker pull hylang@sha256:e828b9a0b8f9b65d4d1ede6d6739b43362c034faf6f4bdac24f4053ae67afd1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23630957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8ae9374e52c4a481c9466d6d52c7bd7f6206a3ed5c72408d144ce15f92bbb6b`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.13.1
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaae7f50b1179fbba9e574ed7f89db6d7ef4b8bfad3f0e758189283f1bd47387`  
		Last Modified: Tue, 12 Nov 2024 13:50:59 GMT  
		Size: 456.0 KB (456034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c78c7aebb2f5af536b813308749bda5acb46aadb31f91d3806044281ec08d9`  
		Last Modified: Wed, 04 Dec 2024 20:37:44 GMT  
		Size: 14.1 MB (14122264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030124c23782f46e6fe9940c46dd83b485e8bd3115ad371aca130edd1a03f1f9`  
		Last Modified: Wed, 04 Dec 2024 20:37:44 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bf5916f43ff33fbe013815371baaf3fb87ebc33a03b03ca96a5501033be19b`  
		Last Modified: Wed, 04 Dec 2024 21:25:51 GMT  
		Size: 5.7 MB (5685814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:003d589cc51a90195c21d5c38cd4e7c8d9bd43d49c8a4f4392c530d96ee4d5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.7 KB (11746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a859f556f573bdcf01e7fc479018cbc81dfed427298416fd512d629488b17ed9`

```dockerfile
```

-	Layers:
	-	`sha256:76f94f3fdfc0bf610f5b930eea46bff77398494ac5fe7942bc79ee73c3f39873`  
		Last Modified: Wed, 04 Dec 2024 21:25:50 GMT  
		Size: 11.7 KB (11746 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine` - linux; arm variant v7

```console
$ docker pull hylang@sha256:3f87c7b28b62d384ef605538b77a7ed50b684fc74df4615bc44ece9844249f61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22849341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13440bd64b41b93c34cb87c37040589ea38c17b5d7eecac675a0c1f8c9ac076e`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.13.1
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be84f58a6ba1e5afec1f980bc5e88789f864d7f484d01c93664b9fff548f3a56`  
		Last Modified: Wed, 13 Nov 2024 02:15:34 GMT  
		Size: 455.2 KB (455163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d40aab0bea0851cd74e3603c60e1011eb69a2364e7d6f4394624197a3eb38a`  
		Last Modified: Wed, 04 Dec 2024 22:06:35 GMT  
		Size: 13.6 MB (13612650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145932f2f22c9bfa52e948db5859a91be8bf76b53f20e6880361cec8664248f1`  
		Last Modified: Wed, 04 Dec 2024 22:06:35 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1c951be41a30b5ea8421819f870bfdcf52fc51cb3828822889aa43461fe7f3`  
		Last Modified: Thu, 05 Dec 2024 03:03:50 GMT  
		Size: 5.7 MB (5685792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:eb9d705a3d4f00eea83981e3916a46de6ead6a71eeed9e6e7d1f1ab4549e727e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.2 KB (641174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b51031daf01d4e714bc737c37749838f07ab5e0377329092267052c9d2dfdf1a`

```dockerfile
```

-	Layers:
	-	`sha256:aee2deb5f6b858edb03d08f0c12e51186003031c32fac544fab6b9b9d5b02c5b`  
		Last Modified: Thu, 05 Dec 2024 03:03:49 GMT  
		Size: 629.2 KB (629212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c890d9b08a0ea9f061e630dfbfa66be23de06836eddbac6748cbe10078e8d61b`  
		Last Modified: Thu, 05 Dec 2024 03:03:49 GMT  
		Size: 12.0 KB (11962 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:e4549f13ba38193fea9e939556e6af4688cb7577b5e3678f1c3578b40500539b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25493624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f303ee8e53be4c2321fdb387603f50c183c4f9dc4d0ae2fa3579973e3a82e9`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.13.1
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe80dd7098fb09d5aa060ba0768ea2b70faad999bc0ab1417de25dfa6fc81e03`  
		Last Modified: Wed, 20 Nov 2024 21:20:29 GMT  
		Size: 457.5 KB (457482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7093bb662347dc2e00b7ea975cbd1e78959eef4a208a5e9009a53263563aea`  
		Last Modified: Wed, 04 Dec 2024 21:45:11 GMT  
		Size: 15.3 MB (15262434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7fd229ff33d08a7f77efd410927cc58523184f02f6ad7c26ed807436e5f460`  
		Last Modified: Wed, 04 Dec 2024 21:45:10 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ff6c5a9d4adcfa733753a9bad95183c0d1a2326d67438acc53bf41397bf272`  
		Last Modified: Thu, 05 Dec 2024 01:09:28 GMT  
		Size: 5.7 MB (5685733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:1f548acef2f82132961d02021fe4d578f835c913733d4ecae586fc592ecadb64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **638.5 KB (638454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9234ef0300d04eb901e32ed7c9bfb9109aa8dc14c92c4692de3de180859f3de7`

```dockerfile
```

-	Layers:
	-	`sha256:73af055b71a5aaba6be0faa77d7214de5375ac036711cd7ae1c634b11fa53820`  
		Last Modified: Thu, 05 Dec 2024 01:09:27 GMT  
		Size: 626.4 KB (626416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:038a1c399d9b45fad4e4dcda4a9d601e84169620fa11a9e02d3f83d2447ac453`  
		Last Modified: Thu, 05 Dec 2024 01:09:27 GMT  
		Size: 12.0 KB (12038 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine` - linux; 386

```console
$ docker pull hylang@sha256:ebf6617894a275b2453d3cb19c290089939a984d7cce670504a0987abd9afcad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.5 MB (24525820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f14815f32b1b011f71f3cb65878744c8cdb62f91fe9b853c44d5ca184361155`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.13.1
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ccdf2ff830cbea417007a754491a5327ad1b770410815aa7eb65b7389a715a`  
		Last Modified: Wed, 04 Dec 2024 20:35:55 GMT  
		Size: 455.6 KB (455597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a31518bbb305c63488d615eb7f6c1faac6d70182abd65407de89e4e121d4e7`  
		Last Modified: Wed, 04 Dec 2024 20:35:55 GMT  
		Size: 14.9 MB (14915023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0a4156c42088270a1ad230b628387a84a7faf9c9c52a781c0a92d580561092`  
		Last Modified: Wed, 04 Dec 2024 20:35:55 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36ff8fa6d2611cb5eb61e4428bde1974d808e6d0a80f5daeca5ef05a27db01e4`  
		Last Modified: Wed, 04 Dec 2024 21:10:26 GMT  
		Size: 5.7 MB (5685733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:830ae16def26fefbda11b069a8c076e99f08835ab70256f7ad318153e1259600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **637.8 KB (637829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff4be97c4c8512671b270d1e9e3fffbbca230a2d186e9cb64d0c87a67a4b9a6`

```dockerfile
```

-	Layers:
	-	`sha256:231c0c6cb7921e542da67ca3aa3bf26f7d52f9fdbd4c6acabd035d6209028d3c`  
		Last Modified: Wed, 04 Dec 2024 21:10:26 GMT  
		Size: 626.1 KB (626131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bce5e9dddb40478e70986e27cda2fb5b36c00f304dce014164c17559076350b7`  
		Last Modified: Wed, 04 Dec 2024 21:10:25 GMT  
		Size: 11.7 KB (11698 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine` - linux; ppc64le

```console
$ docker pull hylang@sha256:73e85b354600eb50c6b8c0c7e0dd878905729264d575a2a289d5043236a9ce79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25084991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83e3028c5bb775c94dc9c9ef521919b6ed4361210db6e9ada642c1b4d8d26375`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.13.1
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f736978a57a234cff95dd3b9f01033e926430f251450e7fa3dd71cc03a2f38d`  
		Last Modified: Wed, 20 Nov 2024 20:49:19 GMT  
		Size: 457.9 KB (457880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad97c04af91326ca89081ef20bdba9e092b91be3d9c304773138fef84fd0ef1`  
		Last Modified: Wed, 04 Dec 2024 21:15:45 GMT  
		Size: 15.4 MB (15368514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c98fbda8de3edd19a6db1f3e527ef46cbff571dc8d57fd92d0fdf6fe636457b`  
		Last Modified: Wed, 04 Dec 2024 21:15:44 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8da4d91e84ecede419e9efdfef4a26cd4b9d2aa4827011755b07abf0424856a5`  
		Last Modified: Thu, 05 Dec 2024 00:03:55 GMT  
		Size: 5.7 MB (5685888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:effe6b2bbf8d065cb4aef1719c630cd077eb27e70ae0eca6d46f5f026f1d0e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.3 KB (636274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a93acda62d24b60244437f62a46c8e98c27467588a3302ceb632c4a984f792a`

```dockerfile
```

-	Layers:
	-	`sha256:921a562d04f34b951698269bdbf464cd093c11985470ad29691415d61dd27b04`  
		Last Modified: Thu, 05 Dec 2024 00:03:55 GMT  
		Size: 624.4 KB (624368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a25633a1185d410984a680099ae53e0ec23bb7fbc718bffe24d27301c6c449f1`  
		Last Modified: Thu, 05 Dec 2024 00:03:54 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine` - linux; s390x

```console
$ docker pull hylang@sha256:800243e6239c1222c1ba8d8b3287cff33e8b9d87032133c59f800bc2e40b80cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24589365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a36859fcaa15eb38e489e0b807379fca6495d0e0945e7ec2cb4433eccc21cb75`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.13.1
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c91a42328865ef2d2ebed00cb001023efad23c6ac21c6a7c59141c748724773`  
		Last Modified: Wed, 20 Nov 2024 21:20:36 GMT  
		Size: 456.1 KB (456135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a4f2cf0f7eb75c89c279d958f4a85c38ad3fdd43c79b33f155518069237036`  
		Last Modified: Wed, 04 Dec 2024 21:10:26 GMT  
		Size: 15.0 MB (14985604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982cb2a7caece3ba98bc0a0f3051a197b0506b21dcca6f4bc787078c7f6cd6f7`  
		Last Modified: Wed, 04 Dec 2024 21:10:26 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd7d3dc10d59209ec80d33a5a5ba1b1071628bc4c1ece47600ed227624a703f`  
		Last Modified: Wed, 04 Dec 2024 23:43:05 GMT  
		Size: 5.7 MB (5685769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:c3e54650b9f9db7062c120c71cdd3583d24c227ca3c5dfabf9f447bc85fafd4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.1 KB (636052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07950e865335bbf93e4c9cb5e7c27efa2002e36abbdb2e9556625842d7a12307`

```dockerfile
```

-	Layers:
	-	`sha256:50e0a80cf5a9e8b95f726e700c695c038be01fb86a7ccadc2746a3d1e3aa029a`  
		Last Modified: Wed, 04 Dec 2024 23:43:04 GMT  
		Size: 624.3 KB (624262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcf6d398ddda941d8e9ef32397ffa1d3bd3284c2931d2999989de21aedc49580`  
		Last Modified: Wed, 04 Dec 2024 23:43:04 GMT  
		Size: 11.8 KB (11790 bytes)  
		MIME: application/vnd.in-toto+json
