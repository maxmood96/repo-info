## `hylang:1-python3.11-alpine3.20`

```console
$ docker pull hylang@sha256:350c85e18d35d06d4091f745df320b78c48bd7c9f211cad41318f6a77f74fbd0
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

### `hylang:1-python3.11-alpine3.20` - linux; amd64

```console
$ docker pull hylang@sha256:74b5bbfd96790a485585e4e8c529d5b2880782a1a8840a06134c166521782a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26387166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77c06ac9bfc2f22d6819702897181d43e2ecb664184b730cad3b5ef9a827db47`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 03 Dec 2024 22:49:59 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c398173f5dabd4c56171b50e28d587a1ac6fafd81f4932cd4bba1bf049f1ef97`  
		Last Modified: Tue, 07 Jan 2025 03:22:31 GMT  
		Size: 443.9 KB (443909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d48094c8f1e9b9b1d507b6c03697347b645ea788d316781d44552dfd57df66`  
		Last Modified: Tue, 07 Jan 2025 03:22:31 GMT  
		Size: 16.1 MB (16111000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593cde2a0bfd6b5d2ca2c8ef388d82d8716adc67106ef2b4fe2814bfa5d401c1`  
		Last Modified: Tue, 07 Jan 2025 03:22:31 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9a21dd2503de9541fcbe062d2f5a9142324a4a005a9139d86f0676f12b16e7`  
		Last Modified: Tue, 07 Jan 2025 04:23:42 GMT  
		Size: 6.2 MB (6218010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:f643552bafaa4eb170df6759f71324a53d6f0d2fd41986adf223b7a77a9471d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **660.4 KB (660377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb5e5771cd52ba839c916842dbbbc33afc6103e05abccb5162258a815a7b1018`

```dockerfile
```

-	Layers:
	-	`sha256:90ed8ca4b00cc8e842aa9dc3f60a3a8c2104bda398734b9dfaa88e610e75d5af`  
		Last Modified: Tue, 07 Jan 2025 04:23:41 GMT  
		Size: 652.3 KB (652339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3667c407cb6425f7f64f44dc2d6f759df2737c2e85c066f6e941b92bfe0ca12`  
		Last Modified: Tue, 07 Jan 2025 04:23:40 GMT  
		Size: 8.0 KB (8038 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.20` - linux; arm variant v6

```console
$ docker pull hylang@sha256:a475e9aa1132f04143fec2d71a1971652541cf19fbcd025062ce3bf78598e393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25728914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:135f2ef813f23c5158046dee8b06ea33ea366da361261bd175559a077324ec7f`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 03 Dec 2024 22:49:59 GMT
ADD alpine-minirootfs-3.20.4-armhf.tar.gz / # buildkit
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
	-	`sha256:9327c400cc7c63bc8696a8da86f21db1ffdb7ce43885aa521a67ab8105dd2af9`  
		Last Modified: Tue, 07 Jan 2025 02:29:49 GMT  
		Size: 3.4 MB (3363944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a987a8d3b34b4101f1f618e5340eb174b6871d02a5c70353eb79a667003bc8a3`  
		Last Modified: Tue, 07 Jan 2025 17:10:13 GMT  
		Size: 444.8 KB (444782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60cbc5105eac8adb92ee6661b4263d76010f1ee7a8debcde514b75e64aca007c`  
		Last Modified: Tue, 07 Jan 2025 17:24:55 GMT  
		Size: 15.7 MB (15701848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381b2f59065a8d566188748250ccbd5b62d4a5a78b0092f7c341d094418fae37`  
		Last Modified: Tue, 07 Jan 2025 17:24:54 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1ed0eab4fd86ab93b95eeee78e8c3178c18d85fc0b7cb026c55ec98fdd339f`  
		Last Modified: Tue, 07 Jan 2025 20:32:29 GMT  
		Size: 6.2 MB (6218091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:3ce98b4ce2b027cb7fb1c29a3c5281ad6687d6ce6a851ef265235c7416193f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 KB (7899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab0563db4e39db59f804b6b0f3e647f508808e8f207ddbd709959a0dbe9218c4`

```dockerfile
```

-	Layers:
	-	`sha256:ca87e6cbc505d3c52c08a0353dddb9d9d50fda6f0c83f6c438322ceda1bdb452`  
		Last Modified: Tue, 07 Jan 2025 20:32:28 GMT  
		Size: 7.9 KB (7899 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.20` - linux; arm variant v7

```console
$ docker pull hylang@sha256:983f55c8b0e76e27e6330891e2f875dd9a8102c9bc0719f3e7a126e3068d49eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26976390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343747763a1691308ecefd993fb7fb6ea2e36f31c4c8cceae6c4d251b159f694`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
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
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a7b3f0e95844a9d728ec36cd0a6d3a25cde46780e99640722e89eb89868dde`  
		Last Modified: Wed, 04 Dec 2024 23:43:27 GMT  
		Size: 455.2 KB (455165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b894d06a2a291b567a77f7ccb50e0169c27840b648f489ee7be031645aa74a9f`  
		Last Modified: Thu, 05 Dec 2024 01:12:09 GMT  
		Size: 17.2 MB (17207147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06f2ea40b02579b01631caa73c531c5be7b607fd95577ae1498c5ddff37f105`  
		Last Modified: Thu, 05 Dec 2024 01:12:09 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015756047f3c7180b7c9385d58ea2189f6da016e6b18201745473a6829ec6de8`  
		Last Modified: Wed, 11 Dec 2024 19:33:10 GMT  
		Size: 6.2 MB (6218341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:5acc7113cb480ddda864bfaa1ca65932379f11d3473e2bbf1f6250202844a30e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.9 KB (668944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:548333ce1236c7a3212334db52f83b6ca7472a462c123560ff4728758c0c25fd`

```dockerfile
```

-	Layers:
	-	`sha256:20bf7874c9eda0eb7ed3a13176fa5715c95efe0c2581f0e13f96d7c2310634ea`  
		Last Modified: Wed, 11 Dec 2024 19:33:09 GMT  
		Size: 660.8 KB (660830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66b07eaed5423edd7fa0db865003790a96961d5fea338002494c528a5c252274`  
		Last Modified: Wed, 11 Dec 2024 19:33:09 GMT  
		Size: 8.1 KB (8114 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:aa5db104eb90d3fcb8cc77e4b5cfde4bf22e35623bc7fd0fc099ec2c1cd6e245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (26995120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37333ab4c1a67798dbe7372e7cba025c5a2ac587fb4f501be80359076156e57d`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 03 Dec 2024 22:49:59 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
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
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721755a35fcbfe0867183d7cb7cd9f5302b052fc3e22ccfe6840442901b14353`  
		Last Modified: Tue, 07 Jan 2025 14:13:18 GMT  
		Size: 446.1 KB (446147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e5b59f54cf98cf32fff7d59d4840859283932682b7aedeb42d14df04e98185`  
		Last Modified: Tue, 07 Jan 2025 14:25:32 GMT  
		Size: 16.2 MB (16243994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b90af33387b06ebda65c66ba9931dc503273a9a3343bdb9bf8d72d64521049d`  
		Last Modified: Tue, 07 Jan 2025 14:25:31 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0257f9ff0724c767e467aee2df1d8c34433bdb17a99460d1c18bdf051c03d51`  
		Last Modified: Tue, 07 Jan 2025 17:41:46 GMT  
		Size: 6.2 MB (6218044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:98b0381a3472286832e4149ca85aaa0320730f2e11e5f4e9a9ec87e2e5bfea0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **660.5 KB (660537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e78078f3229fb9c1b8fea3de95b5f61ebec605d2d3494bc2059e79b6de1684`

```dockerfile
```

-	Layers:
	-	`sha256:d59fa0484915081d4f9530c5c9be9b646cef1dff296a5a66aa6caaaf0dbaebf8`  
		Last Modified: Tue, 07 Jan 2025 17:41:45 GMT  
		Size: 652.4 KB (652395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01cc6dfa16bc630e3528638ad57e3131cee9a8c6fbf009c85eadc950e3c3aaf3`  
		Last Modified: Wed, 08 Jan 2025 01:43:27 GMT  
		Size: 8.1 KB (8142 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.20` - linux; 386

```console
$ docker pull hylang@sha256:427b828619f03cf74d4cc25740a61e37c876ead1641a64d831ece1d65ff1e929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 MB (26469715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4439971abd40cc96a2fe0b56438343200b59edecca30c244bfb3da4cd3328a1`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 03 Dec 2024 22:49:59 GMT
ADD alpine-minirootfs-3.20.4-x86.tar.gz / # buildkit
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
	-	`sha256:a48310298946cd9150f3929f2f8cebe3709f1c7ecd0e99ff2b0c9b6502172586`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3463189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab939807322bc2fe85450bcd7bc3413f82bfb5a200edf3fb933b90d35f074b64`  
		Last Modified: Tue, 07 Jan 2025 03:35:18 GMT  
		Size: 444.4 KB (444382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1272d72b6cd01ed5dd45bb9d398d7e27fab15ba25afd0e0e8f8e102a80f8d053`  
		Last Modified: Tue, 07 Jan 2025 03:35:18 GMT  
		Size: 16.3 MB (16344001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d1f5e4a451af06d06b9b6f5bf0e36e8d3048c3c3d47ae1c6b1ae78f3b8dd7a`  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9c944e912acc90dfc8a7fe821e2ccaaea53365d35068b49130ff29d0aa65b0`  
		Last Modified: Tue, 07 Jan 2025 04:22:28 GMT  
		Size: 6.2 MB (6217894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:5f013353ca1ae131d04ecb9e1ca3d5159d4756327b26e75ace90046acdcf5fe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **660.3 KB (660320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5b4980138eab20d70f03b8e7b2852e5dd3e34ff75914f776d99fad22b22e56`

```dockerfile
```

-	Layers:
	-	`sha256:dc7ec251c08f403ae333b149418f9c5ac6c8ba78808a3f0620600b11b7aa99cd`  
		Last Modified: Tue, 07 Jan 2025 04:22:27 GMT  
		Size: 652.3 KB (652314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:620fa052e7354bf89b7b5a1cd368237ae6b6fdbd0e621b9e6a02890399259806`  
		Last Modified: Tue, 07 Jan 2025 04:22:27 GMT  
		Size: 8.0 KB (8006 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.20` - linux; ppc64le

```console
$ docker pull hylang@sha256:f475e74c9cb12798bdf29f1d5f53e94676ed34307abc8366c58a699b9332086b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27076613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c830b8ae7fa20378a0e9ca53bb1ff4193d5c3fdc6c0896c1e45ff68c07a6d952`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 03 Dec 2024 22:49:59 GMT
ADD alpine-minirootfs-3.20.4-ppc64le.tar.gz / # buildkit
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
	-	`sha256:c96bc34ea0111931eae2007b7db67b205ebd3c8a096d711e1be59e48f25006a3`  
		Last Modified: Tue, 07 Jan 2025 02:32:24 GMT  
		Size: 3.6 MB (3568727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5874797fd4d5c5516c705b7850433463089259824f2b1147ed89224c9b8ac04c`  
		Last Modified: Tue, 07 Jan 2025 08:30:48 GMT  
		Size: 446.5 KB (446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aefbfc78ca0caec149a5de3893a657750a40923ccc1ae325782fbd511a128fd`  
		Last Modified: Tue, 07 Jan 2025 08:46:12 GMT  
		Size: 16.8 MB (16843026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eeec02cf5ceb6c65c8ae7037f19ada201e0db2561a23a0ee6e6db979e7da9be`  
		Last Modified: Tue, 07 Jan 2025 08:46:11 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d944a572bd7e1d3d01f7fde24a1e37d33fd5966eefe3887573fd0dbd6e4c6cf`  
		Last Modified: Tue, 07 Jan 2025 11:41:57 GMT  
		Size: 6.2 MB (6218087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:87a5dd52fce2070d4aaeb0f48a12b4dfb877ca2ce93e78b03e0d4987ab52110f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.5 KB (658504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:186f44069614d8bdffe866a3c64857ae95addbbe058fce90cb7ac1bc76273d5a`

```dockerfile
```

-	Layers:
	-	`sha256:500201f5b627ee50589d4903c6ad02c1a0919cdc152fbe4869fb02c9ab1e965b`  
		Last Modified: Tue, 07 Jan 2025 11:41:56 GMT  
		Size: 650.4 KB (650422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06fdd743f906683c2b210ad7f4e7ff8d310b0252dea6feafb28b0309e5c163b4`  
		Last Modified: Tue, 07 Jan 2025 11:41:56 GMT  
		Size: 8.1 KB (8082 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.20` - linux; s390x

```console
$ docker pull hylang@sha256:8978606111416713583a1d5ae76132e06b1b4691f2195297f55db65cd5ba299e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26714562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18011a8c2a8f48080391408224ea1088c9890e180a0698548a0d9e3dbae52a7`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 03 Dec 2024 22:49:59 GMT
ADD alpine-minirootfs-3.20.4-s390x.tar.gz / # buildkit
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
	-	`sha256:2ed16bdf68dac880df118dfa3d21d44652bc18382729359f97297fa5998086cd`  
		Last Modified: Tue, 07 Jan 2025 02:32:49 GMT  
		Size: 3.5 MB (3459179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60331bd144e0dee0bcf228deaa18c9b2bd2cce3f24e2b721d8dfa614550c029b`  
		Last Modified: Tue, 07 Jan 2025 14:22:27 GMT  
		Size: 444.9 KB (444948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ad4d942ee3fe6818ed072ea0bb0de4be58bf41c7c9cbe11d287394aa6091b0`  
		Last Modified: Tue, 07 Jan 2025 14:34:51 GMT  
		Size: 16.6 MB (16592237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753cdb36717feae1e3701c3e3e92ff8398319ad21c916c232bdfbebcf6a025c3`  
		Last Modified: Tue, 07 Jan 2025 14:34:51 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef1a7d2029b6b2255e5afdc42858049018fe6bd9b4f14f1aea98bb44925d323`  
		Last Modified: Tue, 07 Jan 2025 17:16:36 GMT  
		Size: 6.2 MB (6217949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:623e01b425567269ef5c3fcdf877f563d292494622b8c981d766723030562cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.4 KB (658426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4abd4de61b9dbd63debb4b9477ac4a9ffa182268c0ddeef39bc4d0066f2ad6a5`

```dockerfile
```

-	Layers:
	-	`sha256:d7f3325fd16a67b9bddaf537c6277a5910571ba3ee13d294ccd901a775f0b6e4`  
		Last Modified: Tue, 07 Jan 2025 17:16:36 GMT  
		Size: 650.4 KB (650388 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c19fd45b92190f077aaba9d62023af39bd9f4ef2d97eb1a8fa32efa0cae54faf`  
		Size: 8.0 KB (8038 bytes)  
		MIME: application/vnd.in-toto+json
