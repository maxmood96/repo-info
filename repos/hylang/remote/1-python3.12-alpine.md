## `hylang:1-python3.12-alpine`

```console
$ docker pull hylang@sha256:4b8fd733e771372d92492d49fa065fe2d1fd8ffe4dd2deb9afdd9d89cd7b043f
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

### `hylang:1-python3.12-alpine` - linux; amd64

```console
$ docker pull hylang@sha256:bb26f818173c00dc668a4b87299ddc47bc6e71638f379d47536cad383487883c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23383184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000218a676c4c7f874ca6d063e18b8416faca18538d5154d5c36bfd22f593538`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Feb 2025 21:54:55 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 21:54:55 GMT
ENV LANG=C.UTF-8
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PYTHON_VERSION=3.12.9
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PYTHON_SHA256=7220835d9f90b37c006e9842a8dff4580aaca4318674f947302b8d28f3f81112
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25025a4218eefbda6e3d8944ce25bc217c4ca500ac1457767ef02591c72880f8`  
		Last Modified: Fri, 14 Feb 2025 19:20:13 GMT  
		Size: 458.6 KB (458634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1403b23815912718a1f8e88a3a9058af90f1a899cfbc284dbc1412d5024737f`  
		Last Modified: Fri, 14 Feb 2025 19:20:13 GMT  
		Size: 13.7 MB (13650350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b6003920d887e032cde091a300b7a17810c41ff50841434ba5f5261fe95d66`  
		Last Modified: Fri, 14 Feb 2025 19:20:12 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abc37bff6edf6e12e23d2e0fdb9b8373e73de86f10f46afdca75711ebe7fc26`  
		Last Modified: Wed, 19 Mar 2025 22:58:42 GMT  
		Size: 5.6 MB (5631706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:1a3ccb8a38ed37b982b0691eb2ec01e97d44c1f1f1a1406e3eb9cc62471d6fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.0 KB (669022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:390002555d98fde411cd04bf02bd806fe11da2f0ce804d502dd8d82a47c7e29e`

```dockerfile
```

-	Layers:
	-	`sha256:183d8f1318928de541166c6494d36a2045d41837634b13fa542cb23a0b99d789`  
		Last Modified: Wed, 19 Mar 2025 22:58:42 GMT  
		Size: 659.7 KB (659683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eb38182280b10bc17a23ddc7e4cb266f34307a14926c35b130ae75dd36ff1d4`  
		Last Modified: Wed, 19 Mar 2025 22:58:42 GMT  
		Size: 9.3 KB (9339 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-alpine` - linux; arm variant v6

```console
$ docker pull hylang@sha256:98cbf60a7415688b4ea5958b09dc98a125f3b15574a97f95d427894bef907d4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22645810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64db0378ab39e4735af91041120d7b3f4ca74344d54e227a8ccf7873b1771f05`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Feb 2025 21:54:55 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 21:54:55 GMT
ENV LANG=C.UTF-8
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PYTHON_VERSION=3.12.9
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PYTHON_SHA256=7220835d9f90b37c006e9842a8dff4580aaca4318674f947302b8d28f3f81112
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22a5fbd377f634bd200cb3834402a3cfe9d57ac6cb9dd5cf9fe3147bb665960d`  
		Last Modified: Sat, 15 Feb 2025 08:26:27 GMT  
		Size: 459.4 KB (459436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880119c83d7cf5dc34380d944ef5bc41d9cdbc60835d6d5b0b18c202ecdbafb3`  
		Last Modified: Sat, 15 Feb 2025 08:26:27 GMT  
		Size: 13.2 MB (13189297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb97939a636bbff05c202497c3ef5f883d92a622342ae0f4809cf87b42cdb11b`  
		Last Modified: Sat, 15 Feb 2025 08:26:26 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e197ee761f957587d9fb452657fe2c4dc2f3a4c66ae33edc3b1a881601fe5e28`  
		Last Modified: Wed, 19 Mar 2025 22:59:26 GMT  
		Size: 5.6 MB (5632097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:616e2421bf59ac38d4c3dfeba878cc18e13de032a619d444896c302ec2f45e50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb8d3128c9d4ef54f178177104d44be98017d23f5a65afce1210e55e94d2794f`

```dockerfile
```

-	Layers:
	-	`sha256:8a573b6bbeceda6791c46d1f8ec87feff97fc6d547e2a39d8dec7e600f3dc71c`  
		Last Modified: Wed, 19 Mar 2025 22:59:26 GMT  
		Size: 9.2 KB (9234 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-alpine` - linux; arm variant v7

```console
$ docker pull hylang@sha256:d1ba51876b54885e24e187e09f45b3e2aa472b04d1a03e547bcb81de3db56255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (21989109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f30df6c04e2b493d6d9ac9311eed5c301f31e1cf73067c97b9894a9d5b717989`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Feb 2025 21:54:55 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 21:54:55 GMT
ENV LANG=C.UTF-8
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PYTHON_VERSION=3.12.9
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PYTHON_SHA256=7220835d9f90b37c006e9842a8dff4580aaca4318674f947302b8d28f3f81112
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be29710354556f0f0df673704b6b540828d1087963ffd820135dfcb597033328`  
		Last Modified: Sat, 15 Feb 2025 08:21:33 GMT  
		Size: 458.6 KB (458622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7765fccc1f3c9347762a398c1b2bde043c146bbd6f400bf846ab79e59eb3ac`  
		Last Modified: Sat, 15 Feb 2025 08:21:34 GMT  
		Size: 12.8 MB (12800083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea640fa40681b94ef98c64b3c35c5cd6507e4eeb1b38afa91e5969bced50c69`  
		Last Modified: Sat, 15 Feb 2025 08:21:33 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29d2021b3053ccd0d3746182e5f1f67312167503527c6669ef2dab6df308949`  
		Last Modified: Wed, 19 Mar 2025 23:31:20 GMT  
		Size: 5.6 MB (5632032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:3ce83a6586f840fa06c1fb32bd25c6b377e471ff998f5e0fd2625282ca2927d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.0 KB (672013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c87ad610f9b3792a1d6302a876a5846e000e99401fdbac20c7e11ce819e1ca9`

```dockerfile
```

-	Layers:
	-	`sha256:3c1489c3472a890e0add8adf481edc6081333c37fda116f439dedce230b4eed0`  
		Last Modified: Wed, 19 Mar 2025 23:31:20 GMT  
		Size: 662.6 KB (662564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1df1e3ab44cf5eb20ed43f50cfb79d09188cbfe7d51ee5836868bc06d06401d1`  
		Last Modified: Wed, 19 Mar 2025 23:31:20 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-alpine` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:b64821d7b3c67f559b2e340643c05579d548b88293065dfe15ca8ddc68a204c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.8 MB (23783127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc14bd9760048beb4d6009f83cd540b662e472d6c9a78cdcb757a5a55aa6670`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Feb 2025 21:54:55 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 21:54:55 GMT
ENV LANG=C.UTF-8
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PYTHON_VERSION=3.12.9
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PYTHON_SHA256=7220835d9f90b37c006e9842a8dff4580aaca4318674f947302b8d28f3f81112
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60a29b5b2911d5b8ee9dcdb5f3a38f98e46d2b43ff40db6f826f5497a01cab4`  
		Last Modified: Sat, 15 Feb 2025 05:29:59 GMT  
		Size: 460.7 KB (460730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9f743c4b2d27fb5cf8ff2cbd18a1e506e86a4b444e1a28e42b5fb63964c87f`  
		Last Modified: Sat, 15 Feb 2025 05:30:00 GMT  
		Size: 13.7 MB (13697200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89322d3ac64bf8a79585df322d2034d9f6dff9108bf3134f1430ae711700f749`  
		Last Modified: Sat, 15 Feb 2025 05:29:59 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147f18320028856c051f6db20739aa2004d48ed028c1d0e38cdeb56979b2d9aa`  
		Last Modified: Wed, 19 Mar 2025 23:18:08 GMT  
		Size: 5.6 MB (5631921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:99b10b82548ba4ca0575c98d58da1385ed967b53f6aec8af033dd1d57963d052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.3 KB (669280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec8e733ec37cc68dfc19d26fca5cfb1f1ceacc0922ec6b7bf0d4406de2208562`

```dockerfile
```

-	Layers:
	-	`sha256:9dc1c7b062eeaba79a97a7fc8b2308e670ded44faa09d2a4f20296af51dbf795`  
		Last Modified: Wed, 19 Mar 2025 23:18:07 GMT  
		Size: 659.8 KB (659787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df7259426eabac07965500dec7e8bbc60a49cb1119149e52f15626119f669aa4`  
		Last Modified: Wed, 19 Mar 2025 23:18:07 GMT  
		Size: 9.5 KB (9493 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-alpine` - linux; 386

```console
$ docker pull hylang@sha256:ac95099c1ff632c01e6a81fae35c749ce8a264bcc812aa7db43c1a3e14b636a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23431565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ebeccfd4acc097f788c7b2a546e19143900b1c2ddc56d4bfe4f73167848796a`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Feb 2025 21:54:55 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 21:54:55 GMT
ENV LANG=C.UTF-8
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PYTHON_VERSION=3.12.9
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PYTHON_SHA256=7220835d9f90b37c006e9842a8dff4580aaca4318674f947302b8d28f3f81112
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2647d1f2403ef1caaaec6affe1a5ce6e7b3d40f6833ae9a578e1e2ef8eb219`  
		Last Modified: Fri, 14 Feb 2025 19:31:48 GMT  
		Size: 459.1 KB (459061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f0087715cee5db625b8d1322bb097c860b82f79519c2949366d11f9e5cddc4`  
		Last Modified: Fri, 14 Feb 2025 19:31:48 GMT  
		Size: 13.9 MB (13876618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc1c541b0a8692a714b4516eb6755388e885a7094c6b0bff039bbd7271fd790`  
		Last Modified: Fri, 14 Feb 2025 19:31:48 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b097da9f767b46173e7993f3a897c3fb3dabdd0c48acab8e96861c33ff5070`  
		Last Modified: Wed, 19 Mar 2025 22:59:00 GMT  
		Size: 5.6 MB (5632015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:5c1d5ed90c8f58c08bf09cbd5125c2939901d7bcbaf9c18027f1481d52d10120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.9 KB (668927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dafbea185291a8e80b4be7bc67ed1bee3bfd5d3695c7df5bbf0bb7b97b1ece3`

```dockerfile
```

-	Layers:
	-	`sha256:aef94d050706929b64a9d0ab16b84318154ddc366c066a049d71dc752bad2171`  
		Last Modified: Wed, 19 Mar 2025 22:59:00 GMT  
		Size: 659.6 KB (659638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f06779e6cdd553c3a707d48ef0f58b598f07ef0712a82b141dc0b5d95376013`  
		Last Modified: Wed, 19 Mar 2025 22:59:00 GMT  
		Size: 9.3 KB (9289 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-alpine` - linux; ppc64le

```console
$ docker pull hylang@sha256:4af4afc147c5457640bdaf040a0b349c5589519d740c6ce97c9f768870a1c24f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24089145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e54239fc3debcc8a588bd3a27513f718dd9665bed39ade6f7c9ed16bf07c52`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Feb 2025 21:54:55 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 21:54:55 GMT
ENV LANG=C.UTF-8
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PYTHON_VERSION=3.12.9
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PYTHON_SHA256=7220835d9f90b37c006e9842a8dff4580aaca4318674f947302b8d28f3f81112
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde1b426b09d99aed3ee9095c2aa945af40570fa93947d87e310bf08c98a9391`  
		Last Modified: Fri, 14 Feb 2025 23:55:46 GMT  
		Size: 461.2 KB (461167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad2434aa2215acf20413eef2588ce0abb20ed432641f2d7b305c525a2b9a7a5`  
		Last Modified: Fri, 14 Feb 2025 23:55:46 GMT  
		Size: 14.4 MB (14421603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afa6f1d7402638a78eb487ac738ee753dc92dc28f7a743c2d242c31c5ec174b`  
		Last Modified: Fri, 14 Feb 2025 23:55:45 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71664eba79325711abdeb08a7033e7adcf184e35a15c19504bb340c46efee102`  
		Last Modified: Wed, 19 Mar 2025 23:24:47 GMT  
		Size: 5.6 MB (5631782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:b1bc4df5701b72e7b5aa2b90ca04ffdb03fe78e44f7dc47016ef0cd30cbe50b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.2 KB (667199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b76440291c63a6e7a94d540c28e08763c8f6794b3d3a760d52c9edb3d64f43`

```dockerfile
```

-	Layers:
	-	`sha256:5a015acfec833f6b8024eff3c6516da809aa329997b7c8753f0454d9072fbc52`  
		Last Modified: Wed, 19 Mar 2025 23:24:47 GMT  
		Size: 657.8 KB (657790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82da492cabb891795044b1cc602f54364e2a5dc55772a9547e5536e63f8bfa0f`  
		Last Modified: Wed, 19 Mar 2025 23:24:47 GMT  
		Size: 9.4 KB (9409 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.12-alpine` - linux; s390x

```console
$ docker pull hylang@sha256:39c1f574bb96891b632a1f5423bef022efb5529fd50f8de831c5d2b2f7a3d2ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23739684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b38715aa017144d4806edfc333ec1d14354e07aaef1507802d32a22b6f2531d`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Feb 2025 21:54:55 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
CMD ["/bin/sh"]
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Feb 2025 21:54:55 GMT
ENV LANG=C.UTF-8
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PYTHON_VERSION=3.12.9
# Tue, 04 Feb 2025 21:54:55 GMT
ENV PYTHON_SHA256=7220835d9f90b37c006e9842a8dff4580aaca4318674f947302b8d28f3f81112
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Feb 2025 21:54:55 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b235a0851abb555863d26c3d5c5de5319d2090f8e05fe647e5d2a1b7441a02f8`  
		Last Modified: Sat, 15 Feb 2025 06:21:00 GMT  
		Size: 459.6 KB (459578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1286334792f43896e3125a48c73fdd5e7b88308b0e64560ec95f8d8d62513a22`  
		Last Modified: Sat, 15 Feb 2025 06:21:01 GMT  
		Size: 14.2 MB (14180504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f1d897c1f37a7f4c9a8bf8da1c90e8b30067ef1fd83895bfa2cc296f649d45f`  
		Last Modified: Sat, 15 Feb 2025 06:21:00 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbcc31e0646a5171f516ee8b5af6571f401135748718b9fb1113cf2ae41f18b8`  
		Last Modified: Wed, 19 Mar 2025 23:47:55 GMT  
		Size: 5.6 MB (5631784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.12-alpine` - unknown; unknown

```console
$ docker pull hylang@sha256:44de3a4002c2be730a32a41e56e319493dbf1ef0d9f60d52e29e76370e40eadf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **667.1 KB (667073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0498460d12f6cf031e0cd07ffb284b574b277aeab53f31654f1c0cbaeabbcb4`

```dockerfile
```

-	Layers:
	-	`sha256:05fc5df712d9e94d1e7037228262aa59df568f2006f44a35a556324738b9c224`  
		Last Modified: Wed, 19 Mar 2025 23:47:54 GMT  
		Size: 657.7 KB (657732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41ad2885b5c79be84c503bd1931aa1be74f5aff38b6436885629756391f28965`  
		Last Modified: Wed, 19 Mar 2025 23:47:54 GMT  
		Size: 9.3 KB (9341 bytes)  
		MIME: application/vnd.in-toto+json
