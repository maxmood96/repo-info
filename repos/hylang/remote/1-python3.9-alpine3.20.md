## `hylang:1-python3.9-alpine3.20`

```console
$ docker pull hylang@sha256:4de9937e3df84202a5ae432f5028bce02884817033fa9cc149680dedac5b18ff
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

### `hylang:1-python3.9-alpine3.20` - linux; amd64

```console
$ docker pull hylang@sha256:24de11405c4411d12e53dedf68f427012c4cdd4fc4a485d01a469c1822370f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22523133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:debd5eb5e3ea6371093ba88bcde0279e10d11bed319bbf986920f988c1ce07f0`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 04:30:01 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 04:30:01 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_VERSION=3.9.21
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_SHA256=3126f59592c9b0d798584755f2bf7b081fa1ca35ce7a6fea980108d752a05bb1
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
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
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0cb6c2bca27da74dbd6a29cf914bd615025fb14693684aa09c16c10185a258`  
		Last Modified: Tue, 14 Jan 2025 20:34:29 GMT  
		Size: 458.4 KB (458428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69418a0972ccf42894f459dbb1593ed58853a69514697cf38fc00cc8e6a57e62`  
		Last Modified: Tue, 14 Jan 2025 20:34:30 GMT  
		Size: 14.8 MB (14768227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e749a4cbb95f4773f25a49281f67a3e315777f3e201ca15a7ee1ba1f619690`  
		Last Modified: Tue, 14 Jan 2025 21:54:32 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345b6555f1ac6cd4cc0212c009a49e990ae91b3ae2a6b9e30def97fc88a97ea6`  
		Last Modified: Thu, 23 Jan 2025 01:28:57 GMT  
		Size: 3.7 MB (3669970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:a2787d16cfe7ca6479255c4dc5a8959b4cb84ca384378c9f1dc7f43134156fb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.2 KB (666225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdbb814f020301ae52fbf9ab7cca3c7eeeae10ad5b5d4fb7e434d6e9cd2c8596`

```dockerfile
```

-	Layers:
	-	`sha256:d19d17325dcc11810c7a3841b421c54ae9b7a27cb76322f6fa68f4d18f82d133`  
		Last Modified: Thu, 23 Jan 2025 01:28:57 GMT  
		Size: 658.2 KB (658199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab803af6c504d8b213c8333d5f9e80008a1c2ab74ed9dc2fd282c68f585bc10b`  
		Last Modified: Thu, 23 Jan 2025 01:28:57 GMT  
		Size: 8.0 KB (8026 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-alpine3.20` - linux; arm variant v6

```console
$ docker pull hylang@sha256:d93da96a1f4ff4f5703b26bd7daefb279cde15c35613e05e2ee0c484cf774578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.9 MB (21866205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6687e6c0901aab8f78006ec3033d58c958149cf63ea5eb53c69c92d5dd71341`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 04:30:01 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 04:30:01 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_VERSION=3.9.21
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_SHA256=3126f59592c9b0d798584755f2bf7b081fa1ca35ce7a6fea980108d752a05bb1
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
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
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Tue, 14 Jan 2025 20:34:27 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06475ab9ef588959bc9af33c0c0abe5db6fa1ce5288e003553a7a069a5c7f05`  
		Last Modified: Wed, 15 Jan 2025 02:11:34 GMT  
		Size: 459.2 KB (459192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136709c4fd8e8f377cb0570926fa792d1aeda50cfc897f598523820155dabad9`  
		Last Modified: Thu, 09 Jan 2025 08:21:06 GMT  
		Size: 14.4 MB (14365279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43de47eba0df394c53b986673ff81453a1888da9149d2bf0851e633fe01c9a02`  
		Last Modified: Sun, 09 Feb 2025 22:21:29 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef457153d08880389fa8702d4e3cb912844b7f3e09f2d3e6f34b2cda7f4d304f`  
		Last Modified: Thu, 23 Jan 2025 01:44:37 GMT  
		Size: 3.7 MB (3670012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:814e5fb5f837a411e8144fbcf54e65bb9a66d499bf7c3e605b145b102984bd06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 KB (7886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e577aab921ec9a7e808f5b70f722bddec085a76cde3026b913eed0a11e938bf2`

```dockerfile
```

-	Layers:
	-	`sha256:bea35dd8e03d6426431eb13366540dbacb254cb8c3271aaecadaca51e0b49e26`  
		Last Modified: Thu, 23 Jan 2025 01:44:36 GMT  
		Size: 7.9 KB (7886 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-alpine3.20` - linux; arm variant v7

```console
$ docker pull hylang@sha256:ed2d20be8ca9db6fb2ba81931f73ed71c2071bcdd1ef47f992bea6c30029e632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21184206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:101af6df8ddebbadda6652aa40bbb8ede9176c695297c17e545d809519dbf0d6`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 04:30:01 GMT
ADD alpine-minirootfs-3.20.5-armv7.tar.gz / # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 04:30:01 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_VERSION=3.9.21
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_SHA256=3126f59592c9b0d798584755f2bf7b081fa1ca35ce7a6fea980108d752a05bb1
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
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
	-	`sha256:c8a32ed454e751770c0976636b8d0d0fccc4f778a2dd26c428067d613be1a299`  
		Last Modified: Tue, 14 Jan 2025 20:45:20 GMT  
		Size: 3.1 MB (3095514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c41d5d0fb800601d84faf485d0154f5a08e9c4f4ff9caf700df1ff83eda83db`  
		Last Modified: Wed, 15 Jan 2025 11:00:01 GMT  
		Size: 458.4 KB (458421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cb24bdbce8e997015188d815f73938cb46244f029ec5d331fcad75c7548476`  
		Last Modified: Fri, 14 Feb 2025 21:01:19 GMT  
		Size: 14.0 MB (13959969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0763c7fedc2b1937bfc266b2e98ffb419e54b78c4700c1b1f2aca6a1d2f499`  
		Last Modified: Fri, 14 Feb 2025 21:01:17 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4c7ee015d97466fb5fa89a8b8f0eaef07e3138b1fb18220f6333ea44e4858c`  
		Last Modified: Thu, 23 Jan 2025 05:17:43 GMT  
		Size: 3.7 MB (3670054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:194483e91f289b0ee8f970b46df7b3c88d7c59f26ebfd0fb944b51bfc70266b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.2 KB (669198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8434bd002cdc00299db76dcadf25f5a9de4aeb4d1ac0c08167938ed8da494458`

```dockerfile
```

-	Layers:
	-	`sha256:65c14e0c26661819ecec1ef6e13a3212fe526fa2519ddf4c12787c1fb51ab145`  
		Last Modified: Thu, 23 Jan 2025 05:17:42 GMT  
		Size: 661.1 KB (661096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:112586bdeeb7b4db93895ec61a74ef503734290edcdbd3efec7ddf10e251dedf`  
		Last Modified: Thu, 23 Jan 2025 05:17:42 GMT  
		Size: 8.1 KB (8102 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:126936caa4a78c25f23d6650d2ac6e178349de116d2107393cd846028e06f7c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23102544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b728b76f8381d891d8d2ae2c8364d239157ab19aeb43418dade4dadf390af89`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 04:30:01 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 04:30:01 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_VERSION=3.9.21
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_SHA256=3126f59592c9b0d798584755f2bf7b081fa1ca35ce7a6fea980108d752a05bb1
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
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
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcd6e0cbc06e1fbb5ab80cef8d41b8775ebcc00733d4f1f30773085b1216524`  
		Last Modified: Tue, 14 Jan 2025 21:01:38 GMT  
		Size: 460.6 KB (460581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ef5b371dee564e1902b8e9c3507d8f3c9452a7b7515b4f621b22979bd5ffdf`  
		Last Modified: Tue, 14 Jan 2025 22:01:29 GMT  
		Size: 14.9 MB (14881032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a77261420222d92774da8d52853e36e013f8ef4026d2b25457b742b07f7366`  
		Last Modified: Tue, 14 Jan 2025 21:01:41 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d786270109c34a3b2f50dd46c18328a551f7672da1bbe2e21562fc52f19a2ee`  
		Last Modified: Thu, 23 Jan 2025 04:17:57 GMT  
		Size: 3.7 MB (3669912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:078fced476e59dba93b7ce6356e7d60c031bc53808073a9f80dd8a1f722d9467
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.4 KB (666385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5207ed4ec7b1353fcfb32a956ae3e70ab9fddb5e8f3d9c8fa181af55999347d`

```dockerfile
```

-	Layers:
	-	`sha256:fe513d0e6d9091dabdf45a98f1c6083666ca09acd0bb4dfd9e3c2ef67c46827f`  
		Last Modified: Thu, 23 Jan 2025 04:17:56 GMT  
		Size: 658.3 KB (658255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e8e2f455d151566136abb63e24b053fc96b149db5c6b3c78039ffd8bd8c4250`  
		Last Modified: Thu, 23 Jan 2025 04:17:56 GMT  
		Size: 8.1 KB (8130 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-alpine3.20` - linux; 386

```console
$ docker pull hylang@sha256:57a302fd1b60d49fa6a7bc0c730348d51468b20fd8c7b32c4f1c6db220bdd84a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22606114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4f11aa564f243e2a0f97c5bb2beb6b71d55eef9f4227885e8d37a245e9121f`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 04:30:01 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 04:30:01 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_VERSION=3.9.21
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_SHA256=3126f59592c9b0d798584755f2bf7b081fa1ca35ce7a6fea980108d752a05bb1
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
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
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Tue, 14 Jan 2025 21:25:38 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a49903ce9e19ed30a1eb0a89e84e4dfb4011b28169083beab6f231e5964857`  
		Last Modified: Thu, 13 Feb 2025 13:54:50 GMT  
		Size: 458.8 KB (458844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93f5d006dc3685926c84807d548721b9e0647026ff476deb5f1ee46dc511bee`  
		Last Modified: Thu, 13 Feb 2025 13:54:52 GMT  
		Size: 15.0 MB (15006068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7d6acb64e7eac2bed64386f93081ff04c964bd4656751aedf8481e309f6315`  
		Last Modified: Thu, 13 Feb 2025 13:54:53 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efd2267fb642b8f29ee2974a48b4419f11049aef30b5f87ecca0603021c7669`  
		Last Modified: Thu, 23 Jan 2025 01:28:17 GMT  
		Size: 3.7 MB (3669983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:27e50332c8d45de0aeda2d787b661457f1302428c653d1c1e440e517a48e75f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.2 KB (666167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd8f45a9bf07e93e3c70b3f5268724736fd4d0cb06f4bbb9ced76b2e656fa3ee`

```dockerfile
```

-	Layers:
	-	`sha256:f77a9d2e82f61703078e9fbd9b326dbaf0a347cc54235142b2962da69d723de2`  
		Last Modified: Thu, 23 Jan 2025 01:28:16 GMT  
		Size: 658.2 KB (658174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dcab8dcfea6a78d749baa815829dcf58c7176071096478d15e2133ac6ec42e4`  
		Last Modified: Thu, 23 Jan 2025 01:28:16 GMT  
		Size: 8.0 KB (7993 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-alpine3.20` - linux; ppc64le

```console
$ docker pull hylang@sha256:d04fceabb19cf9558e0a2b10dfd596a760e7549096d68244cc7781f145865a50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23170674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca677b65455d3fee4319208ae71c201720d42362b84462311060a5bd80992cc`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 04:30:01 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 04:30:01 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_VERSION=3.9.21
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_SHA256=3126f59592c9b0d798584755f2bf7b081fa1ca35ce7a6fea980108d752a05bb1
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
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
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Tue, 14 Jan 2025 20:57:44 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236c49b59f7bc6253ef66b11876ac777a6ca1e7bd5b4685cbf246e81c6b11613`  
		Last Modified: Wed, 15 Jan 2025 11:01:01 GMT  
		Size: 461.0 KB (460965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32529799ed1cc4d4b2598455f107f77bfa04df5afdeaac0cc3b7a782ce13bfa`  
		Last Modified: Thu, 09 Jan 2025 00:17:18 GMT  
		Size: 15.5 MB (15464950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872f095fd69711885402c140f4f1af476a54e1a6afff181f2a7d93def71097e1`  
		Last Modified: Thu, 09 Jan 2025 00:17:17 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e8cb500133cd009dd0c582e7fd19d8ccfb2abd5653ed5dd22d7b8fc96fbbc5`  
		Last Modified: Thu, 23 Jan 2025 01:41:56 GMT  
		Size: 3.7 MB (3670104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:7ac079b1358a63e0647bc54c68704940fe249cf16aa5463de6e5e24cfe2a584b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.4 KB (664352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db43f66b0118080968236208477c0965077937eaf0720b1f9231d91dd24b94b`

```dockerfile
```

-	Layers:
	-	`sha256:beddafcef1b29d1a78275efe7a625e01c1748a91ac1b84e129822802cd45f675`  
		Last Modified: Thu, 23 Jan 2025 01:41:55 GMT  
		Size: 656.3 KB (656282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f184835933012ce9d6d6ad707166d44f6f9f662428ddee496f02de339791086b`  
		Last Modified: Thu, 23 Jan 2025 01:41:55 GMT  
		Size: 8.1 KB (8070 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-alpine3.20` - linux; riscv64

```console
$ docker pull hylang@sha256:eba58174a2a340f36cd3753d0facef042d369c0c4180f2e9b27aad6250a42013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22335503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034d25d837fdab699a3b12d94e564fc380bbded3e864f5b027ffcf98ba288d6a`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 04:30:01 GMT
ADD alpine-minirootfs-3.20.5-riscv64.tar.gz / # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 04:30:01 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_VERSION=3.9.21
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_SHA256=3126f59592c9b0d798584755f2bf7b081fa1ca35ce7a6fea980108d752a05bb1
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
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
	-	`sha256:34b7590cc8ea3b21e8c3a0d69270b822d3ba63bc58c6cf0e36c987c95b18eb8d`  
		Last Modified: Tue, 14 Jan 2025 20:50:16 GMT  
		Size: 3.4 MB (3371926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04eeb80f718e5e5c506c0329c716b99592103d59538dc5a050c902382074f2c`  
		Last Modified: Wed, 15 Jan 2025 11:01:18 GMT  
		Size: 459.2 KB (459164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e78fd5b3dd4243c6a7fc6ffbdd8ad26b6ee478f81fc46c93fa2ce857519252`  
		Last Modified: Tue, 11 Feb 2025 14:44:44 GMT  
		Size: 14.8 MB (14833134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198ba1fcb38ca9fb4ed9ea988d3657b3d1d5e77c5f467906ca34cbb6e938e1e4`  
		Last Modified: Fri, 10 Jan 2025 21:51:48 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79788bb63cf213ffe10de2b89386a51fad701b9778b5323777af274608ff75f5`  
		Last Modified: Thu, 23 Jan 2025 01:48:25 GMT  
		Size: 3.7 MB (3671022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:82cb72b1d9a1e2f4057d991843fdb23482e38b5b0296717594c6a6adafa749fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.3 KB (664348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b6e545367d32bdf55e73aa71aa8100d084db37a880841c699550b67374d691a`

```dockerfile
```

-	Layers:
	-	`sha256:9c1af7e55907f61d6c3eda5d9117c1c09d6ce95eca62624a0a50aae99607007e`  
		Last Modified: Thu, 23 Jan 2025 01:48:24 GMT  
		Size: 656.3 KB (656278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dd5e56dcff081d1134b4c10e77e795c3e445562161b7b4a1157927e34384857`  
		Last Modified: Thu, 23 Jan 2025 01:48:24 GMT  
		Size: 8.1 KB (8070 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-alpine3.20` - linux; s390x

```console
$ docker pull hylang@sha256:f6c98e94277212e39b7d59fd12b51d1972bba606a4c8dbab87f8f2ebcae87094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22755495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:332dfdc9a07bedafc945aee46d5276e19759985f3eee38c58d1c5b0e84f4be60`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 04:30:01 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 04:30:01 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_VERSION=3.9.21
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_SHA256=3126f59592c9b0d798584755f2bf7b081fa1ca35ce7a6fea980108d752a05bb1
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
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
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Tue, 14 Jan 2025 21:25:41 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985cab1b685e8021d8265573dee27e7d43bce4b069c5b582887d01978fffc36b`  
		Last Modified: Fri, 24 Jan 2025 01:56:53 GMT  
		Size: 459.4 KB (459369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239848f0acbee33cc93c140df53358f23c1167b4aa77e9e542d45e5a891942ef`  
		Last Modified: Thu, 09 Jan 2025 06:27:11 GMT  
		Size: 15.2 MB (15162731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4bf29b14837c9499afaaeefd21d5d57fa1665844fbd4df37adb8c97c9b20d7`  
		Last Modified: Thu, 09 Jan 2025 06:27:10 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962a9ef83c9fa7ad8559d434621e9ba5e11e9f30c9d4f31b0d90252496319e72`  
		Last Modified: Thu, 23 Jan 2025 03:14:33 GMT  
		Size: 3.7 MB (3669825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:f576a333d10699074084c7483ae8827ab40a38a83e2024085f761aa77dc7c38e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.3 KB (664273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:260bcfaaccc831e71a4f823387281f41bfcacb4b9004db29c30547555ca98e4a`

```dockerfile
```

-	Layers:
	-	`sha256:acdbb5d152d2c217758ee3e358f2fd539dbcedadf502371ce8314bbb7f4b995c`  
		Last Modified: Thu, 23 Jan 2025 03:14:32 GMT  
		Size: 656.2 KB (656248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7390a11f9c1e4a7213ffbd2a93db3c5573ef5ddb129bdacd513045be1f337a6`  
		Last Modified: Thu, 23 Jan 2025 03:14:32 GMT  
		Size: 8.0 KB (8025 bytes)  
		MIME: application/vnd.in-toto+json
