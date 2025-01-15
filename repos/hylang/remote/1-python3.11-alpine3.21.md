## `hylang:1-python3.11-alpine3.21`

```console
$ docker pull hylang@sha256:55f294a0c5f8dae347bcdd8d5895d2dfdc501f1765179d8717de72a29252b96e
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

### `hylang:1-python3.11-alpine3.21` - linux; amd64

```console
$ docker pull hylang@sha256:db2f4606cdde131d575c2ad173b5c628ab5ee61103c9e9c5e96a14dd5787d1eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 MB (26488756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457aba73b3194152c8b27f9df75e216ec5e63cfd892996acf99b30d3749daf1f`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 05 Dec 2024 13:19:52 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:19:52 GMT
ENV LANG=C.UTF-8
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.11.11
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["python3"]
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HY_VERSION=1.0.0
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 08 Jan 2025 17:56:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Jan 2025 17:56:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb81f221332c555fd5a9cd799ece5510b3a131a383a831d5b610f9fe5a040bb`  
		Last Modified: Wed, 08 Jan 2025 18:22:53 GMT  
		Size: 458.8 KB (458842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d04f35a207537b61d6fe9bbd170c391d10ed493d1bf40d4850c170fe4894e9`  
		Last Modified: Wed, 08 Jan 2025 18:22:54 GMT  
		Size: 16.2 MB (16169848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3947958a836ea9bf6f6c0c4ac022493784474649e0500f6d6dad4a3f9be7be`  
		Last Modified: Wed, 08 Jan 2025 18:22:53 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4c1516d3e86f2208f60229c9cd5f97a5da5a1a0b7814bd63aceafc56cb963b`  
		Last Modified: Thu, 09 Jan 2025 22:30:13 GMT  
		Size: 6.2 MB (6218102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:a75310879356600ce15ddf7229c18bc2c7b5f72b709093f8c198771e1113e7cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.8 KB (673817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ba83775f862823ce3366b689ce3ba3d152c8543ec08ab3e50799abb67fd751`

```dockerfile
```

-	Layers:
	-	`sha256:d12cc3b3f950927ff7f248f3865c6f1613c47467fbeca681043296a6a9e50844`  
		Last Modified: Thu, 09 Jan 2025 22:30:13 GMT  
		Size: 664.5 KB (664475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2083f6519e8411b52b55e5d6dd3d9fec6ee8e427ed49da2727ec8e1a83c8404a`  
		Last Modified: Thu, 09 Jan 2025 22:30:13 GMT  
		Size: 9.3 KB (9342 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.21` - linux; arm variant v6

```console
$ docker pull hylang@sha256:9f8c2df74adde3cf91b4578108cad459031525177cbd4de09163069e57053224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25758260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b631715d075bd12869e9252062f2b2de4ed1c6cdcdb8678715b5faca1a40054d`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 05 Dec 2024 13:19:52 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:19:52 GMT
ENV LANG=C.UTF-8
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.11.11
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["python3"]
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HY_VERSION=1.0.0
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 08 Jan 2025 17:56:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Jan 2025 17:56:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff0a4077f329734365423e1f7a8f45ea76ac88dda4e38832db6d82d047e001a`  
		Last Modified: Tue, 14 Jan 2025 22:15:42 GMT  
		Size: 459.6 KB (459577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312b8e196543d3f58bc4782df2c2229ece2a098bcbb159c7c3ec17be001f017e`  
		Last Modified: Thu, 09 Jan 2025 08:02:16 GMT  
		Size: 15.7 MB (15716408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b57ee8acddcdaea8b5989cbd765aef561906fa58410090c9f47ac832e8d4ab28`  
		Last Modified: Tue, 14 Jan 2025 22:00:29 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac482723a548dcfb178eb64dfe5d71705cb3890ede6a5dfc2b666022dd7417b`  
		Last Modified: Thu, 09 Jan 2025 22:35:48 GMT  
		Size: 6.2 MB (6218147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:92b46940c3819996deee4f2885daad8ff9946b50ed46b0a1f2c40310b7f23207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3e3f7ef8abf62b75a930c5eec7a1c0d154983491da4617da49e660ba0bbf73`

```dockerfile
```

-	Layers:
	-	`sha256:0edd909e77b009b82fb9d296a5e133677fec22c30a3fd115bc0c56adc9ad903b`  
		Last Modified: Thu, 09 Jan 2025 22:35:47 GMT  
		Size: 9.2 KB (9235 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.21` - linux; arm variant v7

```console
$ docker pull hylang@sha256:b23276671f5db1f4ccb489cbad0d330486cbeb96ba3352224da93033cfb1b9d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25095180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc7b285593184654555f944eed134eb4934e570257ef869b98673d45b2a799d`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 05 Dec 2024 13:19:52 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:19:52 GMT
ENV LANG=C.UTF-8
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.11.11
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["python3"]
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HY_VERSION=1.0.0
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 08 Jan 2025 17:56:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Jan 2025 17:56:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a362fe3b52ccb4a43ae3d2e7b9f53bdf4eedb49d7cf54acc45450c89f8e0f9`  
		Last Modified: Tue, 14 Jan 2025 22:00:46 GMT  
		Size: 458.7 KB (458732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a5cc0b4bda8b95202bc3c15b1b9cb59c2ce2acf8b6da78f9d71d1c59ab58e7`  
		Last Modified: Tue, 14 Jan 2025 22:00:49 GMT  
		Size: 15.3 MB (15321079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d36cbd36a85c58f56449e82c4cc264cddd5f2568fcc1438e8f0c33b02393e6e6`  
		Last Modified: Thu, 09 Jan 2025 08:34:31 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7e95adf4a8fe2fffc71741e1b30b6fcb959357e6a09c09b022fe6601db0753`  
		Last Modified: Thu, 09 Jan 2025 22:56:57 GMT  
		Size: 6.2 MB (6218008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:c3c69dee18e5883e78a07ddcfcba62be16bccd6dd26dd5481e902dd6e1202501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **676.8 KB (676806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ddd32a1aced3c0609dcb9ab8d703283e961f90924bc34c9ff2b326f289ef48`

```dockerfile
```

-	Layers:
	-	`sha256:615b76e42d55ff13e32b32bf2b9e753ab99e9bbe70b5e4d0dde4f5716f9deb25`  
		Last Modified: Thu, 09 Jan 2025 22:56:57 GMT  
		Size: 667.4 KB (667356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d860e4f851fa4bce941d57979614bcd372b405b13cf928c9ea10666a8cdbfce0`  
		Last Modified: Thu, 09 Jan 2025 22:56:57 GMT  
		Size: 9.4 KB (9450 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:d3af4bd94487ace45706a83deb960728ca1eb6bf8895c492d7a18cb906d9a710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26921990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5f4367c543450a0a1b6d1b5590abafbe0034416fb91de8006b0c34a63df515b`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 05 Dec 2024 13:19:52 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:19:52 GMT
ENV LANG=C.UTF-8
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.11.11
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["python3"]
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HY_VERSION=1.0.0
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 08 Jan 2025 17:56:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Jan 2025 17:56:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21e04dc46d8c3ba8c2c8c030adbf079b391ec9b1000f43530739d086d72e4cf`  
		Last Modified: Tue, 14 Jan 2025 20:33:17 GMT  
		Size: 460.8 KB (460840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84609f5da878f2bafcf42cb70f1232cf6b4c921f939f7ff78ab1b3fbefe34d6`  
		Last Modified: Tue, 14 Jan 2025 20:52:25 GMT  
		Size: 16.3 MB (16250505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ebc9929c943166c7e0c89e78d7a682842bd96a6b913456acdce5a74e343493`  
		Last Modified: Tue, 14 Jan 2025 20:34:11 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fde9626de1272e977c6e6a142f0594622ed42e611f7f178d82cc40c8935c941`  
		Last Modified: Thu, 09 Jan 2025 22:51:55 GMT  
		Size: 6.2 MB (6218037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:efcb14245f0ba09e5bf44f72b75c8f417fbb80a0b47fb1f71f7d9c5bfe131538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.1 KB (674073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736fc3d73a9fc619304f363002ce16d793189d9a7603342e050ac26e0b2e8076`

```dockerfile
```

-	Layers:
	-	`sha256:2125d33bb3380d7796df85e89f18c2bc7843d13b060ce7b49d03594b2b659396`  
		Last Modified: Thu, 09 Jan 2025 22:51:55 GMT  
		Size: 664.6 KB (664579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a32cfdd92d8d4c8de7ff4017c7c8d772d599628397e3005b6df434f7408bfe0`  
		Last Modified: Thu, 09 Jan 2025 22:51:55 GMT  
		Size: 9.5 KB (9494 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.21` - linux; 386

```console
$ docker pull hylang@sha256:6f002a6dc6d6baad94d8977e77ee0658bb13b06311ea2c2732729aed9c6eddfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 MB (26526816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833038b11462c9f2bfb4bdbea15d1d9aa9c024311e911d263d43439504af4843`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 05 Dec 2024 13:19:52 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:19:52 GMT
ENV LANG=C.UTF-8
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.11.11
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["python3"]
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HY_VERSION=1.0.0
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 08 Jan 2025 17:56:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Jan 2025 17:56:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cf4c930eec5b65245dbb03dd469c7cdd93ef2fb0598d18843bf7bb0797b34d`  
		Last Modified: Wed, 08 Jan 2025 18:19:54 GMT  
		Size: 459.2 KB (459164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa971e5a48ce4d0333e87e601233802fc1e3ddc93ba29bdf705ccda45deb41d`  
		Last Modified: Tue, 14 Jan 2025 21:03:34 GMT  
		Size: 16.4 MB (16386196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd17312fecf8b5be0dbbea7c3d867c4e2f41780c5a2363a80038e5a2eb3bb4f3`  
		Last Modified: Tue, 14 Jan 2025 22:02:02 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516d661878533f20d410039fa44ddebb5e9707d4036a0b43fc9fdbd306f5a79f`  
		Last Modified: Thu, 09 Jan 2025 22:30:21 GMT  
		Size: 6.2 MB (6218081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:3a9f0a8d2f63f35c32753a640350f0b1719e22a5ffab4612013e142dc173c37a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **673.7 KB (673719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76bbfb31b0de3c5ba1ceaafff270cc44a75a4cfe5f2cbd20ea9b194e4914ecd9`

```dockerfile
```

-	Layers:
	-	`sha256:efbd07736493a63fd64c9e4c04a1e815aab14a8c54ad9b30296b8da2f2ffaca4`  
		Last Modified: Thu, 09 Jan 2025 22:30:21 GMT  
		Size: 664.4 KB (664430 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9d6fe22a76e076462f7ffb55b5ebb1e6c6d2baefe8b64475f15957d3fcb85c2`  
		Last Modified: Thu, 09 Jan 2025 22:30:20 GMT  
		Size: 9.3 KB (9289 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.21` - linux; ppc64le

```console
$ docker pull hylang@sha256:85c113c3e032f2287d67a12b45711f7e3efd11d7c1385b85ddd7e0b9f22dd26c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27141878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27aede2d9439c51169ea4bbce8e3928a65afd3ee624531b445787f7f2ddbdd1`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 05 Dec 2024 13:19:52 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:19:52 GMT
ENV LANG=C.UTF-8
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.11.11
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["python3"]
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HY_VERSION=1.0.0
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 08 Jan 2025 17:56:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Jan 2025 17:56:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd98bd85d9639dad5088cef5124b34bafc1ef08f075de94ad85e1778cc49e8f`  
		Last Modified: Wed, 08 Jan 2025 23:39:36 GMT  
		Size: 461.3 KB (461300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9753b72320947f04d373aa91ef4ea4b8544e8300c1f3666c961ad76cb067c27f`  
		Last Modified: Wed, 08 Jan 2025 23:55:21 GMT  
		Size: 16.9 MB (16888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7793ef30277cb1d9bd5b338f7578ad5f71f10b06201da02ab67a8a66a29b47b`  
		Last Modified: Tue, 14 Jan 2025 22:01:23 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed439d93816a836f290dbe08b8ff97dbdfcdb12ffb6fb71f449a8982915f61d`  
		Last Modified: Thu, 09 Jan 2025 23:08:09 GMT  
		Size: 6.2 MB (6218131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:7e858d19841b11ab4d747dec6e553eb1445d8871bff5d52c1ddf3e9a24a83192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.0 KB (671992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad02b75ce1c582504b39e64cface770055025816601d8733cb717efe4c45e39`

```dockerfile
```

-	Layers:
	-	`sha256:c721326e0edd78800c0f503c0e5ff8c14e36771e78c05ec6692428df361b93ed`  
		Last Modified: Thu, 09 Jan 2025 23:08:09 GMT  
		Size: 662.6 KB (662582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e468b79165feab0d563d6a93d5ff39e969cebc68963dff2d679911590f5a736`  
		Last Modified: Thu, 09 Jan 2025 23:08:08 GMT  
		Size: 9.4 KB (9410 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.21` - linux; s390x

```console
$ docker pull hylang@sha256:3755f84b2d797ff7451243ee39135bd710e41d7d3b6f5366fb92a102b4f03a50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26790969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeebb38a616b119aae8781c7007a03d346eceec543e4a5749aeecc3c185b2878`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 05 Dec 2024 13:19:52 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:19:52 GMT
ENV LANG=C.UTF-8
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.11.11
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["python3"]
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HY_VERSION=1.0.0
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 08 Jan 2025 17:56:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Jan 2025 17:56:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Tue, 14 Jan 2025 20:34:39 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b60eaccca3a913528bbaa3a3ec5f33b6f8c613d50a6ce6775926b9ada7c0bc4`  
		Last Modified: Tue, 14 Jan 2025 22:01:39 GMT  
		Size: 459.7 KB (459692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fe2b2e51b8b6db0fe04c7aa9fac90d66b454c2bb0570134376c46aa6954ff8`  
		Last Modified: Tue, 14 Jan 2025 22:01:43 GMT  
		Size: 16.6 MB (16646048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86528aa7ec7ffa590d1a0402bd5aa8b44f8b0323c8265f1b0a3007fe72619ed2`  
		Last Modified: Tue, 14 Jan 2025 22:15:29 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c3ff4a8c98aef1ffb221482c7f76c161daf7ea17832e4433fd881839ac4021`  
		Last Modified: Thu, 09 Jan 2025 22:53:54 GMT  
		Size: 6.2 MB (6218112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:87f4eaf7677a32fe524a2af785e1ffa5adc060b8f300c82b03c13b20ffa36b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **671.9 KB (671866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b6644b6e4e5242749b79c959a87085f6064e6b8cdd70c9e8f392b49da2438a`

```dockerfile
```

-	Layers:
	-	`sha256:e618206f5eeadc0df6046807f7c70eb89b45c28f9c16408a3321130408d8c846`  
		Last Modified: Thu, 09 Jan 2025 22:53:53 GMT  
		Size: 662.5 KB (662524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dfecc181cbc9f714853e431292cfb2e95998b045387fd242bb98ef52198334`  
		Last Modified: Thu, 09 Jan 2025 22:53:53 GMT  
		Size: 9.3 KB (9342 bytes)  
		MIME: application/vnd.in-toto+json
