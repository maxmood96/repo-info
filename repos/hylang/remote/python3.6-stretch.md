## `hylang:python3.6-stretch`

```console
$ docker pull hylang@sha256:d37ab06f51912e943ab9d1cea0354e714af4701fc51244f80b67ae88f5ab3a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `hylang:python3.6-stretch` - linux; amd64

```console
$ docker pull hylang@sha256:b4fc4888cab598688f3c0fb681b628281787a27ca8a0d3078c657512fa66d480
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39928409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2606aeb06e1418c54e527b22b53412fcd32407e60b10734c7aa92247ae056f81`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 10 Apr 2021 01:21:54 GMT
ADD file:70cd6967491943999563ddd3ab9abae33791ac320cdc846dc57503cc44f25600 in / 
# Sat, 10 Apr 2021 01:21:54 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 16:18:09 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 16:18:10 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 16:18:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 16:18:17 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Sat, 10 Apr 2021 16:45:22 GMT
ENV PYTHON_VERSION=3.6.13
# Sat, 10 Apr 2021 16:51:20 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Sat, 10 Apr 2021 16:51:21 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 10 Apr 2021 16:51:21 GMT
ENV PYTHON_PIP_VERSION=21.0.1
# Sat, 10 Apr 2021 16:51:21 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/29f37dbe6b3842ccd52d61816a3044173962ebeb/public/get-pip.py
# Sat, 10 Apr 2021 16:51:22 GMT
ENV PYTHON_GET_PIP_SHA256=e03eb8a33d3b441ff484c56a436ff10680479d4bd14e59268e67977ed40904de
# Sat, 10 Apr 2021 16:51:34 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 10 Apr 2021 16:51:34 GMT
CMD ["python3"]
# Sun, 11 Apr 2021 06:25:44 GMT
ENV HY_VERSION=0.20.0
# Sun, 11 Apr 2021 06:25:49 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sun, 11 Apr 2021 06:25:49 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:62deabe7a6db312ed773ccd640cd7cfbf51c22bf466886345684558f1036e358`  
		Last Modified: Sat, 10 Apr 2021 01:28:26 GMT  
		Size: 22.5 MB (22528265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd06fdebd139172033d05bf8a1aa0454df8006ae76fc70c23153739c61d83492`  
		Last Modified: Sat, 10 Apr 2021 16:57:14 GMT  
		Size: 2.5 MB (2506234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca4b7dfdcf15617c8b3111fad82e3258f4d6665a9c93a88004c9b72562465e5`  
		Last Modified: Sat, 10 Apr 2021 16:58:16 GMT  
		Size: 9.6 MB (9632368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02f10217a3ffed175dd11e4ce268dcfcf70e5f8b2cb3edfd7d8a6fe4a8382e4`  
		Last Modified: Sat, 10 Apr 2021 16:58:14 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0445e7eeba5e0098cc2778974766868ea4b9699a3650b302e994c6c909719639`  
		Last Modified: Sat, 10 Apr 2021 16:58:15 GMT  
		Size: 2.4 MB (2447588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2e1bc14075ab7877c309fa2c2efc506cd5a76dba0594ce8cf74d24dcbb951f`  
		Last Modified: Sun, 11 Apr 2021 06:29:09 GMT  
		Size: 2.8 MB (2813714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.6-stretch` - linux; arm variant v5

```console
$ docker pull hylang@sha256:41f79257ef900f0271ddae02e5db20710b428e05644aaea585f4cb27edf65b58
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37895544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d90889d4eb4f718dfb01c3d1ddb82bf6993777731604285c8195f300b76b3bb`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 10 Apr 2021 00:54:52 GMT
ADD file:39c006de64fb65625581d7e13792f641ab1bbdc3a2adb67238cde929283cf015 in / 
# Sat, 10 Apr 2021 00:54:53 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 10:16:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 10:16:55 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 10:17:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 10:17:15 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Sat, 10 Apr 2021 10:54:32 GMT
ENV PYTHON_VERSION=3.6.13
# Sat, 10 Apr 2021 11:00:21 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Sat, 10 Apr 2021 11:00:26 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 10 Apr 2021 11:00:27 GMT
ENV PYTHON_PIP_VERSION=21.0.1
# Sat, 10 Apr 2021 11:00:28 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/29f37dbe6b3842ccd52d61816a3044173962ebeb/public/get-pip.py
# Sat, 10 Apr 2021 11:00:30 GMT
ENV PYTHON_GET_PIP_SHA256=e03eb8a33d3b441ff484c56a436ff10680479d4bd14e59268e67977ed40904de
# Sat, 10 Apr 2021 11:01:04 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 10 Apr 2021 11:01:05 GMT
CMD ["python3"]
# Sat, 10 Apr 2021 18:05:47 GMT
ENV HY_VERSION=0.20.0
# Sat, 10 Apr 2021 18:06:04 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 10 Apr 2021 18:06:05 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b4b5f7646116314498ac5e39f6c79577d25ed5239430a6d8612327d11d1cc09c`  
		Last Modified: Sat, 10 Apr 2021 01:02:12 GMT  
		Size: 21.2 MB (21203935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8033b4aaec4a8aa43a1a43ff39cb7611b3c544da66ffa5ced3cb961fea40a08`  
		Last Modified: Sat, 10 Apr 2021 11:04:12 GMT  
		Size: 2.2 MB (2230999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ad8c95d3b072a36cec9f41a9c31768342882d7ab7676093451e3d2c61e92b8`  
		Last Modified: Sat, 10 Apr 2021 11:05:07 GMT  
		Size: 9.2 MB (9198791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e06966aead3aeb226bbf3d2cede161ea63807e67b673103094f5d2b7630ea75`  
		Last Modified: Sat, 10 Apr 2021 11:05:03 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b859b473fdfe74d5f332af4744beabdc66dd8ac43b40b854065576a8eee6d025`  
		Last Modified: Sat, 10 Apr 2021 11:05:04 GMT  
		Size: 2.4 MB (2447322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c4ab7afbb47d99c3411b64271aa4341b1e338e87dd162cd859469cf9c50c72`  
		Last Modified: Sat, 10 Apr 2021 18:07:34 GMT  
		Size: 2.8 MB (2814256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.6-stretch` - linux; arm variant v7

```console
$ docker pull hylang@sha256:66b2b819a76cd5cede0d0baa23a353066b5e05e909483277e69dc0e937d84da7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35663996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a808a0add22186886556ff0f61d3409c0248b877b022c10764618f41feffca5`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 10 Apr 2021 01:03:06 GMT
ADD file:52c199ce651b807d24bc90d10a436833911230c0a2e5a5e3bc404e8f60acf01f in / 
# Sat, 10 Apr 2021 01:03:08 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 05:21:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 05:21:25 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 05:21:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 05:21:51 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Sat, 10 Apr 2021 05:47:47 GMT
ENV PYTHON_VERSION=3.6.13
# Sat, 10 Apr 2021 05:56:15 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Sat, 10 Apr 2021 05:56:19 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 10 Apr 2021 05:56:20 GMT
ENV PYTHON_PIP_VERSION=21.0.1
# Sat, 10 Apr 2021 05:56:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/29f37dbe6b3842ccd52d61816a3044173962ebeb/public/get-pip.py
# Sat, 10 Apr 2021 05:56:21 GMT
ENV PYTHON_GET_PIP_SHA256=e03eb8a33d3b441ff484c56a436ff10680479d4bd14e59268e67977ed40904de
# Sat, 10 Apr 2021 05:56:53 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 10 Apr 2021 05:56:55 GMT
CMD ["python3"]
# Sat, 10 Apr 2021 18:29:13 GMT
ENV HY_VERSION=0.20.0
# Sat, 10 Apr 2021 18:29:26 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 10 Apr 2021 18:29:28 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:164ab14e0a3227bab5f842df5b955bd3fd592e0d78c5f19d2b1084d61e259f3a`  
		Last Modified: Sat, 10 Apr 2021 01:10:32 GMT  
		Size: 19.3 MB (19315172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f9a26e9373cea855469cbd3dc49f5b5351a8a506776585f97aac6b721aea6a`  
		Last Modified: Sat, 10 Apr 2021 05:59:50 GMT  
		Size: 2.2 MB (2152098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a805d46d7f2b4f231ed3ef80d5887cd4ee30acb9817952125c8b31aa312ed6a6`  
		Last Modified: Sat, 10 Apr 2021 06:00:22 GMT  
		Size: 8.9 MB (8935022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ddc4af2e1894084a2323281b93fb7e4ac92f9b40657526bbe286d881ae0231`  
		Last Modified: Sat, 10 Apr 2021 06:00:19 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e7891727557f681f65a75c69969894b44df97dc6fa4ef290ebc2a6f3d829774`  
		Last Modified: Sat, 10 Apr 2021 06:00:20 GMT  
		Size: 2.4 MB (2447381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f613d9ed4bed01f5539334784a02c4f2eeb9cee864719fcb71c2b68c478995`  
		Last Modified: Sat, 10 Apr 2021 18:31:57 GMT  
		Size: 2.8 MB (2814082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.6-stretch` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:8f34c88b31ae3c5281eb0e698bb542e7c7ec571b6e8b7b6a9c7fa77a0d4cd751
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37226992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638bb304d1e4cdc4fadd25a0df91ea490a8e03f57b2dff33f97d140e3d077ba0`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 10 Apr 2021 00:44:13 GMT
ADD file:a74d7856e70f2e18d2509edd9f0527254a69e9d1347715149c772a0d4ca7d509 in / 
# Sat, 10 Apr 2021 00:44:14 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 14:16:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 14:16:57 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 14:17:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 14:17:15 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Sat, 10 Apr 2021 14:57:53 GMT
ENV PYTHON_VERSION=3.6.13
# Sat, 10 Apr 2021 15:06:22 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Sat, 10 Apr 2021 15:06:26 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 10 Apr 2021 15:06:27 GMT
ENV PYTHON_PIP_VERSION=21.0.1
# Sat, 10 Apr 2021 15:06:28 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/29f37dbe6b3842ccd52d61816a3044173962ebeb/public/get-pip.py
# Sat, 10 Apr 2021 15:06:29 GMT
ENV PYTHON_GET_PIP_SHA256=e03eb8a33d3b441ff484c56a436ff10680479d4bd14e59268e67977ed40904de
# Sat, 10 Apr 2021 15:06:56 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 10 Apr 2021 15:06:57 GMT
CMD ["python3"]
# Sun, 11 Apr 2021 03:40:13 GMT
ENV HY_VERSION=0.20.0
# Sun, 11 Apr 2021 03:40:27 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sun, 11 Apr 2021 03:40:29 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bc16ed4a30c7b74efb2ba46d7df8a6591a02826832c27a5cf55cc6e06111a5a6`  
		Last Modified: Sat, 10 Apr 2021 00:50:10 GMT  
		Size: 20.4 MB (20389366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5068d35a73e4248211478b1d46b749149921e75f358b24f7cb24f71de53de2`  
		Last Modified: Sat, 10 Apr 2021 15:10:49 GMT  
		Size: 2.2 MB (2215318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da0714982a9f81e0ba9d53d60224507db858b014266cb9952412cf6b9068db0`  
		Last Modified: Sat, 10 Apr 2021 15:11:36 GMT  
		Size: 9.4 MB (9360518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e2ef735ee8e09a4d0b1333498feb01da90f0c94d214fae042f7f9e42d98159`  
		Last Modified: Sat, 10 Apr 2021 15:11:34 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f4a0c44ba4b12278a057d8910ceb99dc96af5c6244a7301fa02ba89015fa6e`  
		Last Modified: Sat, 10 Apr 2021 15:11:35 GMT  
		Size: 2.4 MB (2447246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbdeec8dd17adc99b08372d328b9cd9731acd0054eead220d90ce0807ae16889`  
		Last Modified: Sun, 11 Apr 2021 03:43:39 GMT  
		Size: 2.8 MB (2814304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.6-stretch` - linux; 386

```console
$ docker pull hylang@sha256:18dad8a225fd2e84e4d995e33a99a9c7710d63acdba65c022331a1af99435725
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40641357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95be66b9d19df0dd05084d43cf8c1769c559986da4c8a868cd300c61e48fa8ad`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 10 Apr 2021 00:41:29 GMT
ADD file:9cb229e455510ee74de0debdecc6c327e9bda29ac2126c12d9a19d5ef8227d3a in / 
# Sat, 10 Apr 2021 00:41:29 GMT
CMD ["bash"]
# Sat, 10 Apr 2021 01:58:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 10 Apr 2021 01:58:42 GMT
ENV LANG=C.UTF-8
# Sat, 10 Apr 2021 01:58:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 10 Apr 2021 01:58:50 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Sat, 10 Apr 2021 02:20:15 GMT
ENV PYTHON_VERSION=3.6.13
# Sat, 10 Apr 2021 02:28:20 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Sat, 10 Apr 2021 02:28:22 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 10 Apr 2021 02:28:23 GMT
ENV PYTHON_PIP_VERSION=21.0.1
# Sat, 10 Apr 2021 02:28:23 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/29f37dbe6b3842ccd52d61816a3044173962ebeb/public/get-pip.py
# Sat, 10 Apr 2021 02:28:23 GMT
ENV PYTHON_GET_PIP_SHA256=e03eb8a33d3b441ff484c56a436ff10680479d4bd14e59268e67977ed40904de
# Sat, 10 Apr 2021 02:28:44 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 10 Apr 2021 02:28:45 GMT
CMD ["python3"]
# Sat, 10 Apr 2021 15:45:00 GMT
ENV HY_VERSION=0.20.0
# Sat, 10 Apr 2021 15:45:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 10 Apr 2021 15:45:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b18a2540ebf57cd924b9ebbf39001a2241653243e9ee3af58fa9f77a2644b7ee`  
		Last Modified: Sat, 10 Apr 2021 00:49:18 GMT  
		Size: 23.2 MB (23156271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469c83238ca2d74b674ce034318207d9c08fa74cd860b5d09c8775a36b3bdabe`  
		Last Modified: Sat, 10 Apr 2021 02:36:08 GMT  
		Size: 2.5 MB (2509002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2c6a4a8ea9c5c2361d0b63815c7c250d5075089fb2a8b46599ae86a6df3d8c`  
		Last Modified: Sat, 10 Apr 2021 02:37:05 GMT  
		Size: 9.7 MB (9714724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ac8758ab5a724ae7ab3c736e04df0801487c4e5017809f35cdc218957af568`  
		Last Modified: Sat, 10 Apr 2021 02:37:01 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:786e2286559d6a465d2b4eb1587c48243b9e88a7b99f96369079cd6ad87fb19a`  
		Last Modified: Sat, 10 Apr 2021 02:37:03 GMT  
		Size: 2.4 MB (2447331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b23be2f2f0f12bd43e573baa790c0fcc2df5252d42d8d8bf17578a61fd0a870`  
		Last Modified: Sat, 10 Apr 2021 15:51:59 GMT  
		Size: 2.8 MB (2813787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
