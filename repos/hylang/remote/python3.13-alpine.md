## `hylang:python3.13-alpine`

```console
$ docker pull hylang@sha256:ce7069012312d54e19401ede57bbcb0bf0c23383a742149facd6b2dd7bafd12a
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

### `hylang:python3.13-alpine` - linux; amd64

```console
$ docker pull hylang@sha256:9fa4daf5289350cfe01146b02cd71b980ade12f769d2da8abb8211cb1a22f6fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22309014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b433747f2b49edf8856e7fc4f86a9dee8147a9c2eb0f955525e918c343b711bc`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 00:35:28 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 00:35:28 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 04 Dec 2025 00:35:28 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 04 Dec 2025 00:35:28 GMT
ENV PYTHON_VERSION=3.13.10
# Thu, 04 Dec 2025 00:35:28 GMT
ENV PYTHON_SHA256=bc673c04375a1a3f0808c27ba8f0411ab811ad390a8740318ccb9c60fad8fd77
# Thu, 04 Dec 2025 00:41:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 04 Dec 2025 00:41:00 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 04 Dec 2025 00:41:00 GMT
CMD ["python3"]
# Thu, 04 Dec 2025 19:51:11 GMT
ENV HY_VERSION=1.1.0
# Thu, 04 Dec 2025 19:51:11 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 04 Dec 2025 19:51:11 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 04 Dec 2025 19:51:11 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f5e2eb0b6350cca3b143b0e1f88943247597356e5a09114d594538dd7c649d`  
		Last Modified: Thu, 04 Dec 2025 00:41:12 GMT  
		Size: 460.8 KB (460808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e14dabd8b3315df7618d130a59b58a7a4707d5a5aeff2e8f1cf166741cec1f`  
		Last Modified: Thu, 04 Dec 2025 00:41:13 GMT  
		Size: 12.5 MB (12499655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df846d09a0a5c6d2c613af80e8e7d835863bdc4d9e89cb47cc05a7f4d4dc903c`  
		Last Modified: Thu, 04 Dec 2025 00:41:12 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c922a9d5780b88e7aca80b2578c6af169fe43345bf858df0a46206e8a8f0643`  
		Last Modified: Thu, 04 Dec 2025 19:51:24 GMT  
		Size: 5.5 MB (5488988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:16a3896fb464291baa4d12ac01e548f41c3ac372572bc7b7056491178800eaef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **632.0 KB (632024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88d3590be30059c956debd558b679c01642c3698a891e48491e5058f06477d3`

```dockerfile
```

-	Layers:
	-	`sha256:0cd25e905b4ac9aeb94226309fa98b015f865eb94e67955f2574d3248895bb34`  
		Last Modified: Thu, 04 Dec 2025 21:19:49 GMT  
		Size: 622.6 KB (622632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a240fd24c7b239fac3ce95f41b997413b5a3d19e2b31c090df7e51e8e2f0dec`  
		Last Modified: Thu, 04 Dec 2025 21:19:49 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine` - linux; arm variant v6

```console
$ docker pull hylang@sha256:55b7b7b7f444826f4f069dc16550202923ac03aec59bdaaa33cce46adb16ef07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.7 MB (21660216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa8280f5bc18fd480d70db6bde7578cd2e61d4f27e17b26380d520c7a185bf7`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 00:34:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 00:34:47 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 04 Dec 2025 00:34:47 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 04 Dec 2025 00:34:47 GMT
ENV PYTHON_VERSION=3.13.10
# Thu, 04 Dec 2025 00:34:47 GMT
ENV PYTHON_SHA256=bc673c04375a1a3f0808c27ba8f0411ab811ad390a8740318ccb9c60fad8fd77
# Thu, 04 Dec 2025 00:42:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 04 Dec 2025 00:42:08 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 04 Dec 2025 00:42:08 GMT
CMD ["python3"]
# Thu, 04 Dec 2025 19:48:24 GMT
ENV HY_VERSION=1.1.0
# Thu, 04 Dec 2025 19:48:24 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 04 Dec 2025 19:48:24 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 04 Dec 2025 19:48:24 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e6fc46a24e26eae7101a0a6a1f54b3cae9a9ef3523507fa562394067eec225`  
		Last Modified: Thu, 04 Dec 2025 00:37:45 GMT  
		Size: 461.3 KB (461321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89ac6f179cce7dfadd38f52a5ad38ab0e676c970e927a78932290e561ed4b04`  
		Last Modified: Thu, 04 Dec 2025 00:42:20 GMT  
		Size: 12.1 MB (12141806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3214c2baffc14e697f4b38ae620b79b901486f2b684b0a514cc5653f8cf52a6d`  
		Last Modified: Thu, 04 Dec 2025 00:42:19 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee7002296b1a8c405eec45a42b65b7d59a01baa4db2f56bf70a1d35d209fe4f`  
		Last Modified: Thu, 04 Dec 2025 19:48:35 GMT  
		Size: 5.5 MB (5488947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:d06d2d24ef30fc5bb66d209673fba36d8fcb2baa11b1ba6d6fb52d93bb22e5a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a484e3776364d5aa7aec7e631aa8b44eab041692a3b2149494130a443ccb98e`

```dockerfile
```

-	Layers:
	-	`sha256:ea4922b4c330a0b99e62e992481408803cd02aca5a875e8a747a1ebb69bad3df`  
		Last Modified: Thu, 04 Dec 2025 21:19:53 GMT  
		Size: 9.3 KB (9289 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine` - linux; arm variant v7

```console
$ docker pull hylang@sha256:0330aee009c0afb8ad366e8a8a62013e9d00ccfab20bf581e70abb245d7e2633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 MB (21028289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94bdb31e2de1b51fae134b196976147dcbd018627bfe9039f384c47aaeff545b`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 00:35:28 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 00:35:28 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 04 Dec 2025 00:35:28 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 04 Dec 2025 00:35:28 GMT
ENV PYTHON_VERSION=3.13.10
# Thu, 04 Dec 2025 00:35:28 GMT
ENV PYTHON_SHA256=bc673c04375a1a3f0808c27ba8f0411ab811ad390a8740318ccb9c60fad8fd77
# Thu, 04 Dec 2025 00:43:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 04 Dec 2025 00:43:33 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 04 Dec 2025 00:43:33 GMT
CMD ["python3"]
# Thu, 04 Dec 2025 19:45:58 GMT
ENV HY_VERSION=1.1.0
# Thu, 04 Dec 2025 19:45:58 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 04 Dec 2025 19:45:58 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 04 Dec 2025 19:45:58 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c58aea51e3865c747605e89bf6c191f3bab25ddb20fefafc087ecdaf31551bf`  
		Last Modified: Thu, 04 Dec 2025 00:43:47 GMT  
		Size: 460.6 KB (460587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b89a05363be543b5695660831604d8a6a38bb46754c294a7f3e4a4af7fd21e`  
		Last Modified: Thu, 04 Dec 2025 00:43:48 GMT  
		Size: 11.8 MB (11800055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6decd38d6eed5af0144d150e12d5dc3ee1d1f4dac4f8ec855f844a0d5f8f5366`  
		Last Modified: Thu, 04 Dec 2025 00:43:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13db786b6377a55b336f6f2063d77f72688f8c2d821a21f5d4a75495c3f689f`  
		Last Modified: Thu, 04 Dec 2025 19:46:10 GMT  
		Size: 5.5 MB (5488933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:4247ac17eb80507bea9658594d2426cd8e38d14b413449a96c4426467e4b5e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.5 KB (634544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d0cb35353a5fd68b2857715e8927ac9ea0ed26e561a1fb2ed9bad1a35afd45a`

```dockerfile
```

-	Layers:
	-	`sha256:90061265e0d23fb1c1d4494f8737153144df64545c0e938f06fc7b2d2f4b018c`  
		Last Modified: Thu, 04 Dec 2025 21:19:56 GMT  
		Size: 625.0 KB (625040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b970f4544ebd320d270e5564488d71c6a4831a4f461ae732df11e68b35d8fc4b`  
		Last Modified: Thu, 04 Dec 2025 21:19:57 GMT  
		Size: 9.5 KB (9504 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:5f4bc6099fadcd5d277e056833661036743e7c6e2b15fc099f89e188574a0d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22758440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c1cc92ff77fe733ce1c51cad609b9783aa9f44a080dd969311fda509e659d11`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 00:34:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 00:34:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 04 Dec 2025 00:34:00 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 04 Dec 2025 00:34:00 GMT
ENV PYTHON_VERSION=3.13.10
# Thu, 04 Dec 2025 00:34:00 GMT
ENV PYTHON_SHA256=bc673c04375a1a3f0808c27ba8f0411ab811ad390a8740318ccb9c60fad8fd77
# Thu, 04 Dec 2025 00:41:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 04 Dec 2025 00:41:09 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 04 Dec 2025 00:41:09 GMT
CMD ["python3"]
# Thu, 04 Dec 2025 19:51:26 GMT
ENV HY_VERSION=1.1.0
# Thu, 04 Dec 2025 19:51:26 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 04 Dec 2025 19:51:26 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 04 Dec 2025 19:51:26 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80052bb665378e29569939aba30a92ec973822e2da9d0d56e1446a807610005e`  
		Last Modified: Thu, 04 Dec 2025 00:41:20 GMT  
		Size: 462.8 KB (462821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba39df5168011bf2e7eaa3148701e456251bee8acd3c888bc8ffc905b0aff931`  
		Last Modified: Thu, 04 Dec 2025 00:41:22 GMT  
		Size: 12.6 MB (12611162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb67a406069462481a4a5b5b7484a4d6e149babf5b1875e0d2d898771161767`  
		Last Modified: Thu, 04 Dec 2025 00:41:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e887787169e8680a60b3acf384b24fbc40bccd567ea5e2752a1a6764c86d5b`  
		Last Modified: Thu, 04 Dec 2025 19:51:41 GMT  
		Size: 5.5 MB (5489010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:b70a4cabbc223a5d71285a1f466cee8fb4b978d48491e991012f2019aef96e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.6 KB (631630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c82998c0d6d7e3ac53a663d6601eede9678451196bcd44722b34f85c26b0f29`

```dockerfile
```

-	Layers:
	-	`sha256:c7c20b2b239570adc8f9b73c2bcc8244f47bfbe55ce562e9384522cc9cfac8d9`  
		Last Modified: Thu, 04 Dec 2025 21:20:00 GMT  
		Size: 622.1 KB (622086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b31a670c8b15e2e842cfc92dac7bef6d466c42ebf05f15c3f3501ae52e671b43`  
		Last Modified: Thu, 04 Dec 2025 21:20:01 GMT  
		Size: 9.5 KB (9544 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine` - linux; 386

```console
$ docker pull hylang@sha256:68e88895fbe8edf3f249696e51de1833cb7739ef478fa77bd301aad3112e06e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.4 MB (22373093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea75e6e3ac7fb1abaac7c6594912c6d017563981b191be7bb52b0a46610994c`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 00:35:33 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 00:35:33 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 04 Dec 2025 00:35:33 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 04 Dec 2025 00:35:33 GMT
ENV PYTHON_VERSION=3.13.10
# Thu, 04 Dec 2025 00:35:33 GMT
ENV PYTHON_SHA256=bc673c04375a1a3f0808c27ba8f0411ab811ad390a8740318ccb9c60fad8fd77
# Thu, 04 Dec 2025 00:41:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 04 Dec 2025 00:41:13 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 04 Dec 2025 00:41:13 GMT
CMD ["python3"]
# Thu, 04 Dec 2025 19:46:46 GMT
ENV HY_VERSION=1.1.0
# Thu, 04 Dec 2025 19:46:46 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 04 Dec 2025 19:46:46 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 04 Dec 2025 19:46:46 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30ca51673df2bf9c211bb4a134b7660990d179c6065720c8475e9c4aff97a1a`  
		Last Modified: Thu, 04 Dec 2025 00:38:47 GMT  
		Size: 461.1 KB (461120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ccb4c3da1aeab7b5915e910049fc2b78bee58bf1fe5e02fd2ad6f210ea97a8`  
		Last Modified: Thu, 04 Dec 2025 00:41:25 GMT  
		Size: 12.7 MB (12736899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d48cdd60d1611f20515ec768582e9157395fd91617e38e25a89fd038d3fd781`  
		Last Modified: Thu, 04 Dec 2025 00:41:24 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6ccb7b51171a5f1587fdb22d8d388edbaf6c59ae8b891848847159e4ced6d0`  
		Last Modified: Thu, 04 Dec 2025 19:46:58 GMT  
		Size: 5.5 MB (5488969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:8c10fc9be775ab556408c2ac97aa3741feb7de2eb5e2ed924adfb87e8ad206f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.9 KB (631927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8eb25d4ea31d35e3f83d25b48043de28d17e7d6c3fcd584c279e4ad5a86d5f3`

```dockerfile
```

-	Layers:
	-	`sha256:94e666ea139d53f98a683ff97d390dff7c86bfc464288e529dada11f4a17381e`  
		Last Modified: Thu, 04 Dec 2025 21:20:05 GMT  
		Size: 622.6 KB (622587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c613b32e6ee72aa4d1e61a6b3b0a244a47ff005efd1081d2eafe82bff6a17400`  
		Last Modified: Thu, 04 Dec 2025 21:20:05 GMT  
		Size: 9.3 KB (9340 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine` - linux; ppc64le

```console
$ docker pull hylang@sha256:f2c075903dc43c50eb78373d9ac8c6c6125731c714d29f9b132771aba68060d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23083123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b6744677ff0e1630b183d446714730baab517e1053931dc808d3e5599ab50fc`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 00:33:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 00:33:51 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 04 Dec 2025 00:33:51 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 04 Dec 2025 00:33:51 GMT
ENV PYTHON_VERSION=3.13.10
# Thu, 04 Dec 2025 00:33:51 GMT
ENV PYTHON_SHA256=bc673c04375a1a3f0808c27ba8f0411ab811ad390a8740318ccb9c60fad8fd77
# Thu, 04 Dec 2025 00:49:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 04 Dec 2025 00:49:02 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 04 Dec 2025 00:49:02 GMT
CMD ["python3"]
# Thu, 04 Dec 2025 19:57:44 GMT
ENV HY_VERSION=1.1.0
# Thu, 04 Dec 2025 19:57:44 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 04 Dec 2025 19:57:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 04 Dec 2025 19:57:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9eaadc0f25eb346087cdafd7e4d0cc1dc79ec0bbd2a3d9418c2b8760e83ae4`  
		Last Modified: Thu, 04 Dec 2025 00:38:09 GMT  
		Size: 463.4 KB (463358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab1a744b870c39e8567e47d3da06c4b13d5531c2993dffa530e17ee0b7fba19`  
		Last Modified: Thu, 04 Dec 2025 00:49:24 GMT  
		Size: 13.3 MB (13303579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a21c4deb8316e16ec20914e1d20ff3d444c82b7005d261ef9c828513e858e4`  
		Last Modified: Thu, 04 Dec 2025 00:49:23 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5772c9a861d0b14809a1422d3be5ab27ee71ce9aa914c77a0d08e3dbd57cf6`  
		Last Modified: Thu, 04 Dec 2025 19:58:03 GMT  
		Size: 5.5 MB (5488921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:fde6a34ce80b5c33f47e9696b2508eebf7bb1d1153da53c8db08dfb1eb6ebf47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.5 KB (631499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5753e5ec4f1b09a35e8762a7f10082e6cd226ea6f6f5ed9e0e2a368122b4ef8`

```dockerfile
```

-	Layers:
	-	`sha256:c93f71cba539535567b509e1dbce5215018d53cc18d4186452abbbdcc35e0d39`  
		Last Modified: Thu, 04 Dec 2025 21:20:09 GMT  
		Size: 622.0 KB (622039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b432994be73d50a7356c5d2cde7d82003e078b21a27d50bae626a0ff630ee3b`  
		Last Modified: Thu, 04 Dec 2025 21:20:10 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine` - linux; riscv64

```console
$ docker pull hylang@sha256:c8ae105e475ee7116698cfa034e7755ef0f1d7ba3fda6a999bb65d91f5c51bbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (21966731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b26df1dc09ab496f2a954ae25c4cc61e93192a845a14129fc3c07319d6ca37`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Fri, 21 Nov 2025 02:32:45 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 21 Nov 2025 02:32:45 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 21 Nov 2025 02:32:45 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 21 Nov 2025 02:32:45 GMT
ENV PYTHON_VERSION=3.13.10
# Fri, 21 Nov 2025 02:32:45 GMT
ENV PYTHON_SHA256=bc673c04375a1a3f0808c27ba8f0411ab811ad390a8740318ccb9c60fad8fd77
# Wed, 03 Dec 2025 10:05:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 03 Dec 2025 10:05:31 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 03 Dec 2025 10:05:31 GMT
CMD ["python3"]
# Wed, 03 Dec 2025 11:02:25 GMT
ENV HY_VERSION=1.1.0
# Wed, 03 Dec 2025 11:02:25 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 03 Dec 2025 11:02:25 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 03 Dec 2025 11:02:25 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2877bb53774363add4a89387f6600996a5058bff9f65b88b5e8eee6ca3040264`  
		Last Modified: Fri, 21 Nov 2025 03:10:03 GMT  
		Size: 457.3 KB (457273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3724ea06b83935cc6a7bb6faff314c233a4b173e76fe740e20e3bc63e0ad5e2c`  
		Last Modified: Wed, 03 Dec 2025 10:06:25 GMT  
		Size: 12.5 MB (12504632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242f865cf72bcd430c2c0775c70cb7f9fae65f3de5a5c8d95e3515d970ebecaf`  
		Last Modified: Wed, 03 Dec 2025 10:06:24 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d219d173ea2d2a6f5ae1a84f03db45c45116524d8e79b45e75b7303a8f786b`  
		Last Modified: Wed, 03 Dec 2025 11:03:09 GMT  
		Size: 5.5 MB (5489335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:75d7b103a8220ab207c24b1b2b7f1fa04cff234d9c3244e5853c38e9db7daecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **630.2 KB (630200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd052f9ce7ba10b482cd8500e8708634ab1dc23bfbc0b095ea8ad57be3fa2c7`

```dockerfile
```

-	Layers:
	-	`sha256:e88fd553eb4dcd7d8928418cd20da2263335d8338db209567429e109b89bd8dd`  
		Last Modified: Wed, 03 Dec 2025 12:18:30 GMT  
		Size: 620.7 KB (620740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8951c9bb0e3c9b48b7903461dc63e92cd827d50e6d92184d9d5f15804ef89ac8`  
		Last Modified: Wed, 03 Dec 2025 12:18:30 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-alpine` - linux; s390x

```console
$ docker pull hylang@sha256:0df83e799bbd925644b179261a8b67cf097b0acce893bea5c49bc462e3ba413b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22628786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46453030e4c471a92c6e99735cd349a17d01351ebbdf8f19cc8f1af961587679`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Thu, 04 Dec 2025 00:33:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Dec 2025 00:33:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 04 Dec 2025 00:33:19 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 04 Dec 2025 00:33:19 GMT
ENV PYTHON_VERSION=3.13.10
# Thu, 04 Dec 2025 00:33:19 GMT
ENV PYTHON_SHA256=bc673c04375a1a3f0808c27ba8f0411ab811ad390a8740318ccb9c60fad8fd77
# Thu, 04 Dec 2025 00:46:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 04 Dec 2025 00:46:52 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 04 Dec 2025 00:46:52 GMT
CMD ["python3"]
# Thu, 04 Dec 2025 19:50:11 GMT
ENV HY_VERSION=1.1.0
# Thu, 04 Dec 2025 19:50:11 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 04 Dec 2025 19:50:11 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 04 Dec 2025 19:50:11 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73faa9e7c3ab49738e4f049e32f81d5ebda39091b059dcebbaceb398518e722`  
		Last Modified: Thu, 04 Dec 2025 00:40:06 GMT  
		Size: 461.6 KB (461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e00135cc188bbc5c4a27e730a0d35ff8d80bb787062d70bbef99216af6c36e`  
		Last Modified: Thu, 04 Dec 2025 00:47:14 GMT  
		Size: 13.0 MB (12953975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad023393a0d02f282c308aeef4f9debde47bf8c04e29b14b31cfda34f2764e44`  
		Last Modified: Thu, 04 Dec 2025 00:47:10 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eca3866e927fdbe78aa36653114200283c97e3820cf4e719b8ed5ce8b1b121c`  
		Last Modified: Thu, 04 Dec 2025 19:50:33 GMT  
		Size: 5.5 MB (5489143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:cd84529215308303ee00d6efce01a90f0eab330766660e2ca428c624e68a9fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.4 KB (631373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7fe66f4542d34fac7d571b264033e54c6d740379999ff09fb139df3af37dd6f`

```dockerfile
```

-	Layers:
	-	`sha256:3de902def94b6df842072fc2cbb7d8783edbfef340e74f6192f9587199a646dc`  
		Last Modified: Thu, 04 Dec 2025 21:20:13 GMT  
		Size: 622.0 KB (621981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:327081700b50446377ba9db957e1d8d8d4dc718b46b89358987cc07f0078da78`  
		Last Modified: Thu, 04 Dec 2025 21:20:14 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.in-toto+json
