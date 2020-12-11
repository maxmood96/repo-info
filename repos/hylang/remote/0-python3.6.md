## `hylang:0-python3.6`

```console
$ docker pull hylang@sha256:ae1797046def8ca50327bcc660a38e26dc231b5c686ae90ee58121a7583d7e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `hylang:0-python3.6` - linux; amd64

```console
$ docker pull hylang@sha256:57b83c4faad65ec19db3427111f47e88035d0f6f713a767780b3dbe3bf84926e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44769820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b80ffe1bb4525798e26282c56e0009d160cee7c5ab108ff6f49f6bff59fe8e`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:17 GMT
ADD file:d2abb0e4e7ac1773741f51f57d3a0b8ffc7907348842d773f8c341ba17f856d5 in / 
# Tue, 17 Nov 2020 20:21:17 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 13:07:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Nov 2020 13:07:04 GMT
ENV LANG=C.UTF-8
# Wed, 25 Nov 2020 02:39:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 03:10:02 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Wed, 25 Nov 2020 03:52:25 GMT
ENV PYTHON_VERSION=3.6.12
# Wed, 25 Nov 2020 04:00:07 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Wed, 25 Nov 2020 04:00:08 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 03 Dec 2020 22:42:04 GMT
ENV PYTHON_PIP_VERSION=20.3.1
# Thu, 03 Dec 2020 22:42:04 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/91630a4867b1f93ba0a12aa81d0ec4ecc1e7eeb9/get-pip.py
# Thu, 03 Dec 2020 22:42:04 GMT
ENV PYTHON_GET_PIP_SHA256=d48ae68f297cac54db17e4107b800faae0e5210131f9f386c30c0166bf8d81b7
# Thu, 03 Dec 2020 22:42:21 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 03 Dec 2020 22:42:21 GMT
CMD ["python3"]
# Thu, 03 Dec 2020 23:30:50 GMT
ENV HY_VERSION=0.19.0
# Thu, 03 Dec 2020 23:30:56 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 03 Dec 2020 23:30:56 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:852e50cd189dfeb54d97680d9fa6bed21a6d7d18cfb56d6abfe2de9d7f173795`  
		Last Modified: Tue, 17 Nov 2020 20:27:25 GMT  
		Size: 27.1 MB (27105484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334ed303e4ad2f8dc872f2e845d79012ad648eaced444e009ae9a397cc4b4dbb`  
		Last Modified: Wed, 25 Nov 2020 04:26:10 GMT  
		Size: 2.7 MB (2749975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:209dcde762c715ee666cd6492d3e3656ba0ee9fd32ef9b09e43fe80a0c386c36`  
		Last Modified: Wed, 25 Nov 2020 04:27:07 GMT  
		Size: 9.7 MB (9682323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9abeb9ca0990b9fe5016d4ba91f5135c584c2b4cc6a0eb6737c5005ecf2f73d`  
		Last Modified: Wed, 25 Nov 2020 04:27:06 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f750bc3b4393c087fbe6768267aac7cb8677df84233a503c21ae1fd86212abb4`  
		Last Modified: Thu, 03 Dec 2020 22:46:35 GMT  
		Size: 2.4 MB (2424659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9337c5dc1945627361cc97551bc4ad179e37611567555d06ee99c91ee348b3b`  
		Last Modified: Thu, 03 Dec 2020 23:34:23 GMT  
		Size: 2.8 MB (2807147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.6` - linux; arm variant v5

```console
$ docker pull hylang@sha256:84ccb1b0eac96acb5720d48727017b1006cd2b0f2820e127d3d38b8d8509cafc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41901002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5760c17d0b782f2118e6b728e7a86c4e9b94626764d122ccadd782ea04379800`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:49 GMT
ADD file:58ebb3ffaf26d9b7621efba5f109ae9d22832f2f22865cda36604b138cbdb7b8 in / 
# Fri, 11 Dec 2020 02:04:56 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 09:37:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Dec 2020 09:37:41 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 10:32:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 11:01:20 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Fri, 11 Dec 2020 11:48:56 GMT
ENV PYTHON_VERSION=3.6.12
# Fri, 11 Dec 2020 11:59:18 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Fri, 11 Dec 2020 11:59:21 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 11 Dec 2020 11:59:21 GMT
ENV PYTHON_PIP_VERSION=20.3.1
# Fri, 11 Dec 2020 11:59:22 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/91630a4867b1f93ba0a12aa81d0ec4ecc1e7eeb9/get-pip.py
# Fri, 11 Dec 2020 11:59:23 GMT
ENV PYTHON_GET_PIP_SHA256=d48ae68f297cac54db17e4107b800faae0e5210131f9f386c30c0166bf8d81b7
# Fri, 11 Dec 2020 11:59:51 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 11 Dec 2020 11:59:52 GMT
CMD ["python3"]
# Fri, 11 Dec 2020 19:49:40 GMT
ENV HY_VERSION=0.19.0
# Fri, 11 Dec 2020 19:49:54 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Fri, 11 Dec 2020 19:49:56 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8cbd1f790d64c77fcac6c9dbfe4d4c82f0365de9438f1a42b0560dc88f9e6a55`  
		Last Modified: Fri, 11 Dec 2020 02:14:44 GMT  
		Size: 24.8 MB (24843461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27b4d566ef30fb7d8b249e8c3f4dc67d4f4533b1fd094f92eeafd6c135a1ee2`  
		Last Modified: Fri, 11 Dec 2020 12:14:41 GMT  
		Size: 2.4 MB (2449196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b03256fbc92c07bd129973a3d05f9742da840f341fcc3b7847e5bf1f16d6317c`  
		Last Modified: Fri, 11 Dec 2020 12:16:03 GMT  
		Size: 9.4 MB (9376143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1cf4b1f30d85389c270f7c4161564100bf7afd40e9408f41db54bee8a6cb43d`  
		Last Modified: Fri, 11 Dec 2020 12:16:00 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d84ddc56c051c567a54492141f538ca0a3f3e2e533f136dd75a648f94a080db`  
		Last Modified: Fri, 11 Dec 2020 12:16:00 GMT  
		Size: 2.4 MB (2424485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7478d816b0d9ca69d409d6af8ea50df34ee1cb5d945ddf449087cad69769c4`  
		Last Modified: Fri, 11 Dec 2020 19:51:54 GMT  
		Size: 2.8 MB (2807485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.6` - linux; arm variant v7

```console
$ docker pull hylang@sha256:c18743a80540868591ddaf57c50a92865c46669258661bea2bd3f9113f3492aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39252088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1243465b73c2607cb35514793e8f53d7d743b8d69e0a2db356daa0471445256`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 17 Nov 2020 20:21:06 GMT
ADD file:2035658a8d20545ee7b2ab3ee791a371925fca7968ac29435303da24a1378f34 in / 
# Tue, 17 Nov 2020 20:21:10 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 04:10:22 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Nov 2020 04:10:24 GMT
ENV LANG=C.UTF-8
# Wed, 25 Nov 2020 04:09:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 04:36:33 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Wed, 25 Nov 2020 05:28:40 GMT
ENV PYTHON_VERSION=3.6.12
# Wed, 25 Nov 2020 05:38:47 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Wed, 25 Nov 2020 05:38:50 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 03 Dec 2020 22:11:05 GMT
ENV PYTHON_PIP_VERSION=20.3.1
# Thu, 03 Dec 2020 22:11:06 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/91630a4867b1f93ba0a12aa81d0ec4ecc1e7eeb9/get-pip.py
# Thu, 03 Dec 2020 22:11:07 GMT
ENV PYTHON_GET_PIP_SHA256=d48ae68f297cac54db17e4107b800faae0e5210131f9f386c30c0166bf8d81b7
# Thu, 03 Dec 2020 22:11:33 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 03 Dec 2020 22:11:34 GMT
CMD ["python3"]
# Thu, 03 Dec 2020 22:36:21 GMT
ENV HY_VERSION=0.19.0
# Thu, 03 Dec 2020 22:36:31 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 03 Dec 2020 22:36:33 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d5029e4b387017f20ad9f77baf3b81dd41f851d6340363b842a8a1d9786a60a0`  
		Last Modified: Tue, 17 Nov 2020 20:31:46 GMT  
		Size: 22.7 MB (22714186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec03ae065a60d612b08cf275d37676485916d7a2e58f368b3f020874ee7f2e1`  
		Last Modified: Wed, 25 Nov 2020 06:01:25 GMT  
		Size: 2.3 MB (2347460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a531ef3066b6210fbbf6fa705d1fa78bbdaf2f0e96d7e1729aeeaba657ccdd0`  
		Last Modified: Wed, 25 Nov 2020 06:02:56 GMT  
		Size: 9.0 MB (8958325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0954e97f9a60bc403c2ae187dd6c2ec117ca71340fe26b7cc4467ba2770cce`  
		Last Modified: Wed, 25 Nov 2020 06:02:52 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b868bbe6722894ebeec3a49ae62650322433b7f2c8c553b0c0d3cb8a8c08f56e`  
		Last Modified: Thu, 03 Dec 2020 22:17:33 GMT  
		Size: 2.4 MB (2424424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d4546505cbd9feb20a439e9dc97c190e5c39cee6a564b6fccdafa599beac26`  
		Last Modified: Thu, 03 Dec 2020 22:40:08 GMT  
		Size: 2.8 MB (2807459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.6` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:17d208d1f965dd0cb0f497590703532fb2055e42924509341ee5bef1bbbfd865
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43442305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a555590ade9ba654bfbb2026f2844f3f9b3780cb4dc10bc854602e6b557d5d74`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:31 GMT
ADD file:a70d8c01f8f04f36038968567af779883f3b5ba3147b662b7d170d80418bc23c in / 
# Tue, 17 Nov 2020 20:23:32 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 06:36:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Nov 2020 06:36:54 GMT
ENV LANG=C.UTF-8
# Wed, 25 Nov 2020 04:26:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 04:53:05 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Wed, 25 Nov 2020 05:49:29 GMT
ENV PYTHON_VERSION=3.6.12
# Wed, 25 Nov 2020 05:59:46 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Wed, 25 Nov 2020 05:59:49 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 03 Dec 2020 23:08:11 GMT
ENV PYTHON_PIP_VERSION=20.3.1
# Thu, 03 Dec 2020 23:08:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/91630a4867b1f93ba0a12aa81d0ec4ecc1e7eeb9/get-pip.py
# Thu, 03 Dec 2020 23:08:13 GMT
ENV PYTHON_GET_PIP_SHA256=d48ae68f297cac54db17e4107b800faae0e5210131f9f386c30c0166bf8d81b7
# Thu, 03 Dec 2020 23:08:37 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 03 Dec 2020 23:08:38 GMT
CMD ["python3"]
# Thu, 03 Dec 2020 23:26:59 GMT
ENV HY_VERSION=0.19.0
# Thu, 03 Dec 2020 23:27:08 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 03 Dec 2020 23:27:09 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:29ade854e0dcedde295dd89890d45271e9df839e42124558eb5283508ca70f5c`  
		Last Modified: Tue, 17 Nov 2020 20:32:02 GMT  
		Size: 25.9 MB (25862532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb4b1b53d2398c6ce67baee2ca8d9b07e650d136995a79630f5743ce7569461`  
		Last Modified: Wed, 25 Nov 2020 06:28:12 GMT  
		Size: 2.6 MB (2622786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e51a6e07f72f3347e4df589a6b88811355d463768664c3c31c72b0b1ca7c734`  
		Last Modified: Wed, 25 Nov 2020 06:29:57 GMT  
		Size: 9.7 MB (9724299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2cb7494f8e3e3c426763b12822b478c63e192fb4155e111339d7f02030be101`  
		Last Modified: Wed, 25 Nov 2020 06:29:54 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8807bd2b38a4a933c335e9c668283af41d6885548965eb513a53e3cc44d67a5`  
		Last Modified: Thu, 03 Dec 2020 23:14:32 GMT  
		Size: 2.4 MB (2425013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507b6a921101c038b181cca9690ae21431db3e5066583f9b1db1fd807ef7afc7`  
		Last Modified: Thu, 03 Dec 2020 23:31:55 GMT  
		Size: 2.8 MB (2807442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.6` - linux; 386

```console
$ docker pull hylang@sha256:c9f446f46b94e9abbe2f39b1dc79deca87ceb99a1ff422b3a8d9c0a46a232cad
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45554472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9afa3d878f330fd8f7cf319a32b43fc67c60a08d5777924c21a4945d7ba5698d`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 17 Nov 2020 20:19:58 GMT
ADD file:b17dfa607fcb298beb9c58bfbb8b9b0743ceb385875776c56269db2506840edf in / 
# Tue, 17 Nov 2020 20:19:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 12:52:26 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Nov 2020 12:52:26 GMT
ENV LANG=C.UTF-8
# Wed, 25 Nov 2020 03:04:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 03:38:54 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Wed, 25 Nov 2020 04:30:56 GMT
ENV PYTHON_VERSION=3.6.12
# Wed, 25 Nov 2020 04:42:05 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Wed, 25 Nov 2020 04:42:06 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 03 Dec 2020 22:55:41 GMT
ENV PYTHON_PIP_VERSION=20.3.1
# Thu, 03 Dec 2020 22:55:41 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/91630a4867b1f93ba0a12aa81d0ec4ecc1e7eeb9/get-pip.py
# Thu, 03 Dec 2020 22:55:42 GMT
ENV PYTHON_GET_PIP_SHA256=d48ae68f297cac54db17e4107b800faae0e5210131f9f386c30c0166bf8d81b7
# Thu, 03 Dec 2020 22:55:58 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 03 Dec 2020 22:55:58 GMT
CMD ["python3"]
# Thu, 03 Dec 2020 23:07:15 GMT
ENV HY_VERSION=0.19.0
# Thu, 03 Dec 2020 23:07:21 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 03 Dec 2020 23:07:21 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e8e82c9fb36b8f3a9b8f18fe1d88e4d425d5c45968e3f2e94cdbb1255feb4878`  
		Last Modified: Tue, 17 Nov 2020 20:26:45 GMT  
		Size: 27.8 MB (27766186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:355c6c98a4baaba29099c04bccd30528a0a56b877c8861953f5a21c232a43802`  
		Last Modified: Wed, 25 Nov 2020 05:08:45 GMT  
		Size: 2.8 MB (2764064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6389688b28f8e613c3cbfb75546a652c785f7d53d947ee6bfddd0aea76a5c4b4`  
		Last Modified: Wed, 25 Nov 2020 05:10:09 GMT  
		Size: 9.8 MB (9792923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad4fe8cb4b99b1ea74594fd0f4aaecef965f89776cc0186321b5a987b60d151`  
		Last Modified: Wed, 25 Nov 2020 05:10:05 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa1f88798c1eeb5f4916eb2e8fc950e8fc88520d85e2af3e87102158c9a4ca4`  
		Last Modified: Thu, 03 Dec 2020 22:59:56 GMT  
		Size: 2.4 MB (2424143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec904fce656dea60c8ba95c0af7da4ef04668ffa018239c5353ae69f414ec288`  
		Last Modified: Thu, 03 Dec 2020 23:10:41 GMT  
		Size: 2.8 MB (2806923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.6` - linux; mips64le

```console
$ docker pull hylang@sha256:e28c1bcdc0aaa2179515ff96124dd01085ac82123e0a025f4f67798be017ffaa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (42959836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678e69f5a2e0391aec65e1e57688f89982299e9de87eb3091d0016cd7e9d6b99`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 17 Nov 2020 20:19:24 GMT
ADD file:98a1b26b3eefd56b2867344c8c58f4bc3ef9a19c28e35c41df77ab80598d41bc in / 
# Tue, 17 Nov 2020 20:19:24 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 01:21:45 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Nov 2020 01:21:45 GMT
ENV LANG=C.UTF-8
# Wed, 25 Nov 2020 03:20:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 04:00:46 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Wed, 25 Nov 2020 04:40:59 GMT
ENV PYTHON_VERSION=3.6.12
# Wed, 25 Nov 2020 05:11:14 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Wed, 25 Nov 2020 05:11:16 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 03 Dec 2020 22:14:53 GMT
ENV PYTHON_PIP_VERSION=20.3.1
# Thu, 03 Dec 2020 22:14:53 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/91630a4867b1f93ba0a12aa81d0ec4ecc1e7eeb9/get-pip.py
# Thu, 03 Dec 2020 22:14:53 GMT
ENV PYTHON_GET_PIP_SHA256=d48ae68f297cac54db17e4107b800faae0e5210131f9f386c30c0166bf8d81b7
# Thu, 03 Dec 2020 22:15:32 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 03 Dec 2020 22:15:33 GMT
CMD ["python3"]
# Thu, 03 Dec 2020 22:36:44 GMT
ENV HY_VERSION=0.19.0
# Thu, 03 Dec 2020 22:36:58 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 03 Dec 2020 22:36:58 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:071bb0a152ef32db0e7d172bcc4722a6a275885249ddb72bee023e268e82fc16`  
		Last Modified: Tue, 17 Nov 2020 20:26:34 GMT  
		Size: 25.8 MB (25777477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d7f9dc130f3a7ec5f1a9b0a7dabc0207adece0a438dc575b23b6129c531bd73`  
		Last Modified: Wed, 25 Nov 2020 05:14:06 GMT  
		Size: 2.3 MB (2309322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57fa7dd0b206befbec334751994e1add05262534d1b2993cd918a1be9815036`  
		Last Modified: Wed, 25 Nov 2020 05:15:04 GMT  
		Size: 9.6 MB (9641324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64789c21a8f4a323067f5e56b2fb3751c71cd896b788adb4a7d9a127db156357`  
		Last Modified: Wed, 25 Nov 2020 05:14:56 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67dc66f1696588142decf31fd2555a5f798e88cd4c3d13993ada67b001f1a015`  
		Last Modified: Thu, 03 Dec 2020 22:20:12 GMT  
		Size: 2.4 MB (2424268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f926e0ddd42b010772bbbbd630941a651466649e400081d421ff8c35b6f856`  
		Last Modified: Thu, 03 Dec 2020 22:38:23 GMT  
		Size: 2.8 MB (2807211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.6` - linux; ppc64le

```console
$ docker pull hylang@sha256:d1e5257f6765a7f9feabf16f741137f7e6442582b5d6f96286d4b885c07c4018
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49093354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62fbcab4be7d4ac98bc289df81cee824ccdee1e0b164d89daf14cd6621647f61`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 17 Nov 2020 23:23:06 GMT
ADD file:49cd8b08964980901349e1f3d6cb34abd8145dea6e6d9ab83502452281ac73ca in / 
# Tue, 17 Nov 2020 23:23:11 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 07:38:57 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Nov 2020 07:39:00 GMT
ENV LANG=C.UTF-8
# Wed, 25 Nov 2020 06:42:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 25 Nov 2020 07:33:34 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Wed, 25 Nov 2020 08:29:22 GMT
ENV PYTHON_VERSION=3.6.12
# Wed, 25 Nov 2020 09:02:03 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Wed, 25 Nov 2020 09:02:29 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 03 Dec 2020 23:02:30 GMT
ENV PYTHON_PIP_VERSION=20.3.1
# Thu, 03 Dec 2020 23:02:36 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/91630a4867b1f93ba0a12aa81d0ec4ecc1e7eeb9/get-pip.py
# Thu, 03 Dec 2020 23:03:00 GMT
ENV PYTHON_GET_PIP_SHA256=d48ae68f297cac54db17e4107b800faae0e5210131f9f386c30c0166bf8d81b7
# Thu, 03 Dec 2020 23:04:56 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 03 Dec 2020 23:05:02 GMT
CMD ["python3"]
# Fri, 04 Dec 2020 01:38:54 GMT
ENV HY_VERSION=0.19.0
# Fri, 04 Dec 2020 01:39:36 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Fri, 04 Dec 2020 01:39:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d79345c10f03543bff3982aedb35a18ba18626c0074014387ff5e1dc14474e2b`  
		Last Modified: Tue, 17 Nov 2020 23:32:54 GMT  
		Size: 30.5 MB (30531702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1bb6e664ebff5890e2c3c9a17c066289c43d7f7a65fe0425db04455e71d7e7`  
		Last Modified: Wed, 25 Nov 2020 09:26:46 GMT  
		Size: 2.9 MB (2871885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ce424f23a6dceec5e62764c6f77e970225f2f6c1755e1273210c653c09ab62`  
		Last Modified: Wed, 25 Nov 2020 09:28:51 GMT  
		Size: 10.5 MB (10454466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcb72fa4a7542416a5be2e43f68c1e7dae6e1ab30fc9c029d60e4e641655447`  
		Last Modified: Wed, 25 Nov 2020 09:28:49 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:737abf12610ac08a4e40119eb11b8221afcdca1f6a1e2ef83306d4f5e8d40dae`  
		Last Modified: Thu, 03 Dec 2020 23:14:17 GMT  
		Size: 2.4 MB (2426848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca79d045706a7340bf9ed5a76c49e958c06b182575b25d24e4e80beb1b8759f4`  
		Last Modified: Fri, 04 Dec 2020 01:46:13 GMT  
		Size: 2.8 MB (2808218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.6` - linux; s390x

```console
$ docker pull hylang@sha256:7c51760de088f35e7bb1cdbdb5d744c47603fe2ef3a7573896fb5f92a84d8406
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (42956602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0c213dd4bbf48913df139ca1a0aef09387ba0535cd50a82b6c28b4a9ce54f8`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 11 Dec 2020 02:12:11 GMT
ADD file:db86ce5a1665b6d8ac734c54ac249a811c58484f569b935b14772445962428aa in / 
# Fri, 11 Dec 2020 02:12:15 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 06:47:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Dec 2020 06:47:28 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 10:10:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 10:25:20 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Fri, 11 Dec 2020 10:41:36 GMT
ENV PYTHON_VERSION=3.6.12
# Fri, 11 Dec 2020 10:47:41 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		LDFLAGS="-Wl,--strip-all" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 		&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& python3 --version
# Fri, 11 Dec 2020 10:47:45 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 11 Dec 2020 10:47:45 GMT
ENV PYTHON_PIP_VERSION=20.3.1
# Fri, 11 Dec 2020 10:47:46 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/91630a4867b1f93ba0a12aa81d0ec4ecc1e7eeb9/get-pip.py
# Fri, 11 Dec 2020 10:47:47 GMT
ENV PYTHON_GET_PIP_SHA256=d48ae68f297cac54db17e4107b800faae0e5210131f9f386c30c0166bf8d81b7
# Fri, 11 Dec 2020 10:48:00 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 11 Dec 2020 10:48:02 GMT
CMD ["python3"]
# Fri, 11 Dec 2020 17:01:37 GMT
ENV HY_VERSION=0.19.0
# Fri, 11 Dec 2020 17:01:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Fri, 11 Dec 2020 17:01:46 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f4cf10ca9f31aab0854647d7878dc4db838e93b892b843dde3db24f2e909a106`  
		Last Modified: Fri, 11 Dec 2020 02:17:07 GMT  
		Size: 25.7 MB (25713957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cc4fa88463416e86d8734314436620342a8e459fbc15bffe1a3d95ea5244c7`  
		Last Modified: Fri, 11 Dec 2020 10:57:13 GMT  
		Size: 2.4 MB (2444229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8cfe1d5f6543c3d8d129d7ee746fcc34e7075293f40caf8211d4f4dc4a3d7ee`  
		Last Modified: Fri, 11 Dec 2020 10:58:03 GMT  
		Size: 9.6 MB (9566397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f72077978dbcf86575164157313c8280009ad48cc18d7156ecac2f4558732c`  
		Last Modified: Fri, 11 Dec 2020 10:58:01 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a74316b248cc8ee0a38487473fb0a4f9d5d5c927687d13a1ca9ca28351a0a72`  
		Last Modified: Fri, 11 Dec 2020 10:58:02 GMT  
		Size: 2.4 MB (2424464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a5d94c48d7350db1cc1b0f35e8b0eecc24ec9aa2a3dab774e70fbaca2da63b5`  
		Last Modified: Fri, 11 Dec 2020 17:06:26 GMT  
		Size: 2.8 MB (2807323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
