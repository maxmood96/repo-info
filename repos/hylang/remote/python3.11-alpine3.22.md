## `hylang:python3.11-alpine3.22`

```console
$ docker pull hylang@sha256:6b0cef7685fcaebeac5787a065d06476ca93c30c4bf9f08dcfe33aa4bd7a97b4
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
$ docker pull hylang@sha256:3d39302ddc3f7737a96a22b71b0b6600314af147a2df7971ca8eb1c3b039d852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27132546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e72134c09110972ba89be2dc29191365fb256dcf23b8453530daa86dc1b105`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Tue, 03 Mar 2026 20:17:57 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Mar 2026 20:17:57 GMT
ENV LANG=C.UTF-8
# Tue, 03 Mar 2026 20:17:57 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Mar 2026 20:17:57 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Mar 2026 20:17:57 GMT
ENV PYTHON_VERSION=3.11.15
# Tue, 03 Mar 2026 20:17:57 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Tue, 03 Mar 2026 20:21:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Mar 2026 20:21:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Mar 2026 20:21:55 GMT
CMD ["python3"]
# Tue, 03 Mar 2026 21:07:19 GMT
ENV HY_VERSION=1.2.0
# Tue, 03 Mar 2026 21:07:19 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 03 Mar 2026 21:07:19 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 03 Mar 2026 21:07:19 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5961c54ff2693b41e3550b1849b4c21c8fc7163fbf57a43f01ab9424c2ab9e36`  
		Last Modified: Tue, 03 Mar 2026 20:22:01 GMT  
		Size: 457.1 KB (457051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d352c0e1fceb472d620f6d1a42e4dfcacb0f91825b0c2506e7a331ebbfa250dd`  
		Last Modified: Tue, 03 Mar 2026 20:22:02 GMT  
		Size: 16.0 MB (15953372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f09189cd65631d1a483c9e6f02955c3dd641ce39cda1bff2d4517cf96cc71b5`  
		Last Modified: Tue, 03 Mar 2026 20:22:01 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc44740a1c3179671314ec541f9a9461cc4fcac0ccd8fd54385ef01eed96f7f`  
		Last Modified: Tue, 03 Mar 2026 21:07:25 GMT  
		Size: 6.9 MB (6916999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:b9589445295d457348e8c0e8712b3f4ea28382fd78bc1f2f5411f0c908edddd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.7 KB (706729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492e794b9ce6298e64b1e30b074d50085a8b6d4f84d89b74e982719350a26720`

```dockerfile
```

-	Layers:
	-	`sha256:db5100195627bcadee3d8bafee28ec61a1623aa15cea58a77e629729cb49e24a`  
		Last Modified: Tue, 03 Mar 2026 21:07:25 GMT  
		Size: 698.6 KB (698627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2ee014ff84c2f5878a89e1b66d4203ccce6c4a757b8bc7e391d79314c8aa758`  
		Last Modified: Tue, 03 Mar 2026 21:07:25 GMT  
		Size: 8.1 KB (8102 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.22` - linux; arm variant v6

```console
$ docker pull hylang@sha256:c7284f969c1ce56ae32300f5c8116bc9cb12ce52d380533d8404b1a2cea7c663
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26376796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d5f39f902bfc3ae2bb24f51dfb15b6722b69c4421a619d19667a5895e8cd5f`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:06 GMT
ADD alpine-minirootfs-3.22.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:06 GMT
CMD ["/bin/sh"]
# Tue, 03 Mar 2026 20:13:07 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Mar 2026 20:13:07 GMT
ENV LANG=C.UTF-8
# Tue, 03 Mar 2026 20:13:07 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Mar 2026 20:13:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Mar 2026 20:13:07 GMT
ENV PYTHON_VERSION=3.11.15
# Tue, 03 Mar 2026 20:13:07 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Tue, 03 Mar 2026 20:19:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Mar 2026 20:19:41 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Mar 2026 20:19:41 GMT
CMD ["python3"]
# Tue, 03 Mar 2026 20:57:36 GMT
ENV HY_VERSION=1.2.0
# Tue, 03 Mar 2026 20:57:36 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 03 Mar 2026 20:57:36 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 03 Mar 2026 20:57:36 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:835838571e5c80c63481753299e25a9f89f366d8f4a9c1a2043b8fdf98176f17`  
		Last Modified: Wed, 28 Jan 2026 01:18:10 GMT  
		Size: 3.5 MB (3505046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11482d4b91ec703a4b8ab0f107c891e2e5372535de05c4cf8a28ab492db48b46`  
		Last Modified: Tue, 03 Mar 2026 20:19:46 GMT  
		Size: 457.9 KB (457885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003af44295a01a3e989abd06baf72232e864550c94a1e5afd7f2a99655f4ee69`  
		Last Modified: Tue, 03 Mar 2026 20:19:46 GMT  
		Size: 15.5 MB (15496548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62db4319c8d9e318c69e2741cb618acf421f20d7dbcc685df5944ded366259c`  
		Last Modified: Tue, 03 Mar 2026 20:19:46 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6ff8b8a2e2ac5108b74bf213150f1de27079c322717f38b78bd7b49219fb38`  
		Last Modified: Tue, 03 Mar 2026 20:57:41 GMT  
		Size: 6.9 MB (6917068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:74f3ba07e2d101bfcb80277bce6ad32127706b5456602513effc78314cad6c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 KB (7968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c440173a9daa676795fbe0e218d0744eef86d9e7827f1a1f55306c3a52163d9`

```dockerfile
```

-	Layers:
	-	`sha256:4f4e1f924e1ea864662f82cf8e2a62c9b332544cd8103a22b5e8ec238ae468ad`  
		Last Modified: Tue, 03 Mar 2026 20:57:40 GMT  
		Size: 8.0 KB (7968 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.22` - linux; arm variant v7

```console
$ docker pull hylang@sha256:2657e23db2c58ca6511de5b8f6ad6be437fa5fec71470a5a8c2d3037b49a3d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25688965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d4920021581fdf10448c846f9ebecb91496f2b2ffbed60764f8283209a54944`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:29 GMT
ADD alpine-minirootfs-3.22.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:29 GMT
CMD ["/bin/sh"]
# Tue, 03 Mar 2026 20:45:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Mar 2026 20:45:54 GMT
ENV LANG=C.UTF-8
# Tue, 03 Mar 2026 20:45:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Mar 2026 20:45:54 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Mar 2026 20:45:54 GMT
ENV PYTHON_VERSION=3.11.15
# Tue, 03 Mar 2026 20:45:54 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Tue, 03 Mar 2026 20:52:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Mar 2026 20:52:32 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Mar 2026 20:52:32 GMT
CMD ["python3"]
# Tue, 03 Mar 2026 21:00:18 GMT
ENV HY_VERSION=1.2.0
# Tue, 03 Mar 2026 21:00:18 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 03 Mar 2026 21:00:18 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 03 Mar 2026 21:00:18 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:caca1d0e2f8affe80569328af55c755a8480801c5ee912e55aaa828c8209aa6e`  
		Last Modified: Wed, 28 Jan 2026 01:18:35 GMT  
		Size: 3.2 MB (3223629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6a506088830a93904dd9f08a0a8662d04b6e092015c844813c1a367eca16fa`  
		Last Modified: Tue, 03 Mar 2026 20:52:39 GMT  
		Size: 457.1 KB (457068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6636c9888c91cbd834ddab24fc4c7dda364ed59b6dc4d7534853580a8765bb6`  
		Last Modified: Tue, 03 Mar 2026 20:52:39 GMT  
		Size: 15.1 MB (15091045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6560525fe128528ba5bb5835c032690747cbfd8d2707dfa99337d35f40ddee`  
		Last Modified: Tue, 03 Mar 2026 20:52:39 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9843e16f9680185e956825c8beddc1221dcc0553606dd65754431349c5de5a13`  
		Last Modified: Tue, 03 Mar 2026 21:00:29 GMT  
		Size: 6.9 MB (6916975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:00463bbc3a40a9f24b464a1cf13d60029071f41ee6664b20d30d7557cc3122cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.8 KB (709836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eda3f919611dea88fa2d4231739c6305bcced44a05e334718b15d904baf5f2c3`

```dockerfile
```

-	Layers:
	-	`sha256:5af3af9c599abe17b082ea3eae589a734b72abbc4ff40e8f4aa15d9e8ff48d71`  
		Last Modified: Tue, 03 Mar 2026 21:00:25 GMT  
		Size: 701.7 KB (701653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a57f9ccfa36263db14f93358c0654b17da2f45440b81453dee8c08c53c42ed9d`  
		Last Modified: Tue, 03 Mar 2026 21:00:24 GMT  
		Size: 8.2 KB (8183 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:be9beafd85c8df086271a3f872bc5f0d9e943fa012f0c01dcf649e1c6fa3cbfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27546186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40fff3c2203f3a2b5537282cd708b61663ce5dcf5c00168bcae54c961a3ff8ed`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:55 GMT
ADD alpine-minirootfs-3.22.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:55 GMT
CMD ["/bin/sh"]
# Tue, 03 Mar 2026 20:23:44 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Mar 2026 20:23:44 GMT
ENV LANG=C.UTF-8
# Tue, 03 Mar 2026 20:23:44 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Mar 2026 20:23:44 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Mar 2026 20:23:44 GMT
ENV PYTHON_VERSION=3.11.15
# Tue, 03 Mar 2026 20:23:44 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Tue, 03 Mar 2026 20:29:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Mar 2026 20:29:43 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Mar 2026 20:29:43 GMT
CMD ["python3"]
# Tue, 03 Mar 2026 21:05:23 GMT
ENV HY_VERSION=1.2.0
# Tue, 03 Mar 2026 21:05:23 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 03 Mar 2026 21:05:23 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 03 Mar 2026 21:05:23 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d741ee1608f399e21c72d05f0f818c348c6801af33aeb83523893d09dc153957`  
		Last Modified: Wed, 28 Jan 2026 01:18:00 GMT  
		Size: 4.1 MB (4139519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53dc4ee39ef1f3007b83bc944e5bd60678aea3429cebe4dc141a8f729c6b1f5`  
		Last Modified: Tue, 03 Mar 2026 20:29:50 GMT  
		Size: 459.2 KB (459154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69eb146b1c0763df8a2ba623f5484139a90498e8ad09d66af61fb771b293c4e`  
		Last Modified: Tue, 03 Mar 2026 20:29:51 GMT  
		Size: 16.0 MB (16030241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af321f53d5c0d4581fb7ce9f25c11166904a119afb74e125fcdc0381291bd166`  
		Last Modified: Tue, 03 Mar 2026 20:29:50 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2f75a4ee84ea87f1de1327c2d3fd30f2ce331dbb8f7432af5edd45d92f316d`  
		Last Modified: Tue, 03 Mar 2026 21:05:29 GMT  
		Size: 6.9 MB (6917022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:2250ff990e9561dd4c3042bf2c44f64195b26ed61494bfd284ebd2378a2ba841
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.9 KB (706890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d53b224d6bc8f705f33e9fdf7e2f10874501972a5083e940c2a0866b7c969cc6`

```dockerfile
```

-	Layers:
	-	`sha256:33e81e037cccbd922cda8be34e79e38885aba277a6effe9319d2b7a331062ffb`  
		Last Modified: Tue, 03 Mar 2026 21:05:29 GMT  
		Size: 698.7 KB (698683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:478b64452b9a4b49264540a6179530ecc000eaaab9d65a880bf55579da22f5e2`  
		Last Modified: Tue, 03 Mar 2026 21:05:29 GMT  
		Size: 8.2 KB (8207 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.22` - linux; 386

```console
$ docker pull hylang@sha256:55f460ae01693ce18eee09288554a06f9d69a9e189d79af34c67321355592571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27172043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a3cb25f557c2474bb0af79d37042b101f24a4dcc2a1684a99f5877bd4143e6`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:53 GMT
ADD alpine-minirootfs-3.22.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:53 GMT
CMD ["/bin/sh"]
# Tue, 03 Mar 2026 20:19:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Mar 2026 20:19:43 GMT
ENV LANG=C.UTF-8
# Tue, 03 Mar 2026 20:19:43 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Mar 2026 20:19:43 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Mar 2026 20:19:43 GMT
ENV PYTHON_VERSION=3.11.15
# Tue, 03 Mar 2026 20:19:43 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Tue, 03 Mar 2026 20:25:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Mar 2026 20:25:17 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Mar 2026 20:25:17 GMT
CMD ["python3"]
# Tue, 03 Mar 2026 21:00:04 GMT
ENV HY_VERSION=1.2.0
# Tue, 03 Mar 2026 21:00:04 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 03 Mar 2026 21:00:04 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 03 Mar 2026 21:00:04 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:757a99eda61f22434071cfbc7a70f9526b63aeb5479a64272982017ee7cd9cfd`  
		Last Modified: Wed, 28 Jan 2026 01:18:59 GMT  
		Size: 3.6 MB (3620732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d694e8cf7497f549e25e0236c609e598a7f65fc40484222921bed600b47e37`  
		Last Modified: Tue, 03 Mar 2026 20:25:24 GMT  
		Size: 457.5 KB (457512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51a8385b6fc8b141da76d5aa85fde752c3569f764d711027174e46af18731e0`  
		Last Modified: Tue, 03 Mar 2026 20:25:24 GMT  
		Size: 16.2 MB (16176468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2363b1a811b57307fa5a984b51730aef0832032887fa7cbb8143f033dd82ce5`  
		Last Modified: Tue, 03 Mar 2026 20:25:23 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc04b8963657fd43389140f4647c5ab775da9aa254e402446750108e0db5485`  
		Last Modified: Tue, 03 Mar 2026 21:00:11 GMT  
		Size: 6.9 MB (6917081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:9546b5991401832efaf207bcd088b14962c707776cf1207f2c10bf2c35fa736f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.7 KB (706673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d461fe866d5c404b47588dd6dd42087267e8efe3f63e78fa3a2d3c83134659a5`

```dockerfile
```

-	Layers:
	-	`sha256:7bec92c194dbf1721b1b77bf3595e4af08df46bf0e64882efa79e0a3ec3b68ea`  
		Last Modified: Tue, 03 Mar 2026 21:00:10 GMT  
		Size: 698.6 KB (698602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7e2cc26594e35e1ed996a26c78acf3ef16d014210a235983f88ddefd951fa01`  
		Last Modified: Tue, 03 Mar 2026 21:00:10 GMT  
		Size: 8.1 KB (8071 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.22` - linux; ppc64le

```console
$ docker pull hylang@sha256:1277cc8857c55e1ecb257db2231fd49be132eeb60f3b9a25ee9423cfa94f160b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.8 MB (27844299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8c3622fc25545024d16ff2cc7c4fbe414cefcb5a356d97f395259af4278303`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:35 GMT
ADD alpine-minirootfs-3.22.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:35 GMT
CMD ["/bin/sh"]
# Wed, 04 Feb 2026 23:18:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 23:18:55 GMT
ENV LANG=C.UTF-8
# Wed, 04 Feb 2026 23:18:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Feb 2026 23:18:55 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 04 Feb 2026 23:18:55 GMT
ENV PYTHON_VERSION=3.11.14
# Wed, 04 Feb 2026 23:18:55 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Thu, 05 Feb 2026 00:24:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 05 Feb 2026 00:24:10 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 05 Feb 2026 00:24:10 GMT
CMD ["python3"]
# Thu, 05 Feb 2026 01:44:07 GMT
ENV HY_VERSION=1.2.0
# Thu, 05 Feb 2026 01:44:07 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 05 Feb 2026 01:44:07 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 05 Feb 2026 01:44:07 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d7b7d5bab08f20b53e85395b2d6e793469e3acdbe8644bd234992524588b440f`  
		Last Modified: Wed, 28 Jan 2026 01:17:44 GMT  
		Size: 3.7 MB (3734297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19de91782b5210fa2a840570e56f1f0ce967a0dbce407bdbea51661c429df7ef`  
		Last Modified: Wed, 04 Feb 2026 23:29:34 GMT  
		Size: 459.6 KB (459570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89be60950fde2b38b66fdac7ac2fc9b03ebf98c00897b52600cd0e8c8912977`  
		Last Modified: Thu, 05 Feb 2026 00:24:25 GMT  
		Size: 16.7 MB (16675126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc63008d363e8190f469d63776d480c998c718c866f40a7461676e444f77f68`  
		Last Modified: Thu, 05 Feb 2026 00:24:24 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369c7c22ff353f61409782fd38319cecc3fa70273a986e0da73bbe2560670b8a`  
		Last Modified: Thu, 05 Feb 2026 01:44:20 GMT  
		Size: 7.0 MB (6975057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:9e227129a9e3b522f620994b41d9b6ca2d85adc37f1c27d0910ec51af714e2f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **704.9 KB (704857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c288d7e52344f23f45091e7e7a453551cc695847c02b10b092e47e7dc543b2bb`

```dockerfile
```

-	Layers:
	-	`sha256:d06da0c131654c4406c10c2a263e23187b3541ce4aa8540f06bc80f21eea8c50`  
		Last Modified: Thu, 05 Feb 2026 01:44:20 GMT  
		Size: 696.7 KB (696710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da07fd8aca8a110f2a73822b0a1864f510b827d2efafaa54baefaf1a6b9ef33d`  
		Last Modified: Thu, 05 Feb 2026 01:44:19 GMT  
		Size: 8.1 KB (8147 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.22` - linux; riscv64

```console
$ docker pull hylang@sha256:9509a5e2906be8ef39c5fb626b0a2eb9b83a1ee8ba67511f195cfe2104a377ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26835447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e80daeda90de744f3856c3442d7c77acf066f5f01b3c020fe496e2fd71811d1a`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Sat, 07 Feb 2026 06:49:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Feb 2026 06:49:05 GMT
ENV LANG=C.UTF-8
# Sat, 07 Feb 2026 06:49:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sat, 07 Feb 2026 06:49:05 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 07 Feb 2026 06:49:05 GMT
ENV PYTHON_VERSION=3.11.14
# Sat, 07 Feb 2026 06:49:05 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Sat, 07 Feb 2026 09:46:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Sat, 07 Feb 2026 09:46:46 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 07 Feb 2026 09:46:46 GMT
CMD ["python3"]
# Sun, 08 Feb 2026 03:24:20 GMT
ENV HY_VERSION=1.2.0
# Sun, 08 Feb 2026 03:24:20 GMT
ENV HYRULE_VERSION=1.0.1
# Sun, 08 Feb 2026 03:24:20 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sun, 08 Feb 2026 03:24:20 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1b70971b0cebe06b61be54939b8750cc0699f00e0eab86e842620b089131af`  
		Last Modified: Sat, 07 Feb 2026 07:21:38 GMT  
		Size: 457.4 KB (457417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7be2aea51ae713958b7706c6e41970a69d00c31b4c9e23655cf97b622c2f3a3`  
		Last Modified: Sat, 07 Feb 2026 09:47:38 GMT  
		Size: 15.9 MB (15886106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7158092e237e319d80d2fdcd10fbba9b8b537d207e8da25e7509eb26b3e60daa`  
		Last Modified: Sat, 07 Feb 2026 09:47:36 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d374e426fcf1f919faf8f748da420881293156a75cd7e5a15f821e8a13bc607`  
		Last Modified: Sun, 08 Feb 2026 03:25:03 GMT  
		Size: 7.0 MB (6974251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:b2bb9aeb05e340330c2266b53e6b214b8c000582584fb4f9dd8c53adb3006353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **704.9 KB (704853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0a926d5bd1c35a56e8fd7b54a932da7930533b9f1c4737f8c9350923e1edaff`

```dockerfile
```

-	Layers:
	-	`sha256:fb246001cef071fa5f25d31e45b8a919d038319f0b9bcdd3d9b3d2afaaa291c8`  
		Last Modified: Sun, 08 Feb 2026 03:25:02 GMT  
		Size: 696.7 KB (696706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b635cc0f751171c6de9693c242c9a3479c5f38dfa36afd0b09f907b7fe42a947`  
		Last Modified: Sun, 08 Feb 2026 03:25:02 GMT  
		Size: 8.1 KB (8147 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.22` - linux; s390x

```console
$ docker pull hylang@sha256:76737cb9546edb3941d8e3dbd8bb4d45d92ad47f2014e0d4ed5a4d1938b94262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27458619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077bb6a26d2939e1af32da52ab232d27a22ce2a7e70b630d00db3e20dc88163f`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.22.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 03 Mar 2026 20:45:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Mar 2026 20:45:54 GMT
ENV LANG=C.UTF-8
# Tue, 03 Mar 2026 20:45:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Mar 2026 20:45:54 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Mar 2026 20:45:54 GMT
ENV PYTHON_VERSION=3.11.15
# Tue, 03 Mar 2026 20:45:54 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Tue, 03 Mar 2026 20:52:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Mar 2026 20:52:18 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Mar 2026 20:52:18 GMT
CMD ["python3"]
# Tue, 03 Mar 2026 21:20:41 GMT
ENV HY_VERSION=1.2.0
# Tue, 03 Mar 2026 21:20:41 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 03 Mar 2026 21:20:41 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 03 Mar 2026 21:20:41 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:dab48b8d1bab09fede3f54264828e67466f10d64acc37d9412190034dbcbf61f`  
		Last Modified: Wed, 28 Jan 2026 01:17:16 GMT  
		Size: 3.7 MB (3650434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ded8233d21b05e023d666cc0d1556456d5c8cce5e290b46cea0fcdcd2024b7e`  
		Last Modified: Tue, 03 Mar 2026 20:52:29 GMT  
		Size: 458.0 KB (458038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6d7c00821bf8736c787259479f5c31fc95c7b6ef2ed62f4aff74cfecab2904`  
		Last Modified: Tue, 03 Mar 2026 20:52:30 GMT  
		Size: 16.4 MB (16432788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8abd15222cb9a720b29e901590107090652b9ffff13b5b1d29f2bcf91dfd5cc`  
		Last Modified: Tue, 03 Mar 2026 20:52:29 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9687665380511f72232d5aa80d8c43fd4470119ac79883267006ea597a34511d`  
		Last Modified: Tue, 03 Mar 2026 21:20:52 GMT  
		Size: 6.9 MB (6917109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:bf2cce6c542647375eeb06ba55e4d2f2d83ffc4d22ecf95109d9aaac9107238d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **704.8 KB (704779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48bfc1c8e877dab4f4c6c0940179fcd7c4dd21f81be63da4208ba9bf7aeff09f`

```dockerfile
```

-	Layers:
	-	`sha256:e97c7bf75bc670d65c23af6e432b04c33ce44748b03134d8cfe8ee2d7b457525`  
		Last Modified: Tue, 03 Mar 2026 21:20:52 GMT  
		Size: 696.7 KB (696676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59e51d31b401451fa1b44c3e23d8add5dc34959dca3e6225235e2a5dcd6f699b`  
		Last Modified: Tue, 03 Mar 2026 21:20:52 GMT  
		Size: 8.1 KB (8103 bytes)  
		MIME: application/vnd.in-toto+json
