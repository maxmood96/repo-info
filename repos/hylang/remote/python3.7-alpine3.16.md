## `hylang:python3.7-alpine3.16`

```console
$ docker pull hylang@sha256:4a0685cb31296b0a68fb64a6c99fce5930f3a1635a6e6da648785c58a19a9275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `hylang:python3.7-alpine3.16` - linux; amd64

```console
$ docker pull hylang@sha256:11de142eeafa26d3c0a0513f397eaacc40458e358580347bca73ff56305a8485
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.3 MB (21267011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232d896752d26e377e668b2c6a2540c79203a292d4f663d1109f18170771523c`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 08:43:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Feb 2023 11:39:06 GMT
ENV LANG=C.UTF-8
# Sat, 11 Feb 2023 11:39:07 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 11 Feb 2023 12:59:56 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Sat, 11 Feb 2023 12:59:56 GMT
ENV PYTHON_VERSION=3.7.16
# Tue, 14 Mar 2023 04:23:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	PROFILE_TASK='-m test.regrtest --pgo 		test_array 		test_base64 		test_binascii 		test_binhex 		test_binop 		test_bytes 		test_c_locale_coercion 		test_class 		test_cmath 		test_codecs 		test_compile 		test_complex 		test_csv 		test_decimal 		test_dict 		test_float 		test_fstring 		test_hashlib 		test_io 		test_iter 		test_json 		test_long 		test_math 		test_memoryview 		test_pickle 		test_re 		test_set 		test_slice 		test_struct 		test_threading 		test_time 		test_traceback 		test_unicode 	'; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Tue, 14 Mar 2023 04:23:06 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 14 Mar 2023 04:23:06 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Tue, 14 Mar 2023 04:23:06 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Tue, 14 Mar 2023 04:23:07 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d5cb0afaf23b8520f1bbcfed521017b4a95f5c01/public/get-pip.py
# Tue, 14 Mar 2023 04:23:07 GMT
ENV PYTHON_GET_PIP_SHA256=394be00f13fa1b9aaa47e911bdb59a09c3b2986472130f30aa0bfaf7f3980637
# Tue, 14 Mar 2023 04:23:13 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 14 Mar 2023 04:23:13 GMT
CMD ["python3"]
# Tue, 14 Mar 2023 04:57:00 GMT
ENV HY_VERSION=0.26.0
# Tue, 14 Mar 2023 04:57:00 GMT
ENV HYRULE_VERSION=0.3.0
# Tue, 14 Mar 2023 04:57:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Tue, 14 Mar 2023 04:57:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d11a95ca1cbf9833c3d90abde41ba7a6b71c9b493f31722176b1540e38fa8e`  
		Last Modified: Sat, 11 Feb 2023 13:09:00 GMT  
		Size: 661.9 KB (661861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf50ada638d4a2f8638c13eab1a080bca98c79e679e9f4564b15a19531909707`  
		Last Modified: Tue, 14 Mar 2023 04:32:35 GMT  
		Size: 11.2 MB (11159902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1230a89ad53c659192f8049071f7bd26c69c23def06044d7b3b4adca0deb89d4`  
		Last Modified: Tue, 14 Mar 2023 04:32:33 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50df2edac2b9ddb59f68d3cc35151221a7db661cf9ee6535488b4cb309293339`  
		Last Modified: Tue, 14 Mar 2023 04:32:34 GMT  
		Size: 2.9 MB (2881818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8ed9aa41639da0502c4d851552a98b2dc898e96c0c4503bb53a7b357ea4d73`  
		Last Modified: Tue, 14 Mar 2023 05:05:33 GMT  
		Size: 3.8 MB (3755438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.7-alpine3.16` - linux; arm variant v6

```console
$ docker pull hylang@sha256:c1d1ad376b7c6d8a743f8fca9e5fd74f63154a7d9f66d4c348686bce7c6b45f0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20671171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfafcdc9abf1ce6251d7ebd5e27f89791f797bed2320c27efdd71f42cb435fae`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 13 Mar 2023 16:12:48 GMT
ADD file:be37ec4af7b6db1fa6f84ab2c33fc04aaba5914eb2ac433a417e619fed27c5b4 in / 
# Mon, 13 Mar 2023 16:12:48 GMT
CMD ["/bin/sh"]
# Mon, 13 Mar 2023 23:12:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 13 Mar 2023 23:12:30 GMT
ENV LANG=C.UTF-8
# Mon, 13 Mar 2023 23:12:32 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 14 Mar 2023 00:45:22 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Tue, 14 Mar 2023 00:45:22 GMT
ENV PYTHON_VERSION=3.7.16
# Tue, 14 Mar 2023 00:53:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="-Wl,--strip-all"; 	PROFILE_TASK='-m test.regrtest --pgo 		test_array 		test_base64 		test_binascii 		test_binhex 		test_binop 		test_bytes 		test_c_locale_coercion 		test_class 		test_cmath 		test_codecs 		test_compile 		test_complex 		test_csv 		test_decimal 		test_dict 		test_float 		test_fstring 		test_hashlib 		test_io 		test_iter 		test_json 		test_long 		test_math 		test_memoryview 		test_pickle 		test_re 		test_set 		test_slice 		test_struct 		test_threading 		test_time 		test_traceback 		test_unicode 	'; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Tue, 14 Mar 2023 00:53:14 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 14 Mar 2023 00:53:14 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Tue, 14 Mar 2023 00:53:14 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Tue, 14 Mar 2023 00:53:15 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d5cb0afaf23b8520f1bbcfed521017b4a95f5c01/public/get-pip.py
# Tue, 14 Mar 2023 00:53:15 GMT
ENV PYTHON_GET_PIP_SHA256=394be00f13fa1b9aaa47e911bdb59a09c3b2986472130f30aa0bfaf7f3980637
# Tue, 14 Mar 2023 00:53:21 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 14 Mar 2023 00:53:21 GMT
CMD ["python3"]
# Tue, 14 Mar 2023 03:35:40 GMT
ENV HY_VERSION=0.26.0
# Tue, 14 Mar 2023 03:35:40 GMT
ENV HYRULE_VERSION=0.3.0
# Tue, 14 Mar 2023 03:35:58 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Tue, 14 Mar 2023 03:35:58 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c35ac6bda1fd9456dc61d44052491ecd935dcde4eb6088d66765ca8c6b57cb7d`  
		Last Modified: Fri, 10 Feb 2023 20:50:40 GMT  
		Size: 2.6 MB (2616778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc1309a5f014ba861663c27c1590c426da913481a144ed22dcf128aa0c9324d6`  
		Last Modified: Tue, 14 Mar 2023 00:55:22 GMT  
		Size: 666.4 KB (666377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffd3bd2fb05871d7a4ad6f32b20afe967b2a30fa00d6b4cce5cbf88df5ec9def`  
		Last Modified: Tue, 14 Mar 2023 00:58:11 GMT  
		Size: 10.8 MB (10750587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e85584c37d5a9e60da2a5ec8a11547fd15754d3e98d9ef68c8b3cbab97051e4`  
		Last Modified: Tue, 14 Mar 2023 00:58:08 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5deb10db1fdce1ca38a6832741d536b0d31c49c3e0d6c4465ad29cacd0936b06`  
		Last Modified: Tue, 14 Mar 2023 00:58:09 GMT  
		Size: 2.9 MB (2881727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06014eeb702c551861c0cb2d6addb47aa94a3e4b6843bec3babaace26eea53ab`  
		Last Modified: Tue, 14 Mar 2023 03:43:00 GMT  
		Size: 3.8 MB (3755471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.7-alpine3.16` - linux; arm variant v7

```console
$ docker pull hylang@sha256:26f9f4d5efce1c251f001037f4db6d1fa73af71e1f7502d902d81eb2683ae3ca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.0 MB (20015755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3cf0c742470b2beefdd4f67e65b33e512493d377be52b952b8d52398f872bff`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 10 Feb 2023 21:51:37 GMT
ADD file:193f48d48ed2e90a0e81663757e372f59806151c17e82113f03443db0ef723c3 in / 
# Fri, 10 Feb 2023 21:51:37 GMT
CMD ["/bin/sh"]
# Sat, 25 Feb 2023 01:23:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 Feb 2023 01:23:36 GMT
ENV LANG=C.UTF-8
# Sat, 25 Feb 2023 01:23:38 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 25 Feb 2023 05:22:21 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Sat, 25 Feb 2023 05:22:21 GMT
ENV PYTHON_VERSION=3.7.16
# Sat, 25 Feb 2023 05:30:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="-Wl,--strip-all"; 	PROFILE_TASK='-m test.regrtest --pgo 		test_array 		test_base64 		test_binascii 		test_binhex 		test_binop 		test_bytes 		test_c_locale_coercion 		test_class 		test_cmath 		test_codecs 		test_compile 		test_complex 		test_csv 		test_decimal 		test_dict 		test_float 		test_fstring 		test_hashlib 		test_io 		test_iter 		test_json 		test_long 		test_math 		test_memoryview 		test_pickle 		test_re 		test_set 		test_slice 		test_struct 		test_threading 		test_time 		test_traceback 		test_unicode 	'; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 25 Feb 2023 05:30:32 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 25 Feb 2023 05:30:32 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Sat, 25 Feb 2023 05:30:32 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Sat, 25 Feb 2023 05:30:32 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d5cb0afaf23b8520f1bbcfed521017b4a95f5c01/public/get-pip.py
# Sat, 25 Feb 2023 05:30:32 GMT
ENV PYTHON_GET_PIP_SHA256=394be00f13fa1b9aaa47e911bdb59a09c3b2986472130f30aa0bfaf7f3980637
# Sat, 25 Feb 2023 05:30:38 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Sat, 25 Feb 2023 05:30:38 GMT
CMD ["python3"]
# Sat, 25 Feb 2023 06:53:58 GMT
ENV HY_VERSION=0.26.0
# Sat, 25 Feb 2023 06:53:58 GMT
ENV HYRULE_VERSION=0.3.0
# Sat, 25 Feb 2023 06:54:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Sat, 25 Feb 2023 06:54:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:beefe5ad637c7db32e6afc68103fc4e779630219979216a625338ab55f7d191c`  
		Last Modified: Fri, 10 Feb 2023 21:52:51 GMT  
		Size: 2.4 MB (2420494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5fc002b62c4f1166cfc51c7ee1b46bc695c38300e30f5b6f732f94e5a35909`  
		Last Modified: Sat, 25 Feb 2023 05:36:20 GMT  
		Size: 659.4 KB (659390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2730d863cd36d29e0d8e4231a1611fca7235c33832e14fbb7526900d6eb03a86`  
		Last Modified: Sat, 25 Feb 2023 05:44:05 GMT  
		Size: 10.3 MB (10298251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8e77bf69f876e079f31f01d4fb5514a87ee5b2055ae3c32e202c33330d7239`  
		Last Modified: Sat, 25 Feb 2023 05:44:04 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40230cf7931387c24f12dbce485292a7df4737c889cec8eb32485116d4be7b92`  
		Last Modified: Sat, 25 Feb 2023 05:44:05 GMT  
		Size: 2.9 MB (2881831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144a78aa13c6d31aadfcad820b07c2f03e1cad18645bdfa62e65492a5b852d63`  
		Last Modified: Sat, 25 Feb 2023 07:06:47 GMT  
		Size: 3.8 MB (3755561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.7-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:2adefab99de7c9da982cd94365c0e3818394806caa999a9a38cde79756111474
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21230904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a31db87b1a0bfe5700dc04f68b19d3b2b800279f5335be3a15cd42b32ca45e`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:13 GMT
ADD file:738e640812bf6089767190a2976ceffc11f3e809be3e2b1ebb43c85ad3199fba in / 
# Fri, 10 Feb 2023 21:24:13 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 03:34:25 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Feb 2023 03:34:25 GMT
ENV LANG=C.UTF-8
# Sat, 11 Feb 2023 03:34:26 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 11 Feb 2023 04:53:36 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Sat, 11 Feb 2023 04:53:37 GMT
ENV PYTHON_VERSION=3.7.16
# Tue, 14 Mar 2023 04:44:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	PROFILE_TASK='-m test.regrtest --pgo 		test_array 		test_base64 		test_binascii 		test_binhex 		test_binop 		test_bytes 		test_c_locale_coercion 		test_class 		test_cmath 		test_codecs 		test_compile 		test_complex 		test_csv 		test_decimal 		test_dict 		test_float 		test_fstring 		test_hashlib 		test_io 		test_iter 		test_json 		test_long 		test_math 		test_memoryview 		test_pickle 		test_re 		test_set 		test_slice 		test_struct 		test_threading 		test_time 		test_traceback 		test_unicode 	'; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Tue, 14 Mar 2023 04:44:03 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 14 Mar 2023 04:44:03 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Tue, 14 Mar 2023 04:44:03 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Tue, 14 Mar 2023 04:44:03 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d5cb0afaf23b8520f1bbcfed521017b4a95f5c01/public/get-pip.py
# Tue, 14 Mar 2023 04:44:03 GMT
ENV PYTHON_GET_PIP_SHA256=394be00f13fa1b9aaa47e911bdb59a09c3b2986472130f30aa0bfaf7f3980637
# Tue, 14 Mar 2023 04:44:09 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 14 Mar 2023 04:44:09 GMT
CMD ["python3"]
# Tue, 14 Mar 2023 05:24:10 GMT
ENV HY_VERSION=0.26.0
# Tue, 14 Mar 2023 05:24:10 GMT
ENV HYRULE_VERSION=0.3.0
# Tue, 14 Mar 2023 05:24:24 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Tue, 14 Mar 2023 05:24:24 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3760b48202b3e349986edb6fe5dd93cd003726b7c345d51f6fc4ace1b46fc2ba`  
		Last Modified: Fri, 10 Feb 2023 21:24:52 GMT  
		Size: 2.7 MB (2709502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6bfbf2be34530311efb325a41c8edbfd877067f2984a9946627a1b03fd61b58`  
		Last Modified: Sat, 11 Feb 2023 05:02:22 GMT  
		Size: 663.1 KB (663125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d144ca6e413ec847e9991818c943fe457b33bb021041a6adb6f04c5caf82a3`  
		Last Modified: Tue, 14 Mar 2023 04:53:31 GMT  
		Size: 11.2 MB (11220659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d12181cad146b9d4263a163967344392922091dd7db79ab4c71412e5e40228`  
		Last Modified: Tue, 14 Mar 2023 04:53:30 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a2cfbb318fe20ac7700e7514a69af1b920bf8753b04deb9a769571a58b3b953`  
		Last Modified: Tue, 14 Mar 2023 04:53:31 GMT  
		Size: 2.9 MB (2881833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78d4daba054c98395c2c043e7d1e68ea3ce4efc2fe0d4128c7b4daaecc6c2c5`  
		Last Modified: Tue, 14 Mar 2023 05:33:04 GMT  
		Size: 3.8 MB (3755557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.7-alpine3.16` - linux; 386

```console
$ docker pull hylang@sha256:f01625764a4c64271e6e9e2bc2b85e72fe4dd569a9a8332da0324ef48fad0b45
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.4 MB (21445628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ec948f99baba99faf3340028d903cd4958862be7426aea9035d499814a39bb3`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:29 GMT
ADD file:59ac1f8f33f9b9727892b7e45b33f54ef3c20d9d876c49d6a4c057641821d68f in / 
# Fri, 10 Feb 2023 21:24:29 GMT
CMD ["/bin/sh"]
# Sat, 25 Feb 2023 01:14:58 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 25 Feb 2023 01:14:58 GMT
ENV LANG=C.UTF-8
# Sat, 25 Feb 2023 01:15:00 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 25 Feb 2023 06:27:25 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Sat, 25 Feb 2023 06:27:25 GMT
ENV PYTHON_VERSION=3.7.16
# Sat, 25 Feb 2023 06:36:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="-Wl,--strip-all"; 	PROFILE_TASK='-m test.regrtest --pgo 		test_array 		test_base64 		test_binascii 		test_binhex 		test_binop 		test_bytes 		test_c_locale_coercion 		test_class 		test_cmath 		test_codecs 		test_compile 		test_complex 		test_csv 		test_decimal 		test_dict 		test_float 		test_fstring 		test_hashlib 		test_io 		test_iter 		test_json 		test_long 		test_math 		test_memoryview 		test_pickle 		test_re 		test_set 		test_slice 		test_struct 		test_threading 		test_time 		test_traceback 		test_unicode 	'; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 25 Feb 2023 06:36:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 25 Feb 2023 06:36:55 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Sat, 25 Feb 2023 06:36:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Sat, 25 Feb 2023 06:36:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d5cb0afaf23b8520f1bbcfed521017b4a95f5c01/public/get-pip.py
# Sat, 25 Feb 2023 06:36:55 GMT
ENV PYTHON_GET_PIP_SHA256=394be00f13fa1b9aaa47e911bdb59a09c3b2986472130f30aa0bfaf7f3980637
# Sat, 25 Feb 2023 06:37:02 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Sat, 25 Feb 2023 06:37:02 GMT
CMD ["python3"]
# Sat, 25 Feb 2023 07:13:48 GMT
ENV HY_VERSION=0.26.0
# Sat, 25 Feb 2023 07:13:49 GMT
ENV HYRULE_VERSION=0.3.0
# Sat, 25 Feb 2023 07:14:08 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Sat, 25 Feb 2023 07:14:08 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0987f51cd58a7d03bc7d6ff0a3a0a843c1a3fefcd41e3c8adc3999ddde7441e8`  
		Last Modified: Fri, 10 Feb 2023 21:25:30 GMT  
		Size: 2.8 MB (2810653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b46b4ed1a9500772676da09f03658a766a985faeb849b4cfb302b802a11d3c`  
		Last Modified: Sat, 25 Feb 2023 06:42:31 GMT  
		Size: 669.9 KB (669885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13be2d1fbff9d04b3b2fa077fb32d765480823c3469c9dc780ab055e431bc2e5`  
		Last Modified: Sat, 25 Feb 2023 06:50:23 GMT  
		Size: 11.3 MB (11327541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfefc9bad2b20b9d52afbc1c6fe05ab3982e446b524a579c04dc9a87db4920a`  
		Last Modified: Sat, 25 Feb 2023 06:50:21 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa9663c973778d91db6f9fcb7e46061fdd7b8576efca83436d2190b0c7dc050`  
		Last Modified: Sat, 25 Feb 2023 06:50:22 GMT  
		Size: 2.9 MB (2881840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a471a8a089ee79b3aa28e121b5a896d00d1daa94fbf779033ffa551293293a60`  
		Last Modified: Sat, 25 Feb 2023 07:29:39 GMT  
		Size: 3.8 MB (3755481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.7-alpine3.16` - linux; ppc64le

```console
$ docker pull hylang@sha256:ab62215870e3be1d40dcf1c0915cb4f8d2bf3dfb6dfef37f570391fac4d3e8f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.5 MB (21547298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe5b0ff2956f4ba5775983bf67437ccf0412baf906235b5f68ae65e96d7f5a21`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 10 Feb 2023 21:20:44 GMT
ADD file:d9267e5b7618ca1c5ac918cde29e6967fae2132ab0672112ee2c6604e96a0b66 in / 
# Fri, 10 Feb 2023 21:20:45 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 01:09:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Feb 2023 01:09:03 GMT
ENV LANG=C.UTF-8
# Sat, 11 Feb 2023 01:09:06 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 11 Feb 2023 04:01:11 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Sat, 11 Feb 2023 04:01:11 GMT
ENV PYTHON_VERSION=3.7.16
# Sat, 11 Feb 2023 04:16:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="-Wl,--strip-all"; 	PROFILE_TASK='-m test.regrtest --pgo 		test_array 		test_base64 		test_binascii 		test_binhex 		test_binop 		test_bytes 		test_c_locale_coercion 		test_class 		test_cmath 		test_codecs 		test_compile 		test_complex 		test_csv 		test_decimal 		test_dict 		test_float 		test_fstring 		test_hashlib 		test_io 		test_iter 		test_json 		test_long 		test_math 		test_memoryview 		test_pickle 		test_re 		test_set 		test_slice 		test_struct 		test_threading 		test_time 		test_traceback 		test_unicode 	'; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Sat, 11 Feb 2023 04:16:06 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Sat, 11 Feb 2023 04:16:07 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Sat, 11 Feb 2023 04:16:07 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Fri, 24 Feb 2023 23:26:45 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d5cb0afaf23b8520f1bbcfed521017b4a95f5c01/public/get-pip.py
# Fri, 24 Feb 2023 23:26:45 GMT
ENV PYTHON_GET_PIP_SHA256=394be00f13fa1b9aaa47e911bdb59a09c3b2986472130f30aa0bfaf7f3980637
# Fri, 24 Feb 2023 23:26:58 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Fri, 24 Feb 2023 23:26:58 GMT
CMD ["python3"]
# Sat, 25 Feb 2023 00:02:27 GMT
ENV HY_VERSION=0.26.0
# Sat, 25 Feb 2023 00:02:28 GMT
ENV HYRULE_VERSION=0.3.0
# Sat, 25 Feb 2023 00:03:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Sat, 25 Feb 2023 00:03:17 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e3b9153081a195877a8587137034c9b223749c582ea32371419055f7d77c97ba`  
		Last Modified: Fri, 10 Feb 2023 21:21:53 GMT  
		Size: 2.8 MB (2804628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48a86f30c4238772b9bbdc0285d11cbe1774498512ad8bafccaedcbf67132251`  
		Last Modified: Sat, 11 Feb 2023 04:20:17 GMT  
		Size: 670.3 KB (670300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cdbcf4ac56ca4e5236e30cb0c402c83cccad3604645de66f2f6716246e6b87`  
		Last Modified: Sat, 11 Feb 2023 04:24:17 GMT  
		Size: 11.4 MB (11434274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00949f8ec69a35394b76c22a5f25fd31aa1d114af0292bfaabe5c6b2eb74176b`  
		Last Modified: Sat, 11 Feb 2023 04:24:14 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948d65432424c2597b3d88d4e04407c2322542a4000c8d3c6d2473e63247eb7b`  
		Last Modified: Fri, 24 Feb 2023 23:36:09 GMT  
		Size: 2.9 MB (2881843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8679a011110771df4ef5fad148ef38b24c13fa969590637a444638bb21d96885`  
		Last Modified: Sat, 25 Feb 2023 00:12:48 GMT  
		Size: 3.8 MB (3756023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.7-alpine3.16` - linux; s390x

```console
$ docker pull hylang@sha256:86842b142524eb4693aa135f4bd2142c59040039c277373b7cb5b5e45a45e9e2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21054795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:117f422e266cd7405a2db5d23b37b5d6b98a686f2879d84baa10b6fed9817386`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 10 Feb 2023 21:41:31 GMT
ADD file:17af250b49631cf2acf655c85df90977eddab4c9afd67bda3c577db5200364f1 in / 
# Fri, 10 Feb 2023 21:41:32 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 06:07:33 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Feb 2023 06:07:33 GMT
ENV LANG=C.UTF-8
# Sat, 11 Feb 2023 06:07:34 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Sat, 11 Feb 2023 10:35:14 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Sat, 11 Feb 2023 10:35:14 GMT
ENV PYTHON_VERSION=3.7.16
# Tue, 14 Mar 2023 03:17:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	PROFILE_TASK='-m test.regrtest --pgo 		test_array 		test_base64 		test_binascii 		test_binhex 		test_binop 		test_bytes 		test_c_locale_coercion 		test_class 		test_cmath 		test_codecs 		test_compile 		test_complex 		test_csv 		test_decimal 		test_dict 		test_float 		test_fstring 		test_hashlib 		test_io 		test_iter 		test_json 		test_long 		test_math 		test_memoryview 		test_pickle 		test_re 		test_set 		test_slice 		test_struct 		test_threading 		test_time 		test_traceback 		test_unicode 	'; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Tue, 14 Mar 2023 03:17:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 14 Mar 2023 03:17:55 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Tue, 14 Mar 2023 03:17:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Tue, 14 Mar 2023 03:17:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d5cb0afaf23b8520f1bbcfed521017b4a95f5c01/public/get-pip.py
# Tue, 14 Mar 2023 03:17:55 GMT
ENV PYTHON_GET_PIP_SHA256=394be00f13fa1b9aaa47e911bdb59a09c3b2986472130f30aa0bfaf7f3980637
# Tue, 14 Mar 2023 03:18:01 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 14 Mar 2023 03:18:01 GMT
CMD ["python3"]
# Tue, 14 Mar 2023 03:45:34 GMT
ENV HY_VERSION=0.26.0
# Tue, 14 Mar 2023 03:45:34 GMT
ENV HYRULE_VERSION=0.3.0
# Tue, 14 Mar 2023 03:45:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Tue, 14 Mar 2023 03:45:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:667d93a24f321610e24486f3148545191f113ab9ab2444804087dd65ebbda9ed`  
		Last Modified: Fri, 10 Feb 2023 21:42:26 GMT  
		Size: 2.6 MB (2593581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2adb0ada542e535816922b2b2d2d4ff2af513d5807aef216c21245e5a6dc576d`  
		Last Modified: Sat, 11 Feb 2023 10:45:10 GMT  
		Size: 666.7 KB (666653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77bb0a887eb2d51d39384277676557ab3d09800683ef5c9ce3c1675de0fb1965`  
		Last Modified: Tue, 14 Mar 2023 03:25:25 GMT  
		Size: 11.2 MB (11156918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ef2dc2bc9a2b7070a0d15042b7ed23f9ab8ebe2b2ca8a2efe7ac8bbbfed986`  
		Last Modified: Tue, 14 Mar 2023 03:25:24 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c98fe7ab92304780a00986bfcc1d4addb4a324336c2e99f50a52ff23e0078e3`  
		Last Modified: Tue, 14 Mar 2023 03:25:25 GMT  
		Size: 2.9 MB (2881812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff309eb5e97fbbfa61c9c60b54f4f04e809508f5749d4b0e6a6a1714d2cc716`  
		Last Modified: Tue, 14 Mar 2023 03:52:13 GMT  
		Size: 3.8 MB (3755603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
