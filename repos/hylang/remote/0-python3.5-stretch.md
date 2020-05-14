## `hylang:0-python3.5-stretch`

```console
$ docker pull hylang@sha256:6e6d0e6446ab518e37dbd15378d5f9cffb6bbd9bfd21187b60a2ebc3ef71d56c
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

### `hylang:0-python3.5-stretch` - linux; amd64

```console
$ docker pull hylang@sha256:88b4cef6dee1b15145a43c5e16e1d7eac625928e58d66ca934cde5478f2a330d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53253668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6142c54aa21cd3d94d08e46dc9c3ddfc6efc09d047425d8fe99a0285241404`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Apr 2020 00:23:03 GMT
ADD file:08ea1ff3fcd4efc24ab4f262cfa24e55e65844f6858e41a46fe0635d247f174d in / 
# Thu, 23 Apr 2020 00:23:03 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 15:06:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 15:06:54 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 15:07:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 16:13:06 GMT
ENV GPG_KEY=97FC712E4C024BBEA48A61ED3A5CA953F73C700D
# Thu, 23 Apr 2020 16:13:06 GMT
ENV PYTHON_VERSION=3.5.9
# Thu, 23 Apr 2020 16:19:46 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 23 Apr 2020 16:19:47 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 29 Apr 2020 17:43:02 GMT
ENV PYTHON_PIP_VERSION=20.1
# Wed, 29 Apr 2020 17:43:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Wed, 29 Apr 2020 17:43:03 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Wed, 29 Apr 2020 17:43:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 29 Apr 2020 17:43:17 GMT
CMD ["python3"]
# Wed, 29 Apr 2020 18:50:48 GMT
ENV HY_VERSION=0.18.0
# Wed, 29 Apr 2020 18:50:53 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 29 Apr 2020 18:50:53 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b248fa9f6d2ae427ad7f00de3537ab256ae7eb413565f8be0773ee9b86ef57d4`  
		Last Modified: Thu, 23 Apr 2020 00:27:46 GMT  
		Size: 22.5 MB (22513488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510b6d52f6fb488db2cd72b9e1234f1d628f09908a3bee9926dd19e7cbfbcc3c`  
		Last Modified: Thu, 23 Apr 2020 16:21:49 GMT  
		Size: 2.5 MB (2531247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462297a16aaa4a986c1fc00078c2ad53bad697e339161718c7c142a5f9ca3974`  
		Last Modified: Thu, 23 Apr 2020 16:23:59 GMT  
		Size: 23.2 MB (23159523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70766cfb561957f9ec334c071fbbe75de0e23c943e1dfa65f118eefd1d3b72ad`  
		Last Modified: Thu, 23 Apr 2020 16:23:52 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa03931e46f6868da4848ceab15ff1ab945a30b8c8da73573048c8a9263a621c`  
		Last Modified: Wed, 29 Apr 2020 17:46:18 GMT  
		Size: 2.2 MB (2214061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4def2885cdf50e246fe794a8b3b7e23a8fcc6bccbcb822d6b8502978b385f5a9`  
		Last Modified: Wed, 29 Apr 2020 18:53:21 GMT  
		Size: 2.8 MB (2835107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.5-stretch` - linux; arm variant v5

```console
$ docker pull hylang@sha256:ec06e532302bed3b2a5267c33b1a2029985d0f443e30b1ba5b1bbb56b77f0f6e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49972740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d7461758668e76331481b65dca63ad914564189b7aa07be511e37f91b68f318`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 13 May 2020 21:55:26 GMT
ADD file:9ae861b3016cc7e568c2f4f1f2a84ab78e21058bf3e65683c5e32f148bb0d834 in / 
# Wed, 13 May 2020 21:55:27 GMT
CMD ["bash"]
# Thu, 14 May 2020 02:20:28 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2020 02:20:29 GMT
ENV LANG=C.UTF-8
# Thu, 14 May 2020 02:20:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Thu, 14 May 2020 03:36:34 GMT
ENV GPG_KEY=97FC712E4C024BBEA48A61ED3A5CA953F73C700D
# Thu, 14 May 2020 03:36:35 GMT
ENV PYTHON_VERSION=3.5.9
# Thu, 14 May 2020 03:46:16 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 14 May 2020 03:46:20 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 14 May 2020 03:46:22 GMT
ENV PYTHON_PIP_VERSION=20.1
# Thu, 14 May 2020 03:46:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Thu, 14 May 2020 03:46:25 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Thu, 14 May 2020 03:47:05 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 14 May 2020 03:47:06 GMT
CMD ["python3"]
# Thu, 14 May 2020 22:29:46 GMT
ENV HY_VERSION=0.18.0
# Thu, 14 May 2020 22:30:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 14 May 2020 22:30:05 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8d8bd6103e4f9e46eaf8c99b66d0017a7f616535993c72d6d02dce33ad4e616c`  
		Last Modified: Wed, 13 May 2020 22:03:26 GMT  
		Size: 21.2 MB (21190862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7ac4c51bd7334314212b37980b1803f2120da41b270f8d66017b17eff8562e`  
		Last Modified: Thu, 14 May 2020 03:49:30 GMT  
		Size: 2.3 MB (2256624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efdd553c6c762aa1aa8ae1fde61b76348ea60dc0bc943dc111170177c7166afa`  
		Last Modified: Thu, 14 May 2020 03:51:39 GMT  
		Size: 21.5 MB (21475700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a98cd37792747d6cf818459bc928b635cd801aa952e7bd8620aa0a90d8a097`  
		Last Modified: Thu, 14 May 2020 03:51:32 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb47ca9c39057facc1b93709d335f42ee505daa84d9dcfc041820924c20c3bb`  
		Last Modified: Thu, 14 May 2020 03:51:32 GMT  
		Size: 2.2 MB (2214005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fcf1458cca120aa688884452d417132ed17a14d79c02f81b1abf858de83cfa7`  
		Last Modified: Thu, 14 May 2020 22:31:42 GMT  
		Size: 2.8 MB (2835308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.5-stretch` - linux; arm variant v7

```console
$ docker pull hylang@sha256:deb8dff487f62e5a91b96003ea5bb785119cc1d1193325d10e1bf2a42d01d4a1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47496675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:064b78703346c7704705cb7aa34c18d065c17821518ed56129660debe84040de`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Apr 2020 01:07:37 GMT
ADD file:d34df50b16579a75bfaa8cce488b954cd5cdc110c3eeda26cfb1d2e285dd53f2 in / 
# Thu, 23 Apr 2020 01:07:39 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 08:04:28 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 08:04:29 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 08:04:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 09:25:50 GMT
ENV GPG_KEY=97FC712E4C024BBEA48A61ED3A5CA953F73C700D
# Thu, 23 Apr 2020 09:25:51 GMT
ENV PYTHON_VERSION=3.5.9
# Thu, 23 Apr 2020 09:34:49 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 23 Apr 2020 09:34:51 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 29 Apr 2020 17:27:36 GMT
ENV PYTHON_PIP_VERSION=20.1
# Wed, 29 Apr 2020 17:27:36 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Wed, 29 Apr 2020 17:27:37 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Wed, 29 Apr 2020 17:28:08 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 29 Apr 2020 17:28:08 GMT
CMD ["python3"]
# Wed, 29 Apr 2020 18:10:25 GMT
ENV HY_VERSION=0.18.0
# Wed, 29 Apr 2020 18:10:39 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 29 Apr 2020 18:10:41 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9a298b6c339c562fea435ecbf6369ef71a818d1df1539a329088cdd265ed548f`  
		Last Modified: Thu, 23 Apr 2020 01:14:30 GMT  
		Size: 19.3 MB (19298463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34176671853082accf9a607fff5ad7d13288d5eef8c36b5d40fa7cd48ea070a`  
		Last Modified: Thu, 23 Apr 2020 09:38:51 GMT  
		Size: 2.2 MB (2177915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff66dcf19ebbce3619b6a0d9604d4533a6259d805ab7e80e8d40c3e9dd3eaca`  
		Last Modified: Thu, 23 Apr 2020 09:41:42 GMT  
		Size: 21.0 MB (20970470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578db8490c2df5c4f5fa9896dabc3964a1d046e0987ac2b92412b7fd7c38aff1`  
		Last Modified: Thu, 23 Apr 2020 09:41:35 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcde3852dd395b7e3706490fa1b742da1a80d4e4002c5667e16e0268d398042b`  
		Last Modified: Wed, 29 Apr 2020 17:33:29 GMT  
		Size: 2.2 MB (2214176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8739f6fabaa02133a430c2d7501b480afc0673ea218dcbfc6a83de1a3bc35555`  
		Last Modified: Wed, 29 Apr 2020 18:14:30 GMT  
		Size: 2.8 MB (2835410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.5-stretch` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:40ed7025e1a546198a86231346e6268310a4f1d39b4ea646fd6b167644ead3a1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49869685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5193d079cd8d46dcd4e786d712eb594bd484bbd0e3c29b323551023307a7d383`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Apr 2020 00:59:03 GMT
ADD file:da103bb73d1c28697756e3558eaa49cc235b07dfea96895f56929eb8fd0fb67c in / 
# Thu, 23 Apr 2020 00:59:05 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 13:51:16 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 13:51:16 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 13:51:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 15:09:02 GMT
ENV GPG_KEY=97FC712E4C024BBEA48A61ED3A5CA953F73C700D
# Thu, 23 Apr 2020 15:09:03 GMT
ENV PYTHON_VERSION=3.5.9
# Thu, 23 Apr 2020 15:16:56 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 23 Apr 2020 15:16:59 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 29 Apr 2020 18:11:58 GMT
ENV PYTHON_PIP_VERSION=20.1
# Wed, 29 Apr 2020 18:11:59 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Wed, 29 Apr 2020 18:11:59 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Wed, 29 Apr 2020 18:12:34 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 29 Apr 2020 18:12:35 GMT
CMD ["python3"]
# Wed, 29 Apr 2020 19:13:21 GMT
ENV HY_VERSION=0.18.0
# Wed, 29 Apr 2020 19:13:30 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 29 Apr 2020 19:13:31 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:191ef9a1fd49ca372c51c235b6f6f4579bddb73cfd390f67b4878b465f9bdfd2`  
		Last Modified: Thu, 23 Apr 2020 01:05:53 GMT  
		Size: 20.4 MB (20370093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b1e4abd7f0a1aae36a5263ba3c990b6954c9b65fce50d5dbd68eecfa75b13d`  
		Last Modified: Thu, 23 Apr 2020 15:20:31 GMT  
		Size: 2.2 MB (2238946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843b2feb366b72618a16e6b1c03ebb8791ffb1292d7bb00650d8c0fa9262f77c`  
		Last Modified: Thu, 23 Apr 2020 15:21:49 GMT  
		Size: 22.2 MB (22210927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b5192a50fad959aa580289ab2d1d5f7b58db0f92f06666aee7d9c9ebd3a37a`  
		Last Modified: Thu, 23 Apr 2020 15:21:42 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438f517f2311dfdd5efd54ca583cc625ebeeeec0d67ff9a9327460e7ccf51dc2`  
		Last Modified: Wed, 29 Apr 2020 18:17:49 GMT  
		Size: 2.2 MB (2214001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ad090aaed754708c193029a7a4119828ee41065fc553a0ca700b3a6279638`  
		Last Modified: Wed, 29 Apr 2020 19:17:18 GMT  
		Size: 2.8 MB (2835478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.5-stretch` - linux; 386

```console
$ docker pull hylang@sha256:b0735931e9bb245706158534f3eac98a1df824183eb3857a05bcf7d0ef7a34c4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52537810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a34c294ff963f8cb19c9ef76511eff842a8a38f8aae0b632e4cda49f2302ff`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:13 GMT
ADD file:82f76d577eec142f824456d027e5f82f681c9f5a09aeef4f711cef4662dcaea4 in / 
# Thu, 23 Apr 2020 00:42:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 16:36:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 16:36:12 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 16:36:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 18:13:49 GMT
ENV GPG_KEY=97FC712E4C024BBEA48A61ED3A5CA953F73C700D
# Thu, 23 Apr 2020 18:13:49 GMT
ENV PYTHON_VERSION=3.5.9
# Thu, 23 Apr 2020 18:23:29 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 23 Apr 2020 18:23:31 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 29 Apr 2020 18:05:10 GMT
ENV PYTHON_PIP_VERSION=20.1
# Wed, 29 Apr 2020 18:05:10 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Wed, 29 Apr 2020 18:05:10 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Wed, 29 Apr 2020 18:05:25 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 29 Apr 2020 18:05:25 GMT
CMD ["python3"]
# Wed, 29 Apr 2020 18:26:26 GMT
ENV HY_VERSION=0.18.0
# Wed, 29 Apr 2020 18:26:31 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 29 Apr 2020 18:26:31 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7cb0551c4675347b94a8c63d7ee1f99dea4ab34aa7f23602ca587b6894d0211b`  
		Last Modified: Thu, 23 Apr 2020 00:47:39 GMT  
		Size: 23.1 MB (23141423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba7ab7c03374eaf5445304d0d38a302fa1a683430e78556ef03de7fbcb292ac`  
		Last Modified: Thu, 23 Apr 2020 18:27:14 GMT  
		Size: 2.5 MB (2533044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01dad8ae8f38984a088496503b5e6a50201354952504ec1a1406beb2352e1650`  
		Last Modified: Thu, 23 Apr 2020 18:29:14 GMT  
		Size: 21.8 MB (21814341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463d4ec959ddd8360d096494d71dc6d8f5ee820a638d6e67d3924639d927ac2a`  
		Last Modified: Thu, 23 Apr 2020 18:29:04 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d7838eaf6505f53d3c7588bdf2ebcc5c5f00724747307655ccee879d630909`  
		Last Modified: Wed, 29 Apr 2020 18:08:47 GMT  
		Size: 2.2 MB (2213612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0575cfe09d670d2f8da5b376f1f3d32779ab0896a9d31ebd2a3f08d897a7f8a1`  
		Last Modified: Wed, 29 Apr 2020 18:29:06 GMT  
		Size: 2.8 MB (2835142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.5-stretch` - linux; mips64le

```console
$ docker pull hylang@sha256:e9b5f9dfb7bd29bcb2f4e9003bccce8663da95c0b6477cbbb8e544f648a57625
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52193158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7911fd57c145001a981410e07108ecf0b964803ea5d697b6b7afa213c8b327`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Apr 2020 00:12:52 GMT
ADD file:dc054209d749f6588715a73aaca1887c710fb97ac811033cb4a8666323c0b868 in / 
# Thu, 23 Apr 2020 00:12:53 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 13:36:03 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 13:36:03 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 13:36:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 17:10:40 GMT
ENV GPG_KEY=97FC712E4C024BBEA48A61ED3A5CA953F73C700D
# Thu, 23 Apr 2020 17:10:41 GMT
ENV PYTHON_VERSION=3.5.9
# Thu, 23 Apr 2020 17:29:20 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 23 Apr 2020 17:29:23 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 29 Apr 2020 18:03:38 GMT
ENV PYTHON_PIP_VERSION=20.1
# Wed, 29 Apr 2020 18:03:39 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Wed, 29 Apr 2020 18:03:39 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Wed, 29 Apr 2020 18:04:22 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 29 Apr 2020 18:04:23 GMT
CMD ["python3"]
# Wed, 29 Apr 2020 18:26:43 GMT
ENV HY_VERSION=0.18.0
# Wed, 29 Apr 2020 18:26:58 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 29 Apr 2020 18:26:59 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:5e7e347ca6a014954ed1ad62bdc1b0f336c69e620dd8bcef9ba73cb2a8e3bcaf`  
		Last Modified: Thu, 23 Apr 2020 00:23:20 GMT  
		Size: 22.2 MB (22173855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468db8bfd8cf3b1f19e1aa9d6bacd0f04c4d35c9686f93c9cfbbd0f0e0cc5b97`  
		Last Modified: Thu, 23 Apr 2020 17:36:14 GMT  
		Size: 2.1 MB (2110778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7abf44b7f2f895a00dbb3a4467c3276d5fd97282875020cf9a3fddb087c34077`  
		Last Modified: Thu, 23 Apr 2020 17:38:48 GMT  
		Size: 22.9 MB (22859546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63fb02d78b56a842848a744ab351035a315f7161bcdd63bc596e92408a7b6a30`  
		Last Modified: Thu, 23 Apr 2020 17:38:28 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c1607c85b4e06720eca9d3b7376f4a5ce5e8e95d1279659829d10283f30030`  
		Last Modified: Wed, 29 Apr 2020 18:09:00 GMT  
		Size: 2.2 MB (2213442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349c6f976de4f4c31c0133a9d2871722308878ea8a2bf79cfaaa25ac391d41bb`  
		Last Modified: Wed, 29 Apr 2020 18:29:36 GMT  
		Size: 2.8 MB (2835295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.5-stretch` - linux; ppc64le

```console
$ docker pull hylang@sha256:73361a2441a3850e12c067000ab2f4b7a10c6d93bef38f9fd08321b7d1f3f805
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53312578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a94a35c6c9bf8975d915124b27b56344727d767a33d48ca595abca70e158370`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Apr 2020 00:42:37 GMT
ADD file:a18cd8947224196f50b4845289d03b1f4deafb438223194400da0ed4dae92656 in / 
# Thu, 23 Apr 2020 00:42:40 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 13:05:07 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 13:05:09 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 13:05:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 14:40:43 GMT
ENV GPG_KEY=97FC712E4C024BBEA48A61ED3A5CA953F73C700D
# Thu, 23 Apr 2020 14:40:46 GMT
ENV PYTHON_VERSION=3.5.9
# Thu, 23 Apr 2020 14:51:33 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 23 Apr 2020 14:51:42 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 29 Apr 2020 18:03:20 GMT
ENV PYTHON_PIP_VERSION=20.1
# Wed, 29 Apr 2020 18:03:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Wed, 29 Apr 2020 18:03:26 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Wed, 29 Apr 2020 18:04:28 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 29 Apr 2020 18:04:31 GMT
CMD ["python3"]
# Wed, 29 Apr 2020 19:24:26 GMT
ENV HY_VERSION=0.18.0
# Wed, 29 Apr 2020 19:24:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 29 Apr 2020 19:24:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4efde6fe2246d87988ee174dc3ed2e4c3158360e5c80fcb0433bc70a732bd77e`  
		Last Modified: Thu, 23 Apr 2020 00:55:34 GMT  
		Size: 22.8 MB (22785405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b36549097b4ed5a0974197d14362130b168a1c2522b3a98eae342c1d17382a7`  
		Last Modified: Thu, 23 Apr 2020 14:57:39 GMT  
		Size: 2.2 MB (2192692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dafa3831d3057a77c5b0a8358605d7c1dabb21aac4d6d35987a48d57b7100d87`  
		Last Modified: Thu, 23 Apr 2020 14:57:43 GMT  
		Size: 23.3 MB (23283691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64aac38e46bd600e5ec2623150028dbcedec9a543df710281a4b01d4202919d4`  
		Last Modified: Thu, 23 Apr 2020 14:57:37 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d608e9e0aa46d3dd2d4f9438060fd49e36e7e2baa9d012a1232ee4bf242dfa9b`  
		Last Modified: Wed, 29 Apr 2020 18:12:07 GMT  
		Size: 2.2 MB (2215035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8423e784f4b1b0e81df906770bca1d53931ac8fcd3afd6d8d0b523ae0ed0e2c`  
		Last Modified: Wed, 29 Apr 2020 19:30:24 GMT  
		Size: 2.8 MB (2835515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-python3.5-stretch` - linux; s390x

```console
$ docker pull hylang@sha256:4ff4c2a3b64013990ba78874f8d07a7ca519ae30ee5235691da61761f373242f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53918685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdf82a8b0f442569b13ebd5813e51bb389a6e02d8b7965925828446ffd55a6a`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Apr 2020 00:53:44 GMT
ADD file:ac741fad943268754937ce2b60ad871383a702d0493a392bbfb576e660b3d354 in / 
# Thu, 23 Apr 2020 00:53:46 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 08:46:56 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Apr 2020 08:46:56 GMT
ENV LANG=C.UTF-8
# Thu, 23 Apr 2020 08:47:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 09:35:52 GMT
ENV GPG_KEY=97FC712E4C024BBEA48A61ED3A5CA953F73C700D
# Thu, 23 Apr 2020 09:35:53 GMT
ENV PYTHON_VERSION=3.5.9
# Thu, 23 Apr 2020 09:41:26 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 23 Apr 2020 09:41:28 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 29 Apr 2020 18:04:38 GMT
ENV PYTHON_PIP_VERSION=20.1
# Wed, 29 Apr 2020 18:04:38 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Wed, 29 Apr 2020 18:04:39 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Wed, 29 Apr 2020 18:04:57 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 29 Apr 2020 18:04:58 GMT
CMD ["python3"]
# Wed, 29 Apr 2020 19:00:00 GMT
ENV HY_VERSION=0.18.0
# Wed, 29 Apr 2020 19:00:05 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 29 Apr 2020 19:00:05 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d4b19f1c02db3a4e8614b7787d1d77707e6ce727c1ce01c66fe1d87c87ee08ae`  
		Last Modified: Thu, 23 Apr 2020 00:57:36 GMT  
		Size: 22.4 MB (22365462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0146e2567d900ead1bc2653f02fd337432e294a0f093d77eb1f479fd7caa9e`  
		Last Modified: Thu, 23 Apr 2020 09:43:53 GMT  
		Size: 2.3 MB (2269082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012b876e6ee4460f2f7e018d5aaa7b0fb9ddefde4c03f32761cca1beb4a4caaf`  
		Last Modified: Thu, 23 Apr 2020 09:45:42 GMT  
		Size: 24.2 MB (24235275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:054683391f618a1d3e391e8b7c7e4195c9aea25d554f90f3e9053d4e4e955382`  
		Last Modified: Thu, 23 Apr 2020 09:45:43 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf6707efbfb38aeaee9706a98b06e06bc3116639fb27e071b289cac55bb5d30`  
		Last Modified: Wed, 29 Apr 2020 18:09:18 GMT  
		Size: 2.2 MB (2213315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb3c9cd12c79c0eab02a18dc3cd24da71203983cd32c795154ee359091369c8`  
		Last Modified: Wed, 29 Apr 2020 19:03:01 GMT  
		Size: 2.8 MB (2835311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
