## `python:alpine`

```console
$ docker pull python@sha256:b6f01a01e34091438a29b6dda4664199e34731fb2581ebb6fe255a2ebf441099
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

### `python:alpine` - linux; amd64

```console
$ docker pull python@sha256:59b935dc28398059a4f8ec346bdbb90917085bfe14c5c673ea5c47fddfeb4110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16591351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5bfb768070b1903a3e7e2900f9183d0065d820fa3dcfbe3c0dfb6654ebc90a`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 05 Dec 2024 13:19:52 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.13.1
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a862d332164437997f94a48a55e4a936dceeefdfe0fd05c46d2c9870a74c07a`  
		Last Modified: Tue, 14 Jan 2025 20:33:20 GMT  
		Size: 458.8 KB (458751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b112603475e1131289cfe42ace4443b4e764c7b69a7f792d2529cb349fa6c407`  
		Last Modified: Wed, 08 Jan 2025 18:23:20 GMT  
		Size: 12.5 MB (12490637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cdd0abfb159ba8501bec56423ea963db34458b8736d28607431219013b2a17`  
		Last Modified: Wed, 08 Jan 2025 18:23:20 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine` - unknown; unknown

```console
$ docker pull python@sha256:cd104ae95bdcf18019308c1f75a568f42fb413fec5e74017550d6c1ce0e5825e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.0 KB (643004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff5b9c47980b0e2c0ee0472031aba5cc25647ebc7cc336971b5f9046ee239c4`

```dockerfile
```

-	Layers:
	-	`sha256:b724e52df117e527308f1e7f63ccce44c0bf2227107bfd5782ad62e6bb6794c1`  
		Last Modified: Wed, 08 Jan 2025 18:23:20 GMT  
		Size: 621.3 KB (621289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:992897d869459e903a162e96f05c943b9576323f8fec53a423bf1cd363bb47b7`  
		Last Modified: Wed, 08 Jan 2025 18:23:20 GMT  
		Size: 21.7 KB (21715 bytes)  
		MIME: application/vnd.in-toto+json

### `python:alpine` - linux; arm variant v6

```console
$ docker pull python@sha256:ce963fd5c7a2f0ae758f96b127a80ab148924acc4314034b28a20006b7020cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15902231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fcc9376c9e38d1280068fa227e958f54d97dcb8034802b8435a41b04074e084`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 05 Dec 2024 13:19:52 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.13.1
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2dec769123af1f5a0c91c72bfe4e9f0159b1fda485ecb156007cf295004a14`  
		Last Modified: Thu, 09 Jan 2025 07:15:26 GMT  
		Size: 459.6 KB (459577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f5bf6c509711888714b44725ddb8314a7cd0c8616f44120cba68ab338a871d`  
		Last Modified: Thu, 09 Jan 2025 07:33:09 GMT  
		Size: 12.1 MB (12078525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85029bcce07b09c3bca5100f3b3479f04aec178cc28f3eeeed5cbae50553fa18`  
		Last Modified: Tue, 14 Jan 2025 22:15:41 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine` - unknown; unknown

```console
$ docker pull python@sha256:309221a94d2760ab13387c72e86b093969cdd70190aef98cdeb297974f6b8f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 KB (21636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e3f791d0bd48353de720853251adb3e793f73634c6b3b4ad16daafe4b26bf82`

```dockerfile
```

-	Layers:
	-	`sha256:0caeccad5ea26195ccc5a43a40397e1d3b10e67f7e1f2695f7a73fbabbf33689`  
		Last Modified: Thu, 09 Jan 2025 07:33:08 GMT  
		Size: 21.6 KB (21636 bytes)  
		MIME: application/vnd.in-toto+json

### `python:alpine` - linux; arm variant v7

```console
$ docker pull python@sha256:997d88c0c9f1e2b96de30263b9bc1744dedc18840775dfb7a01e63a3184cf14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15301306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b6d6aeb5ebf4263f1697cc67047fe33301823e3e1e1cd465d39ec644c8d035c`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 05 Dec 2024 13:19:52 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.13.1
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52fed4f44c67cbc108822cb67f010dfbf3a64ce27abbeff6c7c380b97b0a0f4`  
		Last Modified: Thu, 09 Jan 2025 07:50:42 GMT  
		Size: 458.7 KB (458718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b984a709735022d801995ac68ec89637537057a51258b42378ec488745c7929d`  
		Last Modified: Thu, 09 Jan 2025 08:05:32 GMT  
		Size: 11.7 MB (11745227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c170c2be395a93e07d23b21d9e135b4c56370dc1d81ccf1d79ae8dfb9a4cb0`  
		Last Modified: Thu, 09 Jan 2025 08:05:32 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine` - unknown; unknown

```console
$ docker pull python@sha256:d400062aaad2ff91241cccf48979709ffc86fbd242c34e91330b9a5ee9815b9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **646.0 KB (646020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6d95d91de8020f25da63efd214bf42866855347d1a7e77ee230ad71fa96812`

```dockerfile
```

-	Layers:
	-	`sha256:824c182822287731c93f9282ef9b3ae7b9dac10c0c6cc0593bc765fbc0b1fe94`  
		Last Modified: Thu, 09 Jan 2025 08:05:32 GMT  
		Size: 624.2 KB (624170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2796a1dbafaffa21341fc5d431be5b95d15141e135b072a93e46152e75dcbccf`  
		Last Modified: Thu, 09 Jan 2025 08:05:32 GMT  
		Size: 21.9 KB (21850 bytes)  
		MIME: application/vnd.in-toto+json

### `python:alpine` - linux; arm64 variant v8

```console
$ docker pull python@sha256:00338399af162ef8df922427c3765c712e2615d6c0de59611df9c9c4b35693b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16949225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac9eec4db20fe3e3daa4435a1885a1e2e68dd51b3e1f1d0ab7a7618aab0b60af`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 05 Dec 2024 13:19:52 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.13.1
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844e1cf46642efec467c0d66e3ca2031dea03979799a64785bcb140b5fce2a70`  
		Last Modified: Tue, 14 Jan 2025 20:33:34 GMT  
		Size: 460.8 KB (460837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5563124400db93cc61de171e1ac0800d2dd387ae27f4e45637f3301a0574e4b1`  
		Last Modified: Thu, 09 Jan 2025 04:28:03 GMT  
		Size: 12.5 MB (12495780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c59c3262a39259d7d7ae734d4a34e21326821f8e19ec3968bb2ba655fd1a8015`  
		Last Modified: Thu, 09 Jan 2025 04:28:02 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine` - unknown; unknown

```console
$ docker pull python@sha256:3c6a691b9b98f27ee9495184aa76f649f121aee7beba1bb0b483752b7bb444aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **643.3 KB (643292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11e71f448ce0fc7bae47f0105f976330d704fe1772521827984af50900e4e3e5`

```dockerfile
```

-	Layers:
	-	`sha256:de748218dcaf71d2648e12cbb6d88c310465a07d871d283084bc955529188d30`  
		Last Modified: Thu, 09 Jan 2025 04:28:03 GMT  
		Size: 621.4 KB (621393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baa8496c79d1a36abb4b21ca4572cff5a7f84e8bc62a48c905436237b31e8257`  
		Last Modified: Thu, 09 Jan 2025 04:28:02 GMT  
		Size: 21.9 KB (21899 bytes)  
		MIME: application/vnd.in-toto+json

### `python:alpine` - linux; 386

```console
$ docker pull python@sha256:56888c6db1942b8f52afe0fc729dd750fe98dc90b6a0be50d2cb42ac6ed3f568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.7 MB (16659725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed5910e630486141b2e5f73def0d8b651f41c47e821c16adadb3892c80fe3fad`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 05 Dec 2024 13:19:52 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.13.1
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59acc65d8d3b609c5ff8caeec1f3b39e90b6ef14b55b4d174da8bcef3eec5cb8`  
		Last Modified: Tue, 14 Jan 2025 22:15:39 GMT  
		Size: 459.2 KB (459187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e644070b127f8893e9865b703660b6fe363203ab039ef6127ff32c9e446ed20`  
		Last Modified: Wed, 08 Jan 2025 18:19:34 GMT  
		Size: 12.7 MB (12737164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c30b9c6c7df112c0cf687dac15a643ffe50649c5294062ecb9729cbac06c67b`  
		Last Modified: Wed, 08 Jan 2025 18:19:33 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine` - unknown; unknown

```console
$ docker pull python@sha256:5903be024060c852d6f8603c343708910de6d10805494201c931d5015b31f588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **642.9 KB (642905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fdbb8061b2b84ec87cb5c669247c50bf51c4762ea15fa876811a00890dc6a7`

```dockerfile
```

-	Layers:
	-	`sha256:ffd6e1eac001730c26570bed6d4a21610adcc991af71a98303105442904fa252`  
		Last Modified: Wed, 08 Jan 2025 18:19:33 GMT  
		Size: 621.2 KB (621244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c99cdd32dc43d0251f492ce60755680968e7bc26ed05f9c08e6e44e77520561f`  
		Last Modified: Wed, 08 Jan 2025 18:19:33 GMT  
		Size: 21.7 KB (21661 bytes)  
		MIME: application/vnd.in-toto+json

### `python:alpine` - linux; ppc64le

```console
$ docker pull python@sha256:0aa8113fc3dcbf6da3dc8bae4342ff8cfea37faed50ca2b39a02d60e5659e059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17194072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5daa75ecc5a073a20eb76cd779d6e97fd471d6fade147f0ed6c2fa546dc31ef7`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 05 Dec 2024 13:19:52 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.13.1
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78682beede19196d68ea8312fad482211dddc22810f3e520b446a72a6396fc56`  
		Last Modified: Wed, 08 Jan 2025 23:06:50 GMT  
		Size: 461.3 KB (461293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61127848696fe1469fc229d4a8d9539ec5f12604118349c58cb6369079b3ce85`  
		Last Modified: Wed, 08 Jan 2025 23:23:34 GMT  
		Size: 13.2 MB (13158928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d63bf5f02ed4160f84a317b8c72d34a9a3c1d45b3a7eac06f69fddd2fead07`  
		Last Modified: Wed, 08 Jan 2025 23:23:33 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine` - unknown; unknown

```console
$ docker pull python@sha256:8005245a7dd2711b17dc80cbc1926d921e06c8edfb4d1fe3dd1123d5aa5c9399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.2 KB (641184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3792eeca9e363fe053a237e42c91761d10316a93e6c37b3ea7f9adf369a42248`

```dockerfile
```

-	Layers:
	-	`sha256:d17afbae05bacf4ca22b2cdcc1cc94aeee7b53f4a87f55f32b74529cdd6b2977`  
		Last Modified: Wed, 08 Jan 2025 23:23:33 GMT  
		Size: 619.4 KB (619396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51195a3fa2981f81d4ad3c2835ead5ec030525a25f8f4e1856a5088b322e7487`  
		Last Modified: Wed, 08 Jan 2025 23:23:33 GMT  
		Size: 21.8 KB (21788 bytes)  
		MIME: application/vnd.in-toto+json

### `python:alpine` - linux; s390x

```console
$ docker pull python@sha256:af4ebee4ec79ff0505522945a7a811197a7b63a2bd99dc388af1c239afb14b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16828472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf48835a0700b536b9a0693abdaa3a79877f2e71db8689968d6256fb61996c9`
-	Default Command: `["python3"]`

```dockerfile
# Thu, 05 Dec 2024 13:19:52 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["/bin/sh"]
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_VERSION=3.13.1
# Thu, 05 Dec 2024 13:19:52 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 05 Dec 2024 13:19:52 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ba53597a2004ea77723ad280fa3859e5c80d6ba286dd12179ceb5e3e7dc776`  
		Last Modified: Thu, 09 Jan 2025 05:24:30 GMT  
		Size: 459.7 KB (459691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61281a81b7ccd9118b5444aa7d5106c17f2f79abd7a99a0c75e1b77544d2e211`  
		Last Modified: Thu, 09 Jan 2025 05:39:18 GMT  
		Size: 12.9 MB (12901664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4be1fb9cb7b302c9d75dbfacbbfce53ec1a585f4cfffea4db5a45b824583d8`  
		Last Modified: Thu, 09 Jan 2025 05:39:17 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:alpine` - unknown; unknown

```console
$ docker pull python@sha256:392d9190401b51e4b03b2353036e88ea6212c37d0e2072bef9ad160a65107b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.1 KB (641055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e4b50a7bf364e76267c79ee42e90599cdd010c766196e240b636208c0d9dc8`

```dockerfile
```

-	Layers:
	-	`sha256:60a89e9eef2d52c5a69c187a59c86c70ad7e375b5314a4567a975f2337f5e6b7`  
		Last Modified: Thu, 09 Jan 2025 05:39:17 GMT  
		Size: 619.3 KB (619338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c572026c98a8a33710c927f4b3e3158319f7d1c989e0a0f5f8af9ac05272074`  
		Last Modified: Thu, 09 Jan 2025 05:39:17 GMT  
		Size: 21.7 KB (21717 bytes)  
		MIME: application/vnd.in-toto+json
