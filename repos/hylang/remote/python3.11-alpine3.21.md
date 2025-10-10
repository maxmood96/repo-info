## `hylang:python3.11-alpine3.21`

```console
$ docker pull hylang@sha256:0b565c3ca0ab43394a0e1a9cc84e5ca1cb4f6957b0e0b5254374fd48d77f8083
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

### `hylang:python3.11-alpine3.21` - linux; amd64

```console
$ docker pull hylang@sha256:3abbf91f5e4d331d1fe6fb913d02d726ea3e7676defbf40cae548ae96474ec21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 MB (26533195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee42753971577fb5dc47f5d0693c79ca95e016ca9078c0978b16b4f20d068c56`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.11.13
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=8fb5f9fbc7609fa822cb31549884575db7fd9657cbffb89510b5d7975963a83a
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Wed, 08 Oct 2025 12:54:09 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ab52ad278d0c82c0efb3f01c4b61bf61d0928a1077ec37b4d1f3f8ac9d9349`  
		Last Modified: Wed, 08 Oct 2025 23:50:02 GMT  
		Size: 456.9 KB (456885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbea5374690fe3da73d8eba94d6f33619a31c35b5ae3c1d644f448cdc534aca2`  
		Last Modified: Wed, 08 Oct 2025 23:50:03 GMT  
		Size: 16.2 MB (16214280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d612e511e33a0747555fd86472cd7b1d5d739b8dc9579f88df92fe08964072cb`  
		Last Modified: Wed, 08 Oct 2025 23:50:02 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ccadec4a98ae816932133a79f91c5c49b98e1358b876cc356119be3d9cf955`  
		Last Modified: Wed, 08 Oct 2025 23:50:28 GMT  
		Size: 6.2 MB (6219212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:b31f11e9c802043cc23d12ed884fe18ae6c3a4593a569906ab68f297de89150e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.0 KB (664955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4339c4f58acf129787b44d5a6461f48c256bd668df44c8de89ab419598fb4bc2`

```dockerfile
```

-	Layers:
	-	`sha256:6073eb2088b77b3a98a6b2de7fd1546db0ab371957929b4d2a0378a04ceb2b69`  
		Last Modified: Thu, 09 Oct 2025 02:22:28 GMT  
		Size: 656.9 KB (656917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9bdb1ddc870fd287cd84151e6d7661a9a5dd9da605045d4e06b8bf507902484`  
		Last Modified: Thu, 09 Oct 2025 02:22:28 GMT  
		Size: 8.0 KB (8038 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.21` - linux; arm variant v6

```console
$ docker pull hylang@sha256:5e4f3c673ef72b9ab02f83086773c5b0de6109fa1c9574ba3347db005e7825f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.0 MB (24984676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b39c5c541c05d71a7b318e426a71037bc53364fd08ad9b5b97dd8a742661f8a`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 19:19:01 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_VERSION=3.11.14
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f8b30cbd0fab9e5a803578a09c973d18d7450816d914e63e04e5c2edd79f8bee`  
		Last Modified: Wed, 08 Oct 2025 21:00:33 GMT  
		Size: 3.4 MB (3365468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a354d4eda470b43231cbf360a76cdb7d0ba148fa93e4cf4d4b530e71891d9c`  
		Last Modified: Thu, 09 Oct 2025 22:41:22 GMT  
		Size: 457.7 KB (457683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d8d1c4154262c8a6963f80720f54f36252f17e8e7a20e6db2323f1afdd49a0`  
		Last Modified: Thu, 09 Oct 2025 22:48:13 GMT  
		Size: 15.5 MB (15480534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18bba80edf81b3f968dc3b25901f21382e8bec92bf01fbd0511647101184ac6f`  
		Last Modified: Thu, 09 Oct 2025 22:48:03 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b18b7a1e199eb9a2e08430d3e36ca9de69584f37c784db43c4545a4c0fa8df2`  
		Last Modified: Thu, 09 Oct 2025 23:24:19 GMT  
		Size: 5.7 MB (5680743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:6f972ff69439c132183f735f8b95cca8427ab05b713ea6beba2faed3ad8eb425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 KB (7903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37bab3214203def5f175b2b95bf7d6e81cc33718a1a58cebacfb070f99a6616e`

```dockerfile
```

-	Layers:
	-	`sha256:0c0a20d1128056dae38ca5c859957c3e74083c68641fdaaa5eec444525e427ec`  
		Last Modified: Fri, 10 Oct 2025 02:18:01 GMT  
		Size: 7.9 KB (7903 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.21` - linux; arm variant v7

```console
$ docker pull hylang@sha256:fabdd43d509fd4f5f1acd48d7dcdb870570afbd9d351189d2c00f935bb97a9bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25131623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d58f1f20f0ca940f5d7be4a23b05c7e0de7d16e8b317853ceb2b326a6e15abc`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.11.13
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=8fb5f9fbc7609fa822cb31549884575db7fd9657cbffb89510b5d7975963a83a
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:520d06ecc3ba4ec2920319fa6f2cc6bea9a9c1d5a43808c1d2388522c37d7b30`  
		Last Modified: Wed, 08 Oct 2025 16:24:34 GMT  
		Size: 3.1 MB (3098611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a71654c73a263f6d4a5da8e724eece33247c9a7dd305e7b954166fc5f506a96`  
		Last Modified: Wed, 08 Oct 2025 23:34:03 GMT  
		Size: 456.9 KB (456877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64a28df2f798e06be35a2eb1ea4c058b1908c41be35a97c82c5042822e9b660`  
		Last Modified: Wed, 08 Oct 2025 23:34:04 GMT  
		Size: 15.4 MB (15356299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecd09656fc60f31fcae2522da97a68182b3c3f820d81ec0a1b488bee80a897f`  
		Last Modified: Wed, 08 Oct 2025 23:34:03 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c22babc66a5775e3730206e80f1fe5021f6b3bb04d69ab3ac3debc969a3326`  
		Last Modified: Thu, 09 Oct 2025 00:18:06 GMT  
		Size: 6.2 MB (6219587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:5a7c8de3ab57123cf564c812ee126f451f9e1ebba9976c9604540c23b6b7c053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.1 KB (668061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056f79d09d6268975855767ff8a6679a1a96717ddfd67255ff35313178c7c1b4`

```dockerfile
```

-	Layers:
	-	`sha256:3f998439efcff10a330dc9b6832f1f4faef080ab114016913b5959098dc058e1`  
		Last Modified: Thu, 09 Oct 2025 02:22:35 GMT  
		Size: 659.9 KB (659943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08e884adc80f8c08f7c878d54e106e759f339e5de530fb4660e13d54233745f7`  
		Last Modified: Thu, 09 Oct 2025 02:22:36 GMT  
		Size: 8.1 KB (8118 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:b4f601c1a3af32f4924a5127f362304ec172b324a5302cefb1b533f15101b1f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26962417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604d6ffe287daf7bb1c9e253dd24fdfbc87989e021dd2b91ecfdf6f8db8d038b`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.11.13
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=8fb5f9fbc7609fa822cb31549884575db7fd9657cbffb89510b5d7975963a83a
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Wed, 08 Oct 2025 16:24:46 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b1d3b7966c94ea0c32bdceb9d304050c37324869cd18219f78514c7423c3c8`  
		Last Modified: Thu, 09 Oct 2025 00:13:17 GMT  
		Size: 459.0 KB (458991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccc71ce4b26bc30373ad3556b4fc8f23143dc391da46c6da60b475df7d5d324`  
		Last Modified: Thu, 09 Oct 2025 00:13:41 GMT  
		Size: 16.3 MB (16291466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64b1739585620869b319fac65e009193f88f5ba0ae027c83c534d5a7c5bb4e0`  
		Last Modified: Thu, 09 Oct 2025 00:13:14 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d961dcd629fee7a1b49dad73ef60c4830c94b25e2f4fbe61beacfe5bf70960`  
		Last Modified: Wed, 08 Oct 2025 23:33:33 GMT  
		Size: 6.2 MB (6219360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:448da8c31fd9c38a6a0b6235d60d39fec2dcd0556ef88855df008d6babb5b38e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.1 KB (665115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e925c5cdadf29ca5b078d78fd50c684acf0878658f19b20876e3bdbd21e415a1`

```dockerfile
```

-	Layers:
	-	`sha256:9beb50f16d22afd5fd64a2c0568b6fca21a17a1661f07a7fdbaa424eb3721442`  
		Last Modified: Thu, 09 Oct 2025 02:22:39 GMT  
		Size: 657.0 KB (656973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31a5cf4452f8df6040f8373987fd20c477e409ec79cfa70259f565de276ed1e5`  
		Last Modified: Thu, 09 Oct 2025 02:22:40 GMT  
		Size: 8.1 KB (8142 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.21` - linux; 386

```console
$ docker pull hylang@sha256:2ae945030d11f902770366cec3f45899268c2b1461a1ffdeddb5a0f0a14aa421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26573698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4549023a8a86b43150e63f78abb732c1a33c489d0d16fb8841bb13654af4a8cc`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.11.13
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=8fb5f9fbc7609fa822cb31549884575db7fd9657cbffb89510b5d7975963a83a
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bbedd1c05bb5090fc3fc2356be88d60b2a60937565b56e91fb4be42c5c73d485`  
		Last Modified: Wed, 08 Oct 2025 16:25:36 GMT  
		Size: 3.5 MB (3464704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823c782fae353640c6b8e0284f26c3ece5a3eab18bcc72194ae4bf5ba08b62a6`  
		Last Modified: Wed, 08 Oct 2025 21:55:04 GMT  
		Size: 457.3 KB (457337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9ed3a79127c7aa2bd83faf97970f36c346902abbbc875e715d1549b67e3bfd`  
		Last Modified: Wed, 08 Oct 2025 21:55:05 GMT  
		Size: 16.4 MB (16431992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6c72ff582c08d8d58ef9bbb18421f0faf9b9d23b6ae680bebd6271fc08caac`  
		Last Modified: Wed, 08 Oct 2025 21:55:04 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959fb4249c4fe12f4848e1844dc10c8537e7e9a737b067555d997eca9faab41d`  
		Last Modified: Wed, 08 Oct 2025 22:28:32 GMT  
		Size: 6.2 MB (6219416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:13b9a12f13db66843f4d39648f755b9fc19899b2d400bc8c657209cdafc55b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.9 KB (664898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5567004582c0307ce0615dad6fd990d90f9fbee0ed6ac7d462a95d4abd0ca93b`

```dockerfile
```

-	Layers:
	-	`sha256:258dcbe8d1809dd4e23aa2500fd852c37cf773a2560631cf78060d0c44f8cb17`  
		Last Modified: Wed, 08 Oct 2025 23:30:48 GMT  
		Size: 656.9 KB (656892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b819ec81c2262bd930df436f5b3d51b272eaadcfc4042e9268c848be3c4a9d4`  
		Last Modified: Wed, 08 Oct 2025 23:30:49 GMT  
		Size: 8.0 KB (8006 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.21` - linux; ppc64le

```console
$ docker pull hylang@sha256:16ffdc44256f38e4683d7d7a31c8719b2c11bf151955db8c1c750d099a87cb55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27190937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:910dc02996fcdfbe5482004cf6b43b8ffb8e6be1de92843500cb7b2b59efdfe4`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.11.13
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=8fb5f9fbc7609fa822cb31549884575db7fd9657cbffb89510b5d7975963a83a
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e99908f6ead74bb809123fe0d40505509ed6113949496be71629433c6ea3fa1a`  
		Last Modified: Wed, 08 Oct 2025 16:25:03 GMT  
		Size: 3.6 MB (3574075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0026c7dc43c0a7255a1ad9f4da34ccbef2597f65b422a86bda4c70ee1f6cbd4`  
		Last Modified: Thu, 09 Oct 2025 08:37:20 GMT  
		Size: 459.4 KB (459409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb30a52db485bd8220412852824bab3ce0f1f1f0d513125b46f51ceb4ce4dac`  
		Last Modified: Thu, 09 Oct 2025 12:07:26 GMT  
		Size: 16.9 MB (16937232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15d81a03b0a12912401411d37321e1f58a6e99efa4339e76e86bff56c793abc`  
		Last Modified: Thu, 09 Oct 2025 09:51:06 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f761378df19da96416f94ebb911dce894765534d70b594a00d12c3d9fbcf8728`  
		Last Modified: Thu, 09 Oct 2025 11:20:14 GMT  
		Size: 6.2 MB (6219971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:efc0f0d7ec2e4b88226841152d79bf9bb7b6a3a1ea609eeede797bcf34e62ebe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.1 KB (663082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eb724f08fb51d4fc05906f90c4220d6dd7a73ef5c2b5bf2516a39465cfd7402`

```dockerfile
```

-	Layers:
	-	`sha256:1c3711074c3ba5f3ba868faaed67fd64db423ad5e99c2440e4bcd15643a81e4d`  
		Last Modified: Thu, 09 Oct 2025 14:18:35 GMT  
		Size: 655.0 KB (655000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5dc7f95c3e63e54b82a3f8247f11bd3b366c46476cdeb39c76be702b1eb7871e`  
		Last Modified: Thu, 09 Oct 2025 14:18:36 GMT  
		Size: 8.1 KB (8082 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.21` - linux; riscv64

```console
$ docker pull hylang@sha256:a42247833940d7069b7ec1550cd8779bcc9268201261a9c4cc415c6617cd2e1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 MB (26169812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:155ef58361dd02a48da1b2fb1bf3791bf936aea550556add54ae9a3003c37b1d`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 18:20:34 GMT
ENV LANG=C.UTF-8
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PYTHON_VERSION=3.11.13
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PYTHON_SHA256=8fb5f9fbc7609fa822cb31549884575db7fd9657cbffb89510b5d7975963a83a
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
CMD ["python3"]
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HY_VERSION=1.1.0
# Wed, 13 Aug 2025 21:03:27 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 13 Aug 2025 21:03:27 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 13 Aug 2025 21:03:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3275b496853d19cc6428a9543a3884d79627e13cc07be788b5bd163f6892e987`  
		Last Modified: Tue, 15 Jul 2025 19:00:59 GMT  
		Size: 3.3 MB (3349090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab0152f745fe105bd917dd035bf213e5a0afdd2b6b1e0eb9374377da919271d`  
		Last Modified: Thu, 17 Jul 2025 19:53:24 GMT  
		Size: 448.0 KB (448014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28eb6b410a800bb15388f6f435e08a65fc3ef324a0df7a78a3468696949ad49`  
		Last Modified: Wed, 13 Aug 2025 07:52:35 GMT  
		Size: 16.2 MB (16151505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae3e1dfe49cd25b596ed969f9c65cb4ccea840048ce2e0f674460914806e25b`  
		Last Modified: Wed, 13 Aug 2025 07:52:36 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7959f75b4e1de5434878b762a58f668a5a6798cf4ecfe978d6f6d33f51cd006d`  
		Last Modified: Sun, 17 Aug 2025 12:57:09 GMT  
		Size: 6.2 MB (6220953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:89807bb7d7126027e78d0703122cdebc6159c62192a082399090d70e02adc131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **660.5 KB (660465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9409e858ac349fe2ec563682624c90bde629b71ed57aef96bd645de74eef8b2`

```dockerfile
```

-	Layers:
	-	`sha256:93cfb8f6c77c9a0401e44d5145aee580fdad670663e08091dc96514dd67fe48e`  
		Last Modified: Sun, 17 Aug 2025 14:18:16 GMT  
		Size: 652.4 KB (652383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c020ef5555afda097aa18cd451b1731147ffcf2d6b527a5c8a1f86c135faa53`  
		Last Modified: Sun, 17 Aug 2025 14:18:17 GMT  
		Size: 8.1 KB (8082 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.21` - linux; s390x

```console
$ docker pull hylang@sha256:208e8d32fe699b06e61573e9f672a6fe716645097f12cb29d41ca0bfa54ff700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26833421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ab75c63457b6e8988069ecfb81d76b71b56431c556f03215144daa447894832`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 18:52:37 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_VERSION=3.11.13
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=8fb5f9fbc7609fa822cb31549884575db7fd9657cbffb89510b5d7975963a83a
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 18:52:37 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9f2ceebb28b6c8480d6ae26501eda06bf0b6029f7c797c80673b95a60276e050`  
		Last Modified: Wed, 08 Oct 2025 16:25:19 GMT  
		Size: 3.5 MB (3466434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d403476d77f3c6d174042f0a35c75c77af9283be8ed3f5fdc93ad0cd153034`  
		Last Modified: Thu, 09 Oct 2025 13:06:21 GMT  
		Size: 457.9 KB (457870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c766838040ae3f6a4e2aca2ca48198030a0b47d34760e4d2778f39aaf79ddb8`  
		Last Modified: Thu, 09 Oct 2025 13:19:17 GMT  
		Size: 16.7 MB (16689522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e82894c82e46314ab21f2860ec450e467121ec083cea03893139089d4e5de682`  
		Last Modified: Thu, 09 Oct 2025 13:19:15 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd7cc1309cfdfb729b305c2933d9881699a803bb4e5e6b4d6b251a58ede4833`  
		Last Modified: Thu, 09 Oct 2025 21:08:20 GMT  
		Size: 6.2 MB (6219345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:f9022b5de8c421cb4378ec0eea6fff61ec14165ae751a908c0e3bf559fd6975a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.0 KB (663003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c7029bf520765add32dd3bea4106cead2811596b46511fe432e9120e36a36c`

```dockerfile
```

-	Layers:
	-	`sha256:14d29f3635a1548befb6c32c8210c029897c4d08b29134c079d591bfb9b40518`  
		Last Modified: Thu, 09 Oct 2025 17:18:27 GMT  
		Size: 655.0 KB (654966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59f17a916ec8de7f74aa9aef21224e75bc2913d93b2070e4f8a954ff1ae81d1a`  
		Last Modified: Thu, 09 Oct 2025 17:18:28 GMT  
		Size: 8.0 KB (8037 bytes)  
		MIME: application/vnd.in-toto+json
