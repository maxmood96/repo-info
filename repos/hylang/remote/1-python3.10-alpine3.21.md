## `hylang:1-python3.10-alpine3.21`

```console
$ docker pull hylang@sha256:c16729c3ae7c071e12365a386698b318c4d0ba5cf69d7c510d1bdd9cb991fe71
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

### `hylang:1-python3.10-alpine3.21` - linux; amd64

```console
$ docker pull hylang@sha256:8567dc3b82c79c16615ab9bf0e21272f276dc7fd04e1552e2113fa5ae38bc232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23939361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5044a513cf01f97d2a6df2c5bd6470aadb1d172014f4038d1946d98fed841b2`
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
ENV PYTHON_VERSION=3.10.18
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=ae665bc678abd9ab6a6e1573d2481625a53719bc517e9a634ed2b9fefae3817f
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
	-	`sha256:f098359a897447309b7d33d6eec59f6f409a37482bedf589e256d194889f720a`  
		Last Modified: Wed, 08 Oct 2025 23:16:19 GMT  
		Size: 456.9 KB (456883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0070a5bd41540f674f5b7435fd56cfcb74a0b6638aac5968e502cba9585bac04`  
		Last Modified: Wed, 08 Oct 2025 23:16:21 GMT  
		Size: 15.6 MB (15645294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f9a285eab2e86f7c140689df2a3dbe3743707d3b8125abf4e4d0a5932903e7`  
		Last Modified: Wed, 08 Oct 2025 23:16:19 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04072b4035cf78eaa6e11d2c66ca79f4f0e29ae69fd8fe9d6fed2c71aacc6b91`  
		Last Modified: Wed, 08 Oct 2025 23:50:30 GMT  
		Size: 4.2 MB (4194367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:edd780a3d57acd8fb7bc340ff8a7c42214950f9f2b9d90207001f1f560cd2437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.0 KB (664995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b8add5d633780dc15cdaf4d0925e2191837e6e4ca8cfb2d73e424e05757e7b`

```dockerfile
```

-	Layers:
	-	`sha256:7147076987d8c460b48b5163f6f16b1f026604bd377ad6877b0eeda0a36995cd`  
		Last Modified: Thu, 09 Oct 2025 02:22:14 GMT  
		Size: 657.0 KB (656957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:469921ad2d5329a63b5cee5749006177d277258cfcddac784206ffc9b172b30d`  
		Last Modified: Thu, 09 Oct 2025 02:22:15 GMT  
		Size: 8.0 KB (8038 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-alpine3.21` - linux; arm variant v6

```console
$ docker pull hylang@sha256:beb72ca5c2dec3d254b70bc27f3b3259a85137d77b7f0c459dc1336b0890efaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22634066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e484704e56386333cacd20c9011890543c3d089158ac39069c88d8866eaf5bba`
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
ENV PYTHON_VERSION=3.10.19
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
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
	-	`sha256:9f01130e1da81ed181950f44eff387bb284ed99e4c4a6fb3e584a2113c38fbde`  
		Last Modified: Thu, 09 Oct 2025 22:56:24 GMT  
		Size: 457.7 KB (457694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345196cde6ee7efff6d914bf6fa3b1fe01ad4d50898bd2c3023b34584d3d0749`  
		Last Modified: Thu, 09 Oct 2025 22:56:27 GMT  
		Size: 14.9 MB (14949032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7fb7199ec82743b7e2c1b80d2c980df807e5e276825ef874a1490df64b0a99`  
		Last Modified: Thu, 09 Oct 2025 22:56:25 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6e301b312159e4388227147bad653b165bb3a6929ec3216e421dda6f619e52`  
		Last Modified: Thu, 09 Oct 2025 23:27:23 GMT  
		Size: 3.9 MB (3861623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:db6cbeac4900aee7a2827373a81d674babdd3e6c90184c3fbc6a9091d3a6db2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 KB (7903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4246c7beb8cc54aab4764a7a165850a577fbbd8a7e46e6cc2953da42bed6d09e`

```dockerfile
```

-	Layers:
	-	`sha256:97aee5521d9e093032285c3c5482a5b177daf59634e21bd8bd35057ff16ce9ce`  
		Last Modified: Fri, 10 Oct 2025 02:17:42 GMT  
		Size: 7.9 KB (7903 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-alpine3.21` - linux; arm variant v7

```console
$ docker pull hylang@sha256:ec32858e91aa69c8166b8f8e774389fae6378a5ad5b344d69b6360e706084739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22573433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a1e4808294dfc8d7be5cd3b79aeb7cf3ff595f735ed90a5bc9189b3d48ae38f`
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
ENV PYTHON_VERSION=3.10.18
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=ae665bc678abd9ab6a6e1573d2481625a53719bc517e9a634ed2b9fefae3817f
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
	-	`sha256:a4e1893475ae269b5a27148b0266882e1d5a1b88068b4021b4024ee9262e5b8f`  
		Last Modified: Wed, 08 Oct 2025 23:48:09 GMT  
		Size: 456.9 KB (456876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621acdbdcc915ee71c12f20d6303d3cf4f423fd5a4068327e538d633e954690c`  
		Last Modified: Thu, 09 Oct 2025 00:17:24 GMT  
		Size: 14.8 MB (14823024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd58ed2163e046dc590f4d6d78482ce614003c44bc048bf9a20ceada1536e506`  
		Last Modified: Wed, 08 Oct 2025 23:48:16 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff4b42597d87c6cf4fae1b1117ce6dde32d6fd24839bfbb280f7672eb4887e1`  
		Last Modified: Thu, 09 Oct 2025 00:18:06 GMT  
		Size: 4.2 MB (4194672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:ac2ae10d04449a4537de5f0304f3224b909a3b0256199ea0aaad2448085e4304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.1 KB (668101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543078c1d75627d112461e82074497d0c73ba62cc3add5c4763d03332f9eeeca`

```dockerfile
```

-	Layers:
	-	`sha256:573b9bf65c22fc61179d03faf12363f21bd52e6909c5ca812fa210cad20c7811`  
		Last Modified: Thu, 09 Oct 2025 02:22:21 GMT  
		Size: 660.0 KB (659983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d74fafbea41cafbe6ce03b7459883c8849cc12d15d73a9997e15e1b6f3f8c1bc`  
		Last Modified: Thu, 09 Oct 2025 02:22:22 GMT  
		Size: 8.1 KB (8118 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:c19a908a1fb0a61dc26a5ad36df511f0874fcd7c7555c2c529c2ec10e2dd0970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24354745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09580a824920c375a10530f7b7f193c6a1cc8d3a3498010a2a8f787fed2e4230`
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
ENV PYTHON_VERSION=3.10.18
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=ae665bc678abd9ab6a6e1573d2481625a53719bc517e9a634ed2b9fefae3817f
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
	-	`sha256:9b6539867f73bf12b31b63d2970400252ce85beda9748f25277477558a0f3681`  
		Last Modified: Wed, 08 Oct 2025 23:14:29 GMT  
		Size: 459.0 KB (458981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc4ef9685b80643c91cbb6265fc838a4af5ffc593ec94c0c9e8395d491c89ae`  
		Last Modified: Wed, 08 Oct 2025 23:14:44 GMT  
		Size: 15.7 MB (15708634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d0405cbad38932e03d86b269ee8a12c6fa47ca38fa6425c37e33c7c79a163f`  
		Last Modified: Wed, 08 Oct 2025 23:14:29 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8431e090c27e79b1db0fadfd433b59e0fe343e181407391240d3c3788afa1c6`  
		Last Modified: Wed, 08 Oct 2025 23:34:03 GMT  
		Size: 4.2 MB (4194530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:26b474fd046a7dab11e71df8ff2f52f53fb6ce01eddf250055ae4915898b023f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **665.2 KB (665155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27769f16389bdd237511f3ccf4a7949e952da2ae4994c5bd1fed0015044c7c68`

```dockerfile
```

-	Layers:
	-	`sha256:599e1bc312c1ea9df1ede32675d1da97707e4ca2f33d9846c846f5cbbb818621`  
		Last Modified: Thu, 09 Oct 2025 02:22:26 GMT  
		Size: 657.0 KB (657013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad174fd84d9b8090c23d1a1869d347239098971bbb97a6e3ad2f8808d6633919`  
		Last Modified: Thu, 09 Oct 2025 02:22:27 GMT  
		Size: 8.1 KB (8142 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-alpine3.21` - linux; 386

```console
$ docker pull hylang@sha256:ce251accedc7ba92e2de9bddf2ee825f5d3140f4141056258eec1d86b7f5596c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (24004942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19020069231c76f66acabc1abe4be39d477931cddd07dcd1a5b3c235d36311f0`
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
ENV PYTHON_VERSION=3.10.18
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=ae665bc678abd9ab6a6e1573d2481625a53719bc517e9a634ed2b9fefae3817f
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
	-	`sha256:2b7b9b7cb9eeef1d6aa616d4abf79417fd1fc47fa5b7e4fd1e4f737fe5192856`  
		Last Modified: Wed, 08 Oct 2025 22:09:39 GMT  
		Size: 457.3 KB (457337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58312e162930c2d83d2f2abd29da45c72d687eef86a8a3f0b799a8c9d25cfb49`  
		Last Modified: Wed, 08 Oct 2025 22:28:15 GMT  
		Size: 15.9 MB (15888328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f38f970c2f28058c575bd5119450f217676cedb3f28b65895b67b960a778fee`  
		Last Modified: Wed, 08 Oct 2025 22:09:48 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e38ebcb439386ae88fcfae4d7a1c275d7372dd1633d233692f000ba4e0db1e`  
		Last Modified: Wed, 08 Oct 2025 22:28:33 GMT  
		Size: 4.2 MB (4194323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:3f6aab69bc670b731e5e36cdecc115ba82646ab921da3d844ee46c38d882c7f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.9 KB (664938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73127cfef159bc13243167776e97f01679550ac436f6fb67b9fbfedd9ddcf752`

```dockerfile
```

-	Layers:
	-	`sha256:48fc38e3f2268b8fd2060f435d0532904b9fc32a1ecd85640937251129443684`  
		Last Modified: Wed, 08 Oct 2025 23:30:04 GMT  
		Size: 656.9 KB (656932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e05c1e3cf87003da8c36d441f70ad4953646ba4afe73bccd35b88ddcd67eed2`  
		Last Modified: Wed, 08 Oct 2025 23:30:05 GMT  
		Size: 8.0 KB (8006 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-alpine3.21` - linux; ppc64le

```console
$ docker pull hylang@sha256:895befdc78957d7cf519813f10f419d175c18dbe65e006a0a1d9e9a53df7dd7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24573020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb4a1adee72be03fbe6dc05d3c8b34b74069c1051211a85edec0de59baab243`
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
ENV PYTHON_VERSION=3.10.18
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=ae665bc678abd9ab6a6e1573d2481625a53719bc517e9a634ed2b9fefae3817f
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
	-	`sha256:9728d05bcf50e4cdcdda22e7ad2d9941a4e7bcf29e919fce5d8aa3734459415c`  
		Last Modified: Thu, 09 Oct 2025 09:06:11 GMT  
		Size: 16.3 MB (16344424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c46eb16da86da58c2286c39abdff2df57f003bdebd64094f5fa637277e56076`  
		Last Modified: Thu, 09 Oct 2025 09:06:10 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7bbf0437634d9401c68e5baef61a234e0ce508dd8aa5ff358f4045ae30aa821`  
		Last Modified: Thu, 09 Oct 2025 11:22:09 GMT  
		Size: 4.2 MB (4194864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:2628ff6d0f15ad6a5481ef4ed5028bc67056977933366db96762b721b16699e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.1 KB (663122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ace552ba18c2699af830512e31609deb2aa6e2ab31b5e2d1721ce0a9da1d37e`

```dockerfile
```

-	Layers:
	-	`sha256:c9f0e1f9be2395f08f30e1e3bd74255118b3448eea2f8319298438a8e48d443a`  
		Last Modified: Thu, 09 Oct 2025 14:20:34 GMT  
		Size: 655.0 KB (655040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ea2f882717e5effb53fde63d7f6cc7e42d44397e932448a239f94b907982871`  
		Last Modified: Thu, 09 Oct 2025 14:20:35 GMT  
		Size: 8.1 KB (8082 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-alpine3.21` - linux; riscv64

```console
$ docker pull hylang@sha256:0bed288c9cdfd85c92642590cd4dc2815307bc5b4afd9186fc137056b8700663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23655087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843eadadbf34b990ed170c86a425c733ac7274ec3ce5b6d8a5b162efa64fc45c`
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
ENV PYTHON_VERSION=3.10.18
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PYTHON_SHA256=ae665bc678abd9ab6a6e1573d2481625a53719bc517e9a634ed2b9fefae3817f
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
	-	`sha256:b10eb172143027f050a2b728fd41a2e467893d8727478668b2b0b34a5e49bd45`  
		Last Modified: Wed, 13 Aug 2025 09:15:57 GMT  
		Size: 15.7 MB (15661977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39d73a7f1a19e049fd170976939a12dd173c3e7ead90b904490fe7b362a5732a`  
		Last Modified: Wed, 13 Aug 2025 07:26:00 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5e1eb359653c67026abbe8917eabec61929364a3e84d9aaa4882b14f9a0091`  
		Last Modified: Sun, 17 Aug 2025 13:13:03 GMT  
		Size: 4.2 MB (4195756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:59bd8a3ccf4b14335c1bf681b8d0e2257d94ce26605f95e4687019c39410be39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **660.5 KB (660505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7bfc902ad9a8a048ec5c2f80ef2530c392405f320d3326e1b24f7b59d938e7`

```dockerfile
```

-	Layers:
	-	`sha256:e83122cb3103c41d7d40027835af207a29d85627327eda4f648248a4a613ed43`  
		Last Modified: Sun, 17 Aug 2025 14:17:56 GMT  
		Size: 652.4 KB (652423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49c96338f89692a60d5c5d02c3c927fca542726f0601d78cad7235fd926a75cd`  
		Last Modified: Sun, 17 Aug 2025 14:17:57 GMT  
		Size: 8.1 KB (8082 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-alpine3.21` - linux; s390x

```console
$ docker pull hylang@sha256:cd7b9efb9d518d2328e367f28af4b2c32d7995b760e2ed8b7e5d950ac1e2818a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.2 MB (24181990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4152d9436d31d9b70ebbb8a8d89fa0ec4a11b619763ecdad7660dc70eacd51e7`
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
ENV PYTHON_VERSION=3.10.18
# Wed, 08 Oct 2025 18:52:37 GMT
ENV PYTHON_SHA256=ae665bc678abd9ab6a6e1573d2481625a53719bc517e9a634ed2b9fefae3817f
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
	-	`sha256:a23a20c70e0421cbbaa83817255c65f974762d5196b8e5ad1635f92eff70f7fe`  
		Last Modified: Thu, 09 Oct 2025 13:27:09 GMT  
		Size: 16.1 MB (16062969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb7fbb090dc26362f7395adc454a870c754f810b73ed4a43708199e7d890093`  
		Last Modified: Thu, 09 Oct 2025 13:27:08 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2087170bafc74be9f1778acc00cfb52d7af58229eb3d7459ffbf4f7c86cf33`  
		Last Modified: Thu, 09 Oct 2025 15:50:07 GMT  
		Size: 4.2 MB (4194470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-alpine3.21` - unknown; unknown

```console
$ docker pull hylang@sha256:96bb37b5097bf184df3a93b78e6258d68d6982c66eeb5c318c2887d20c14f932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.0 KB (663044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c77eaa8303c49f51b08caccb7011f9c45fe12b4e1f069687874efc367ae93a4`

```dockerfile
```

-	Layers:
	-	`sha256:4f9f9530d3205a68054ac627162d9de5c5ae4bd403a277b1a6fceca00f15aaad`  
		Last Modified: Thu, 09 Oct 2025 17:18:05 GMT  
		Size: 655.0 KB (655006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:190051e1aae15bb99719d3b6a7594c8a53e3cb4a777d5c122002cbdfec163aaa`  
		Last Modified: Thu, 09 Oct 2025 17:18:06 GMT  
		Size: 8.0 KB (8038 bytes)  
		MIME: application/vnd.in-toto+json
