## `hylang:python3.9-alpine3.19`

```console
$ docker pull hylang@sha256:6f87b182176674beed79eb6a39d3997e8d5a712478b6857734e0eb777f12299f
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

### `hylang:python3.9-alpine3.19` - linux; amd64

```console
$ docker pull hylang@sha256:089d8de4757609e41c6675f32d57b706b797feb183ef891c071be8b28b409ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (21998626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8940629e72f5de291bd1c439d615bf9e2aa581120afbb291c938a14dfdde79c2`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 29 Aug 2024 19:15:55 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 19:15:55 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.9.19
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["python3"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HY_VERSION=0.29.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 29 Aug 2024 19:15:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8015745de94b1cda440223b642ce64356dfd77e1527e95dbfdc5d6a468e3392`  
		Last Modified: Fri, 06 Sep 2024 23:20:23 GMT  
		Size: 627.9 KB (627912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c747a26f30bbe08acccef085913796446ff9b900aa4275ebfc9877106282b6`  
		Last Modified: Fri, 06 Sep 2024 23:20:23 GMT  
		Size: 11.6 MB (11607330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c594f28d0df4906cb2dc3f0cbf3781a703ea57685de7cf30ab229f90709db8`  
		Last Modified: Fri, 06 Sep 2024 23:20:23 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68c7d4c075d20c8ba3c7ff6a9792e2e0d63a485cc6cff2e94a7a3e4b1afc281`  
		Last Modified: Fri, 06 Sep 2024 23:20:23 GMT  
		Size: 2.7 MB (2695906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cc0c0fb1694ea8ba381973c72b889a76850edecbef77887598d2bd144e5d7d`  
		Last Modified: Sat, 07 Sep 2024 00:10:43 GMT  
		Size: 3.6 MB (3647542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:eeb608ddd2c8af46647b666fffbf868610ca633f9bced2f6869f2c1b58479123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1044701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159284afd30927a7e9f3f18cdb3ad9d0f9fb83f8735c70018f29d5c5caf94717`

```dockerfile
```

-	Layers:
	-	`sha256:cf0094d8b4862a4715595355cad49bb7e1400ffb308ab3e349e312a1062e9015`  
		Last Modified: Sat, 07 Sep 2024 00:10:43 GMT  
		Size: 1.0 MB (1036201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:886c0b6057d06d8ab9b3620bc0db8f9ab4af75670f4707822a509607bef81557`  
		Last Modified: Sat, 07 Sep 2024 00:10:43 GMT  
		Size: 8.5 KB (8500 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-alpine3.19` - linux; arm variant v6

```console
$ docker pull hylang@sha256:a3fadf1c126e76f2dff2504f75264afb56fc42193783b8ba122012d1ba54c591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21395138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67153c1b004b62f3d5579fe948c923716e122f28bfebccaf76f58a1aa7ffb0a8`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 29 Aug 2024 19:15:55 GMT
ADD file:87d4cb9e99b4a12939a030198a62d49f1c5b7856f27d62fea0e948cd2120d51d in / 
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 19:15:55 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.9.19
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["python3"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HY_VERSION=0.29.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 29 Aug 2024 19:15:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8922ced57063579c37aeb21c1c664433762d26f8051e187a63b559c21b36da53`  
		Last Modified: Fri, 06 Sep 2024 22:49:59 GMT  
		Size: 3.2 MB (3176391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a39bdf9d326d55be66a6472913d0bdbe3b64af11a3fa17f368b4581b594e62`  
		Last Modified: Sat, 07 Sep 2024 10:50:50 GMT  
		Size: 628.8 KB (628820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522e5f1dea571d094f0b0b31709bcfd1f76392fc1ac5d347f2eceda65987e889`  
		Last Modified: Sat, 07 Sep 2024 11:53:20 GMT  
		Size: 11.2 MB (11245950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c387cce80780598ae2971cd992aad8b469348c39279142d5ddf6f64bb8a90249`  
		Last Modified: Sat, 07 Sep 2024 11:53:19 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6f911d36d34f883e551e22abf49026c22cf7f9b7c109070300a8c1ee21600f`  
		Last Modified: Sat, 07 Sep 2024 11:53:19 GMT  
		Size: 2.7 MB (2695913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ab70e5aa0a64573ff6bda6c57078a2145d2a7a81fe5edf8e5715611833d537`  
		Last Modified: Sat, 07 Sep 2024 13:49:29 GMT  
		Size: 3.6 MB (3647833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:cd91c31e74b69e02d48b946c81e6eeb5a7f324b8f65ed93f6f7814ce8eabe97f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 KB (8369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e18df2dfc770df4158357471f3b7e0111b42f9aee213b5a70c6fde2a6e439594`

```dockerfile
```

-	Layers:
	-	`sha256:045a7d271fb4abf670f074db2ca0641ef059599b36f24d4e83555e686544ab2d`  
		Last Modified: Sat, 07 Sep 2024 13:49:28 GMT  
		Size: 8.4 KB (8369 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-alpine3.19` - linux; arm variant v7

```console
$ docker pull hylang@sha256:799e15d1d8bf5decf2fe2f9d8d9bf9657205d2cb9ed50ed8760ab9209336e42f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20751150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ac15319d2a72e63d1a255057559b88a6de04b0e24a4581431b51b5fbf40b9c`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 29 Aug 2024 19:15:55 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 19:15:55 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.9.19
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["python3"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HY_VERSION=0.29.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 29 Aug 2024 19:15:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:426a5537ab470cede64a1b269dbc9f485fa674bec59555cdaa5a1c96e6675b0d`  
		Last Modified: Fri, 06 Sep 2024 22:08:37 GMT  
		Size: 2.9 MB (2927664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2773a0915bfcbc78e079faa18251ac0d879f0f82697ee83220c411ab06dd1bb`  
		Last Modified: Sat, 07 Sep 2024 11:07:13 GMT  
		Size: 628.0 KB (627974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c008571f9ae5c8dd26e2efb615cfa2e54decb165e68fd93257927c8d22b00a8d`  
		Last Modified: Sat, 07 Sep 2024 12:13:28 GMT  
		Size: 10.9 MB (10851620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30eb84f6b9498b2fe9c30fbc5c44f342cc960d25e17064b68aec80277ad975a4`  
		Last Modified: Sat, 07 Sep 2024 12:13:28 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6255bab872203a2e5f04530293020ffde86123c3d925fee9976f40401f0d603f`  
		Last Modified: Sat, 07 Sep 2024 12:13:28 GMT  
		Size: 2.7 MB (2695938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5135982aa72b892eb87d022ce8e99d5edf7b9861fec07965628a17afdc24e8d6`  
		Last Modified: Sat, 07 Sep 2024 14:25:15 GMT  
		Size: 3.6 MB (3647726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:4136facec43662db2a88d5861a4bfceb8fe404bed1016105be09a5baf87fe44d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1047689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db56b95f67057e7f8b442790cf9f8c153ca3c9f6b5b8422d5e59c058cb1710a`

```dockerfile
```

-	Layers:
	-	`sha256:6ac81f1b05b6714fcc2ac1ab4036205ec1053505e7ff61736ecce97d4361e8a5`  
		Last Modified: Sat, 07 Sep 2024 14:25:14 GMT  
		Size: 1.0 MB (1039101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4574e478b809a367108617a4cf342dd1379ba4bd057a53153ce8dd60d0797d27`  
		Last Modified: Sat, 07 Sep 2024 14:25:14 GMT  
		Size: 8.6 KB (8588 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:698c6738c392b383c39324ffbed043b93447bc0df386d1b21d6b8bb144855902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (22019832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60287d2e588fcc898bdfbc36eec2e9235cf3f7f3c4a20add7d80e1ad0de8b564`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 29 Aug 2024 19:15:55 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 19:15:55 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.9.19
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["python3"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HY_VERSION=0.29.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 29 Aug 2024 19:15:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf2f2790992c8c78211ff5181c3fb0eb2710f0d4ab4c29278770b838db532c2`  
		Last Modified: Sat, 07 Sep 2024 10:20:39 GMT  
		Size: 630.3 KB (630335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29ea2ca03eb81c7b9740aac1fb42028e7d462f51402a8a347100d43d086f36f`  
		Last Modified: Sat, 07 Sep 2024 11:12:44 GMT  
		Size: 11.7 MB (11686526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4cb9e06a819c7ae10454b49437fcb5911419f463f865c3981881a56fba0347`  
		Last Modified: Sat, 07 Sep 2024 11:12:44 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5153f1857201a905590d3c064b591adb2ae12969fecb7a91fd7415a210eb4099`  
		Last Modified: Sat, 07 Sep 2024 11:12:44 GMT  
		Size: 2.7 MB (2695921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2f77cfffdf9d24f344dfe86088164d400b72a407a414d2492627ce742029da`  
		Last Modified: Sat, 07 Sep 2024 13:57:53 GMT  
		Size: 3.6 MB (3647717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:49ac1a297bc96d0c2db6915c6106fee933293975232eac0e98a1a1e09a0fdf9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1045153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db8510d585e6c583017b94c7b01acae595cc18f07540a263b2562ff0a985601`

```dockerfile
```

-	Layers:
	-	`sha256:962d710c036092f1c881d0407691e64d0084dabd778c7c7c311726338b6d865d`  
		Last Modified: Sat, 07 Sep 2024 13:57:52 GMT  
		Size: 1.0 MB (1036257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25e9aeab7ee5ba1606fce164a50e84427bbe23c4faa5906b1b62e185ef736dff`  
		Last Modified: Sat, 07 Sep 2024 13:57:52 GMT  
		Size: 8.9 KB (8896 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-alpine3.19` - linux; 386

```console
$ docker pull hylang@sha256:82e07a4d72e6866d03e4f337df7c2c932f263c316be534bae9c7595e25a75226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 MB (22069484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aceb900394b6a8542053e42b866493881be70203899d3e2186d683e798f2400f`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 29 Aug 2024 19:15:55 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 19:15:55 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.9.19
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["python3"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HY_VERSION=0.29.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 29 Aug 2024 19:15:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d11b5d4e6c42ded431860a7f88f135e6fdaf352d33f9ae8f8c92bb34c7206a68`  
		Last Modified: Fri, 06 Sep 2024 23:25:56 GMT  
		Size: 628.4 KB (628424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fae23a2e09ae25a3c924d6de6e6e199d86448650826141478fec14f91c7aaaa`  
		Last Modified: Fri, 06 Sep 2024 23:25:56 GMT  
		Size: 11.8 MB (11843474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d9f741409eb6ee6197372554590fb807aeea8a17804a59dc2a9d4eb50889a9`  
		Last Modified: Fri, 06 Sep 2024 23:25:55 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9179623f37e5b445fe8b6199e171356b1590c7804cf665684289ed5166c514`  
		Last Modified: Fri, 06 Sep 2024 23:25:56 GMT  
		Size: 2.7 MB (2695929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17e23ac1fd50f32eec86c530d625ac9bd29057716cb79ed13b8edbb2d8ee717`  
		Last Modified: Sat, 07 Sep 2024 00:10:49 GMT  
		Size: 3.6 MB (3647823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:106c685c592e7b7681c6df97e0cf0de3ab93f03cc0ea649fd26c35ec8d7a9254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1044644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe15ac917eda30095950303d2ab7e80d5b4972dcb97fada17e034dd385e47050`

```dockerfile
```

-	Layers:
	-	`sha256:c5e02c4a16779c2a444e37201a0b74d310b366bb9bef844f61a75288ce53fe62`  
		Last Modified: Sat, 07 Sep 2024 00:10:49 GMT  
		Size: 1.0 MB (1036176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdded511902a1914a489679063abade2088675805acc914381efef46094e3526`  
		Last Modified: Sat, 07 Sep 2024 00:10:48 GMT  
		Size: 8.5 KB (8468 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-alpine3.19` - linux; ppc64le

```console
$ docker pull hylang@sha256:7f46d36eb7cf8e92ef89914563bfbeda7f3ed51936f5ae556679730bad471fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.4 MB (22420693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff52358fe3868cbe3d4a7703b640e6e260af3d0795097d7971bafabb7e19cc93`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 29 Aug 2024 19:15:55 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 19:15:55 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.9.19
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["python3"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HY_VERSION=0.29.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 29 Aug 2024 19:15:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5749dced5c3ea885609ac4ce0f87b1f345b6e9df997e9a8b0aaceac5eaaa6e3f`  
		Last Modified: Sat, 07 Sep 2024 09:58:37 GMT  
		Size: 630.8 KB (630837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435a3ea056201ec0f18ba34e4cbba787fdfe1ee83dc108e9bfdb7b0c97ecd451`  
		Last Modified: Sat, 07 Sep 2024 11:03:28 GMT  
		Size: 12.1 MB (12081359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc6030988115d2a52af4479e64aded102d2a727e0b8f88f3772c023f7bc2a95e`  
		Last Modified: Sat, 07 Sep 2024 11:03:27 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b438f58f14235bf33ef0cb533941770c6cce913329892eaabea1ee72a8d4366`  
		Last Modified: Sat, 07 Sep 2024 11:03:28 GMT  
		Size: 2.7 MB (2695914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dad74baeadceb2aa68a4120b3699ba867e253c8b1b2275b5f7c59fc9baab259`  
		Last Modified: Sat, 07 Sep 2024 14:00:18 GMT  
		Size: 3.6 MB (3647886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:d7244b6c552f4cad546a9bcb4bee78536e91a2198254ed7633ee95cc30a9a6cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1042837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7c55c822a2b70c75b6808b8a56433058dcc7a154697d73406ee0c095537512`

```dockerfile
```

-	Layers:
	-	`sha256:9aed0cf84ee0552c55a7073f26b02c6156985dc3c50c7b4e3819b2684dbf1603`  
		Last Modified: Sat, 07 Sep 2024 14:00:18 GMT  
		Size: 1.0 MB (1034281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2784e0dba01c4df48c7602486b8c9ba30ee51d2c4ef8434b1605d7d88d2c795`  
		Last Modified: Sat, 07 Sep 2024 14:00:18 GMT  
		Size: 8.6 KB (8556 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-alpine3.19` - linux; s390x

```console
$ docker pull hylang@sha256:3264c3453e6de83c6a0d3731e7e083c2190947ac2d097432acb60eeba0c33eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 MB (22102988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b2381cfd6b22a9365ed9b1c64e0cb975b557643dc5c8ed908a088852827a551`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 29 Aug 2024 19:15:55 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 19:15:55 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.9.19
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["python3"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HY_VERSION=0.29.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 29 Aug 2024 19:15:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf180b200a9685ef5f8a9f8ba267cdaf8e59fe28f3b974eee5118a914d262ab`  
		Last Modified: Sat, 07 Sep 2024 09:10:44 GMT  
		Size: 629.0 KB (628993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a01ad990fa193abcfa40f8e849ba8d3c5b27bb1e3fc26bd46dcc46e1bc7c96a`  
		Last Modified: Sat, 07 Sep 2024 10:06:30 GMT  
		Size: 11.9 MB (11876745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24a85d7397c54b2a541c8bea84581d63ed2afb2dd424c7c28cae4dc4d1fe680`  
		Last Modified: Sat, 07 Sep 2024 10:06:30 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c6e998b1a285a5565b79653807a7f062ad8e3fa6287f1cfcc025d679b55308`  
		Last Modified: Sat, 07 Sep 2024 10:06:30 GMT  
		Size: 2.7 MB (2695918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808d65cd4ee3b2842764f131814682434c9e7d4e9076a550bbd88c366d043f39`  
		Last Modified: Sat, 07 Sep 2024 11:53:43 GMT  
		Size: 3.6 MB (3647745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:8dc54e61d2eba3a5b90017c28c94add5d079e706b68fcafc78045be0a19282ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1042759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:175c25e16c962b5999365c12712ab90474af4e96a3339ff543cb8e153426a955`

```dockerfile
```

-	Layers:
	-	`sha256:db8f0ce13d6b5e3761507b24d00d90a205bda07db4d184a573cdf0f6fad3deba`  
		Last Modified: Sat, 07 Sep 2024 11:53:43 GMT  
		Size: 1.0 MB (1034247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64a48244ed7e897ad6bdb2028cb917bc1447844bd2e66c9ccfc452bdb37fa980`  
		Last Modified: Sat, 07 Sep 2024 11:53:43 GMT  
		Size: 8.5 KB (8512 bytes)  
		MIME: application/vnd.in-toto+json
