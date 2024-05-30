## `hylang:python3.10-alpine3.20`

```console
$ docker pull hylang@sha256:bcaa6860dbb05d6ada94e22f1ad5a304cc05cf660d6fe026dd3bfaef6c06645d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `hylang:python3.10-alpine3.20` - linux; amd64

```console
$ docker pull hylang@sha256:53766d23a13294547be964f52ac631cc344d60ca590dbd0a87bcc12111e4cb7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23558010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3038178bb08545e3741875eae65a46db6fbdbc4ed1a4441a9dd0d6354cb3fa`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:26:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:26:30 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 22 May 2024 12:26:30 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_VERSION=3.10.14
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 22 May 2024 12:26:30 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c04aca259ccbbbd92a78c0452532b76b5b2812b06999bafaaae910297770a9`  
		Last Modified: Thu, 23 May 2024 01:33:11 GMT  
		Size: 463.2 KB (463227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f727dcd054d6e34f2ab9652e820098454ae98fe10c047fca115ee33a1beb5a`  
		Last Modified: Thu, 23 May 2024 01:33:56 GMT  
		Size: 12.2 MB (12218593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3c627c22003e7e917c7d7078f5f3d498d74a2456d8d8a3be6c7e8fe33f8bc1`  
		Last Modified: Thu, 23 May 2024 01:33:55 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8076064cc4958105c57ec9674268ac24e78c4928f18874eb6585d57ed5f279ff`  
		Last Modified: Thu, 23 May 2024 01:33:56 GMT  
		Size: 3.1 MB (3081150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f129a9195015579a2696cb4a4f1fdeeefea2d97110742388cb39a207ad1823fc`  
		Last Modified: Wed, 29 May 2024 22:01:40 GMT  
		Size: 4.2 MB (4172700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:9cf5dd647ef3595b861d988d75c1d9ad765ce3d306dcaa283d2f90e18ea949d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **654.4 KB (654395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef979041f1d99334057bb0e4fadf16f12272b045ab9d2780a3cc5cbbd2313ec`

```dockerfile
```

-	Layers:
	-	`sha256:c6b9dd1371ef54e1e0abbb9e284ba12f71e2d0a0e04cd66328e8e9d6a5e964f4`  
		Last Modified: Wed, 29 May 2024 22:01:40 GMT  
		Size: 646.1 KB (646062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ac65b4eff29155d786089c8448612caa8207173033aa46b6949885812b2ef3b`  
		Last Modified: Wed, 29 May 2024 22:01:40 GMT  
		Size: 8.3 KB (8333 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:c4e661a5d55caf377fbd2c6a3b648eafde41ff29ce7d969e9b8e20ba40d85de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24106451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d313d633c424b5125bb5fd3d6ef0a7cc1c8ab0ccb6be090c4661af51787e9c13`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:26:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:26:30 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 22 May 2024 12:26:30 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_VERSION=3.10.14
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 22 May 2024 12:26:30 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce85f8c24c4866f123c48cc4731d43c87d5ca38a72bb33fb4fe10f138a16c7f`  
		Last Modified: Thu, 23 May 2024 01:21:51 GMT  
		Size: 465.6 KB (465559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56ee77c1179b2cc883ccf7e613a9867f869ac06059094ea793d87e00bf26d33`  
		Last Modified: Thu, 23 May 2024 01:22:37 GMT  
		Size: 12.3 MB (12300017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d9af7c1a7eec3704d97fb2b447fec4aa66f52c3f78e60a1d57a11b4d789788`  
		Last Modified: Thu, 23 May 2024 01:22:36 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20af32e3b47bc997615753c4b3f48fcd0c620b4fda866848b6807631c564d0d`  
		Last Modified: Thu, 23 May 2024 01:22:36 GMT  
		Size: 3.1 MB (3081128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4427a6fe833a0603eeb5fdbeb3d488e87f4944eb50cecc8deb47b531174f8c8`  
		Last Modified: Thu, 30 May 2024 14:48:16 GMT  
		Size: 4.2 MB (4172731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:7fa7c649fe5bcddd38f38bf3f1b93d55b5c15f4c28ca5d39b02e1f2d545d3ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **654.8 KB (654762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c3117a63fac71d03a36d8eea66a5eae4df3d71df0ef28464010fc68e12225da`

```dockerfile
```

-	Layers:
	-	`sha256:90e545eeda4df8d7df47dfcc829dc275550faa44811118076f9af906d269409f`  
		Last Modified: Thu, 30 May 2024 14:48:16 GMT  
		Size: 646.1 KB (646118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15843e5f9906a33dba3ff0cebb716338aa7240336212ebc241ae7ea3b2387152`  
		Last Modified: Thu, 30 May 2024 14:48:15 GMT  
		Size: 8.6 KB (8644 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-alpine3.20` - linux; s390x

```console
$ docker pull hylang@sha256:e3411790d93df15930b1b60e7c5d11492ca3f4817058f94fe61ceb6ce0f31fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.7 MB (23673533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ede53095a887b862514d583aa2058e5a8f75f0bb5c8484b8df6684233804714`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 12:26:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 May 2024 12:26:30 GMT
ENV LANG=C.UTF-8
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 22 May 2024 12:26:30 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_VERSION=3.10.14
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Wed, 22 May 2024 12:26:30 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Wed, 22 May 2024 12:26:30 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Wed, 22 May 2024 12:26:30 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54731744988f9706a5f3a112bf8ec682a61504506e23cc6c16a1b475a945b5b0`  
		Last Modified: Thu, 23 May 2024 00:50:28 GMT  
		Size: 464.2 KB (464183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdbad05f1b5c599c332fbeab607a682adb78279f2f92578292846f5ae0f751a`  
		Last Modified: Thu, 23 May 2024 00:51:13 GMT  
		Size: 12.5 MB (12495044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f923d443ff89e8223c1965a57a1b400dd09b14aba712fc93debfb9580cd02a`  
		Last Modified: Thu, 23 May 2024 00:51:12 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5146a7038c74afb9fbb326b259fabc682c1d85d356913fc9a9f8ed445eb1d6df`  
		Last Modified: Thu, 23 May 2024 00:51:12 GMT  
		Size: 3.1 MB (3081110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c683618bfa4d048f6da4e3748866b5d7ac8b8afbb173817f935f0e0476d7218b`  
		Last Modified: Thu, 30 May 2024 00:53:08 GMT  
		Size: 4.2 MB (4172612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:d40799a7c252e8e193e43ec6a363c0c2e4ec78abf40be1cf9ec61b85464ba2cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **652.4 KB (652440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd09912c3c0a453d76bd6063dc68e2272172e6245507e2d707feda086ccbc44d`

```dockerfile
```

-	Layers:
	-	`sha256:3a2585b4f5115c8568476aa2e7a94d11c43e1876e0785ed7e99181407ce7d3e3`  
		Last Modified: Thu, 30 May 2024 00:53:08 GMT  
		Size: 644.1 KB (644108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cbd28fb1e8e3c2fb5ad9104114277369a45db9f581c0d6a7cb6ba5ae8f3227c`  
		Last Modified: Thu, 30 May 2024 00:53:08 GMT  
		Size: 8.3 KB (8332 bytes)  
		MIME: application/vnd.in-toto+json
