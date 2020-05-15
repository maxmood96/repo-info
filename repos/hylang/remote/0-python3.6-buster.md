## `hylang:0-python3.6-buster`

```console
$ docker pull hylang@sha256:f4100e9a04d5a0ad15612feeafea4447c3f8fbeb64d9d4e18c7123bdbcfdb6e8
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

### `hylang:0-python3.6-buster` - linux; amd64

```console
$ docker pull hylang@sha256:af3687a0698b3fef65b65185113bd4ea90403fe1e5419b0bea4842a1a68cf1cb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61425776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8d451cbd9ed8506ebf2c753ec1a921d60617704745ad603efd66cb17aaec2be`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:32 GMT
ADD file:9b8be2b52ee0fa31da1b6256099030b73546253a57e94cccb24605cd888bb74d in / 
# Thu, 23 Apr 2020 00:20:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 14:23:49 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 14:23:49 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 14:23:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 14:45:50 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Thu, 23 Apr 2020 15:25:32 GMT
ENV PYTHON_VERSION=3.6.10
# Thu, 23 Apr 2020 15:34:15 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 23 Apr 2020 15:34:16 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 29 Apr 2020 17:40:24 GMT
ENV PYTHON_PIP_VERSION=20.1
# Wed, 29 Apr 2020 17:40:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Wed, 29 Apr 2020 17:40:24 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Wed, 29 Apr 2020 17:40:47 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 29 Apr 2020 17:40:47 GMT
CMD ["python3"]
# Wed, 29 Apr 2020 18:50:03 GMT
ENV HY_VERSION=0.18.0
# Wed, 29 Apr 2020 18:50:07 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 29 Apr 2020 18:50:08 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:54fec2fa59d0a0de9cd2dec9850b36c43de451f1fd1c0a5bf8f1cf26a61a5da4`  
		Last Modified: Thu, 23 Apr 2020 00:25:10 GMT  
		Size: 27.1 MB (27098254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3f35d84caba5a287676eeaea3d371e1ed5af8c57c33532228a456e0505b2d5`  
		Last Modified: Thu, 23 Apr 2020 16:21:00 GMT  
		Size: 2.7 MB (2749038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0907fdf4800ebca52819187ad2237c25f8ab882c12f3515ed5a69c732aa957d8`  
		Last Modified: Thu, 23 Apr 2020 16:22:32 GMT  
		Size: 26.6 MB (26606748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc57da2fafb6978d00423e215b1ce8889be05d8133d8cdf12ca033405bd0073d`  
		Last Modified: Thu, 23 Apr 2020 16:22:26 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9455d6f4fa942a6bebd3392fa1f3487e4f2e9c7f18de67aa2d1bfa3c5e6f95f9`  
		Last Modified: Wed, 29 Apr 2020 17:45:40 GMT  
		Size: 2.2 MB (2218983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d490d5440b3770e7bfe55ef901788c3940aff3b9236eba99502147e9f721d4`  
		Last Modified: Wed, 29 Apr 2020 18:52:53 GMT  
		Size: 2.8 MB (2752520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.6-buster` - linux; arm variant v5

```console
$ docker pull hylang@sha256:5b12dd2bd8f01866575c64a8fdb4992d474db0fb9728e94fb710dc666c7d8c79
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56640462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a762d71a961f0d2a3f48542cca442142ebff865a98ff0d1643f9c284c8ab4b93`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 13 May 2020 21:50:06 GMT
ADD file:8a04dde48abba80d9184ad860f6e6c4ac165162590487ead2834f603d3fee2d2 in / 
# Wed, 13 May 2020 21:50:13 GMT
CMD ["bash"]
# Thu, 14 May 2020 01:24:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2020 01:24:12 GMT
ENV LANG=C.UTF-8
# Thu, 14 May 2020 01:24:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 01:53:34 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Thu, 14 May 2020 02:42:30 GMT
ENV PYTHON_VERSION=3.6.10
# Thu, 14 May 2020 02:52:54 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 14 May 2020 02:52:57 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 14 May 2020 02:52:57 GMT
ENV PYTHON_PIP_VERSION=20.1
# Thu, 14 May 2020 02:52:58 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Thu, 14 May 2020 02:52:58 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Thu, 14 May 2020 02:53:28 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 14 May 2020 02:53:29 GMT
CMD ["python3"]
# Thu, 14 May 2020 22:28:37 GMT
ENV HY_VERSION=0.18.0
# Thu, 14 May 2020 22:28:50 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 14 May 2020 22:28:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:273d90ed0ae4725b27ca04e3f382ad8c985987bdfcdd95a01a5599e9f5540fdd`  
		Last Modified: Wed, 13 May 2020 21:59:22 GMT  
		Size: 24.8 MB (24830573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcd05660d91c720efcdd8e035bddddc7ec8b01df457ce14399f8c0f11a1f989`  
		Last Modified: Thu, 14 May 2020 03:48:23 GMT  
		Size: 2.4 MB (2448215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a611491f9ded971ff074da057072cab9943a3d7291089d0eb6cc0ca966c21b`  
		Last Modified: Thu, 14 May 2020 03:50:06 GMT  
		Size: 24.4 MB (24389830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9150265c8014e02d875836da441f3d7328eb351e13c50bbf6b13b2aa16c91a6c`  
		Last Modified: Thu, 14 May 2020 03:49:57 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f333b4dbe9a257f8c34808ea45a05f7f2d74110abdfbc2593ba97dd52a41cbc`  
		Last Modified: Thu, 14 May 2020 03:49:58 GMT  
		Size: 2.2 MB (2218703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d430d47383ef2b8d688d0877723069d2323fdbbbba8e8e93f1213a696cd61ce`  
		Last Modified: Thu, 14 May 2020 22:31:14 GMT  
		Size: 2.8 MB (2752908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.6-buster` - linux; arm variant v7

```console
$ docker pull hylang@sha256:cf0702a1fdd5ce7dbddd8ab32733599f21e83537d06bf1db5b730cde10e8e21e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53970202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9702aaf3215c093c1cea2ebbd6a4794488d988325648d21ce55207ec062e0893`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Apr 2020 01:03:26 GMT
ADD file:db6122b36f3e70c5f490b50afba99d49fa345f11d0f5c77bb3c6749f8e2a4f81 in / 
# Thu, 23 Apr 2020 01:03:28 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 07:05:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 07:05:39 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 07:05:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 07:35:33 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Thu, 23 Apr 2020 08:28:42 GMT
ENV PYTHON_VERSION=3.6.10
# Thu, 23 Apr 2020 08:39:16 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 23 Apr 2020 08:39:20 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 29 Apr 2020 17:23:38 GMT
ENV PYTHON_PIP_VERSION=20.1
# Wed, 29 Apr 2020 17:23:39 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Wed, 29 Apr 2020 17:23:39 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Wed, 29 Apr 2020 17:24:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 29 Apr 2020 17:24:11 GMT
CMD ["python3"]
# Wed, 29 Apr 2020 18:08:33 GMT
ENV HY_VERSION=0.18.0
# Wed, 29 Apr 2020 18:08:45 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 29 Apr 2020 18:08:46 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:50fb0052086928803f00724ca465c89c45dde5b082b1e59dadb8101286dd5ab6`  
		Last Modified: Thu, 23 Apr 2020 01:11:08 GMT  
		Size: 22.7 MB (22705377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9eabbae7363920ecfeebec7f1e8caf59ce3bb9d93b9ef7870afbeedc508d1b`  
		Last Modified: Thu, 23 Apr 2020 09:37:17 GMT  
		Size: 2.3 MB (2345921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b82cc17bd063e7838b41ff711f7b6d4f895399b38e44eb503e693e41cb2cd2`  
		Last Modified: Thu, 23 Apr 2020 09:39:35 GMT  
		Size: 23.9 MB (23946943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a8934673490605874823e94ba010de27d0ecfc6a6a56c084a71e2ca4a5aeb7`  
		Last Modified: Thu, 23 Apr 2020 09:39:26 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a431797c761283b5359a12173a2ec9ab31636de3764791a855d0d7feed8dc22`  
		Last Modified: Wed, 29 Apr 2020 17:32:27 GMT  
		Size: 2.2 MB (2218828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47bc99d9562a2bb69be70266d39d6eb8e0de73ba692dd3c6ce0fb99983a7ebfb`  
		Last Modified: Wed, 29 Apr 2020 18:13:43 GMT  
		Size: 2.8 MB (2752898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.6-buster` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:0e169bf3f090057ac6cf8b4543ae073c3bfa3a7b4971699d7c824a0966d2dbe3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59137443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366607edb74100830f3ae793ddfd35b87ba496fc7a3a23afcfbc36020f3329fd`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Apr 2020 00:54:55 GMT
ADD file:581ee9c3c19f0d971aeda008fd399f59171cae75e8936b967dbf3888db4fc0d0 in / 
# Thu, 23 Apr 2020 00:54:58 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 12:59:33 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 12:59:33 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 12:59:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 13:24:11 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Thu, 23 Apr 2020 14:15:51 GMT
ENV PYTHON_VERSION=3.6.10
# Thu, 23 Apr 2020 14:25:06 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 23 Apr 2020 14:25:09 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 29 Apr 2020 18:07:03 GMT
ENV PYTHON_PIP_VERSION=20.1
# Wed, 29 Apr 2020 18:07:04 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Wed, 29 Apr 2020 18:07:05 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Wed, 29 Apr 2020 18:07:35 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 29 Apr 2020 18:07:37 GMT
CMD ["python3"]
# Wed, 29 Apr 2020 19:11:59 GMT
ENV HY_VERSION=0.18.0
# Wed, 29 Apr 2020 19:12:07 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 29 Apr 2020 19:12:08 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bdc84a41f2513e28e99efeff9fcbb196b7df9883fb30532184bd67ca415b4673`  
		Last Modified: Thu, 23 Apr 2020 01:03:27 GMT  
		Size: 25.9 MB (25857800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538d0f6124c2ad1cad6bcdbcfb70e62d493c2e5220f52cb7f64772a6c92919cb`  
		Last Modified: Thu, 23 Apr 2020 15:19:22 GMT  
		Size: 2.6 MB (2622296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd7d2e34b93de5a7b7816c05c8ca661cdfa10fd85b6698a2f49752418d55b870`  
		Last Modified: Thu, 23 Apr 2020 15:20:01 GMT  
		Size: 25.7 MB (25685286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80922750228696e0058d1f7b44d29b45d1c0aa525b84b1895672c8ecc1f02a74`  
		Last Modified: Thu, 23 Apr 2020 15:19:52 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d9011a002de705bdb8d4d96c11a52f59d374a7a58aaf2cff8f5c9a35609d68`  
		Last Modified: Wed, 29 Apr 2020 18:16:52 GMT  
		Size: 2.2 MB (2219106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6815bd22bec86c161df7b3d1b78c3fa8ddbb814519805045d7a2fb38cbefffd8`  
		Last Modified: Wed, 29 Apr 2020 19:16:33 GMT  
		Size: 2.8 MB (2752721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.6-buster` - linux; 386

```console
$ docker pull hylang@sha256:caf9f7d8baf4a61ced17d387b3d69dcf8e8217f0f5af8e7281c731a61902d157
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60413508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9482dc0ee3e23ebf780e214759b1795af2c9b35f21e665ac0ff84235ef1b57a`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Apr 2020 00:39:36 GMT
ADD file:ca6a74f6b738c738c033152fab2a9aacf22bec5f19a994e6a02b5f919ee33ee9 in / 
# Thu, 23 Apr 2020 00:39:36 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 14:21:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 14:21:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 15:42:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 16:11:18 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Thu, 23 Apr 2020 17:03:02 GMT
ENV PYTHON_VERSION=3.6.10
# Thu, 23 Apr 2020 17:16:48 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 23 Apr 2020 17:16:50 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 29 Apr 2020 18:03:14 GMT
ENV PYTHON_PIP_VERSION=20.1
# Wed, 29 Apr 2020 18:03:14 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Wed, 29 Apr 2020 18:03:14 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Wed, 29 Apr 2020 18:03:29 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 29 Apr 2020 18:03:29 GMT
CMD ["python3"]
# Wed, 29 Apr 2020 18:25:39 GMT
ENV HY_VERSION=0.18.0
# Wed, 29 Apr 2020 18:25:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 29 Apr 2020 18:25:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:5d3da8f33b97fc107a05b3255a55836b76df9f817de632b1fb63c6e9c024f0df`  
		Last Modified: Thu, 23 Apr 2020 00:44:35 GMT  
		Size: 27.8 MB (27753972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b380695a7873440a76f6b09b0b6e62d86c8c20c95cb7e7a4f61758763d6789`  
		Last Modified: Thu, 23 Apr 2020 18:26:07 GMT  
		Size: 2.8 MB (2762521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75bc562b235c2d5344248a03dc8b3b456b4d169f4bfce94e0f147c224ebaa7f`  
		Last Modified: Thu, 23 Apr 2020 18:27:45 GMT  
		Size: 24.9 MB (24925695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a966ede039a9406221f214a3f0e9fc899146e12ca012e7ea47f7f18330763c`  
		Last Modified: Thu, 23 Apr 2020 18:27:40 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c9ec42236d12c90c507fce59655e9cee3e71418e3001fd4ab07ea5d1fdc5135`  
		Last Modified: Wed, 29 Apr 2020 18:08:06 GMT  
		Size: 2.2 MB (2218699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5d99ecfb7d45d3abd502e9e5a62440e777a6cade358f1c7b962b7dd29135ab`  
		Last Modified: Wed, 29 Apr 2020 18:28:25 GMT  
		Size: 2.8 MB (2752386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.6-buster` - linux; mips64le

```console
$ docker pull hylang@sha256:84312b2e180091366991c9a6d9dae0447b5c9cb5f3cae59d5932cc4fe233c307
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59182462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64c0b822ee389f241293d3479f3aa7c1bbcf8bd2503d06093905195870b2b54f`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Apr 2020 00:09:47 GMT
ADD file:7509945bd8a224048260e88b466aa3b156615e16b64e0a6702da277052fcb98b in / 
# Thu, 23 Apr 2020 00:09:48 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 11:01:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 11:01:59 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 11:02:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 12:26:36 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Thu, 23 Apr 2020 14:36:58 GMT
ENV PYTHON_VERSION=3.6.10
# Thu, 23 Apr 2020 15:09:53 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 23 Apr 2020 15:09:56 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 29 Apr 2020 17:59:51 GMT
ENV PYTHON_PIP_VERSION=20.1
# Wed, 29 Apr 2020 17:59:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Wed, 29 Apr 2020 17:59:51 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Wed, 29 Apr 2020 18:00:32 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 29 Apr 2020 18:00:32 GMT
CMD ["python3"]
# Wed, 29 Apr 2020 18:25:43 GMT
ENV HY_VERSION=0.18.0
# Wed, 29 Apr 2020 18:25:58 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 29 Apr 2020 18:25:58 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ae8f0fa6cb0d971b4b8fedf7fc9b00f61f780b383fe7d64e6c2e4be8d20c3987`  
		Last Modified: Thu, 23 Apr 2020 00:17:46 GMT  
		Size: 25.8 MB (25762125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb99573784b2c87a7d6f167c4737d4052d11f190aae3ffc34fd9208c3f4463f`  
		Last Modified: Thu, 23 Apr 2020 17:32:11 GMT  
		Size: 2.3 MB (2308953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd71c568db17d004d49fd757e75088685129c44ddb4034260d2144f5aecac3ce`  
		Last Modified: Thu, 23 Apr 2020 17:35:23 GMT  
		Size: 26.1 MB (26139997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820be6f0741be0c2ab6b12375bb4ed47e6eafcd1fec0304cfbd0c8dc76e09d1a`  
		Last Modified: Thu, 23 Apr 2020 17:34:56 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c2fe906a479a5230fe713382e4d41fd5ebb606c011c4cb0a0001fc523bc5f4`  
		Last Modified: Wed, 29 Apr 2020 18:07:37 GMT  
		Size: 2.2 MB (2218388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2114ff12f121a0bcfc2e40e92e4343e4d26b8aa5f3f0004f6dbfc411237fbf6`  
		Last Modified: Wed, 29 Apr 2020 18:28:37 GMT  
		Size: 2.8 MB (2752764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.6-buster` - linux; ppc64le

```console
$ docker pull hylang@sha256:908ac2575d725cf7ae3d587ba67adea3d8baf9f77b092967feb5e2c77313160f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65744607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a879a52c88807a8998b3110b494ef1cccabd7793e03df7e599a04c1d05f226`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Apr 2020 00:36:00 GMT
ADD file:5b3c3d2945800e1743dc02a4f68bd830fe2f67ca437223692eb460147c158c2b in / 
# Thu, 23 Apr 2020 00:36:04 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:59:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 00:59:56 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 12:06:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 12:34:55 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Thu, 23 Apr 2020 13:31:39 GMT
ENV PYTHON_VERSION=3.6.10
# Thu, 23 Apr 2020 13:44:30 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 23 Apr 2020 13:44:35 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 29 Apr 2020 17:53:50 GMT
ENV PYTHON_PIP_VERSION=20.1
# Wed, 29 Apr 2020 17:53:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Wed, 29 Apr 2020 17:53:58 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Wed, 29 Apr 2020 17:54:50 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 29 Apr 2020 17:54:54 GMT
CMD ["python3"]
# Wed, 29 Apr 2020 19:21:58 GMT
ENV HY_VERSION=0.18.0
# Wed, 29 Apr 2020 19:22:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 29 Apr 2020 19:22:18 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:012c6cdbd1af202bbfbea5945fafbb9aca9097f1fa3cb493a29155fdc02cc43c`  
		Last Modified: Thu, 23 Apr 2020 00:50:14 GMT  
		Size: 30.5 MB (30524638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2cb5076c799329dc89187a26d1abe3fce98e16a90a828966bf55c6bf1d915d2`  
		Last Modified: Thu, 23 Apr 2020 14:54:54 GMT  
		Size: 2.9 MB (2871706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:225025a55c9c5a2504e47d9e8e552e3df679d0038a585387f47018b20e0adacc`  
		Last Modified: Thu, 23 Apr 2020 19:57:52 GMT  
		Size: 27.4 MB (27374622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c417ce8d5b45b472ed5f54375b7629808f9f26a21dc7f48e547ef7f467914c`  
		Last Modified: Thu, 23 Apr 2020 19:57:40 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba01f4aca9c42488b192cbf4f60c71c437d9cd3d5a9790d983d478f62db9be6`  
		Last Modified: Wed, 29 Apr 2020 18:10:29 GMT  
		Size: 2.2 MB (2220124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2949e854a25d07d9f384cd39ff93c24b493c35c559f6314ac30ce220e0334454`  
		Last Modified: Wed, 29 Apr 2020 19:28:59 GMT  
		Size: 2.8 MB (2753282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.6-buster` - linux; s390x

```console
$ docker pull hylang@sha256:c65a2859e6cf22667947f5950df4c3dfacb379e1bde7dd3721618c0db058256b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59353657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffc01c0d0fded803fa19e44a7481afb98a487f86171bf4c69575a8468c60ca2`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 14 May 2020 23:06:40 GMT
ADD file:a29e647b8dccf726d8610d8c599d6727d6145426f9374720b985fc9be9ac906c in / 
# Thu, 14 May 2020 23:06:41 GMT
CMD ["bash"]
# Thu, 14 May 2020 23:29:06 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2020 23:29:06 GMT
ENV LANG=C.UTF-8
# Thu, 14 May 2020 23:29:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 23:34:41 GMT
ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D
# Thu, 14 May 2020 23:47:04 GMT
ENV PYTHON_VERSION=3.6.10
# Thu, 14 May 2020 23:51:02 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 14 May 2020 23:51:04 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 14 May 2020 23:51:05 GMT
ENV PYTHON_PIP_VERSION=20.1
# Thu, 14 May 2020 23:51:05 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Thu, 14 May 2020 23:51:05 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Thu, 14 May 2020 23:51:15 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 14 May 2020 23:51:16 GMT
CMD ["python3"]
# Fri, 15 May 2020 00:09:57 GMT
ENV HY_VERSION=0.18.0
# Fri, 15 May 2020 00:10:00 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Fri, 15 May 2020 00:10:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bdb298e230dde60bfce8a476ae8ea8988828f7ec9f5452f38f46102a609f57c1`  
		Last Modified: Thu, 14 May 2020 23:11:24 GMT  
		Size: 25.7 MB (25712933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b7df72789485ce816b1118bfcfc62a6bf98e3302780d2d7832d4da361dfba3a`  
		Last Modified: Fri, 15 May 2020 00:06:50 GMT  
		Size: 2.4 MB (2442337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9d545ae162766e53166a16765e206559fae4f82ec0ff9d90de6cf4e6c19e50`  
		Last Modified: Fri, 15 May 2020 00:07:43 GMT  
		Size: 26.2 MB (26227050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f6b94648c629a3b23222619c812b7ca9e108cb7a3b02bde19d04cfbba10c6d`  
		Last Modified: Fri, 15 May 2020 00:07:43 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7bf5565009b747a535cb5f8d7973cc4b57472b96c04576a3cdddb3bf0899cb`  
		Last Modified: Fri, 15 May 2020 00:07:53 GMT  
		Size: 2.2 MB (2218553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfc965e09e29f0a36c098148b66d207f2410bc166deb92ce21d10b1216bcf7cc`  
		Last Modified: Fri, 15 May 2020 00:12:41 GMT  
		Size: 2.8 MB (2752553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
