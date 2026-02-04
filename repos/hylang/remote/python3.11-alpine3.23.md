## `hylang:python3.11-alpine3.23`

```console
$ docker pull hylang@sha256:e92abe65cc55208106bdf4ef2facd7da8f58cd53c47fabc86ed82c85fc1a09b6
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

### `hylang:python3.11-alpine3.23` - linux; amd64

```console
$ docker pull hylang@sha256:7500e6681b710638d0f492a3d6b9f0530e9e14203acb4f51d8133c01c2621dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27315297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8454a08d9bac35d71e785d0fc5c94dc37f69d7622dec1f3f256b92fd6514cc`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:15:29 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:15:29 GMT
ENV LANG=C.UTF-8
# Wed, 04 Feb 2026 20:15:29 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:15:29 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 04 Feb 2026 20:15:29 GMT
ENV PYTHON_VERSION=3.11.14
# Wed, 04 Feb 2026 20:15:29 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Wed, 04 Feb 2026 20:26:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:26:00 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:26:00 GMT
CMD ["python3"]
# Wed, 04 Feb 2026 21:12:37 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:12:37 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:12:37 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Feb 2026 21:12:37 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca07fe076f12b62834e15448c6ec1858845fe8029d75d7ba1d1f6e7940ee649`  
		Last Modified: Wed, 04 Feb 2026 20:20:53 GMT  
		Size: 460.9 KB (460942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dafe251d3131d84dde86c5a4fb9672beca30c86adaed314cde03077205b426d`  
		Last Modified: Wed, 04 Feb 2026 20:26:07 GMT  
		Size: 16.0 MB (16017452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa340e77c3361ba75d12b0cf1ebf4be40465ef37250c57ae647b5cde12d890b7`  
		Last Modified: Wed, 04 Feb 2026 20:26:06 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a8412ed06b44054b1bdf33b479bbb236e2e8c71ce7fd47962bdde5ec210cc4`  
		Last Modified: Wed, 04 Feb 2026 21:12:44 GMT  
		Size: 7.0 MB (6974835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:c629613e0560a449feeae3445f50dd658c58038f010849b74b44104e340cfc0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.3 KB (709333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af623d9acff4b5195e049acd7e9ec064e983139df2d60bed1cff330763083f0e`

```dockerfile
```

-	Layers:
	-	`sha256:f974f38a34bd58c07805082834f45b747796b065683ca8a2f83676742a2e0f1a`  
		Last Modified: Wed, 04 Feb 2026 21:12:43 GMT  
		Size: 699.9 KB (699926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3db25824dba720ddb5e373bc42c637b6d0d2adf14d1b5fbaad2cbd708a8f7d7`  
		Last Modified: Wed, 04 Feb 2026 21:12:43 GMT  
		Size: 9.4 KB (9407 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.23` - linux; arm variant v6

```console
$ docker pull hylang@sha256:3d6ab3c0e76539106c076bd223b90f6831e39b889ff6f34c1a27533da2775020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26575756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a30aa45f5da51bb5008ecbaed360a1f96b15a51e70f53fafc1f96f8285041e`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:28:07 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:28:07 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 03:28:07 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 03:28:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 28 Jan 2026 03:28:07 GMT
ENV PYTHON_VERSION=3.11.14
# Wed, 28 Jan 2026 03:28:07 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Wed, 28 Jan 2026 03:35:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 03:35:03 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 03:35:03 GMT
CMD ["python3"]
# Wed, 28 Jan 2026 04:46:15 GMT
ENV HY_VERSION=1.2.0
# Wed, 28 Jan 2026 04:46:15 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 28 Jan 2026 04:46:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 28 Jan 2026 04:46:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885af615128c2ecb52058128093a464acd81bc244f04608683db3c7219bb21c9`  
		Last Modified: Wed, 28 Jan 2026 03:35:08 GMT  
		Size: 461.4 KB (461433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7091a3c5485774a95ec104bf8acd3f1c4b92da496c9c1f76f3d9e999a0e88b6`  
		Last Modified: Wed, 28 Jan 2026 03:35:08 GMT  
		Size: 15.6 MB (15569513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f57a444f52585c9e66fbcca58e04a9191b02a9fa77ba5d1528113b1f92cd74`  
		Last Modified: Wed, 28 Jan 2026 03:35:08 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a872a00f0fe85cc741d912cc1f6637f1a280a83c9b3013a1ca51fad9822fa442`  
		Last Modified: Wed, 28 Jan 2026 04:46:19 GMT  
		Size: 7.0 MB (6974739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:ffb6db98bfa9d90a99e17b7acf93d7274347cee7a1013752b409841bd943e1f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c7d9b750fc2b61ef593ae3bdd5f650edaf842e6037e2fceebd7318d0c69fd7`

```dockerfile
```

-	Layers:
	-	`sha256:af07a353ae555c244a42fb21faf7e16ce020d965a0c9322a08fca7c3fc26d157`  
		Last Modified: Wed, 28 Jan 2026 04:46:19 GMT  
		Size: 9.3 KB (9303 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.23` - linux; arm variant v7

```console
$ docker pull hylang@sha256:94adda68f222cd72701e1cd345594658b9e2bde6da4d83a75d3dbf4529ea5660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 MB (25876812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c37357c1bc8065c473bef3113e8712df4a22742726a3190d8f57988edafb1891`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 03:34:10 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 03:34:10 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 03:34:10 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 03:34:10 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 28 Jan 2026 03:34:10 GMT
ENV PYTHON_VERSION=3.11.14
# Wed, 28 Jan 2026 03:34:10 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Wed, 28 Jan 2026 03:41:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 03:41:13 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 03:41:13 GMT
CMD ["python3"]
# Wed, 28 Jan 2026 04:30:30 GMT
ENV HY_VERSION=1.2.0
# Wed, 28 Jan 2026 04:30:30 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 28 Jan 2026 04:30:30 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 28 Jan 2026 04:30:30 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db97676e2d6d2a8f77dbd18a0b92a71fc802200fca5f7b4d42af3d7568ae639c`  
		Last Modified: Wed, 28 Jan 2026 03:41:21 GMT  
		Size: 460.7 KB (460734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3c5881b382a5ca278d414dd7bd76ed973395dd88a12ca38f2ba4817369f8ef`  
		Last Modified: Wed, 28 Jan 2026 03:41:21 GMT  
		Size: 15.2 MB (15159449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7f6d621b2e1085d59c74f675da76cb08091c0a71745351bf260c89e73aee35`  
		Last Modified: Wed, 28 Jan 2026 03:41:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb05b934beabc7e46759dd134c7da1e718537a027cd16f87eb2d6c29e82ffdd`  
		Last Modified: Wed, 28 Jan 2026 04:30:36 GMT  
		Size: 7.0 MB (6974658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:650080fbc3f4afa420468cffb7c83cfbcea78dd9b0f124be6d0c07523eb4fef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **711.9 KB (711853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32522fef55b81bf29431e1f4ca9e02ea0663aa32cadce161980755f93623eff`

```dockerfile
```

-	Layers:
	-	`sha256:9a76fe3a40e2c95384af276be3c97c0bf11693f95fcc9768393404cf75e78c7e`  
		Last Modified: Wed, 28 Jan 2026 04:30:36 GMT  
		Size: 702.3 KB (702334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a437b332f9ecfd0e55a894642a565e7bb794ce2a37dff4e7140e204649ae860f`  
		Last Modified: Wed, 28 Jan 2026 04:30:36 GMT  
		Size: 9.5 KB (9519 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:8bea5dbda06e5c5dc639e21552fa5cf498dac4dfd4c707b6b9c072093b11dac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.8 MB (27827128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a1b753166f4128a98e16bf09cc57eb0d76e25614c0fbed806ff83ae0d561f42`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:25:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:25:40 GMT
ENV LANG=C.UTF-8
# Wed, 04 Feb 2026 20:25:40 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:25:40 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 04 Feb 2026 20:25:40 GMT
ENV PYTHON_VERSION=3.11.14
# Wed, 04 Feb 2026 20:25:40 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Wed, 04 Feb 2026 20:32:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:32:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:32:40 GMT
CMD ["python3"]
# Wed, 04 Feb 2026 21:10:45 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:10:45 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:10:45 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Feb 2026 21:10:45 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92c27998e47516709ccefc4a8b6d37cf87d978769fb6b29bed07eba722e20d5`  
		Last Modified: Wed, 04 Feb 2026 20:32:47 GMT  
		Size: 463.1 KB (463106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69cdea34044e4bd8256e3399a193baa802f19d79d326e2274a76b754c83b5f59`  
		Last Modified: Wed, 04 Feb 2026 20:32:48 GMT  
		Size: 16.2 MB (16191786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b33d1c032048a893e06f76e7f80bd5e0b429ecd1ecba99c2b100fbff5cc5dc`  
		Last Modified: Wed, 04 Feb 2026 20:32:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec963269844a77283f3ba90d62cda179c8f15c3338b761aebc41cd15e366bd53`  
		Last Modified: Wed, 04 Feb 2026 21:10:51 GMT  
		Size: 7.0 MB (6974897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:f61f8771a6888b5383edcaaa418deaf3c0c90fe0fb35596983573d0cc10659b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **708.9 KB (708939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc2571aff4cfcc5fdda1dc9a95882d20d139367e53ebcf1c9a653f277e02c282`

```dockerfile
```

-	Layers:
	-	`sha256:81e88d01324ba926e6764b1c09bb90622da700ad4a0f375865c01b99a3935cef`  
		Last Modified: Wed, 04 Feb 2026 21:10:51 GMT  
		Size: 699.4 KB (699380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2503842a0198cce6588fbde6b14ede1cfc98d93e1b050eecc5a3a94618d1a917`  
		Last Modified: Wed, 04 Feb 2026 21:10:51 GMT  
		Size: 9.6 KB (9559 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.23` - linux; 386

```console
$ docker pull hylang@sha256:10034dfceb72854608100978fa38478058fb957222fba5d384829e12a1e44506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27340741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7f37edef1ab88d2c10a32aef2369ff786dd8125dbeb036f44c6359cfc3756f`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 20:23:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:23:05 GMT
ENV LANG=C.UTF-8
# Wed, 04 Feb 2026 20:23:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 20:23:05 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 04 Feb 2026 20:23:05 GMT
ENV PYTHON_VERSION=3.11.14
# Wed, 04 Feb 2026 20:23:05 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Wed, 04 Feb 2026 20:28:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:28:11 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:28:11 GMT
CMD ["python3"]
# Wed, 04 Feb 2026 21:06:52 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:06:52 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:06:52 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Feb 2026 21:06:52 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7643f91903010128d66a8ba3ee31d3f7ccecb8fbd0bfe04dfea362e0bd8191a0`  
		Last Modified: Wed, 04 Feb 2026 20:28:18 GMT  
		Size: 461.2 KB (461239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8734daa4194a6b5d5239e0fff99938bd6eda6d254f117053b1abf8e7101b5a41`  
		Last Modified: Wed, 04 Feb 2026 20:28:19 GMT  
		Size: 16.2 MB (16217244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7945932e9734f36b7a17b5d20f490e615978b263c177afc8898250c740bc27a5`  
		Last Modified: Wed, 04 Feb 2026 20:28:18 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7c19bfd180aa9b2a335b0a449a2e8d72c841504d7fd69499d578982315a5e0`  
		Last Modified: Wed, 04 Feb 2026 21:06:58 GMT  
		Size: 7.0 MB (6975011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:9807cf6b36a77d73573afe4b9c23d5fcc30cdf5c537f4fe3d192aa2c3f30ae4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.2 KB (709236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c746cdf78adf40ca4b58ee2629395f4c7441fab75df3075559128c6021bedc7`

```dockerfile
```

-	Layers:
	-	`sha256:52f4cfa3222ed54fbed747355a3d3db73dde22b9b2267b5b94563cf6bb45861a`  
		Last Modified: Wed, 04 Feb 2026 21:06:58 GMT  
		Size: 699.9 KB (699881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a87711aec9ff434d3b25511996a8b7df6135bc25dde42f89dda718318a82f5d`  
		Last Modified: Wed, 04 Feb 2026 21:06:57 GMT  
		Size: 9.4 KB (9355 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.23` - linux; ppc64le

```console
$ docker pull hylang@sha256:9efcea14d94cac56d6f3919909127677f0c94f9a3cf6c7243b67b5f7bda4e2da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28088831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:326fd500679569a5211f1007d1788ef67a7288125f1bed1d134869a4e69f8e9f`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 04:59:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 04:59:53 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:59:53 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 04:59:53 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 28 Jan 2026 04:59:53 GMT
ENV PYTHON_VERSION=3.11.14
# Wed, 28 Jan 2026 04:59:53 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Wed, 28 Jan 2026 05:18:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 05:18:17 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 05:18:17 GMT
CMD ["python3"]
# Wed, 28 Jan 2026 07:08:14 GMT
ENV HY_VERSION=1.2.0
# Wed, 28 Jan 2026 07:08:14 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 28 Jan 2026 07:08:14 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 28 Jan 2026 07:08:14 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88aafecdf803f0bda53169e0b4516ebe803ec0a6efe23323aab9048a5a31b23`  
		Last Modified: Wed, 28 Jan 2026 05:09:03 GMT  
		Size: 463.5 KB (463504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e120f4e7290397735a1c7e95154e17892da03e3518cbe272cc575521f298b94`  
		Last Modified: Wed, 28 Jan 2026 05:18:31 GMT  
		Size: 16.8 MB (16820692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020c10bef0e4e45aae91bec9f8b3aa22b971c6a3dde44086ad33fc0ae3edcf6b`  
		Last Modified: Wed, 28 Jan 2026 05:18:30 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d6cfa60cb2831fdd595a3fa0427e65d3dafbd523da27b341dc2df1e681e4ed`  
		Last Modified: Wed, 28 Jan 2026 07:08:26 GMT  
		Size: 7.0 MB (6974737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:1cb25891d45523115d34941cf8deb6c4094c212b1b5297a614475dd11a98f402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **708.8 KB (708808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eb73015a971f579a5e25f54d720e228d5bdac01c4390d17d476581dc665104b`

```dockerfile
```

-	Layers:
	-	`sha256:0d81d360cae01b5eb6e5609ff837be934a2e302e8813ef41929bfd3989c42f79`  
		Last Modified: Wed, 28 Jan 2026 07:08:26 GMT  
		Size: 699.3 KB (699333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26c7ab0b15fd1fe9e52d2af0278ce7b6c1f737c312cb3cd99ff62e824167574b`  
		Last Modified: Wed, 28 Jan 2026 07:08:26 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.23` - linux; riscv64

```console
$ docker pull hylang@sha256:d4742d4cfbde1f21e71b1aea8801abf9f39e6886a033da0fadcaaf47402e94c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26926037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de93acbfb1fa846ab173078a3676c5842c3095af6d93e8dda66b5e5004245d9`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 23:27:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 23:27:38 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 23:27:38 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Jan 2026 23:27:38 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 29 Jan 2026 23:27:38 GMT
ENV PYTHON_VERSION=3.11.14
# Thu, 29 Jan 2026 23:27:38 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Fri, 30 Jan 2026 01:08:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 30 Jan 2026 01:08:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 30 Jan 2026 01:08:59 GMT
CMD ["python3"]
# Sun, 01 Feb 2026 06:16:57 GMT
ENV HY_VERSION=1.2.0
# Sun, 01 Feb 2026 06:16:57 GMT
ENV HYRULE_VERSION=1.0.1
# Sun, 01 Feb 2026 06:16:57 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sun, 01 Feb 2026 06:16:57 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a24d3312840a658b2b4b8edfb5495fcefd5c5898b617c59e7367d3e6b834e59`  
		Last Modified: Fri, 30 Jan 2026 00:02:56 GMT  
		Size: 461.2 KB (461191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6d237ab0062aceaa837d6b4972988abfb5afdba3858af2a15529e8517dc089`  
		Last Modified: Fri, 30 Jan 2026 01:09:52 GMT  
		Size: 15.9 MB (15903975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e4217ef5241da4e3a9dad56517eb27ffe81072f6a6a02f496cec366bb2e453`  
		Last Modified: Fri, 30 Jan 2026 01:09:49 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eba2f19e96904830323fc5f0dc1d6c864657639a4531148db67fee4fecd8525`  
		Last Modified: Sun, 01 Feb 2026 06:17:42 GMT  
		Size: 7.0 MB (6975335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:b57c79d4fc9676fb58a24875a36a06c245596ec07cb68a76068a00d187d36836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **708.8 KB (708804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4542e7b9286eaf17809e98c040ad5c9a7876d88b72362a0574dcde986d255f13`

```dockerfile
```

-	Layers:
	-	`sha256:dfbbaed42f6e15b4b351165cb5c6a500b1c5b34cd0f7be9a222c5b128bc88df5`  
		Last Modified: Sun, 01 Feb 2026 06:17:41 GMT  
		Size: 699.3 KB (699329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2e83d92a09970020065da6d26bc9f2d430e184aac76af140b1b76370d53747d`  
		Last Modified: Sun, 01 Feb 2026 06:17:41 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.23` - linux; s390x

```console
$ docker pull hylang@sha256:d8faaad8473c5da184e3806ddf592ffb2034b24159e1dab44a539e7210caca4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27617805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a83d16e7692144f0819db89a43d74e0879b54d0a284ae44e33592179efdc4a1`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 06:36:39 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 06:36:39 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 06:36:39 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 28 Jan 2026 06:36:39 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 28 Jan 2026 06:36:39 GMT
ENV PYTHON_VERSION=3.11.14
# Wed, 28 Jan 2026 06:36:39 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Wed, 28 Jan 2026 06:48:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 28 Jan 2026 06:48:26 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 28 Jan 2026 06:48:26 GMT
CMD ["python3"]
# Wed, 28 Jan 2026 07:28:40 GMT
ENV HY_VERSION=1.2.0
# Wed, 28 Jan 2026 07:28:40 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 28 Jan 2026 07:28:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 28 Jan 2026 07:28:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f9179b3fe8452fc5c8afc7711dc4c6ac20b66ab481cd6af0553ff47cf92d0f`  
		Last Modified: Wed, 28 Jan 2026 06:43:21 GMT  
		Size: 461.7 KB (461740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656212cc2961c34e7945b1e1eb5c566a040e88a058f03aef1b3cdb716f38be57`  
		Last Modified: Wed, 28 Jan 2026 06:48:37 GMT  
		Size: 16.5 MB (16455737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe9e139b9bbb4850311097170843b56f07ca7fd170bda3993aba57da23e5bda`  
		Last Modified: Wed, 28 Jan 2026 06:48:37 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cc8c6f5c487446b2e119761ccaf3ac8789e7a364a8e6282164fbe4fc534925`  
		Last Modified: Wed, 28 Jan 2026 07:28:49 GMT  
		Size: 7.0 MB (6974747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:0bf6d231b346e4fc3b1511ae010a0e513e6864f001faa417e508f10245483f70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **708.7 KB (708680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0547f0784db9ff359c5cae51d6956875d1091542a51ff7bb5963aaae64a2b31`

```dockerfile
```

-	Layers:
	-	`sha256:e8937023deba1bcd5326c08a5eff5f43760053866c508dea53e0046939f14e88`  
		Last Modified: Wed, 28 Jan 2026 07:28:49 GMT  
		Size: 699.3 KB (699275 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2c6ecf0157f847615bcdbb3622b2fd534d64a76e45c6268c4fcf8a2deea4b23`  
		Last Modified: Wed, 28 Jan 2026 07:28:49 GMT  
		Size: 9.4 KB (9405 bytes)  
		MIME: application/vnd.in-toto+json
