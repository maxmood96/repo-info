## `hylang:python3.11-alpine3.20`

```console
$ docker pull hylang@sha256:09408886c6ba191927558ef65a99fa8eb8294b4f8df36d5699c50651a7e0dd80
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

### `hylang:python3.11-alpine3.20` - linux; amd64

```console
$ docker pull hylang@sha256:25dc8da0273ac63fdf20640c71a482827a072795359562e3ede5192b5ff9277f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26085408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d2e459820a4ac54b183d012548068ff573464a29c3d3024f51d65de4b392880`
-	Default Command: `["hy"]`

```dockerfile
# Sun, 07 Jul 2024 22:31:37 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Sun, 07 Jul 2024 22:31:37 GMT
CMD ["/bin/sh"]
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 07 Jul 2024 22:31:37 GMT
ENV LANG=C.UTF-8
# Sun, 07 Jul 2024 22:31:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sun, 07 Jul 2024 22:31:37 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_VERSION=3.11.9
# Sun, 07 Jul 2024 22:31:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sun, 07 Jul 2024 22:31:37 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_PIP_VERSION=24.0
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Sun, 07 Jul 2024 22:31:37 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sun, 07 Jul 2024 22:31:37 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee56b2bb681231de28a0b9ef07f6b2cc88281aae9eb609811ffeb0be2aee4d7`  
		Last Modified: Mon, 22 Jul 2024 23:19:49 GMT  
		Size: 461.8 KB (461798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed00986c027d83e0da7822f5b24acbbd8839f0a0d113b50fbb3b09c2a44d1c7`  
		Last Modified: Mon, 22 Jul 2024 23:19:49 GMT  
		Size: 12.7 MB (12672628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3cc4ee895667bf789d843fcfda3fcbc91247f09f2beac68174d743dc2b765f1`  
		Last Modified: Mon, 22 Jul 2024 23:19:49 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f60bffdf79a467e4b3580b524120f7ebb3e0fd9c164464149eb6c68032dd7d`  
		Last Modified: Mon, 22 Jul 2024 23:19:49 GMT  
		Size: 3.1 MB (3130004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c85e5ab6a41f1ce17105f52fa432343771dc35225413e037b15c64ba34507a7`  
		Last Modified: Tue, 23 Jul 2024 00:08:26 GMT  
		Size: 6.2 MB (6197857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:3f58c37e07ad3321bfcaafd05270aa15f60f9ca5d7cd4a6bda06112d2add365b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.6 KB (666619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083b5bb1368d79a0a9ae4c4565ab6b63296a2be583a038cab297994438b69e9f`

```dockerfile
```

-	Layers:
	-	`sha256:d6e8c37797c4dbafec28c32226972c421543373f83a3d716b7d7f1e0cbe0e33c`  
		Last Modified: Tue, 23 Jul 2024 00:08:26 GMT  
		Size: 658.1 KB (658111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b62d8a74fbe7f0238fb480b0ceca51e5b918046eba5db33c4ac5ffc367e0d32`  
		Last Modified: Tue, 23 Jul 2024 00:08:26 GMT  
		Size: 8.5 KB (8508 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.20` - linux; arm variant v6

```console
$ docker pull hylang@sha256:8b59c15bdec001e7211a3581f1c5542db7f782bea206ad85f52d24175e060571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25429049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe0db4baeff3cbf9506d1b0a63eb43346682c52e62943a0ccb65c8f994ede537`
-	Default Command: `["hy"]`

```dockerfile
# Sun, 07 Jul 2024 22:31:37 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Sun, 07 Jul 2024 22:31:37 GMT
CMD ["/bin/sh"]
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 07 Jul 2024 22:31:37 GMT
ENV LANG=C.UTF-8
# Sun, 07 Jul 2024 22:31:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sun, 07 Jul 2024 22:31:37 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_VERSION=3.11.9
# Sun, 07 Jul 2024 22:31:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sun, 07 Jul 2024 22:31:37 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_PIP_VERSION=24.0
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Sun, 07 Jul 2024 22:31:37 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sun, 07 Jul 2024 22:31:37 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126e5ccd77b81560c6b7069081d2336863a705860fc28b7e2f94e7716213c5c5`  
		Last Modified: Tue, 23 Jul 2024 09:20:45 GMT  
		Size: 462.6 KB (462569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b0c13accfa6cfee5c1db8eab924017def6849d345edb815bdfb3df152a6165`  
		Last Modified: Tue, 23 Jul 2024 09:58:44 GMT  
		Size: 12.3 MB (12273107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68653edde3ea77201262d4d5411a616aae67ddf5720acbb23e6f71a9e956ada3`  
		Last Modified: Tue, 23 Jul 2024 09:58:44 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c44f8d047a89cd605670f2eb5614f8f60f84c415a8a58b76a103836377359d`  
		Last Modified: Tue, 23 Jul 2024 09:58:45 GMT  
		Size: 3.1 MB (3130018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de04a3fac76034e364f25138309254b0d46e8b4cbd39a40b786a88004a6b24f`  
		Last Modified: Tue, 23 Jul 2024 12:59:17 GMT  
		Size: 6.2 MB (6197936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:16d691fc2f202b0783ffb10c8d5d046cc03bfda35eb0737ac0f9fc21fba2511e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 KB (8378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dee709c1c73035bc34956349a1781f2101279024dfc083ff2cb95b13e86bbda`

```dockerfile
```

-	Layers:
	-	`sha256:3ea8682bdec16240dc43b12c5b84bccdebe4e3666843871e6b2afb21cae8f52e`  
		Last Modified: Tue, 23 Jul 2024 12:59:16 GMT  
		Size: 8.4 KB (8378 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.20` - linux; arm variant v7

```console
$ docker pull hylang@sha256:db6098af9fd4ddafcd0949452a5e969a18c212cf05357f0b0ba21a7a4388f980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24735255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d5948060a6320368dd34064a6c2cedee0170c64f758e2fbba72819f51be451`
-	Default Command: `["hy"]`

```dockerfile
# Sun, 07 Jul 2024 22:31:37 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Sun, 07 Jul 2024 22:31:37 GMT
CMD ["/bin/sh"]
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 07 Jul 2024 22:31:37 GMT
ENV LANG=C.UTF-8
# Sun, 07 Jul 2024 22:31:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sun, 07 Jul 2024 22:31:37 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_VERSION=3.11.9
# Sun, 07 Jul 2024 22:31:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sun, 07 Jul 2024 22:31:37 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_PIP_VERSION=24.0
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Sun, 07 Jul 2024 22:31:37 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sun, 07 Jul 2024 22:31:37 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
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
	-	`sha256:263ce6bc77ee83d912528cb01fd0cc058fcb592a302f363e704edda3473c3df7`  
		Last Modified: Wed, 24 Jul 2024 11:23:43 GMT  
		Size: 11.9 MB (11850404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7f11162112099b1dc0f61965a5348be22e16bdb0b3450da8d7f19396e5aad8`  
		Last Modified: Wed, 24 Jul 2024 11:23:43 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0193d83370cde67add0869904a8e3dd117cb5388804b6711b10397efe192f03`  
		Last Modified: Wed, 24 Jul 2024 11:23:43 GMT  
		Size: 3.1 MB (3129982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6319f83ad6f3f67e138ae3931a396f6d2c6307a3f8085054e6927f94da481fe`  
		Last Modified: Wed, 24 Jul 2024 19:16:31 GMT  
		Size: 6.2 MB (6197928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:2d8306d29fe1ee2957009b941a0272025467338cf38b5e97dd3347fdf57fa45d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.6 KB (669608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ed253d5597950c2510a5bf25ab7d0e7c5547a22af2b991a804c34d774e3bb0`

```dockerfile
```

-	Layers:
	-	`sha256:34b5696f39d15e005c71879d0fd4d5f4c490db7e4b98337e55b494513ae31021`  
		Last Modified: Wed, 24 Jul 2024 19:16:30 GMT  
		Size: 661.0 KB (661011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:108b8e02f1ae71b175079d881bc6cd8ff881fdbbc40e29ba087fe60205a4608f`  
		Last Modified: Wed, 24 Jul 2024 19:16:30 GMT  
		Size: 8.6 KB (8597 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:0369b7e8c7b0d9e2d4b048216db7d53730afcd76f0c56fc39d9a54f2aef88914
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26637508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b726263af6f2dd86b86427d7530d7dd9bd28998bc08cb16a55c37147661e064f`
-	Default Command: `["hy"]`

```dockerfile
# Sun, 07 Jul 2024 22:31:37 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Sun, 07 Jul 2024 22:31:37 GMT
CMD ["/bin/sh"]
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 07 Jul 2024 22:31:37 GMT
ENV LANG=C.UTF-8
# Sun, 07 Jul 2024 22:31:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sun, 07 Jul 2024 22:31:37 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_VERSION=3.11.9
# Sun, 07 Jul 2024 22:31:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sun, 07 Jul 2024 22:31:37 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_PIP_VERSION=24.0
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Sun, 07 Jul 2024 22:31:37 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sun, 07 Jul 2024 22:31:37 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2711f91d5f9c677eb6883af3f381a64f628a585ad46fcfcfeecf39228185c2b2`  
		Last Modified: Wed, 24 Jul 2024 04:24:38 GMT  
		Size: 463.8 KB (463841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295e5a578ce97f013e967edc018934ab3a697f6e8ef07676b83164b430192dde`  
		Last Modified: Wed, 24 Jul 2024 05:32:29 GMT  
		Size: 12.8 MB (12758664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bfa99e5076d4152b1cbafb761c351d09c210f3f1f30b7492747cb5b3e4c4f0`  
		Last Modified: Wed, 24 Jul 2024 05:32:28 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c898ad883ec8655d245739a9df6dbf0b5d26839520099621ee01aae325dba824`  
		Last Modified: Wed, 24 Jul 2024 05:32:29 GMT  
		Size: 3.1 MB (3129985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1bad37b25b881bb2d6136ad391ccdf98ad96e7f3d35db569c0bc7d5f256008`  
		Last Modified: Wed, 24 Jul 2024 15:30:37 GMT  
		Size: 6.2 MB (6197856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:a631eca9c65ea1e72842b5ca7d39759904b91578142cbab7d6e7070b345146d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.1 KB (667073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1caba13c704ec649604208e1872b9841cd542e406c231390b0f0025a42cbae80`

```dockerfile
```

-	Layers:
	-	`sha256:f3e94025d3449dc998d1910bad274f314fc34eb28e1e148204610fed64494018`  
		Last Modified: Wed, 24 Jul 2024 15:30:36 GMT  
		Size: 658.2 KB (658167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc78f66e9fc455ace1c3a2d28ef326743ddf90073ea163e49780b4b654ac23be`  
		Last Modified: Wed, 24 Jul 2024 15:30:36 GMT  
		Size: 8.9 KB (8906 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.20` - linux; 386

```console
$ docker pull hylang@sha256:2bc70cf93ad1aaed6c355541df3774bd7503d5f165b6bcaa33326d83fc6f87f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26126908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b100b6e998c3119627c174bbfa45948596d1e34b7c5c08f455f621e0cad6b0b1`
-	Default Command: `["hy"]`

```dockerfile
# Sun, 07 Jul 2024 22:31:37 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Sun, 07 Jul 2024 22:31:37 GMT
CMD ["/bin/sh"]
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 07 Jul 2024 22:31:37 GMT
ENV LANG=C.UTF-8
# Sun, 07 Jul 2024 22:31:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sun, 07 Jul 2024 22:31:37 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_VERSION=3.11.9
# Sun, 07 Jul 2024 22:31:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sun, 07 Jul 2024 22:31:37 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_PIP_VERSION=24.0
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Sun, 07 Jul 2024 22:31:37 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sun, 07 Jul 2024 22:31:37 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ded3441563202004b2104eb763a693f81904868f56b79cb6224cf143952b1a7`  
		Last Modified: Mon, 22 Jul 2024 22:26:29 GMT  
		Size: 462.2 KB (462182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464b5d2f17d74f2b5f9498aea6729de2bee878f04334f22aa468a4b73d8eebe0`  
		Last Modified: Mon, 22 Jul 2024 22:26:29 GMT  
		Size: 12.9 MB (12868513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c261bbdbe353a5e410de9a359c3c69b0f9fc7b18b39d7fdfca2f07b63aebb8`  
		Last Modified: Mon, 22 Jul 2024 22:26:28 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343b8c5e080fc8a34625f5cfb74d5c1cec4e72227789d82537d2fdf77e5ad0a5`  
		Last Modified: Mon, 22 Jul 2024 22:26:29 GMT  
		Size: 3.1 MB (3129995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2a16652892f56d450b72cee4bf51ed7bd1695dd6c6999c1091d6b9aa6d938a`  
		Last Modified: Mon, 22 Jul 2024 23:08:15 GMT  
		Size: 6.2 MB (6197919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:9c760b47ee4474fcfb6c5ed6211dff5706273376933341cb422c2eee684a4367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.6 KB (666563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:919049c0323d919344c9acc56d9b22a3e1fcf635e6a0df2f14241930ec323f31`

```dockerfile
```

-	Layers:
	-	`sha256:17698d1d7861fec545b7e8422835aeb00ca56b4ecd3a880146b64a5e74c06f2a`  
		Last Modified: Mon, 22 Jul 2024 23:08:15 GMT  
		Size: 658.1 KB (658086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2cf8a37cf5f5a0ae537709c8db931f53ba4fb6bbc77d938c878cca43c7d6bce`  
		Last Modified: Mon, 22 Jul 2024 23:08:15 GMT  
		Size: 8.5 KB (8477 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.20` - linux; ppc64le

```console
$ docker pull hylang@sha256:1a33eea1fbd27f084aaa1fb2693b30d93815dee54ed93b5b602e00251b75ce4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 MB (26533954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:467eb92a06075033a3d64c73086a319d70c9326dda024b87e11ccb585b5e5f8b`
-	Default Command: `["hy"]`

```dockerfile
# Sun, 07 Jul 2024 22:31:37 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Sun, 07 Jul 2024 22:31:37 GMT
CMD ["/bin/sh"]
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 07 Jul 2024 22:31:37 GMT
ENV LANG=C.UTF-8
# Sun, 07 Jul 2024 22:31:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sun, 07 Jul 2024 22:31:37 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_VERSION=3.11.9
# Sun, 07 Jul 2024 22:31:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sun, 07 Jul 2024 22:31:37 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_PIP_VERSION=24.0
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Sun, 07 Jul 2024 22:31:37 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sun, 07 Jul 2024 22:31:37 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
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
	-	`sha256:ead1cee62e650ef1d369660d0555e6ce75839546ac88c16a6c7cf59b09edb34d`  
		Last Modified: Wed, 24 Jul 2024 07:55:44 GMT  
		Size: 13.2 MB (13170125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d824c4988cad5adaea869de8e590494cbb820e6d88d3eef6ed776a03b9c99876`  
		Last Modified: Wed, 24 Jul 2024 07:55:43 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22639717ecaab5e476c68995caeea6af5f44ace44522c82ca364375d48e74222`  
		Last Modified: Wed, 24 Jul 2024 07:55:43 GMT  
		Size: 3.1 MB (3129976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c144599f0e8595f1fa5bac9e5fe4681d82f9f0085408c9f9bc10f2c708d9c7d8`  
		Last Modified: Thu, 25 Jul 2024 02:06:04 GMT  
		Size: 6.2 MB (6197844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:32fecf2c560f2684cec27090230e6b96119d615377110667b6bd775c5d8e1c51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.8 KB (664756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:decd1feaa8f84e7303b53d4308a6d82b0865586046b5a506de63244963bc704c`

```dockerfile
```

-	Layers:
	-	`sha256:d287aab6d2e29ca5390d029d924dd34970de398fed246f7bf58bf35e824fd330`  
		Last Modified: Thu, 25 Jul 2024 02:06:03 GMT  
		Size: 656.2 KB (656191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1226791ed89c8ea1d766dd2e95971e6842a55d35c842061d83a85d0e399a55d3`  
		Last Modified: Thu, 25 Jul 2024 02:06:03 GMT  
		Size: 8.6 KB (8565 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.20` - linux; s390x

```console
$ docker pull hylang@sha256:d65339e2f1bc9dd58f1d3e5c44f78a5b72e3d8a556765cf85392e01fde0e7b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 MB (26241094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7bdc57f826039dd7d4d0e1ebc6ac8367cb7f11b0306be5fe0dad74fcefaf35`
-	Default Command: `["hy"]`

```dockerfile
# Sun, 07 Jul 2024 22:31:37 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Sun, 07 Jul 2024 22:31:37 GMT
CMD ["/bin/sh"]
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 07 Jul 2024 22:31:37 GMT
ENV LANG=C.UTF-8
# Sun, 07 Jul 2024 22:31:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sun, 07 Jul 2024 22:31:37 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_VERSION=3.11.9
# Sun, 07 Jul 2024 22:31:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sun, 07 Jul 2024 22:31:37 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_PIP_VERSION=24.0
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/e03e1607ad60522cf34a92e834138eb89f57667c/public/get-pip.py
# Sun, 07 Jul 2024 22:31:37 GMT
ENV PYTHON_GET_PIP_SHA256=ee09098395e42eb1f82ef4acb231a767a6ae85504a9cf9983223df0a7cbd35d7
# Sun, 07 Jul 2024 22:31:37 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sun, 07 Jul 2024 22:31:37 GMT
CMD ["python3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baecdfe02d59eacf44954894e7c2146a3d5c7099ff70061111d0789211a6fae0`  
		Last Modified: Wed, 24 Jul 2024 05:44:07 GMT  
		Size: 462.7 KB (462738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdb48798badcb9d57c36e5ecadc8d3335dd93995a71f83ee5908acb5c28a194`  
		Last Modified: Wed, 24 Jul 2024 06:55:29 GMT  
		Size: 13.0 MB (12989270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ef48985f8a68a2ef2711281ee7f1935ceed1355b74ca32e9e1add2e5849bd5`  
		Last Modified: Wed, 24 Jul 2024 06:55:29 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82fde7cb2854631bb8b1224fe5bc390e5934a872614b944a3bbd743750f4c6fa`  
		Last Modified: Wed, 24 Jul 2024 06:55:30 GMT  
		Size: 3.1 MB (3129986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5be9b22eb3c01892f5f7325aced4ab4ad1989fcebdde59f6a759358e8f0b68`  
		Last Modified: Wed, 24 Jul 2024 16:33:08 GMT  
		Size: 6.2 MB (6197804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:94666577a8902a2dd23e99502763fc3f51a92a7bac3d11509758b14c2ff6c8c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.7 KB (664678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eec33f8270d1e88768097cc8ce88a797144285a6fb15e411b5e99051b76001b`

```dockerfile
```

-	Layers:
	-	`sha256:1b43a13331da4206bb21c48251b04869be6ffc6808c6d825aafd00706b37bfe5`  
		Last Modified: Wed, 24 Jul 2024 16:33:08 GMT  
		Size: 656.2 KB (656157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6ccb4f4759638d7ea98ed66ed7b11f41ca82c2a6c956364c538167a3f48d48d`  
		Last Modified: Wed, 24 Jul 2024 16:33:08 GMT  
		Size: 8.5 KB (8521 bytes)  
		MIME: application/vnd.in-toto+json
