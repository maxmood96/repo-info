## `hylang:0-python3.6-alpine3.10`

```console
$ docker pull hylang@sha256:07d826f6e44a0e729dcd5f5bde78badfb952dc30750271be87bd3d3563731454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `hylang:0-python3.6-alpine3.10` - linux; amd64

```console
$ docker pull hylang@sha256:34577c84338a06e59132811a6bdf3af6f24e90028c3010e083570a603abd50e7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35146705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18cac581fbf69c9166aec81c0259385c1cc91c38585f66e1e0865669a87db3a0`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 18:05:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2020 23:09:17 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2020 23:09:19 GMT
RUN apk add --no-cache ca-certificates
# Thu, 23 Jan 2020 23:32:58 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Fri, 24 Jan 2020 02:34:30 GMT
ENV PYTHON_VERSION=3.6.10
# Fri, 24 Jan 2020 02:41:25 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Fri, 24 Jan 2020 02:41:26 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 25 Jan 2020 02:52:43 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Thu, 06 Feb 2020 01:39:49 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Thu, 06 Feb 2020 01:39:49 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Thu, 06 Feb 2020 01:39:54 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 06 Feb 2020 01:39:55 GMT
CMD ["python3"]
# Thu, 06 Feb 2020 02:16:01 GMT
ENV HY_VERSION=0.18.0
# Thu, 06 Feb 2020 02:16:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 06 Feb 2020 02:16:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1baf8a687be7ffea0d5471a91e524515128c316739abda79ead8135ca464ea15`  
		Last Modified: Fri, 24 Jan 2020 05:53:56 GMT  
		Size: 301.7 KB (301729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee7638ed7289a0225bab0e65b3a41d11481353040f3d30e2a831f2bcb3d1fd7`  
		Last Modified: Fri, 24 Jan 2020 05:56:48 GMT  
		Size: 27.4 MB (27412602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7453b11fd5045f20ef3177427e4eafb65d29c38abfd1d1565cc3d17d9b9f9139`  
		Last Modified: Fri, 24 Jan 2020 05:56:30 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:182e21ae3174dd4650643a9e39984e03ccb07a3bfcae37d1f09cba45f5502150`  
		Last Modified: Thu, 06 Feb 2020 01:45:13 GMT  
		Size: 1.9 MB (1892202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e887a094ba9becad46283a40255c5455fb08ee6efde598def412420829bea05`  
		Last Modified: Thu, 06 Feb 2020 02:18:44 GMT  
		Size: 2.8 MB (2752977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.6-alpine3.10` - linux; arm variant v6

```console
$ docker pull hylang@sha256:a36b2be1c670a2e7e708f9169f199f26718eaac697cf8fd8ac4ed3a914e6b4b9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32240622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f6d495ff173d1b4dc6847b82babbcf786a83637c17a2db620f5c0a5e95d77f`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:35 GMT
ADD file:ef75120295e25a8e67c5ef378df2cf4ce9f7b83b44709452fcaf247b54fabd16 in / 
# Thu, 23 Apr 2020 15:51:36 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 20:38:44 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 20:38:45 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 20:38:48 GMT
RUN apk add --no-cache ca-certificates
# Thu, 23 Apr 2020 21:05:04 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Thu, 23 Apr 2020 21:30:08 GMT
ENV PYTHON_VERSION=3.6.10
# Thu, 23 Apr 2020 21:38:54 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 23 Apr 2020 21:38:59 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 23 Apr 2020 21:39:00 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Thu, 23 Apr 2020 21:39:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Thu, 23 Apr 2020 21:39:02 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Thu, 23 Apr 2020 21:39:16 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 23 Apr 2020 21:39:17 GMT
CMD ["python3"]
# Fri, 24 Apr 2020 01:51:21 GMT
ENV HY_VERSION=0.18.0
# Fri, 24 Apr 2020 01:51:34 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Fri, 24 Apr 2020 01:51:35 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e745d1dc1c9e0be26166278da7632765ca98fa1be8179a7cc440b3bdc5671860`  
		Last Modified: Thu, 23 Apr 2020 15:52:15 GMT  
		Size: 2.6 MB (2572512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b57a40f256a36351da43ee93685238f00bc7c6b0457d57f43b6de40365dc27eb`  
		Last Modified: Thu, 23 Apr 2020 21:58:11 GMT  
		Size: 301.3 KB (301254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a63621787fefd2470be647499a1b83c1d4a88781696e5dea5f2e8a03b2367395`  
		Last Modified: Thu, 23 Apr 2020 21:59:37 GMT  
		Size: 24.7 MB (24722780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9797d5de01f3c8e1122f930b06a7b1c86c59fa0fea8b3bd57a42155dc5ab37bd`  
		Last Modified: Thu, 23 Apr 2020 21:59:28 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b30a0b73e55b066fe79ddd6dbecb06fc39644e57a93547850182170e90f7a90`  
		Last Modified: Thu, 23 Apr 2020 21:59:29 GMT  
		Size: 1.9 MB (1891418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7b6d57f380ca6c860064079159bbd2b6ab2d6a03fc95da1490b6fb3c288d98`  
		Last Modified: Fri, 24 Apr 2020 01:54:06 GMT  
		Size: 2.8 MB (2752427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.6-alpine3.10` - linux; arm variant v7

```console
$ docker pull hylang@sha256:a0ec12bcec1bac64261b10e68e9cf3566b364c0b61fa6b51bbede9e450e479ba
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.0 MB (31986878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:156637ab3c80fac4b0717dc2b51876d359765b53577d89bf9f9f9c42364a8dc2`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:31 GMT
ADD file:d05c9f9143d11d12045d4faef882e5985e6b38fabe52237dd8d8c0627a9620ab in / 
# Thu, 23 Jan 2020 16:53:32 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:16:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2020 19:16:24 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2020 19:16:27 GMT
RUN apk add --no-cache ca-certificates
# Thu, 23 Jan 2020 19:34:45 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Thu, 23 Jan 2020 19:49:45 GMT
ENV PYTHON_VERSION=3.6.10
# Thu, 23 Jan 2020 19:57:42 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 23 Jan 2020 19:57:52 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 25 Jan 2020 02:36:48 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Thu, 06 Feb 2020 02:22:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Thu, 06 Feb 2020 02:22:22 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Thu, 06 Feb 2020 02:22:38 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 06 Feb 2020 02:22:39 GMT
CMD ["python3"]
# Thu, 06 Feb 2020 02:42:17 GMT
ENV HY_VERSION=0.18.0
# Thu, 06 Feb 2020 02:42:28 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 06 Feb 2020 02:42:29 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4e972d957a606327b0b6c2e8aa4a6045c263b7496a536298aaebf690e9d85f1d`  
		Last Modified: Thu, 23 Jan 2020 16:53:59 GMT  
		Size: 2.4 MB (2378408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7d55ab1b842311f10b795319bc80abba3cf485d9888a91d16898a5e2ac9c3c`  
		Last Modified: Thu, 23 Jan 2020 20:16:54 GMT  
		Size: 300.9 KB (300937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8ae4d1a13f4cd500e2a1b997e0573535c7b9e2cbc8716ea9c526a1bbf54fe4`  
		Last Modified: Thu, 23 Jan 2020 20:18:48 GMT  
		Size: 24.7 MB (24661285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff6b592797b2896b9aed40cd5809e346b11c6acc256b64ea3c9fd3f589bb018`  
		Last Modified: Thu, 23 Jan 2020 20:18:36 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af71144b0820e90feac492e53dd0de29da0bf76a3d118ecd550a250b1767e34c`  
		Last Modified: Thu, 06 Feb 2020 02:34:11 GMT  
		Size: 1.9 MB (1892457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d2cc824fa04221bf0c89fa0119042ca7cbd56983649d06e017824822704032c`  
		Last Modified: Thu, 06 Feb 2020 02:47:31 GMT  
		Size: 2.8 MB (2753561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.6-alpine3.10` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:68ce29a70e30e5f8c4d7548d177d9d5608e79031527a58b43ba4f95f67c80b6a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.9 MB (33920217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71126490da24c480ab77bb32ffd0332193a39a033bad574bf92b513e5a698064`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:52 GMT
ADD file:75529f7e83edb6d0457a3b8bbfe33d4e3a12f339c5ace517d0f52dbedd9a146b in / 
# Fri, 24 Apr 2020 00:14:53 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 07:16:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2020 07:16:39 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2020 07:16:41 GMT
RUN apk add --no-cache ca-certificates
# Fri, 24 Apr 2020 07:38:45 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Fri, 24 Apr 2020 08:00:22 GMT
ENV PYTHON_VERSION=3.6.10
# Fri, 24 Apr 2020 08:07:31 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Fri, 24 Apr 2020 08:07:33 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 24 Apr 2020 08:07:34 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Fri, 24 Apr 2020 08:07:35 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Fri, 24 Apr 2020 08:07:35 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Fri, 24 Apr 2020 08:07:46 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 24 Apr 2020 08:07:46 GMT
CMD ["python3"]
# Fri, 24 Apr 2020 08:30:39 GMT
ENV HY_VERSION=0.18.0
# Fri, 24 Apr 2020 08:30:50 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Fri, 24 Apr 2020 08:30:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b038bcb63e9c8905cc879c957302f686a9b43f24a18dcfc4186ab236ddf04cad`  
		Last Modified: Fri, 24 Apr 2020 00:15:54 GMT  
		Size: 2.7 MB (2718734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00770a9e6c343f414a2bac6b7ff8cb12c89d6b8559f1cb74ed38ea04ff029cd`  
		Last Modified: Fri, 24 Apr 2020 08:25:29 GMT  
		Size: 301.6 KB (301579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18bec331ea1f9868c81a5c5bcbd556076ef0461204024b89ae3c7d13d09bb8d`  
		Last Modified: Fri, 24 Apr 2020 08:27:13 GMT  
		Size: 26.3 MB (26255648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f98ff97134ffc15fad38d278ea0fd0dbf9ff9de2805c94daecfa82935608790`  
		Last Modified: Fri, 24 Apr 2020 08:27:04 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9623a9dafd5c8cf3b45b743caa2a0ea0ee0b839f386cee074741ecbce1a058b`  
		Last Modified: Fri, 24 Apr 2020 08:27:05 GMT  
		Size: 1.9 MB (1891571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2f44bd4c810a82b2debd50f0447599cd23cac50679cc360d12a0632e3f6de9`  
		Last Modified: Fri, 24 Apr 2020 08:35:05 GMT  
		Size: 2.8 MB (2752451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.6-alpine3.10` - linux; 386

```console
$ docker pull hylang@sha256:28a2947396bceb3270992fa44257d2a67e5213a5007426654663319ac8e8a475
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 MB (33175305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43ad15f5f60d25c6849850f38b927d861781ef5008b1842da71254b9d0b7c1e4`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:11 GMT
ADD file:2e9fb162fdd20e7ac6e9edcb9e1ce9ece750f125c93824c5709a2800ae397f89 in / 
# Thu, 23 Apr 2020 21:16:11 GMT
CMD ["/bin/sh"]
# Thu, 23 Apr 2020 21:38:22 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 21:38:22 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 21:38:24 GMT
RUN apk add --no-cache ca-certificates
# Thu, 23 Apr 2020 21:58:55 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Thu, 23 Apr 2020 22:18:12 GMT
ENV PYTHON_VERSION=3.6.10
# Thu, 23 Apr 2020 22:26:27 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 23 Apr 2020 22:26:28 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 23 Apr 2020 22:26:28 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Thu, 23 Apr 2020 22:26:28 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Thu, 23 Apr 2020 22:26:28 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Thu, 23 Apr 2020 22:26:36 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 23 Apr 2020 22:26:36 GMT
CMD ["python3"]
# Fri, 24 Apr 2020 04:00:46 GMT
ENV HY_VERSION=0.18.0
# Fri, 24 Apr 2020 04:00:52 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Fri, 24 Apr 2020 04:00:52 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:294658c31053f36b08a64158e37d4fb84478e6fe8f4d5127c51a6334c8a3c36d`  
		Last Modified: Thu, 23 Apr 2020 21:16:37 GMT  
		Size: 2.8 MB (2787128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61cc54eae371e15077a5272fb58cfef3e4a13587edf5fe05700b05ee682c5cd`  
		Last Modified: Thu, 23 Apr 2020 22:44:54 GMT  
		Size: 301.6 KB (301596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d715f4fb6297ceec5598cfd08c659470db4b531abe9960fb859ada9825e445`  
		Last Modified: Thu, 23 Apr 2020 22:45:49 GMT  
		Size: 25.4 MB (25443428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a46334908ecb89666ed1de53b3c10eaa847cbbe960273c0cb2b682372af3087`  
		Last Modified: Thu, 23 Apr 2020 22:45:43 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716f937cb8a6dbeb8cb63c9c0230b118138af83c9e16eead97e4c2f0d28d78b2`  
		Last Modified: Thu, 23 Apr 2020 22:45:43 GMT  
		Size: 1.9 MB (1891046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5983cfc72a3dfb39c6b0c96e635cb066a29f30ce059d67772c0dddeb4dec59`  
		Last Modified: Fri, 24 Apr 2020 04:03:06 GMT  
		Size: 2.8 MB (2751876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.6-alpine3.10` - linux; ppc64le

```console
$ docker pull hylang@sha256:0cc1eb78d44c564511e11aa4aef19beb1b486b8a31c47431604788c37d124835
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.9 MB (35928745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:917f4fef51a54a3cd35f49f61cb718e0250ec0c0a6658956abbb81df0d749092`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Jan 2020 16:57:54 GMT
ADD file:5e383dfaf3281b9cc17caf519d1aeba934fa92632c10afb8cc189f6ba12d9f64 in / 
# Thu, 23 Jan 2020 16:57:58 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:41:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2020 19:41:01 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2020 19:41:08 GMT
RUN apk add --no-cache ca-certificates
# Thu, 23 Jan 2020 20:00:22 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Thu, 23 Jan 2020 20:13:29 GMT
ENV PYTHON_VERSION=3.6.10
# Thu, 23 Jan 2020 20:21:18 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 23 Jan 2020 20:21:27 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 25 Jan 2020 02:43:40 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Thu, 06 Feb 2020 01:37:06 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Thu, 06 Feb 2020 01:37:09 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Thu, 06 Feb 2020 01:37:28 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 06 Feb 2020 01:37:31 GMT
CMD ["python3"]
# Thu, 06 Feb 2020 02:25:46 GMT
ENV HY_VERSION=0.18.0
# Thu, 06 Feb 2020 02:26:03 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 06 Feb 2020 02:26:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4ae00dedbff84a762d4b8b9176da2beee50017c43fe09a5ae92c2417d5634510`  
		Last Modified: Thu, 23 Jan 2020 16:58:43 GMT  
		Size: 2.8 MB (2808535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40439424ae05468c06dc5cd9b4cc43c689b897b0a75c281fb7c5279017124aa`  
		Last Modified: Thu, 23 Jan 2020 20:40:47 GMT  
		Size: 304.5 KB (304458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8c6fa3171598997de6b575e8e1b40f9cb000db2d69444c3c477b885a0df13f`  
		Last Modified: Thu, 23 Jan 2020 20:42:49 GMT  
		Size: 28.2 MB (28169366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4fbfafb852e06d850b73606b626526424043f472d3abd44834ba91f65a00b7a`  
		Last Modified: Thu, 23 Jan 2020 20:42:27 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d08843e6d03073c844a6ebbe339fc225166da1ace62a58ecf23f9cae725319`  
		Last Modified: Thu, 06 Feb 2020 01:54:11 GMT  
		Size: 1.9 MB (1892443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce891f5b23ee64d8e062c4e733c3dbd3572ed9a4276f1b1b29c926c404c0e9d0`  
		Last Modified: Thu, 06 Feb 2020 02:32:16 GMT  
		Size: 2.8 MB (2753714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.6-alpine3.10` - linux; s390x

```console
$ docker pull hylang@sha256:5b3e7507a324c4136c987a57df7a4facbda86633140e9476d8bbd407dfe518f4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.4 MB (34373449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f555fa88ca61b697881c375c917796df17735d325a0830a9a0d5db7517262b1e`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Apr 2020 17:51:08 GMT
ADD file:53e1d2e5396547a2d7109e4b73078911bd069ae5d762f816d90e89ec9731ab13 in / 
# Thu, 23 Apr 2020 17:51:08 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 00:08:22 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2020 00:08:22 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2020 00:08:23 GMT
RUN apk add --no-cache ca-certificates
# Fri, 24 Apr 2020 00:19:24 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Fri, 24 Apr 2020 03:26:19 GMT
ENV PYTHON_VERSION=3.6.10
# Fri, 24 Apr 2020 10:06:38 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Fri, 24 Apr 2020 10:06:44 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Fri, 24 Apr 2020 10:06:45 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Fri, 24 Apr 2020 10:06:45 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Fri, 24 Apr 2020 10:06:46 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Fri, 24 Apr 2020 10:06:54 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 24 Apr 2020 10:06:55 GMT
CMD ["python3"]
# Fri, 24 Apr 2020 10:10:50 GMT
ENV HY_VERSION=0.18.0
# Fri, 24 Apr 2020 10:10:54 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Fri, 24 Apr 2020 10:10:54 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ab92bebeb6027138cd65f1f6658fd3428e21c60c95bdc978e0c57bf0b2a53970`  
		Last Modified: Thu, 23 Apr 2020 17:51:46 GMT  
		Size: 2.6 MB (2574478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9effbbafa6dfb00bba9beef1c64dca1e9ac011970f2065747370e7774a9109a7`  
		Last Modified: Fri, 24 Apr 2020 06:43:43 GMT  
		Size: 301.7 KB (301709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb8dde267d52e04f4e0669cb78a9c9d885647dd397b3c3e8bc2e2edbc98a1749`  
		Last Modified: Fri, 24 Apr 2020 10:08:44 GMT  
		Size: 26.9 MB (26853794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fada138608528192ec036c4d44ed7dd327bb51951733c42420030134a732421`  
		Last Modified: Fri, 24 Apr 2020 10:08:44 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb25ec990cf0433a08c51dda06466824c64e5250d8cb12474c26c1a36041703c`  
		Last Modified: Fri, 24 Apr 2020 10:08:39 GMT  
		Size: 1.9 MB (1891235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37d86a806c45a51f4c4defdb689ec1dcb510c94761f69d1cbbd6e9f0b2b7e14`  
		Last Modified: Fri, 24 Apr 2020 10:13:07 GMT  
		Size: 2.8 MB (2752001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
