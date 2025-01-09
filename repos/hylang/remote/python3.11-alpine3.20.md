## `hylang:python3.11-alpine3.20`

```console
$ docker pull hylang@sha256:2907d35e126d3e4f9e41f177b802672577d17daee01208c7c4dc3995553f96fc
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
$ docker pull hylang@sha256:2f19c663eca8abdb2f4758ce67a66f2c81e5c19d092a521b3180fce2702fde6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26413840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60be3fc25bd105b018b14f0d0138541e74f49935b9fdb9a5a6d32b25716bbcfe`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 03 Dec 2024 22:49:59 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 22:49:59 GMT
ENV LANG=C.UTF-8
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_VERSION=3.11.11
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
CMD ["python3"]
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HY_VERSION=1.0.0
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HYRULE_VERSION=0.7.0
# Wed, 11 Dec 2024 00:16:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 11 Dec 2024 00:16:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a1bc7353c62946b5992abb31549d0823f8904ca3ecedd64be6d502d48eeaca`  
		Last Modified: Wed, 08 Jan 2025 18:22:06 GMT  
		Size: 458.4 KB (458440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d9463d3caf6661f058fa6756216c7d78f0b37063fe66760d27be6b7d644050`  
		Last Modified: Wed, 08 Jan 2025 18:22:07 GMT  
		Size: 16.1 MB (16110829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edda734ffd05bef7132ecefe171e3bf5ad2c77b0ffe7884700234746e0037c6`  
		Last Modified: Wed, 08 Jan 2025 18:22:06 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf73f54d2da3fc63de001b82a761c30d4af5cda6b8dbab0122a9c9e9e91b57ac`  
		Last Modified: Wed, 08 Jan 2025 19:16:24 GMT  
		Size: 6.2 MB (6218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:35ecdd73fd4ad78397fd69dfb65284841ff881d15db81bf72bd5a0882f681015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.3 KB (666255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee56d71d02d13cb900fd798b91ac1595277ffb94d60edf7eb619f713a81c2ef`

```dockerfile
```

-	Layers:
	-	`sha256:ab50590ee7e88c637d96354814521704edfb06f0f150ce34bacff7171ec4d6a1`  
		Last Modified: Wed, 08 Jan 2025 19:16:23 GMT  
		Size: 658.2 KB (658217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0374b1faf882c9d4bb51a22c1e4af119b53624d072cee4c0a13ec642d22f16b1`  
		Last Modified: Wed, 08 Jan 2025 19:16:23 GMT  
		Size: 8.0 KB (8038 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.20` - linux; arm variant v6

```console
$ docker pull hylang@sha256:3cf10111f687cd0684a8371bcc438cf2ce1e84d67262c92efc96965677459c4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25750865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac29e9c9a641290db76fa78bd0648a0f7dc20e6d23e6c1a4808cda96dd2f5fe`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 03 Dec 2024 22:49:59 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 22:49:59 GMT
ENV LANG=C.UTF-8
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_VERSION=3.11.11
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
CMD ["python3"]
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HY_VERSION=1.0.0
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HYRULE_VERSION=0.7.0
# Wed, 11 Dec 2024 00:16:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 11 Dec 2024 00:16:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Wed, 08 Jan 2025 17:23:56 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06475ab9ef588959bc9af33c0c0abe5db6fa1ce5288e003553a7a069a5c7f05`  
		Last Modified: Thu, 09 Jan 2025 07:55:21 GMT  
		Size: 459.2 KB (459192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da5f2d349d4fa6a5a2f1232d4b10bfc9233682759f052ff2259ab85f066ee40`  
		Last Modified: Thu, 09 Jan 2025 08:08:50 GMT  
		Size: 15.7 MB (15701943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56f05c973f797663626d090d8b1acaf56be5cd3fa251de6f7ca0dfc2f25489b`  
		Last Modified: Thu, 09 Jan 2025 08:08:49 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7dddd761f9417aefa73bc65fb218d21a1111b7c240d4ceb62682372660ef691`  
		Last Modified: Thu, 09 Jan 2025 10:19:21 GMT  
		Size: 6.2 MB (6218010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:a79c5214530d974be9527d85371e354a9c2ffe991f8f4800a841eb2e4ad13d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 KB (7899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c7d3d3a5a60e798e95382f90642d2da4bd6424b3ca2257c6bc88b45dc2d69b`

```dockerfile
```

-	Layers:
	-	`sha256:93df29f365c36f7e589f7430ce435c3d46171732b6ca624c03589e89351e844e`  
		Last Modified: Thu, 09 Jan 2025 10:19:20 GMT  
		Size: 7.9 KB (7899 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.20` - linux; arm variant v7

```console
$ docker pull hylang@sha256:eafb5a0ff9a2ca639804f59290f9c0451e7179197d337579a6132a4dd6981fdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25054253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd5a424754ce7aa05b17051c802c31af6600bef0d8bca94213cd3b814ae4f30`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 03 Dec 2024 22:49:59 GMT
ADD alpine-minirootfs-3.20.5-armv7.tar.gz / # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 22:49:59 GMT
ENV LANG=C.UTF-8
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_VERSION=3.11.11
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
CMD ["python3"]
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HY_VERSION=1.0.0
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HYRULE_VERSION=0.7.0
# Wed, 11 Dec 2024 00:16:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 11 Dec 2024 00:16:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c8a32ed454e751770c0976636b8d0d0fccc4f778a2dd26c428067d613be1a299`  
		Last Modified: Wed, 08 Jan 2025 17:34:15 GMT  
		Size: 3.1 MB (3095514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c41d5d0fb800601d84faf485d0154f5a08e9c4f4ff9caf700df1ff83eda83db`  
		Last Modified: Thu, 09 Jan 2025 08:27:05 GMT  
		Size: 458.4 KB (458421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e501e14cf03041206726eb5655a661c7d262d5ba7cf2538800c2c621c22851e2`  
		Last Modified: Thu, 09 Jan 2025 08:41:22 GMT  
		Size: 15.3 MB (15281858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aec970c52aff2c3433353104fde60ac095293e486c9e5ba889b58d8df35ef36`  
		Last Modified: Thu, 09 Jan 2025 08:41:21 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5226998bc23851e94eeb6d173aca52042657fee94c5d0fc872ec27285395137a`  
		Last Modified: Thu, 09 Jan 2025 12:17:36 GMT  
		Size: 6.2 MB (6218210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:71be9c3e0774729787b71f73916bec76db78752cf8f7a5623400cec9f8b37bbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.2 KB (669228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb9e0201cef2fda90b112c3c28a7daa43a54c2791455ff9f2fb0f9faf912241c`

```dockerfile
```

-	Layers:
	-	`sha256:053a207f589f0daed3f28c89ece117bd498c55c60bf35d00923b570c55a8baff`  
		Last Modified: Thu, 09 Jan 2025 12:17:36 GMT  
		Size: 661.1 KB (661114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b11dd7c9dd3d1ae5da37647faa27cde5c81d7d4e865affbdb6c1d72593075114`  
		Last Modified: Thu, 09 Jan 2025 12:17:35 GMT  
		Size: 8.1 KB (8114 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:5c4a0a9bc5c969bd3be40ddeb2e80b1c6e9fc38cf2d147f7c8cbf12d47e4b47b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (27014384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a512433a6548b73ba69edb2820caf2fc2fda06b6932991bfce11ffaea3033af`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 03 Dec 2024 22:49:59 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 22:49:59 GMT
ENV LANG=C.UTF-8
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_VERSION=3.11.11
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
CMD ["python3"]
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HY_VERSION=1.0.0
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HYRULE_VERSION=0.7.0
# Wed, 11 Dec 2024 00:16:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 11 Dec 2024 00:16:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcd6e0cbc06e1fbb5ab80cef8d41b8775ebcc00733d4f1f30773085b1216524`  
		Last Modified: Thu, 09 Jan 2025 04:46:01 GMT  
		Size: 460.6 KB (460581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497031680e280a91d943516016e43443d1d2db397adf134ad1741da2ee912547`  
		Last Modified: Thu, 09 Jan 2025 04:57:48 GMT  
		Size: 16.2 MB (16244747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a8044108c0919cfc4bf41c32f793d7da5e8044762147918eb87bdede518755`  
		Last Modified: Thu, 09 Jan 2025 04:57:47 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46704162e69326f303da22dc060bfdbdbadf8c76b7b3ae6aafc4bf6ca5997252`  
		Last Modified: Thu, 09 Jan 2025 08:23:29 GMT  
		Size: 6.2 MB (6218037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:2bacc3b022b136040943bbc55081893d690512f620d6b58a035043d6408f5aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.4 KB (666415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca3afe8ba872ced2410392f9c799e2bfc2ae61e21db51ab94608655c85f12c6`

```dockerfile
```

-	Layers:
	-	`sha256:af11330fdbd7ae79bcabe7b12c4f9718a5e28347df914078467b6f5bc066783c`  
		Last Modified: Thu, 09 Jan 2025 08:23:29 GMT  
		Size: 658.3 KB (658273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04b48c85379f318da8fb2354ad88dd352e350bbd167f7732efc8811a163aa3db`  
		Last Modified: Thu, 09 Jan 2025 08:23:28 GMT  
		Size: 8.1 KB (8142 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.20` - linux; 386

```console
$ docker pull hylang@sha256:e9bceb6d6d6337772942c4186d461e6beeba8f056172f88c911b0030eddb04d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 MB (26492179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:087c36f6779f379455003b0993b346bf571aaf2d6ecd67d924f695165ccd8310`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 03 Dec 2024 22:49:59 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 22:49:59 GMT
ENV LANG=C.UTF-8
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_VERSION=3.11.11
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
CMD ["python3"]
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HY_VERSION=1.0.0
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HYRULE_VERSION=0.7.0
# Wed, 11 Dec 2024 00:16:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 11 Dec 2024 00:16:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Wed, 08 Jan 2025 17:23:34 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9207b2dbe02748ce4601cb478d39c3616b5673d8febc39002efa2983de2743b5`  
		Last Modified: Wed, 08 Jan 2025 18:19:23 GMT  
		Size: 458.8 KB (458836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96e7ca750d43b4f3219e5cf02a3b69668595236c396fe9ba03baa3998253ca3`  
		Last Modified: Wed, 08 Jan 2025 18:19:23 GMT  
		Size: 16.3 MB (16344064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ff40bbf441fea0191a572a00571e101fb919ba910cd75251966f4e8917c5b8`  
		Last Modified: Wed, 08 Jan 2025 18:19:22 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:353ec11ce7c660c09df24d69a2e1707c08c1284ab0c3148aaefc5e2476d01b26`  
		Last Modified: Wed, 08 Jan 2025 19:15:17 GMT  
		Size: 6.2 MB (6218060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:1750b5dbed46741b41e8b26654cbbca334ce6cb45eab823190d8be7fe12f5e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.2 KB (666198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a75ffbf405cb21f6f4534e3f663116322a987b4429d2d48bb9c8b97038343e58`

```dockerfile
```

-	Layers:
	-	`sha256:10b4191e52ba7385039ffdd2816c332be3eda79f0bdcb45b2173947210a43b28`  
		Last Modified: Wed, 08 Jan 2025 19:15:17 GMT  
		Size: 658.2 KB (658192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54e16ba818f9e2728dea8ae8592a959c121f6551166d5936fd693d20bb515eab`  
		Last Modified: Wed, 08 Jan 2025 19:15:17 GMT  
		Size: 8.0 KB (8006 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.20` - linux; ppc64le

```console
$ docker pull hylang@sha256:94755288e8ed48f3e3b700769829ec716047479b5d393dbed49976463c3b7843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27097173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9903aca47b11b6dccc13d7f5c4e5ca68a0a7dd80ad042027c103784c224245c`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 03 Dec 2024 22:49:59 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 22:49:59 GMT
ENV LANG=C.UTF-8
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_VERSION=3.11.11
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
CMD ["python3"]
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HY_VERSION=1.0.0
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HYRULE_VERSION=0.7.0
# Wed, 11 Dec 2024 00:16:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 11 Dec 2024 00:16:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Wed, 08 Jan 2025 17:24:56 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236c49b59f7bc6253ef66b11876ac777a6ca1e7bd5b4685cbf246e81c6b11613`  
		Last Modified: Wed, 08 Jan 2025 23:47:09 GMT  
		Size: 461.0 KB (460965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922da47dc22036756c1ebb3c52c47dc6ef8344684363309bb69d08827b590f7f`  
		Last Modified: Thu, 09 Jan 2025 00:03:06 GMT  
		Size: 16.8 MB (16843449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb35d96f51f61585889323368266b38db69be6c993904ccab1867ea4e4002e7e`  
		Last Modified: Thu, 09 Jan 2025 00:03:04 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ac842af09f4f4414bff2e678817bae6a0ccb4efff8fe813aa56e5230ff1250`  
		Last Modified: Thu, 09 Jan 2025 03:51:20 GMT  
		Size: 6.2 MB (6218105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:0189c02e6cef281203ed0594ade18a551cc1ea7f542e1c3eb713aab58f0495d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.4 KB (664382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87fbbbf1b938e906d1542f12daf81ea96b62d132c7ab0561a048d87bb13018eb`

```dockerfile
```

-	Layers:
	-	`sha256:42551801ff0fd3b72dbce39da7f2e41e63a9fc5e315f8aa8b00db22722f37573`  
		Last Modified: Thu, 09 Jan 2025 03:51:20 GMT  
		Size: 656.3 KB (656300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61d1900456342f3bbe3d59017a4b2d4ab279f1bfe1a561a6ff2f0c4d1225cda8`  
		Last Modified: Thu, 09 Jan 2025 03:51:19 GMT  
		Size: 8.1 KB (8082 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.20` - linux; s390x

```console
$ docker pull hylang@sha256:88a4053c72f11b21153e3d9472645443222a262f62293bc1c17d3635cc927761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26734235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88b73827c14c774417ca68bff0e795d67d6b3800c0979dbbd1407c7f69b88eb6`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 03 Dec 2024 22:49:59 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 22:49:59 GMT
ENV LANG=C.UTF-8
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_VERSION=3.11.11
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
CMD ["python3"]
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HY_VERSION=1.0.0
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HYRULE_VERSION=0.7.0
# Wed, 11 Dec 2024 00:16:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 11 Dec 2024 00:16:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Wed, 08 Jan 2025 17:25:57 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985cab1b685e8021d8265573dee27e7d43bce4b069c5b582887d01978fffc36b`  
		Last Modified: Thu, 09 Jan 2025 06:00:40 GMT  
		Size: 459.4 KB (459369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5639218b82c2b4703d0c93f561e6b6d43c5fbacbb568b98b9304dfee3c41b22e`  
		Last Modified: Thu, 09 Jan 2025 10:09:32 GMT  
		Size: 16.6 MB (16593276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30845a8a818867f399b9b864406783028c9ea0873d6a4938681cb4b4032d3f8`  
		Last Modified: Thu, 09 Jan 2025 10:09:30 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe898af13bfd4f75008f75216036ae3c8ecf2383afd994cd8efc9d5df526a77`  
		Last Modified: Thu, 09 Jan 2025 10:54:09 GMT  
		Size: 6.2 MB (6218017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:231d9eb97956d20350ac5abf421efdb5e44b8886f72107556a9c76705c884726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.3 KB (664304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:589451cf50f9d19cface17b7439694840a2db1bcf33bed5ebc417e88908caa8e`

```dockerfile
```

-	Layers:
	-	`sha256:dba2c67ad2ee9ff64c6582dda3020a2a891ad8c84f6c672dfcea48336fba0e4a`  
		Last Modified: Thu, 09 Jan 2025 10:54:09 GMT  
		Size: 656.3 KB (656266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f702cae30aa30339b4c106115f16c4807db322e0c7d815ee625435632889354`  
		Last Modified: Thu, 09 Jan 2025 10:54:09 GMT  
		Size: 8.0 KB (8038 bytes)  
		MIME: application/vnd.in-toto+json
