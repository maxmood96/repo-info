## `hylang:python3.8-alpine3.20`

```console
$ docker pull hylang@sha256:db0ca7195a8841b917c829cea7d9c3febf33d9c4acad4536a57003d46e8492ea
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

### `hylang:python3.8-alpine3.20` - linux; amd64

```console
$ docker pull hylang@sha256:0dbff97d5a5d2745318afd85e120a291b3a1586f2fbf9feeba8e2a542e3ef703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.9 MB (21899362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6ad32bea137604dc17902dba797e7c33f4b9eb517335447f448681a522971d1`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jul 2024 10:56:26 GMT
ENV LANG=C.UTF-8
# Mon, 29 Jul 2024 10:56:26 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 29 Jul 2024 10:56:26 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_VERSION=3.8.19
# Mon, 29 Jul 2024 10:56:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 29 Jul 2024 10:56:26 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Mon, 29 Jul 2024 10:56:26 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 29 Jul 2024 10:56:26 GMT
CMD ["python3"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HY_VERSION=0.29.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 29 Aug 2024 19:15:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef947e97ee7ce91207cca5472c1a626754d7162297d0900ba37cbea22d5b4b1`  
		Last Modified: Fri, 02 Aug 2024 14:35:55 GMT  
		Size: 461.8 KB (461810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:605f3cc7940647a5eb471f210f1fc1226eebd5dc887ba52e8874d8418e93d0bb`  
		Last Modified: Fri, 02 Aug 2024 14:35:55 GMT  
		Size: 11.4 MB (11361308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915797fb089ebf35d46072bca49cfd3ae57ea71911fd595d079bd8c4c82d2083`  
		Last Modified: Fri, 02 Aug 2024 14:35:55 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b75c80edccceac3afaf05d6d6d4de9d755220f6751d6f2a184572c1ae12f9d3`  
		Last Modified: Fri, 02 Aug 2024 14:35:55 GMT  
		Size: 2.7 MB (2697324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0b9c34d9e37507ec28e2e684d8f07ed89a8d6cfb47c1e66b5259e706fbde58`  
		Last Modified: Thu, 29 Aug 2024 19:57:40 GMT  
		Size: 3.8 MB (3755799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:33ed6506e763cbb54104bdb7dbfc01e8d54632a7a8a760968ce346b9635997ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.7 KB (671673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef0c5af31d429240a60ca84f409d2d1c7ac01bcd91b9aa9da0508e484b1b3ff5`

```dockerfile
```

-	Layers:
	-	`sha256:9ee52091ec874cd90ad266597f528fc3c9dc0360bd27447a6ecbd59713d2d046`  
		Last Modified: Thu, 29 Aug 2024 19:57:40 GMT  
		Size: 661.9 KB (661873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:265bae2d898deb766a00c4c2b744abf55edd313fc6cc6bda0b9e7fa726eeca10`  
		Last Modified: Thu, 29 Aug 2024 19:57:40 GMT  
		Size: 9.8 KB (9800 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.20` - linux; arm variant v6

```console
$ docker pull hylang@sha256:dff2e03f9446f0d9eb6c4bb220eaa7ff1ea7e7865ad7a43290200d41899776e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21316357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:788e3a95eeed6368ab19b45a6c216f7d8cea6a4b4e2c0af98a6b0fadc65610ce`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jul 2024 10:56:26 GMT
ENV LANG=C.UTF-8
# Mon, 29 Jul 2024 10:56:26 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 29 Jul 2024 10:56:26 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_VERSION=3.8.19
# Mon, 29 Jul 2024 10:56:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 29 Jul 2024 10:56:26 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Mon, 29 Jul 2024 10:56:26 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 29 Jul 2024 10:56:26 GMT
CMD ["python3"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HY_VERSION=0.29.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 29 Aug 2024 19:15:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7037f99c575ff7fb3ee810dfd3275219c3931b5eca73cdd908d52fd17a84d30c`  
		Last Modified: Thu, 01 Aug 2024 19:03:26 GMT  
		Size: 462.6 KB (462579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390b4ad1b58aa312cf669b0f8246540d9b78f97bbeded85c81340768a025ab9c`  
		Last Modified: Thu, 01 Aug 2024 20:52:14 GMT  
		Size: 11.0 MB (11034846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f72931bd7ad4c469a6e4a8cbf7b1238f48db2d75df7175ba455ee3e6b3f59e1`  
		Last Modified: Thu, 01 Aug 2024 20:52:14 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9c79dc0257e69143f8a10bd812fa795c37d71c5c6e5dad61471666093d4871`  
		Last Modified: Thu, 01 Aug 2024 20:52:14 GMT  
		Size: 2.7 MB (2697334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc2f3ba0dad9ab0a4db398803f0da98ab682c2dbac2b58c1443a2384bde8bf0`  
		Last Modified: Thu, 29 Aug 2024 20:01:26 GMT  
		Size: 3.8 MB (3756180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:cfb98b8f1a841706a6f721bbe643efd4f7b4991983772bae833842eb70ab05e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 KB (9701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ab3605e0c6189d0dbd1ad9c19c13b67de3b8d8882643ef3af9f941b6a8b86a`

```dockerfile
```

-	Layers:
	-	`sha256:01c8be4cce4839c39f00b2a43fc43b7092b1e4135459fa59ac97c6b152b463ee`  
		Last Modified: Thu, 29 Aug 2024 20:01:26 GMT  
		Size: 9.7 KB (9701 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.20` - linux; arm variant v7

```console
$ docker pull hylang@sha256:915067b3dd764f9bf5551827b5b073f7ed6c1a2ad4380529f0ebd9b9ecf17bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20657171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdd0b53b51b284180fd43ed3ba99212b0bde446b9352e4ce7ae030edfc0f8330`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 22 Jul 2024 21:59:47 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Mon, 22 Jul 2024 21:59:47 GMT
CMD ["/bin/sh"]
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jul 2024 10:56:26 GMT
ENV LANG=C.UTF-8
# Mon, 29 Jul 2024 10:56:26 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 29 Jul 2024 10:56:26 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_VERSION=3.8.19
# Mon, 29 Jul 2024 10:56:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 29 Jul 2024 10:56:26 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Mon, 29 Jul 2024 10:56:26 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 29 Jul 2024 10:56:26 GMT
CMD ["python3"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HY_VERSION=0.29.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 29 Aug 2024 19:15:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ef77f3591f9a13a2d038b8d57b659d41ac91d2de7301c4ab9e6c12c44d058c`  
		Last Modified: Wed, 24 Jul 2024 09:43:23 GMT  
		Size: 461.8 KB (461753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96d4f39fe325efadd1b3ab39efeb3afc64604b20fbc2ad4221039f38a1d0749`  
		Last Modified: Wed, 24 Jul 2024 13:03:05 GMT  
		Size: 10.6 MB (10646848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fa917eefc1e310537efb4ac1c9332abe8987b1026e8d59274baf4096af1d16`  
		Last Modified: Wed, 24 Jul 2024 13:03:04 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5807a5a8e0791dcd4b1e097b2ff0f79a190c1281252ec533b88c17bc1ce1094`  
		Last Modified: Thu, 01 Aug 2024 23:02:34 GMT  
		Size: 2.7 MB (2697292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f1ee35b400bf481029a93e768ce01a635f3c78523bde2732519d6ef52b6c37`  
		Last Modified: Thu, 29 Aug 2024 20:15:40 GMT  
		Size: 3.8 MB (3756089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:944e6c812c27fea123e3495a13bab06069cec4d10ef57f680046aecc17bebdc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.7 KB (674725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8323af06b007f7dbaff65527d58999465cf0b1f2cfc99801e463ebe4c210f204`

```dockerfile
```

-	Layers:
	-	`sha256:defd0d11739c05def81c840e319ca5dcba486fcf320a8e74653d920308ed6d99`  
		Last Modified: Thu, 29 Aug 2024 20:15:39 GMT  
		Size: 664.8 KB (664805 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae52dac9da493e37d70ddf8c69a6f063ca6443a8b7b88ee4a080c07841294e71`  
		Last Modified: Thu, 29 Aug 2024 20:15:39 GMT  
		Size: 9.9 KB (9920 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:089aab23c169dd8f6433ffd232b146f0dbde40eac9db3af623476ef77c8a4306
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22463621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4c1c02cb2dd6378247481cb191b17af752d1082b6ffe57a6c04219e76a2a0a`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 22 Jul 2024 21:44:13 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Mon, 22 Jul 2024 21:44:13 GMT
CMD ["/bin/sh"]
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jul 2024 10:56:26 GMT
ENV LANG=C.UTF-8
# Mon, 29 Jul 2024 10:56:26 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 29 Jul 2024 10:56:26 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_VERSION=3.8.19
# Mon, 29 Jul 2024 10:56:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 29 Jul 2024 10:56:26 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Mon, 29 Jul 2024 10:56:26 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 29 Jul 2024 10:56:26 GMT
CMD ["python3"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HY_VERSION=0.29.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 29 Aug 2024 19:15:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1917e6dd97e362f99311c5c1c709d7a3296716a53eebc0b290edadac35281719`  
		Last Modified: Thu, 01 Aug 2024 21:51:43 GMT  
		Size: 463.8 KB (463822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4045c08ab251746747b356217d3c1fe788f4828d86ca03ca3b518d7edad4a988`  
		Last Modified: Fri, 02 Aug 2024 03:17:36 GMT  
		Size: 11.5 MB (11459179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed77a393af5a03fd6818d3b3e8a9cb7baacc41c6c8dcf5ca305f29b5f79d7714`  
		Last Modified: Fri, 02 Aug 2024 03:17:35 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2743c6e84eb02e0ad548086e9930efa6dc3d4618bdc534cbc27b6aef6f1bbb77`  
		Last Modified: Fri, 02 Aug 2024 03:17:36 GMT  
		Size: 2.7 MB (2697320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e22f4bde0b49069a8a56067aa91ebf88c4d55465228a47a11695139621ba301`  
		Last Modified: Thu, 29 Aug 2024 20:14:03 GMT  
		Size: 3.8 MB (3756138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:5b81536626e559fd02ef251cd56e4ac9c752d8ed69d7f8649252ff46ddcdbad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.2 KB (672222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:212741df39b4ed9faeae014022b9c64761bc689576f3706bf2ba7adea3f8f8f2`

```dockerfile
```

-	Layers:
	-	`sha256:aaf34a3a74e9c626c0ba1f983549700f11eeeafb604d9fab5bef1388d89298c2`  
		Last Modified: Thu, 29 Aug 2024 20:14:03 GMT  
		Size: 662.0 KB (661977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddb7e04aea3962b482ac0df6e1f21ff608c000731bc7285a499c0c4e2eabd46f`  
		Last Modified: Thu, 29 Aug 2024 20:14:03 GMT  
		Size: 10.2 KB (10245 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.20` - linux; 386

```console
$ docker pull hylang@sha256:cb03097665b1e33731ef32fec55f796b5208b508cf0308ca32b71cf48b9afcd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (21977313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d12d2f6f8f1dd74bb8498993e379b3e6d8ded5b195cfb21320c54ccfb854d502`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 22 Jul 2024 21:38:29 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Mon, 22 Jul 2024 21:38:30 GMT
CMD ["/bin/sh"]
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jul 2024 10:56:26 GMT
ENV LANG=C.UTF-8
# Mon, 29 Jul 2024 10:56:26 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 29 Jul 2024 10:56:26 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_VERSION=3.8.19
# Mon, 29 Jul 2024 10:56:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 29 Jul 2024 10:56:26 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Mon, 29 Jul 2024 10:56:26 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 29 Jul 2024 10:56:26 GMT
CMD ["python3"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HY_VERSION=0.29.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 29 Aug 2024 19:15:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e0744dfc667fae71a3482a4f5572c5fd4e83247527baca8df20bd0829b5a0e4`  
		Last Modified: Fri, 02 Aug 2024 14:36:13 GMT  
		Size: 462.2 KB (462189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccf43d71622f83eb00717629a69afc6e60e1b027bb2a8b28d30ecbef6a587db`  
		Last Modified: Fri, 02 Aug 2024 14:36:13 GMT  
		Size: 11.6 MB (11593318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c14b8fb8fac8d69eeaa7edfe981fb737332dfc700e745f1cca929676110272`  
		Last Modified: Fri, 02 Aug 2024 14:36:13 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a066adc9d0a38b917f9daefda4c1c024530a9aa52988addfcbf452d1b50dd3`  
		Last Modified: Fri, 02 Aug 2024 14:36:13 GMT  
		Size: 2.7 MB (2697310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1b97502727d58d1b52a432eb9644766d493082e2f1343809fc30ca2b6e4382`  
		Last Modified: Thu, 29 Aug 2024 19:57:35 GMT  
		Size: 3.8 MB (3756197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:11e24d98a95bd632ef9b4d2450162124062e7308d6395ed1dc538c2115229411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.6 KB (671576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77fc030bd666dfc8796409975992fb834ca270d275b9dc2833a8b4f85434dc96`

```dockerfile
```

-	Layers:
	-	`sha256:57c0f720f17e389127eb2a1232b25d9dc9eb06b045a6c36c2ff872a06a949445`  
		Last Modified: Thu, 29 Aug 2024 19:57:35 GMT  
		Size: 661.8 KB (661828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cded844acb82424be7faf0ef982a23f5568c228570079693d8fbc8039e5daa2`  
		Last Modified: Thu, 29 Aug 2024 19:57:35 GMT  
		Size: 9.7 KB (9748 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.20` - linux; ppc64le

```console
$ docker pull hylang@sha256:5302e33d07bccc208744ba2e29a194159c5e48ae38944220d966c58cec8ea39a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22332249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f71063bdb40f930f3ec2cedf3eb83482c93d14c36a9f682f9f17bead46ef69a`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
CMD ["/bin/sh"]
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jul 2024 10:56:26 GMT
ENV LANG=C.UTF-8
# Mon, 29 Jul 2024 10:56:26 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 29 Jul 2024 10:56:26 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_VERSION=3.8.19
# Mon, 29 Jul 2024 10:56:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 29 Jul 2024 10:56:26 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Mon, 29 Jul 2024 10:56:26 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 29 Jul 2024 10:56:26 GMT
CMD ["python3"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HY_VERSION=0.29.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 29 Aug 2024 19:15:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd9dca3c71557146b76d34caf51ce31845024af597b3e49a8a753cc001f0db0`  
		Last Modified: Wed, 24 Jul 2024 06:19:23 GMT  
		Size: 464.2 KB (464224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ff3278d71d6f418eeb3e60da246f2bcf03b6198cc3133bb162c7b55cf5efb7`  
		Last Modified: Wed, 24 Jul 2024 09:50:59 GMT  
		Size: 11.8 MB (11842699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3bd09d914ca1a6bc7e09878e3de09ac45e5ae9316f625887a6c389bfe79017`  
		Last Modified: Wed, 24 Jul 2024 09:50:58 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43263a8eab791c88b9c4030488d51dbe81abf8cff99c7e9e02e9f786536864d`  
		Last Modified: Thu, 01 Aug 2024 23:53:03 GMT  
		Size: 2.7 MB (2697328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01ed4d5df460c327550864d551227d606e62991700f5a71c2ab6f3ee39a14af`  
		Last Modified: Thu, 29 Aug 2024 20:20:43 GMT  
		Size: 3.8 MB (3756213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:9fa4e63177d60231e1decf27f37acfcf4b479f0b5e1bb71d38f81d244e87b835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.9 KB (669857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1209f1f6e2e4c5f6e3a41ebc283f00d6b64b73a993ca9a918d30f633ecdc2655`

```dockerfile
```

-	Layers:
	-	`sha256:ec2d5111f941d00b8a0fb9d1bd2048cad3e57f1463ec07ee704ee086ffeea639`  
		Last Modified: Thu, 29 Aug 2024 20:20:43 GMT  
		Size: 660.0 KB (659977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:968c2e54765b3b0fdf12af2207ed391d66429002468c01b8dce77126512405d8`  
		Last Modified: Thu, 29 Aug 2024 20:20:42 GMT  
		Size: 9.9 KB (9880 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.20` - linux; riscv64

```console
$ docker pull hylang@sha256:d7b780f87dc566444e4cf04735677d741810b2415a612c0e8aa9e47f861ecb01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21631675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff9e2a6cef7581cc39cf6c0f45a087e06f1ea87a657e756112399405a91eae63`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 22 Jul 2024 22:21:00 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Mon, 22 Jul 2024 22:21:00 GMT
CMD ["/bin/sh"]
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jul 2024 10:56:26 GMT
ENV LANG=C.UTF-8
# Mon, 29 Jul 2024 10:56:26 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 29 Jul 2024 10:56:26 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_VERSION=3.8.19
# Mon, 29 Jul 2024 10:56:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 29 Jul 2024 10:56:26 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Mon, 29 Jul 2024 10:56:26 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 29 Jul 2024 10:56:26 GMT
CMD ["python3"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HY_VERSION=0.29.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 29 Aug 2024 19:15:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61ada1c505e26eb1f7498a8db10f175226ab1693958a5e1f5d7e73020d75af8`  
		Last Modified: Thu, 01 Aug 2024 19:42:26 GMT  
		Size: 462.5 KB (462502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5a0d72310fcf4f86487699a942d797c7ebbe22d39fbff87f2fadbbbe9af79b`  
		Last Modified: Thu, 01 Aug 2024 23:23:26 GMT  
		Size: 11.3 MB (11343725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcd6fb6e378fcc0f09afb9c339fa01eb589102b3c5ca8f53d42c3c232e03c30`  
		Last Modified: Thu, 01 Aug 2024 23:23:24 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8ec2356b9855e5c8f3a77ef174f9c68b930eed306261ee80e70c9d1fe1c8e9`  
		Last Modified: Thu, 01 Aug 2024 23:23:25 GMT  
		Size: 2.7 MB (2697366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d3289e5e6d1d2abfd50d1b8244c65c5a2a31be8f581419960965ff40170b71`  
		Last Modified: Fri, 02 Aug 2024 06:02:18 GMT  
		Size: 3.8 MB (3757180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:bddc13e38d1652c586765c127b9172ab625257dde81e9b555ad5211f48fc97ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.9 KB (669852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e2d2df5d7f9f8533541b7e0f2cfec0b1eadc45f3cf1c18fbf4b5065785b8a82`

```dockerfile
```

-	Layers:
	-	`sha256:41376e73fc17cbb42e70f62a834c8326fe357695f2c2aa92b187f3e222d554cf`  
		Last Modified: Thu, 29 Aug 2024 20:33:11 GMT  
		Size: 660.0 KB (659973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af746ca9addd260befb137f48b6ed89c79c06bcbb1061f92e6a6a87d3ef04b28`  
		Last Modified: Thu, 29 Aug 2024 20:33:11 GMT  
		Size: 9.9 KB (9879 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.20` - linux; s390x

```console
$ docker pull hylang@sha256:0b5e9087922a9ad8b10990012b3437c8edda011b763d563dc274ce7c7c5c8114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (22022149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e629a5ecaaa3c09c1f9f34f93f410a41d1608c4df58142bf1939baf0ef274a6`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 22 Jul 2024 21:50:06 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Mon, 22 Jul 2024 21:50:07 GMT
CMD ["/bin/sh"]
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Jul 2024 10:56:26 GMT
ENV LANG=C.UTF-8
# Mon, 29 Jul 2024 10:56:26 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 29 Jul 2024 10:56:26 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_VERSION=3.8.19
# Mon, 29 Jul 2024 10:56:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 29 Jul 2024 10:56:26 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Mon, 29 Jul 2024 10:56:26 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Mon, 29 Jul 2024 10:56:26 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 29 Jul 2024 10:56:26 GMT
CMD ["python3"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HY_VERSION=0.29.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 29 Aug 2024 19:15:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f8748ca9fe65528fe04e9a4486c3e19566db99083ba57256706f0da3ffb2d6`  
		Last Modified: Mon, 05 Aug 2024 06:19:51 GMT  
		Size: 462.7 KB (462745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a50995461e96ab2eadbeac3f869641f80e6e2a0e716968136f73dc1d17eee13`  
		Last Modified: Mon, 05 Aug 2024 19:31:36 GMT  
		Size: 11.6 MB (11646936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a08a4e482fa17691f2a04764f95322dd1531e2a94370b3fee503a95a2a06768`  
		Last Modified: Mon, 05 Aug 2024 19:31:36 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85e29aa6a1cf23f8f41e23a48dce7646381fe0f79120adac2badfd680ab44c9`  
		Last Modified: Mon, 05 Aug 2024 19:31:36 GMT  
		Size: 2.7 MB (2698313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051a4d72a1fc4ca0b047951f5cd9ae56effc7a72d8672ed6179b91fb183afdcf`  
		Last Modified: Thu, 29 Aug 2024 20:18:26 GMT  
		Size: 3.8 MB (3752859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:7a8743d1534a0875b294c075af03998db712b5dc93a78b373e56d9839a7d0cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.7 KB (669713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae3f2ca592dda4f47de1087abdbf38b065f853dfd78cb04dfe574b4ec75f500`

```dockerfile
```

-	Layers:
	-	`sha256:74a1fb5e5539c473cc73fb44dbbfcafcab4f0c4c7e027109ec9ef3ad472022f4`  
		Last Modified: Thu, 29 Aug 2024 20:18:26 GMT  
		Size: 659.9 KB (659901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f321c2fe5e981f53202988a999ab7aaabc638ad1de8c4c19a2927748c7a0a90f`  
		Last Modified: Thu, 29 Aug 2024 20:18:26 GMT  
		Size: 9.8 KB (9812 bytes)  
		MIME: application/vnd.in-toto+json
