## `hylang:python3.11-alpine3.22`

```console
$ docker pull hylang@sha256:52ea2b1e350ba602bea9050a3b4ca697ca5469f8c2baaf96156fa5d5d4714b0e
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

### `hylang:python3.11-alpine3.22` - linux; amd64

```console
$ docker pull hylang@sha256:cf5a4592faf425f3dacb0efc438d3dc0ab557ea31b76d5a6350d66245d9812e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27181609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bee276877126405f3513440e735f0aa3076eda85f2de72f99b84784da3109dd`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:30:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:30:59 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:30:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:30:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 17 Apr 2026 00:30:59 GMT
ENV PYTHON_VERSION=3.11.15
# Fri, 17 Apr 2026 00:30:59 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Fri, 17 Apr 2026 00:35:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 00:35:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 00:35:59 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:45:55 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:45:55 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:45:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:45:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df53a89c0f42f83bc7aabe3219368a7a07f91c01d26df826ad018dcdcbe12c2`  
		Last Modified: Fri, 17 Apr 2026 00:36:06 GMT  
		Size: 455.0 KB (454972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca0c990548b90611452accb73caff22dd22ed3b8f9a5ff4e57794013cfe79ed`  
		Last Modified: Fri, 17 Apr 2026 00:36:06 GMT  
		Size: 16.0 MB (15953262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2468f2064dc96c59da89b52bee21c81fbb8fed8cede1e44484fce7b7bc642c6a`  
		Last Modified: Fri, 17 Apr 2026 00:36:05 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1676191b76b447d735d10f784a410d2ad277fe005149d248ac092af130fd4831`  
		Last Modified: Mon, 08 Jun 2026 22:46:01 GMT  
		Size: 7.0 MB (6964938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:175300b0323d831b98d7fc78a22e0843e5111937f3d55c3b4dcbe4a20042d2e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.0 KB (706042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0f20eb448e074a28d7ec36fa9e8ed9054dd8551f8fe4370eaf24bdb8d6c5a2`

```dockerfile
```

-	Layers:
	-	`sha256:36454e61840db68fed494ccc58683c4b4ef04f88b15501b63414d30251d808ab`  
		Last Modified: Mon, 08 Jun 2026 22:46:01 GMT  
		Size: 697.9 KB (697940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7de7da5191764e9cbec6fdadd6ed64db960b7cb6675ddf5760f1b437e8c60061`  
		Last Modified: Mon, 08 Jun 2026 22:46:01 GMT  
		Size: 8.1 KB (8102 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.22` - linux; arm variant v6

```console
$ docker pull hylang@sha256:a06a4a07388452fccbba4a6d6ad0eaabbb4b73a536637911670574c3cf78a8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26425021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf991884e31b87185255df25e0ba2be8c28cd8339aa60fff9865bbc18caa541`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:32:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:32:14 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:32:14 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:32:14 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 17 Apr 2026 00:32:14 GMT
ENV PYTHON_VERSION=3.11.15
# Fri, 17 Apr 2026 00:32:14 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Fri, 17 Apr 2026 00:38:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 00:38:43 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 00:38:43 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:44:41 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:44:41 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:44:41 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:44:41 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff0462c99f42d64940d449078f07489e2cad7e67b06c74315442afdadf90073`  
		Last Modified: Fri, 17 Apr 2026 00:38:48 GMT  
		Size: 455.9 KB (455909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2236b8fa033f13b71ea88a9bd43b091c0c32d1943d48f595475bcf62051712`  
		Last Modified: Fri, 17 Apr 2026 00:38:48 GMT  
		Size: 15.5 MB (15496548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8157b6f1d10ee717becf1fa16e238be380db625b7f76841e4b6bbed958bfbcf6`  
		Last Modified: Fri, 17 Apr 2026 00:38:48 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6755c74c346b61940b6045514ccb777f4ddfada918781a7530d1f2604d4c7690`  
		Last Modified: Mon, 08 Jun 2026 22:44:46 GMT  
		Size: 7.0 MB (6964935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:4b78be0944e95717dd7a4bb7cb9e3505958d16fe87a262044d06c61eb45cf4f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 KB (7968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4a08abf876f41a5d6d8b9db5535a0d110d1abbd94c143094825343cb127545`

```dockerfile
```

-	Layers:
	-	`sha256:a52fbccf7efc5d3c6476f87d49dd9ceb538707a98e5be2b38b30ef5fcdc69956`  
		Last Modified: Mon, 08 Jun 2026 22:44:46 GMT  
		Size: 8.0 KB (7968 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.22` - linux; arm variant v7

```console
$ docker pull hylang@sha256:64ca3003fd291f3e5cc2179427c5f9c0657cd4d535c919c41de8d1315693659e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25737497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bcc27746e17ef4a8dc46ed4f085098a10614c49f487f6dc03acb9605c8294de`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:38:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:38:20 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:38:20 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:38:20 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 17 Apr 2026 00:38:20 GMT
ENV PYTHON_VERSION=3.11.15
# Fri, 17 Apr 2026 00:38:20 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Fri, 17 Apr 2026 00:44:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 00:44:52 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 00:44:52 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:48:19 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:48:19 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:48:19 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:48:19 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2883c41d5cffede81ce509208a0bebb67686bd9f6d3a66450ef1b0d4680dab3`  
		Last Modified: Fri, 17 Apr 2026 00:44:59 GMT  
		Size: 455.0 KB (455005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5320d7fb18affe77fe5966adecd6c28f2cc065d39324e0ed5a04034280a98a64`  
		Last Modified: Fri, 17 Apr 2026 00:44:59 GMT  
		Size: 15.1 MB (15091376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79b0bc62561b972349f5f2858cddf96bc20a7dd4592ae5647f51afbf2491bf5`  
		Last Modified: Fri, 17 Apr 2026 00:44:59 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b4aa2c0aea9ec16a3065071e0fd695e58490d3eca0dbb3a2b2d48587e230c8`  
		Last Modified: Mon, 08 Jun 2026 22:48:26 GMT  
		Size: 7.0 MB (6965037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:61106cce609977ffaf0d414be1b7e409cd8c7312b882400dd18732aa85857e09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.1 KB (709149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:434fef29a94231f7e360fb3262ffa5d8458a61046c64356330147e54487f0d9e`

```dockerfile
```

-	Layers:
	-	`sha256:b2475ce8af0791487765bdafb370ac2998ff25a9053d0005fde991032d41b849`  
		Last Modified: Mon, 08 Jun 2026 22:48:26 GMT  
		Size: 701.0 KB (700966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ee5c652332ce3a4d543ea7264d83bb94fd3ec79197019197fc911db8d7e51c6`  
		Last Modified: Mon, 08 Jun 2026 22:48:25 GMT  
		Size: 8.2 KB (8183 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:8ee3ae083baf20b61241b700e9e98f1d65aad29fc309b9a9cd5ddb7b1bcbc66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27594633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f8bb5bd77abe69db735a66c7933e5147777085c5c1e8bf6990a802977ee5c3`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:34:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:34:01 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:34:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:34:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 17 Apr 2026 00:34:01 GMT
ENV PYTHON_VERSION=3.11.15
# Fri, 17 Apr 2026 00:34:01 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Fri, 17 Apr 2026 00:39:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 00:39:54 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 00:39:54 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:46:08 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:46:08 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:46:08 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:46:08 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f21ca51a14dcd86052a498fa06f0530189b9ff326a749eb27917a1a8a57268`  
		Last Modified: Fri, 17 Apr 2026 00:40:01 GMT  
		Size: 457.3 KB (457326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc179f724180a4cd8ddcbbf0bb407305c21e3802cffaee3a6efdac3143f78967`  
		Last Modified: Fri, 17 Apr 2026 00:40:02 GMT  
		Size: 16.0 MB (16030273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77254010d09a671c64ad0799c2db74e7c6aa0de7990e4b960a4b00470c80478`  
		Last Modified: Fri, 17 Apr 2026 00:40:01 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f51948a04005913d751b25259dadfe540dbbf1e4e44320378607b4d3952458e`  
		Last Modified: Mon, 08 Jun 2026 22:46:14 GMT  
		Size: 7.0 MB (6964894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:b58056ce3d7572e5342f12821a68d4853eec3bd4c142b3cda504ee3361fae964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.2 KB (706203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b13365ae24163971a77236816081912c0a76bcbc75f57c9e7109c7353da50f`

```dockerfile
```

-	Layers:
	-	`sha256:3bc61751789292aa3be4e18de766b37fb64ab7051d941b3bec6caff39d2d40d7`  
		Last Modified: Mon, 08 Jun 2026 22:46:14 GMT  
		Size: 698.0 KB (697996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5dd00c4f34222ff7b31b747c955a2d4f3c8e8516b48884d2625f4eb8aab8da1`  
		Last Modified: Mon, 08 Jun 2026 22:46:14 GMT  
		Size: 8.2 KB (8207 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.22` - linux; 386

```console
$ docker pull hylang@sha256:b07e76ba57d81d2c80832319789e0f2650cec79cdbf5d112a805a4740f6db6d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27221976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5de84b1e33aefeded5c71dcb01f1d1e37d878f15d9eb800b7a8d406c24ce6f7`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 05:55:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 05:55:59 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 05:55:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 05:55:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 17 Apr 2026 05:55:59 GMT
ENV PYTHON_VERSION=3.11.15
# Fri, 17 Apr 2026 05:55:59 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Fri, 17 Apr 2026 06:00:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 06:00:31 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 06:00:31 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:48:15 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:48:15 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:48:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:48:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7db66acce49090c649f7d3afa599b5f0b706312dca19f11949d6b94753e6b8a`  
		Last Modified: Fri, 17 Apr 2026 06:00:38 GMT  
		Size: 455.4 KB (455437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1545d317034c64b483d0912dcd6fd4bd2986eda2106a2ab9cbc68a18c32790c1`  
		Last Modified: Fri, 17 Apr 2026 06:00:39 GMT  
		Size: 16.2 MB (16176615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a4041bc695d3522ccd88f6b0eb251511570e607c77e05d39734879cd7f3372`  
		Last Modified: Fri, 17 Apr 2026 06:00:39 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfeefb9601d7c4f2cd3b87cf86ebece1f3758d4471e63545f643bface6ec2614`  
		Last Modified: Mon, 08 Jun 2026 22:48:21 GMT  
		Size: 7.0 MB (6964954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:a151bbefcc7c938a772c2ffa36dd2c4a783b89d2836009994e4f7fb9568983e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.0 KB (705985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d498804a82cc0b82dd5bb492e0cfb29a90c33c7c24144828e6115617544835`

```dockerfile
```

-	Layers:
	-	`sha256:07a8b293be1c4d715c69b8ffb9f09bd5582d7aa9cd6168a87a7e6369f66399f5`  
		Last Modified: Mon, 08 Jun 2026 22:48:21 GMT  
		Size: 697.9 KB (697915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edc87cf637c3fd3fca018776231d96728ba9a2e4f8837bedce902357a739dfaa`  
		Last Modified: Mon, 08 Jun 2026 22:48:21 GMT  
		Size: 8.1 KB (8070 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.22` - linux; ppc64le

```console
$ docker pull hylang@sha256:d6b7f7b8c90e5a47af1803d7e35efa25ddb5c8a18d4b577045d5bca986eeea72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.8 MB (27837045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4a803c79758067dd3e65e773b7b0bb44646749fe22a42afc588b56f4ecfe3b4`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 01:45:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 01:45:13 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 01:45:13 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 01:45:13 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 17 Apr 2026 01:45:13 GMT
ENV PYTHON_VERSION=3.11.15
# Fri, 17 Apr 2026 01:45:13 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Fri, 17 Apr 2026 01:57:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 01:57:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 01:57:37 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 23:21:37 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 23:21:37 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 23:21:37 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 23:21:37 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6535d603abd5fcf706978ed3c1d5730eecc849310feff44ea8ce5422f4cacb32`  
		Last Modified: Fri, 17 Apr 2026 01:54:57 GMT  
		Size: 457.7 KB (457732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cbf8bc8fb087171baddaf342940c9718a4618c269701f98d0cb58163ba1678`  
		Last Modified: Fri, 17 Apr 2026 01:57:53 GMT  
		Size: 16.7 MB (16677208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d285d1359f06018d68e88943dda31549531ba645e4826d0741c1f69553f01ef0`  
		Last Modified: Fri, 17 Apr 2026 01:57:52 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8353170ac3b764ee09ac28c3f015a6c77f304e8fd95371d6059290f8c19eb62`  
		Last Modified: Mon, 08 Jun 2026 23:21:53 GMT  
		Size: 7.0 MB (6965199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:404702179772cfd80a597c9afbcf4d8145c25e5a511a022ee7b7d88cf125f41c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **704.2 KB (704169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae54ae0f600b7b6c55c5a793f6df67cb862ac235557f0e7df6db30424dd72504`

```dockerfile
```

-	Layers:
	-	`sha256:3a98a149d75c4ab9740810773bde5dea0eb742c4c0e0fffbcc04b853efb0c776`  
		Last Modified: Mon, 08 Jun 2026 23:21:52 GMT  
		Size: 696.0 KB (696023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:492e45537ea32eee7f47ac7a2cd549e3a1a902543003e8d35725f313d875426f`  
		Last Modified: Mon, 08 Jun 2026 23:21:52 GMT  
		Size: 8.1 KB (8146 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.22` - linux; riscv64

```console
$ docker pull hylang@sha256:0d0250fd5ea92591840f7eb6d72b531af0d69f991357876c5a20d5d4f4f2e1a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26829021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972f89733cab6fd1ef897d87d2df1cc27cd9640717e8b0e56ed271fb07e73673`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 17 Apr 2026 07:18:45 GMT
ADD alpine-minirootfs-3.22.4-riscv64.tar.gz / # buildkit
# Fri, 17 Apr 2026 07:18:45 GMT
CMD ["/bin/sh"]
# Sun, 19 Apr 2026 09:05:48 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 19 Apr 2026 09:05:48 GMT
ENV LANG=C.UTF-8
# Sun, 19 Apr 2026 09:05:48 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sun, 19 Apr 2026 09:05:48 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sun, 19 Apr 2026 09:05:48 GMT
ENV PYTHON_VERSION=3.11.15
# Sun, 19 Apr 2026 09:05:48 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Sun, 19 Apr 2026 10:07:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Sun, 19 Apr 2026 10:07:39 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 19 Apr 2026 10:07:39 GMT
CMD ["python3"]
# Thu, 28 May 2026 12:39:01 GMT
ENV HY_VERSION=1.3.0
# Thu, 28 May 2026 12:39:01 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 28 May 2026 12:39:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 28 May 2026 12:39:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:fbc07c8b85a3c60e503ffd0cbe3e1b3947fd65764784e1bd9d943ac21097cce7`  
		Last Modified: Fri, 17 Apr 2026 07:19:08 GMT  
		Size: 3.5 MB (3520880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aeed008a6d8d1e40ebaae2c80002f0322389f1116f4720d7b5fd2a403859e89`  
		Last Modified: Sun, 19 Apr 2026 09:37:50 GMT  
		Size: 455.3 KB (455335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c9686507900006e5716795ff8b696209b16209d914c4e45894b61711895178`  
		Last Modified: Sun, 19 Apr 2026 10:08:30 GMT  
		Size: 15.9 MB (15888950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5b2937cdf31b1757b266fdf79171299e97a3c3883641413283c60e6e7b7adf`  
		Last Modified: Sun, 19 Apr 2026 10:08:28 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1ad8e9f91ef9ab83b7138bcbb225c68d66db16a6c13b4bdd3b17b94a9a5012`  
		Last Modified: Thu, 28 May 2026 12:39:46 GMT  
		Size: 7.0 MB (6963607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:856737d044bdb2b7138a420405b8af64f6fd1aa9dd1e3f9eb58e8a1edc66e6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **704.2 KB (704166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5518e59c0704cb3cd98c24af0407fa2ab4c49d1698b588c97078485e466d8157`

```dockerfile
```

-	Layers:
	-	`sha256:ef4c4f93c261458640dbb38e83a586950f8dd6f040741f7a1daff554c94be43b`  
		Last Modified: Thu, 28 May 2026 12:39:44 GMT  
		Size: 696.0 KB (696019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00de9b9051293ae511e50206233aded89653ace88e8aaed58a292550ed05047b`  
		Last Modified: Thu, 28 May 2026 12:39:44 GMT  
		Size: 8.1 KB (8147 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.22` - linux; s390x

```console
$ docker pull hylang@sha256:5dfee55f29d25cbc74e758cf1eaeeacfe890ace1037cfae8a75c1aec850f976e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27507908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac35e65ebbd8af28ce3d8d73f45ee484e81e2309acb014d1ce199f06c85deec6`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 02:16:31 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 02:16:31 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 02:16:31 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 02:16:31 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 17 Apr 2026 02:16:31 GMT
ENV PYTHON_VERSION=3.11.15
# Fri, 17 Apr 2026 02:16:31 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Fri, 17 Apr 2026 02:24:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 02:24:29 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 02:24:29 GMT
CMD ["python3"]
# Mon, 08 Jun 2026 22:56:58 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:56:58 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:56:58 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 08 Jun 2026 22:56:58 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1fdcb8ad0e779755845989eacbda8ae5c94610f08898bcfa49aa15041fcbba0`  
		Last Modified: Fri, 17 Apr 2026 02:23:58 GMT  
		Size: 456.0 KB (456002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3703b9949bedc421adc9c462b164141cec6e4c187a1d3ecec01ee6e39c75097`  
		Last Modified: Fri, 17 Apr 2026 02:24:40 GMT  
		Size: 16.4 MB (16432753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3859ec1efe80c1f6857deb8d0409991b3bdabd87b5aed049ef6c623a4c62b2c2`  
		Last Modified: Fri, 17 Apr 2026 02:24:40 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c973c2884bd9040eccd250ef64e13e283a02920b4ba6de6140c9f63bc71d263a`  
		Last Modified: Mon, 08 Jun 2026 22:57:09 GMT  
		Size: 7.0 MB (6965032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:1c47da84cae8ab8e4e1d5bddf393af8c9b1b07dc72cf5773645e45d329226366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **704.1 KB (704092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b4746a58e09fdce15aebae4ded364b40aa14867a430160661e49b956f6b63e`

```dockerfile
```

-	Layers:
	-	`sha256:510f0da39aa30a16022724a23d2b24e4bc65b1e96a8fb1f0c0e50fa8e58f9541`  
		Last Modified: Mon, 08 Jun 2026 22:57:09 GMT  
		Size: 696.0 KB (695989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d9291f532ea99dfb181a253ac69d5e83a43d5f1e04bff88788780b7e2289f6f`  
		Last Modified: Mon, 08 Jun 2026 22:57:09 GMT  
		Size: 8.1 KB (8103 bytes)  
		MIME: application/vnd.in-toto+json
