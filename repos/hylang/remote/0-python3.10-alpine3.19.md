## `hylang:0-python3.10-alpine3.19`

```console
$ docker pull hylang@sha256:6c50ffe804c66f68ae6c7831a9565fc7f5b5bb04d0ef207c2fe31ec74c179c43
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

### `hylang:0-python3.10-alpine3.19` - linux; amd64

```console
$ docker pull hylang@sha256:22dbe31ed5e98ceb0189fc057cca0d8f75b22f2775f02a671b29174a540341c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23514765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e77c783442282c4514f0e47630342bd5ea753eb4cb417d247c6df562e441fb`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 29 Aug 2024 19:15:55 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 19:15:55 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.10.14
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
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
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb7c4ea4cd654e86a0a5a4e648139bfa4da78971fc4bc972622db5b4ac76e9e`  
		Last Modified: Fri, 06 Sep 2024 23:25:29 GMT  
		Size: 627.9 KB (627921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bad3b808f40245c6eebdb0210f385e97a98e5ca5b303ad4f5ec7c703f033893`  
		Last Modified: Fri, 06 Sep 2024 23:25:29 GMT  
		Size: 12.2 MB (12215803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28978ce9af6b330929286fcb5b29599e63f215c7ce0915ab6da55c873c19c6a4`  
		Last Modified: Fri, 06 Sep 2024 23:25:29 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ca6340b682d171dc429618b9a4d1cd0a876b7e9f548ed24fba65c8dffb1fe9`  
		Last Modified: Fri, 06 Sep 2024 23:25:29 GMT  
		Size: 3.1 MB (3081749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ecd74cbb31696455c8a195c67704f1f9edc2038e2f173447d5ebd910eacabe4`  
		Last Modified: Sat, 07 Sep 2024 00:10:56 GMT  
		Size: 4.2 MB (4169356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:4643ccf99311b29fcf867c3e08cd35713a9cf4636dac29ec6b73a3e1e07184f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1044743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abe790d76bc70e30d3ad9b0ebf3162e71a8598940432ff4d2d78c16ad2c3e9e2`

```dockerfile
```

-	Layers:
	-	`sha256:98fda6f4805886958ed26808cd8496ff6a05912e1106ac85ef4f4e5bebe526fa`  
		Last Modified: Sat, 07 Sep 2024 00:10:57 GMT  
		Size: 1.0 MB (1036231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfe11154936053b8e2fe6d446bb5c037c9ed9a13d15029a219b226666a581d6f`  
		Last Modified: Sat, 07 Sep 2024 00:10:56 GMT  
		Size: 8.5 KB (8512 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-alpine3.19` - linux; arm variant v6

```console
$ docker pull hylang@sha256:83d5ba57ceef2fdcad2c9a431eaaed5082e7f8b2f62805c2c9e60a0259aa03aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22923146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:378e843524904878573e59c1226a70933f9a0bfc9e8f681270386f0103493d73`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 29 Aug 2024 19:15:55 GMT
ADD file:87d4cb9e99b4a12939a030198a62d49f1c5b7856f27d62fea0e948cd2120d51d in / 
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 19:15:55 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.10.14
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
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
	-	`sha256:8922ced57063579c37aeb21c1c664433762d26f8051e187a63b559c21b36da53`  
		Last Modified: Fri, 06 Sep 2024 22:49:59 GMT  
		Size: 3.2 MB (3176391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a39bdf9d326d55be66a6472913d0bdbe3b64af11a3fa17f368b4581b594e62`  
		Last Modified: Sat, 07 Sep 2024 10:50:50 GMT  
		Size: 628.8 KB (628820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce5f700df5cde24892a5cb39abc66ffb26e48cb046cd50f9bd78c4447dfb382`  
		Last Modified: Sat, 07 Sep 2024 11:47:18 GMT  
		Size: 11.9 MB (11866001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b6884a213d3dd1b80300e8a572ca84652ecd05735e72374912f5b29ba5b302`  
		Last Modified: Sat, 07 Sep 2024 11:47:17 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161fa61ce1dfd8c93cc2be082c1a113df6c1c7462da250b68e61d77dce596823`  
		Last Modified: Sat, 07 Sep 2024 11:47:18 GMT  
		Size: 3.1 MB (3081760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e44cbf5249210f032df9bc7e13a415bd50b7bc52e5a0963bf9110f80f6a66f`  
		Last Modified: Sat, 07 Sep 2024 13:41:35 GMT  
		Size: 4.2 MB (4169943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:99f67eec79d007efaf0696dced94eeb0bed9bf699f8f0f6e87b60da63c258d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 KB (8381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68960331ab40d2fdac89fa7822e4bc78da97199cea57264cbc05f66b49deddf`

```dockerfile
```

-	Layers:
	-	`sha256:285b00e78fe0baf8b392ab26a9ea469e5c6a28d125d4b622216dcbe672fa1b41`  
		Last Modified: Sat, 07 Sep 2024 13:41:34 GMT  
		Size: 8.4 KB (8381 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-alpine3.19` - linux; arm variant v7

```console
$ docker pull hylang@sha256:52b4e830a50b27094e869b31ecdb7d0e189960ad9492e9439a6abbbb9d66a799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22255682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0781412e3e00258a17611658625ab95456fd2b45d0c1366d4ec10c454a545bdd`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 29 Aug 2024 19:15:55 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 19:15:55 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.10.14
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
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
	-	`sha256:426a5537ab470cede64a1b269dbc9f485fa674bec59555cdaa5a1c96e6675b0d`  
		Last Modified: Fri, 06 Sep 2024 22:08:37 GMT  
		Size: 2.9 MB (2927664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2773a0915bfcbc78e079faa18251ac0d879f0f82697ee83220c411ab06dd1bb`  
		Last Modified: Sat, 07 Sep 2024 11:07:13 GMT  
		Size: 628.0 KB (627974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553602f3fad8fd2e21148441138eee22fa76812304ec8aa151ffbcdbd5c766f6`  
		Last Modified: Sat, 07 Sep 2024 12:06:20 GMT  
		Size: 11.4 MB (11448388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10bc3b7763f47deb3d83ab0846ed9ad16a39dc7942fb2e2d0615b8c358b051d8`  
		Last Modified: Sat, 07 Sep 2024 12:06:20 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3547b68a1639283d9f25335ecaaf14e4da17e633a18da9ac4eff82e29f5f6224`  
		Last Modified: Sat, 07 Sep 2024 12:06:20 GMT  
		Size: 3.1 MB (3081775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1711792eef50ab65c8efcbebefdf3422a111f3016f7aa9c176de5755c094d7a`  
		Last Modified: Sat, 07 Sep 2024 14:24:05 GMT  
		Size: 4.2 MB (4169651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:ee6725507222c95cb2601be93b3df32afecfde6604e9b6ba68abc886bc4475ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1047731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37ecc2590d43d5d5d5acda0e2d1a9de1090f7ccf62cc2b3541cfad909749908`

```dockerfile
```

-	Layers:
	-	`sha256:0773a901e491247287887881f5e8cdf565b6d7817c99e126a66e6c3e59792fd2`  
		Last Modified: Sat, 07 Sep 2024 14:24:04 GMT  
		Size: 1.0 MB (1039131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0a89773fba285996754303612d4c4ed7d7ba805c91b6586bc1f172abfd84ac0`  
		Last Modified: Sat, 07 Sep 2024 14:24:04 GMT  
		Size: 8.6 KB (8600 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:720b5e562c961b04691e9d63db6ffb979014fcd5f05f1d4ae5e2677c14ce170c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23534852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b872b4ae6a0be194a5710cea70b31e6df9f6c56dff2cb396518c5637523a56`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 29 Aug 2024 19:15:55 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 19:15:55 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.10.14
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
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
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf2f2790992c8c78211ff5181c3fb0eb2710f0d4ab4c29278770b838db532c2`  
		Last Modified: Sat, 07 Sep 2024 10:20:39 GMT  
		Size: 630.3 KB (630335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921843cb30a63fd6bf528bce6c367f74de8b41b54c5e994165ce46a485f85ab2`  
		Last Modified: Sat, 07 Sep 2024 11:07:55 GMT  
		Size: 12.3 MB (12293791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571a4fe23d58e942a73686e017577a032786ca206d27d6ef97a768369afb7a9c`  
		Last Modified: Sat, 07 Sep 2024 11:07:54 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7073148b374a17e3665487ec3945655f3c3af6eae59ac8f498b14013d3491f17`  
		Last Modified: Sat, 07 Sep 2024 11:07:54 GMT  
		Size: 3.1 MB (3081747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86f6202bae10cc22dac1d349e663c2512ef3e47a410df77406fd5e7f7fb692d`  
		Last Modified: Sat, 07 Sep 2024 13:56:49 GMT  
		Size: 4.2 MB (4169646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:149efb700a412f07824f867bf5ffb8d14c8079d26b81c74f9f0e9fe9258a3df1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1045196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259c7123d472ea39dabe4df39edacdcb2e084d74118e17cd6f6f5689932e47f4`

```dockerfile
```

-	Layers:
	-	`sha256:e95d9e995f1a80fae8174eb8be581748c9e89e80c5f62988df9f5c3830a6632f`  
		Last Modified: Sat, 07 Sep 2024 13:56:49 GMT  
		Size: 1.0 MB (1036287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9908e761e78705e310723056dc897c17869a5fbda4d4c03588b3b1d85dc71c1`  
		Last Modified: Sat, 07 Sep 2024 13:56:49 GMT  
		Size: 8.9 KB (8909 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-alpine3.19` - linux; 386

```console
$ docker pull hylang@sha256:e152ccb73c14a44efd3bb5a27a15d4707f625e07a46573c5535984883e4ca13c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23574961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1b73ef4ad68b2b122e3750ae70f38e301db45ce023f1de935d86cf0b7f8c84`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 29 Aug 2024 19:15:55 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 19:15:55 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.10.14
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
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
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9afc3f14ad7501519764297e34592e0755d21d08ea0fef6f21479680a2dc3ca`  
		Last Modified: Fri, 06 Sep 2024 23:26:16 GMT  
		Size: 628.4 KB (628406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33ef7760c77b1e4c179a614179d169ee6e7824cc37e12d44998648e1af626cf1`  
		Last Modified: Fri, 06 Sep 2024 23:26:16 GMT  
		Size: 12.4 MB (12441480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df96305a33364d1408d5ef4f30020865db10fb76ff591fb64367eea2a08cf667`  
		Last Modified: Fri, 06 Sep 2024 23:26:16 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ddb34ea753deed2eb8e002ae9687419657e6999051ecfef7f71ae6d4390d0f`  
		Last Modified: Fri, 06 Sep 2024 23:26:16 GMT  
		Size: 3.1 MB (3081755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f41fd389fa5eb309cc121f8b9be616de490afa3f751666dffc02b1ba755be1e`  
		Last Modified: Sat, 07 Sep 2024 00:10:43 GMT  
		Size: 4.2 MB (4169487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:8f177a482b134d2469510ab6bbab00dcbf51ee0276cbddfd6b0af6f89d19f409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1044685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:869d69af3d0a8754bc35c369157cd0e8dc86738d5a5eec9b541b8baad61a154f`

```dockerfile
```

-	Layers:
	-	`sha256:7c203479448e7f72526aa6eba81ae03f6c87657c987365e47c78499e6f7af979`  
		Last Modified: Sat, 07 Sep 2024 00:10:43 GMT  
		Size: 1.0 MB (1036206 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b08f27a77657b66a65435de55a4c5a3fa07280a1135748fedd5a7f9fcdce9271`  
		Last Modified: Sat, 07 Sep 2024 00:10:43 GMT  
		Size: 8.5 KB (8479 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-alpine3.19` - linux; ppc64le

```console
$ docker pull hylang@sha256:f27976327349176843748579511989b5c06c61ca28e5470f4b331e6429e3847b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23968873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59b3824c924b3b6cf44e229fe69a57225f8bf869ec49d0e80d80c9043ba3c79`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 29 Aug 2024 19:15:55 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 19:15:55 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.10.14
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
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
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5749dced5c3ea885609ac4ce0f87b1f345b6e9df997e9a8b0aaceac5eaaa6e3f`  
		Last Modified: Sat, 07 Sep 2024 09:58:37 GMT  
		Size: 630.8 KB (630837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ef943a2b850da544bbb4193723c258ac3af916c8dc6947383b54872e85a11e`  
		Last Modified: Sat, 07 Sep 2024 10:57:54 GMT  
		Size: 12.7 MB (12721982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baeeddc7e166b723a933d51226076e889bd9dd0e78b19e8a6587e464dbf34a82`  
		Last Modified: Sat, 07 Sep 2024 10:57:53 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e7ab019b72b4a3169a9ae53ce2d98dadaee2a66d82b5603729797f2688912e`  
		Last Modified: Sat, 07 Sep 2024 10:57:54 GMT  
		Size: 3.1 MB (3081732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8830c9c882dcd93ab19b05a86ede8cea687825b4d8353668d4cd2d28a21d9c7`  
		Last Modified: Sat, 07 Sep 2024 13:58:46 GMT  
		Size: 4.2 MB (4169624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:4e83a2f6a1263637b3018c1c42fceac19e06ca58b7b0532777e503dadf892489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1042877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc693a3be3a8dfbdabde30392056fac7c2ef500b0761eb3848a7626a4cbe79d1`

```dockerfile
```

-	Layers:
	-	`sha256:3ea159bf219305cadc6acaf975df05cbc13aa7ea956f3adcd3be78107bb3d387`  
		Last Modified: Sat, 07 Sep 2024 13:58:46 GMT  
		Size: 1.0 MB (1034311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7789c04c5e9a43147be86366fef74032b1cbcccc38df2b6b44ea87532f8fb85`  
		Last Modified: Sat, 07 Sep 2024 13:58:45 GMT  
		Size: 8.6 KB (8566 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-alpine3.19` - linux; s390x

```console
$ docker pull hylang@sha256:a4938763de0f09b55f01a83c5520377fc622a2868b10696ec50d5678108befdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23623024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c511b264af7a098fa0b37b76619e461812251f2f2be01b9a5bad2f4a72d47d6`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 29 Aug 2024 19:15:55 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 19:15:55 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.10.14
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
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
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf180b200a9685ef5f8a9f8ba267cdaf8e59fe28f3b974eee5118a914d262ab`  
		Last Modified: Sat, 07 Sep 2024 09:10:44 GMT  
		Size: 629.0 KB (628993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ade7f5d6a0e35d2dd5e2208fb9f66696182a8c8b3ae906d3838291b972b827`  
		Last Modified: Sat, 07 Sep 2024 09:59:38 GMT  
		Size: 12.5 MB (12489307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15aae961598def738bf22a3a510839332f3e1eacb6346751237474511c51770`  
		Last Modified: Sat, 07 Sep 2024 09:59:38 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d49996ee0dabe5f245cdf22b92dc01b89ac16050b904fb845cfe03c194bef7`  
		Last Modified: Sat, 07 Sep 2024 09:59:39 GMT  
		Size: 3.1 MB (3081702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07021e82b68055f89b6263e7234ec27ec9ce6ac4dc56e2cfe738f51a18c528d`  
		Last Modified: Sat, 07 Sep 2024 11:52:27 GMT  
		Size: 4.2 MB (4169436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:ca84dd49f1c4de20a8fc8d00ce8b6075e60744b86288432a2afdac4ce3f6a7e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1042801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d9a29b684ae7eaa4908ae00c2da07642e7013d369a8c5afd4101474ba20a786`

```dockerfile
```

-	Layers:
	-	`sha256:99a8f9a8cc8398c8f407d292b9a51bb89b7af7ecfd7bf7764b1a7769c01a3a44`  
		Last Modified: Sat, 07 Sep 2024 11:52:27 GMT  
		Size: 1.0 MB (1034277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65aa9446c1a72bf57bf86450d623a9def28223e870f931b19d4d744a1b490e5d`  
		Last Modified: Sat, 07 Sep 2024 11:52:26 GMT  
		Size: 8.5 KB (8524 bytes)  
		MIME: application/vnd.in-toto+json
