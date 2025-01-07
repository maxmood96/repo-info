## `hylang:alpine3.20`

```console
$ docker pull hylang@sha256:38cf746bf5bf0382a886c86b9c654b02cb911b3c43256913a98aa33a9a00f06a
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

### `hylang:alpine3.20` - linux; amd64

```console
$ docker pull hylang@sha256:7570cce24d917d2580101b54e8428513649a3fe9f8b20585c4fed6588a3c9717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.2 MB (22154267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7b47440dc2669e1e51173efc841c5298297e6834e7533dc78ca05a00ee5b7f`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 02:30:19 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PYTHON_VERSION=3.13.1
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
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
	-	`sha256:17806adfd2bf0bc2a62bf1e130b05fc09dd4cd7984a172fa80dbe7bbfb3c6c20`  
		Last Modified: Tue, 07 Jan 2025 03:23:03 GMT  
		Size: 443.9 KB (443906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628237ce03b437c1af4a3daff673872b5f77a059c2f245d823d3f3e9101b1fc8`  
		Last Modified: Tue, 07 Jan 2025 03:23:04 GMT  
		Size: 12.4 MB (12410421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a79194e1b65e06f4bbd090f4b751b5b71003dcfdbf4d4199801c644e3f57bd9`  
		Last Modified: Tue, 07 Jan 2025 03:23:03 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd894dff2f7ac01795b77b12ae3ea6ba06be51a3b0d00c4ba6644b2ec839955`  
		Last Modified: Tue, 07 Jan 2025 04:23:33 GMT  
		Size: 5.7 MB (5685692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:ad52799472fb73ea8cc3db9440a3165371ea6d3b53a99d8ccf3c2e2806e97a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.4 KB (627396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fddc4260ead0c1bb98dd25612f701c54a18bdee8b68ac7ba6ccbdf939c9a5c0`

```dockerfile
```

-	Layers:
	-	`sha256:fe240e5cb05a99722ad06d08d16c96719c7081dcb2be8ffeaf03775b37afc5dc`  
		Last Modified: Tue, 07 Jan 2025 04:23:33 GMT  
		Size: 618.1 KB (618126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52c0359ead5d046b550ef7d431d72d007feed5d3c2649a2562ca3e02fc1a2623`  
		Last Modified: Tue, 07 Jan 2025 04:23:33 GMT  
		Size: 9.3 KB (9270 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:alpine3.20` - linux; arm variant v6

```console
$ docker pull hylang@sha256:d8c728a7ea56af4c2b62a16678e8e571773e940a6dc7f2fc1d46bef333a91381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23630957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91462853de595a65891e2f95f9c67f5ed5ff3e122033e1336c2046d2253e4297`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PYTHON_VERSION=3.13.1
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
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
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaae7f50b1179fbba9e574ed7f89db6d7ef4b8bfad3f0e758189283f1bd47387`  
		Last Modified: Tue, 12 Nov 2024 13:50:59 GMT  
		Size: 456.0 KB (456034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c78c7aebb2f5af536b813308749bda5acb46aadb31f91d3806044281ec08d9`  
		Last Modified: Wed, 04 Dec 2024 20:37:44 GMT  
		Size: 14.1 MB (14122264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030124c23782f46e6fe9940c46dd83b485e8bd3115ad371aca130edd1a03f1f9`  
		Last Modified: Wed, 04 Dec 2024 20:37:44 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bf5916f43ff33fbe013815371baaf3fb87ebc33a03b03ca96a5501033be19b`  
		Last Modified: Wed, 04 Dec 2024 21:25:51 GMT  
		Size: 5.7 MB (5685814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:7f6dae6c717e8894b664eeec9c60d88d82b635d6f820b3c7857b6c49771d62db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 KB (9163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e22a0092e3c492616a09663e3d0b8dc2af7c3bdcf9ab15ad02579f7d7f5bdab3`

```dockerfile
```

-	Layers:
	-	`sha256:8f43af06f0ff61bb6aae06f31ca0b87ffd48f33d49175ccfb87fc27c7669adca`  
		Last Modified: Wed, 11 Dec 2024 19:28:32 GMT  
		Size: 9.2 KB (9163 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:alpine3.20` - linux; arm variant v7

```console
$ docker pull hylang@sha256:db10602b85423d81f6359ff1528a2f523c3f02d3c242cc8e839edbd49aec4083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22849399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2756e0ad1c8a68bf6e90a101779b2ca0080050b5f19f7cefb59187f875305d04`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PYTHON_VERSION=3.13.1
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
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
	-	`sha256:be84f58a6ba1e5afec1f980bc5e88789f864d7f484d01c93664b9fff548f3a56`  
		Last Modified: Wed, 13 Nov 2024 02:15:34 GMT  
		Size: 455.2 KB (455163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d40aab0bea0851cd74e3603c60e1011eb69a2364e7d6f4394624197a3eb38a`  
		Last Modified: Wed, 04 Dec 2024 22:06:35 GMT  
		Size: 13.6 MB (13612650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145932f2f22c9bfa52e948db5859a91be8bf76b53f20e6880361cec8664248f1`  
		Last Modified: Wed, 04 Dec 2024 22:06:35 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7893dcf852880f68df62e5d273435ce90df4ed577f19955745132978c1ee219b`  
		Last Modified: Wed, 11 Dec 2024 19:28:28 GMT  
		Size: 5.7 MB (5685850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:e4b10783858781388dbd6f3cfa4485738168face6bb60feb46bb93a420b0f7f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **636.0 KB (636006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c90413c17cf76f0e69d70cdf552a51edd3572709ae5f749f8c61a5a034612a75`

```dockerfile
```

-	Layers:
	-	`sha256:f24d12c1ef943645346b1ececde56d2eb9bc1e82aa8a3ffced9af15ccd5d46a4`  
		Last Modified: Wed, 11 Dec 2024 19:28:28 GMT  
		Size: 626.6 KB (626628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffcbfe41f9f24d374291b983f08f51a0f773ab691a85a0e9af3a5208fd4c6685`  
		Last Modified: Wed, 11 Dec 2024 19:28:27 GMT  
		Size: 9.4 KB (9378 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:alpine3.20` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:4aca412e68b0f12e1f82b360e934cf5653c73e6fb6cbddf8867ed40c154bc6ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 MB (25493761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64264b60185562d342cf040d565d59cbc112f2950f4639d3f00f4e2304ad123`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PYTHON_VERSION=3.13.1
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
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
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe80dd7098fb09d5aa060ba0768ea2b70faad999bc0ab1417de25dfa6fc81e03`  
		Last Modified: Wed, 20 Nov 2024 21:20:29 GMT  
		Size: 457.5 KB (457482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7093bb662347dc2e00b7ea975cbd1e78959eef4a208a5e9009a53263563aea`  
		Last Modified: Wed, 04 Dec 2024 21:45:11 GMT  
		Size: 15.3 MB (15262434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7fd229ff33d08a7f77efd410927cc58523184f02f6ad7c26ed807436e5f460`  
		Last Modified: Wed, 04 Dec 2024 21:45:10 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99a8beba45873b4803736f9ac4b5c266a6975ec2a8add640def8b67a3daafde`  
		Last Modified: Wed, 11 Dec 2024 19:29:06 GMT  
		Size: 5.7 MB (5685870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:366d7de577c2fca62f8d91914fa4475166de7384099e1054d049e80926507ae1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **633.2 KB (633222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beb5ae6f73aacd1fb562d6efb0648d419700523e08a49d67d76637a8dade2ea1`

```dockerfile
```

-	Layers:
	-	`sha256:6c32b2012c950f39035cbedb28ba47243664ae40565ad4a4577ad5c2e614b136`  
		Last Modified: Wed, 11 Dec 2024 19:29:06 GMT  
		Size: 623.8 KB (623800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40c5aa16acc34839e38ad921d95e3bca4ab3bb5a2746303e3502e27c35c95b7a`  
		Last Modified: Wed, 11 Dec 2024 19:29:06 GMT  
		Size: 9.4 KB (9422 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:alpine3.20` - linux; 386

```console
$ docker pull hylang@sha256:139039a945416667fbfd4d844900df0c49bb85936c14078537c65cdeaa188a43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22267589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ae1c2416751851b1cfe8b78e1933c6948f7311eca006d06063301ea04043a5`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 02:30:19 GMT
ADD alpine-minirootfs-3.20.4-x86.tar.gz / # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PYTHON_VERSION=3.13.1
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
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
	-	`sha256:4f7ec2480da0dad6b2a9f4fdbc6494f53619d7f8ef865f4492da6c85903903e7`  
		Last Modified: Tue, 07 Jan 2025 03:23:16 GMT  
		Size: 444.4 KB (444364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f841ff2bb62dede7eaeb6f12d85fdeb27a362d04b0a70ab093d7fbabc26dca4c`  
		Last Modified: Tue, 07 Jan 2025 03:23:17 GMT  
		Size: 12.7 MB (12674209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96e0298e96c822c225c6ea1131ca4873eb59a6d95bf5fd4596c453908722940`  
		Last Modified: Tue, 07 Jan 2025 03:23:16 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41176c1ca2f3110a59d6f8f6d5a61f235c546f0d1983df5f868db86f01c7972`  
		Last Modified: Tue, 07 Jan 2025 04:21:56 GMT  
		Size: 5.7 MB (5685579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:437dab38c6bbf289d03cfec225449219ca3fd9e9a07ed171289dd22792e3fef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **627.3 KB (627299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e18af5919b21f40b3a98d8bfffc6628ab348760dfbec4f93923832b5ebe6070b`

```dockerfile
```

-	Layers:
	-	`sha256:1dac5300188fb476a0725884462647562fcb60cf84e849bc2edb260d16e2f7e1`  
		Last Modified: Tue, 07 Jan 2025 04:21:55 GMT  
		Size: 618.1 KB (618081 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fe6170ad488dbaf455055fe6de0680fbc4e0ad7b366a8f7cce8aed27963443c`  
		Last Modified: Tue, 07 Jan 2025 04:21:55 GMT  
		Size: 9.2 KB (9218 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:alpine3.20` - linux; ppc64le

```console
$ docker pull hylang@sha256:85c9505d41155e0cbf34ce6a2cdbdc57098f715451b03b4e8ee5c3df75422d52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22797372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0d25a5a5149dbcdeb870283a906c0a8a544bdb7cfb839d1a00eda692a4c19d`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 02:30:19 GMT
ADD alpine-minirootfs-3.20.4-ppc64le.tar.gz / # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PYTHON_VERSION=3.13.1
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
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
	-	`sha256:c101c5a3cc754ad132d3f74c562f61f79a483a2c6fa0a64583b68815f5bcb07b`  
		Last Modified: Tue, 07 Jan 2025 07:59:01 GMT  
		Size: 446.5 KB (446524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1a4ae9c7af410e22ceb4bdb4265571aaf9a2c292034e4b6358dda9d2bbf2a9`  
		Last Modified: Tue, 07 Jan 2025 08:15:18 GMT  
		Size: 13.1 MB (13096184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e826d01dc67c7711552009e0f660c8d4f83c45c2acda501f8578407c65a78153`  
		Last Modified: Tue, 07 Jan 2025 08:15:17 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d618560b4d31b65107d2e6aa979e276d8e0799a2c23fb2a1b49d8f9a5701836e`  
		Last Modified: Tue, 07 Jan 2025 11:38:25 GMT  
		Size: 5.7 MB (5685686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:741f33c32d888f7d473cce1b3fa6a07a318439d18cbb7a3a8ee57b15185931f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **625.6 KB (625571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c1b23ab68ca49023b34ee1265696410cf275757a67a96949432fb441c5f747c`

```dockerfile
```

-	Layers:
	-	`sha256:76a597a85b3180e30456e28e18afcbe443392f90d78ba58dc7a0ca2c4b55ba6b`  
		Last Modified: Tue, 07 Jan 2025 11:38:24 GMT  
		Size: 616.2 KB (616233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d65892b0dcd840dba506bcd6bebfff2f08bd4225b318a5e5b154445799040d0`  
		Last Modified: Tue, 07 Jan 2025 11:38:24 GMT  
		Size: 9.3 KB (9338 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:alpine3.20` - linux; s390x

```console
$ docker pull hylang@sha256:0a3abd299c0cdd5ba5c5f831b6b0ce271c5104263c5348063bf0dac2e4a68693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.6 MB (24589405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb5b43a1c845bed6549d77fe21a8ce69e5ee4c0c9ac471c9a0a0e08a86ae80d8`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PYTHON_VERSION=3.13.1
# Wed, 04 Dec 2024 02:30:19 GMT
ENV PYTHON_SHA256=9cf9427bee9e2242e3877dd0f6b641c1853ca461f39d6503ce260a59c80bf0d9
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 02:30:19 GMT
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
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c91a42328865ef2d2ebed00cb001023efad23c6ac21c6a7c59141c748724773`  
		Last Modified: Wed, 20 Nov 2024 21:20:36 GMT  
		Size: 456.1 KB (456135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a4f2cf0f7eb75c89c279d958f4a85c38ad3fdd43c79b33f155518069237036`  
		Last Modified: Wed, 04 Dec 2024 21:10:26 GMT  
		Size: 15.0 MB (14985604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982cb2a7caece3ba98bc0a0f3051a197b0506b21dcca6f4bc787078c7f6cd6f7`  
		Last Modified: Wed, 04 Dec 2024 21:10:26 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6bcd401799046854d97da916b3c58a24a5eb96feb7362df631376ffdbfdd1d`  
		Last Modified: Wed, 11 Dec 2024 19:29:57 GMT  
		Size: 5.7 MB (5685809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:d89b6b9a0d078f85f35380c8c8f51be897c639e5dc6fcd00af02fdeb3752e47f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **631.0 KB (631012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:627458c827ffcdf701ef1402123b5a3ae07928922b8148e944270046c1a38e83`

```dockerfile
```

-	Layers:
	-	`sha256:916c90e58e0caf95de3790b4191032d5a1e39111b2f1c7cac14ff0d87ffb4f6d`  
		Last Modified: Wed, 11 Dec 2024 19:29:57 GMT  
		Size: 621.7 KB (621742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:650917d043b4a56d2c9527b96872680781cee1b3cc54635b9bde056b6975f43f`  
		Last Modified: Wed, 11 Dec 2024 19:29:57 GMT  
		Size: 9.3 KB (9270 bytes)  
		MIME: application/vnd.in-toto+json
