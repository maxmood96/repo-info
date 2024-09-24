## `hylang:alpine3.19`

```console
$ docker pull hylang@sha256:704f97c53b1718d8e514a66bfb4dff0971ec29a307d57d2b9b8d6c5b383c5aa7
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

### `hylang:alpine3.19` - linux; amd64

```console
$ docker pull hylang@sha256:e661675a849e28431944c15d078892ba61b4e51bd2bb64ccb7ef512a384fe9f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22836965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb7594b6aa80b03eb957fd8c9de076c7f50829e4ffb5935bbd51338911bb2b3`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 17:16:05 GMT
ENV LANG=C.UTF-8
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PYTHON_VERSION=3.12.6
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["python3"]
# Wed, 11 Sep 2024 00:07:32 GMT
ENV HY_VERSION=0.29.0
# Wed, 11 Sep 2024 00:07:32 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 11 Sep 2024 00:07:32 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 11 Sep 2024 00:07:32 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90242465ba1fec3f3a94945d1a69dd981c4229d7381391e7a36065f73123c7a`  
		Last Modified: Thu, 12 Sep 2024 21:19:13 GMT  
		Size: 627.9 KB (627915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f98da0a565fe0bf138ee9fe66c1cce1847f3fdb4cf5fbd4082a338c933ad0ca`  
		Last Modified: Thu, 12 Sep 2024 21:19:14 GMT  
		Size: 13.2 MB (13181508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f2767c59777361a0a8065189cc159fa5891f3121a5777feb955e57ed1a3faf`  
		Last Modified: Thu, 12 Sep 2024 21:19:13 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5617be5f79b54a282d766a37dee02899d09026225a29fe9aa0f27e050b6f865`  
		Last Modified: Thu, 12 Sep 2024 22:03:25 GMT  
		Size: 5.6 MB (5607587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:4bac1cd06cb0d61b13438b2d9852f6887551e158b975899f2261ae9c912145b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1042359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18403ca5372eb10e5c4a68ce769091d6c044632bf678f84d6c2e071d078c8eed`

```dockerfile
```

-	Layers:
	-	`sha256:23b861ac6badbe2f8c4dbee21d0a5204ccd6bf3b9d34fee9aa13f8dcaa59f15f`  
		Last Modified: Thu, 12 Sep 2024 22:03:25 GMT  
		Size: 1.0 MB (1033180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3807cffde18e0aa967694d50fa459a52d247b7fba302c54d310cc3d602ea196`  
		Last Modified: Thu, 12 Sep 2024 22:03:24 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:alpine3.19` - linux; arm variant v6

```console
$ docker pull hylang@sha256:4b0b61e2cb038ee74a9f4594058402446da0017eb19b5394ad33b7e82eb84dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.2 MB (22182011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad56a8f313b4a4c4c9afb6037e865d593c29b3c94a71009422eb5ce19fb4ad51`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:26 GMT
ADD file:87d4cb9e99b4a12939a030198a62d49f1c5b7856f27d62fea0e948cd2120d51d in / 
# Fri, 06 Sep 2024 22:49:27 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 17:16:05 GMT
ENV LANG=C.UTF-8
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PYTHON_VERSION=3.12.6
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["python3"]
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HY_VERSION=1.0.0
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HYRULE_VERSION=0.7.0
# Mon, 23 Sep 2024 18:27:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 23 Sep 2024 18:27:06 GMT
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
	-	`sha256:7d4e58b9dea7c45310b53b62810f28226b8c67ac169ff93bd585750d54d56c53`  
		Last Modified: Thu, 12 Sep 2024 22:06:25 GMT  
		Size: 12.8 MB (12762764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4873a9e69d697af390e04fe6be5dc8d3110603b05715adab31d5ff36e636711`  
		Last Modified: Thu, 12 Sep 2024 22:06:24 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f93a5d78aee913938336327b605553539479840ffffaa609bbbff9538c843f`  
		Last Modified: Tue, 24 Sep 2024 01:17:59 GMT  
		Size: 5.6 MB (5613786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:ff36f37502df94c4b59ad7702e939a27888fd9c9f01345e601c0318aefdbe78e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.1 KB (9071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f781a738ac2f1b2336f9221f7f58e5053464674c836f01fe86bdd89531872aa8`

```dockerfile
```

-	Layers:
	-	`sha256:cbd526c3266765ce68f071c12203385c0fe59206c0bb8f2c7e3abfa70b0a9032`  
		Last Modified: Tue, 24 Sep 2024 01:17:58 GMT  
		Size: 9.1 KB (9071 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:alpine3.19` - linux; arm variant v7

```console
$ docker pull hylang@sha256:346085fcd083927ad8498ece61dd65f02d5162ddcbfb16179b642fd77c02c6af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.5 MB (21504128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa9de69746f07b2af01bfb13b1ca42900702da8f9fed35c8f42624e2fec4f1b9`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:05 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
# Fri, 06 Sep 2024 22:08:06 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 17:16:05 GMT
ENV LANG=C.UTF-8
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PYTHON_VERSION=3.12.6
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["python3"]
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HY_VERSION=1.0.0
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HYRULE_VERSION=0.7.0
# Mon, 23 Sep 2024 18:27:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 23 Sep 2024 18:27:06 GMT
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
	-	`sha256:a0614b5325a2ea097af5ef3f9774e1884cd12e46ce16b201796dae3dc0a906e3`  
		Last Modified: Fri, 13 Sep 2024 00:46:57 GMT  
		Size: 12.3 MB (12334492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a20c6ea67b6b7962a281845b53874cea6a59d44d391ffdd6e9bdfb97248d22`  
		Last Modified: Fri, 13 Sep 2024 00:46:56 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddf05b36217f8f4cc3115ca6b3fa438583d208e7194d122fd79d373ed82b40c`  
		Last Modified: Tue, 24 Sep 2024 01:29:13 GMT  
		Size: 5.6 MB (5613749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:164cb72096662e592213a8190799c7a3a58609f9feba977c5c2870003008be90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1045389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a2da044ab242b6df1c88df24ad666a01da0d47b78db5700d58f338c1928518`

```dockerfile
```

-	Layers:
	-	`sha256:67bf0e16ee3893da459c93035fec71b2059f95663913afff7de86b6429f2f400`  
		Last Modified: Tue, 24 Sep 2024 01:29:12 GMT  
		Size: 1.0 MB (1036099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba586e73a2aacc2e0ac41afbfa2ecb3676297b488cea24c25829f693700fad4f`  
		Last Modified: Tue, 24 Sep 2024 01:29:12 GMT  
		Size: 9.3 KB (9290 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:2a59fb49de5ec07de3a415ea3f2f599df59db3481b9244976fba3fe6bedd1106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22846088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628c253beb89ff71d1f2c801eba8cf3a87c0c5ca97491f71010ac1f0bd0288ea`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 17:16:05 GMT
ENV LANG=C.UTF-8
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PYTHON_VERSION=3.12.6
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["python3"]
# Wed, 11 Sep 2024 00:07:32 GMT
ENV HY_VERSION=0.29.0
# Wed, 11 Sep 2024 00:07:32 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 11 Sep 2024 00:07:32 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 11 Sep 2024 00:07:32 GMT
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
	-	`sha256:f77972eeffb8bd5bb8dda73ecad37a5a3fbad2060b60a1bda404c17ee7bbfaf1`  
		Last Modified: Thu, 12 Sep 2024 23:33:35 GMT  
		Size: 13.2 MB (13248858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebaa128b36d62d3ab266aead4a225936da7476d921854b809f7b7cc6ca736402`  
		Last Modified: Thu, 12 Sep 2024 23:33:34 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d225f311a1e35ef8dba46b3fd97b652abfadc5db19203cbd14534575c085cb26`  
		Last Modified: Fri, 13 Sep 2024 02:41:50 GMT  
		Size: 5.6 MB (5607544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:5348b0bf6eaac79c6dddca78ffe567474e19d9c5ec22515af1840231ecabc37f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1042908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb695145e148ada2e12e514cb18bce0fe83a9705cd7966b499ffd8d339bd876`

```dockerfile
```

-	Layers:
	-	`sha256:4b447e9aad368fac25e0b26286c159e6264d6b66e03bee9cdd6d03344df2861d`  
		Last Modified: Fri, 13 Sep 2024 02:41:50 GMT  
		Size: 1.0 MB (1033284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:416427451074a2cc901bbecaa64365baa58eb94b4448354dad22a6a5bb987351`  
		Last Modified: Fri, 13 Sep 2024 02:41:49 GMT  
		Size: 9.6 KB (9624 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:alpine3.19` - linux; 386

```console
$ docker pull hylang@sha256:17d640809fba9d4d73b7f5d8b4644eb1aed29b8889cf84d3315ff5dd02477586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22873705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdaca0c29f5f165b9a6a830bffb04c6f167ae826d3171b123125778cbb5c9541`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:25 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Fri, 06 Sep 2024 22:41:25 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 17:16:05 GMT
ENV LANG=C.UTF-8
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PYTHON_VERSION=3.12.6
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["python3"]
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HY_VERSION=1.0.0
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HYRULE_VERSION=0.7.0
# Mon, 23 Sep 2024 18:27:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 23 Sep 2024 18:27:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58aa52a341aa73b3dbd9bc5d1d8d104d775f8cfba754754a5b422ff88fa59de1`  
		Last Modified: Thu, 12 Sep 2024 21:21:38 GMT  
		Size: 628.4 KB (628423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be60cf6e627e5d88dd07d3e7a2013cd2630bdcf5b3a3db82e14085045672470d`  
		Last Modified: Thu, 12 Sep 2024 21:21:39 GMT  
		Size: 13.4 MB (13377731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a2d3db154d3c4279ec8ba394948726e1d4e23ebb7eb864bb7a3e93f6133be1`  
		Last Modified: Thu, 12 Sep 2024 21:21:38 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4b62a3641dd28bcb1012049d9e3597b1f38ea5367b0855943a6685a12d3f97`  
		Last Modified: Tue, 24 Sep 2024 01:02:00 GMT  
		Size: 5.6 MB (5613695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:5ab8842c849357ff2cb85fac7fbc8b33f331eea40b6fe94313b0ef3fa6859ea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 KB (8898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e049b4899edc7d2f58f3276d08f4904a55e6f0486405c68ef61eabc99e8f361d`

```dockerfile
```

-	Layers:
	-	`sha256:a4bb01f6e82b0fd51b40209df36b3d5c5e4dd349ac2fe679cc6833375a8aa8e9`  
		Last Modified: Tue, 24 Sep 2024 01:02:00 GMT  
		Size: 8.9 KB (8898 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:alpine3.19` - linux; ppc64le

```console
$ docker pull hylang@sha256:cd3867abdb0d7ceac0c267be41d4e65ed314bf7effea541c99752c77071437b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23290301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c026b458fc7a6bb75eaacf4e9bc27ff9823599ebc4ab7ce993ee38be932cdc83`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:13 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
# Fri, 06 Sep 2024 22:26:13 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 17:16:05 GMT
ENV LANG=C.UTF-8
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PYTHON_VERSION=3.12.6
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["python3"]
# Wed, 11 Sep 2024 00:07:32 GMT
ENV HY_VERSION=0.29.0
# Wed, 11 Sep 2024 00:07:32 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 11 Sep 2024 00:07:32 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 11 Sep 2024 00:07:32 GMT
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
	-	`sha256:d32622da6a5a5ad0ae514930bee013f2c600e4767d95a32ad2081f7099ca8c00`  
		Last Modified: Fri, 13 Sep 2024 01:30:23 GMT  
		Size: 13.7 MB (13687189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3596a34eb5f7cf197288e2a4b84bc7c6bc02c6e6e0f45d54f1761bda7a1428`  
		Last Modified: Fri, 13 Sep 2024 01:30:22 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbf362ceed8a4834d0041e30c231ff82065a2a80e5b4d526ee1cd80f525eff8c`  
		Last Modified: Fri, 13 Sep 2024 06:51:52 GMT  
		Size: 5.6 MB (5607559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:083327ae6b84b1cbfc4fcdbcdf9bfc7ab412a909a9509949f01a587cf9f8ecb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1040543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b01747f12d8a4b2f9f33d4a298e90905ecf637ec173c7d7fae0c60c74ee123ab`

```dockerfile
```

-	Layers:
	-	`sha256:07a3bc2e52895c958be1f03b0805b1ae456c1340e69cf6436161a182e07f6e69`  
		Last Modified: Fri, 13 Sep 2024 06:51:52 GMT  
		Size: 1.0 MB (1031284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3eaeee93b1feccdfc2f33277ca5ba35864899a28482090cd5460352f23b970cc`  
		Last Modified: Fri, 13 Sep 2024 06:51:51 GMT  
		Size: 9.3 KB (9259 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:alpine3.19` - linux; s390x

```console
$ docker pull hylang@sha256:9e2f0648a6a15eef503b61512416a8cb39c449be7f3e4f44de334cd3a9162556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (23027276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4baea61d2fb74cb5a09bdb3c9ced9b548f7b1a39c7247f426e0f666c9a978d`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:26 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
# Fri, 06 Sep 2024 22:48:26 GMT
CMD ["/bin/sh"]
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 17:16:05 GMT
ENV LANG=C.UTF-8
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PYTHON_VERSION=3.12.6
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["python3"]
# Wed, 11 Sep 2024 00:07:32 GMT
ENV HY_VERSION=0.29.0
# Wed, 11 Sep 2024 00:07:32 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 11 Sep 2024 00:07:32 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 11 Sep 2024 00:07:32 GMT
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
	-	`sha256:08521185ef15bc12b9d58b1248d27d1e95452755a7d1a032008da2b5ada8ad29`  
		Last Modified: Thu, 12 Sep 2024 23:35:04 GMT  
		Size: 13.5 MB (13537153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb716403e2e89afa6f722893a64e8e12654f9e6b1fe83aad2f10425a64302fd`  
		Last Modified: Thu, 12 Sep 2024 23:35:03 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce547e6e3a7f89528a9014332ade76127f64a69fc80105bf6e1a48432a0d52e`  
		Last Modified: Fri, 13 Sep 2024 03:18:04 GMT  
		Size: 5.6 MB (5607525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:84102032063b9eab7679eccf57c914216a7d15206bb87081078df74a87cca1a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1040416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b5ce2cafa107022950b0b499d1916b41b1c7ecc858aa1081c2073578e408b63`

```dockerfile
```

-	Layers:
	-	`sha256:18f92a4aa936883ef402fc8ccf2ee4f1ef4145a0c8186792564b696309e98c4c`  
		Last Modified: Fri, 13 Sep 2024 03:18:04 GMT  
		Size: 1.0 MB (1031226 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:839fbae76ae19e7593d3a25f8c7df7d122d30c01ad5f7c8541532c8e2903c47d`  
		Last Modified: Fri, 13 Sep 2024 03:18:04 GMT  
		Size: 9.2 KB (9190 bytes)  
		MIME: application/vnd.in-toto+json
